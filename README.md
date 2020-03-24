# First-PHP-Task
Creating A Contact Form that Submits to a file.


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Boffinjegz Contact Me!! form</title>
</head>
<body>
<img src="C:\Users\USER\Documents\BOFFINJEGZ\SHIELD LOGO PROJECT\Transparent\boffin logo.png" width="10%" />    
<h3> Contact Me! </h3>
	<form action="processform.php" method="POST">
	
    <p>
	<label for="first_name"> First Name</label><br/>
	<input type="text" name="first_name" placeholder="Enter Your Firstname" />
	</P>
	
    <p>
	<label for="last_name"> Last Name</label><br/>
	<input type="text" name="last_name" placeholder="Enter Your Lastname" />
	</p>
	
    <p>
	<label for="email"> Email</label><br/>
	<input type="email" name="email" placeholder="Enter Email" required />
	</p>
	
    <p>
	<label for="department"> Department </label><br/>
	 <select name="department">
	  <option>Select Department</option>
	  <option>HR</option>
	  <option>Board</option>
  	  <option>Marketing</option>
 	  <option>Business Development</option>
	</select>
	</p>

    <p>
	<label for="email"> Your Message </label><br/>
	<textarea name="message" col="5" row="5"> </textarea>
	</p>
	
	<p>
	<label for="gender">Gender</label><br/>
	<input type="radio" value="female" name="gender" /> Female
	<input type="radio" value="male" name="gender" />Male
	</p>

	<p>
	<input type="checkbox" name="terms" required /> By Checking this box you agree to our terms and conditions.
	</P>


	<button type="submit"> send message </button>
	
	
</form>
<p>
Feel free to exclusively express yourself...<br/>
I love Feedback!
</p>
</body>
</html>



<?php 
print_r($_POST);
echo file_put_contents("$_POST[first_name] $_POST[last_name].txt", $_POST);

?>
