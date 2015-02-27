# JQuery/Ajax Quiz

Write your answer below each question.

### Question 1
(a) What is a click handler?

  # a click handler is a method that gets attached to a tag that you want to click.

(b) Where in your JS file should you put it, and WHY?
  # It is recommened to be put at the end of the body tag. As for the why... for loading purposes but I am not very sure.

### Question 2
If you get the error `$ is undefined`, what does that mean and what could you do to fix it?
  # It means that Jquery is not being referenced. To solve it just add the link to the Jquery library.
### Question 3
What should go in the `$(document).ready()` part of your JS file?
  # Whatever script of code that you want to run only until the page has finished loding or when the DOM is done being created... ?
### Question 4
In an AJAX GET request, what does the argument of the `.done()` callback - in the example below, that would be `data` - represent?

```
$.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'GET',
  })
  .done(function(data) {
    console.log("success!")
  });
```
  # data is the JSON information (data) that its going to be returned from the server.
### Question 5
In an AJAX POST request, what does the argument of the `.done()` callback - in the example below, that would be `data` - represent? (Hint: it's not the same as in Question 4.)

```
  $.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'POST',
    dataType: 'JSON',
    data: { user: { name: "Anna", about: "instructor", email: "hi@gmail.com" } },
  })
  .done(function(data) {
    console.log("success!");
  });
```
  # data in the case of a POST request refers back to the item that was just created. In this case "Anna" ...
### Question 6
Suppose you had the following form in your HTML file. Use jQuery to write a single line of code that takes whatever the user entered in the textbox and saves it to the variable `user_input`.

```
  <form>
    <p>The dress is:</p><input type="text" id="color">
    <input type="submit" value="Submit" id="submit">
  </form>
```
```
    var user_input = $("#color").append('<li>' + color + '</li>');
```

### Question 7
This code looks like it works, but when you run it, you see that the `UserApp.add_all_users()` function executes but `console.log` displays `undefined`. What's wrong with the code?

```
UserApp.get_all_users = function() {
  $.ajax({
    url: 'http://ig-hacker-news.herokuapp.com/users',
    type: 'GET',
  })
  .done(function(data) {
    console.log("success!")
  UserApp.get_all_users(data);  // was the function not being called to display the data?
  });
  UserApp.add_all_users(data);
};

UserApp.add_all_users = function(data) {
  console.log(data);
};
```



