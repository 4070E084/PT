DVWA

# Brute Force

<?php

if(isset($_GET['Login'])){
//Getusername
$user=$_GET['username'];

//Getpassword
$pass=$_GET['password'];
$pass=md5($pass);

//Checkthedatabase
$query="SELECT*FROM`users`WHEREuser='$user'ANDpassword='$pass';";
$result=mysql_query($query)ordie('<pre>'.mysql_error().'</pre>');

if($result&&mysql_num_rows($result)==1){
//Getusersdetails
$avatar=mysql_result($result,0,"avatar");

//Loginsuccessful
echo"<p>Welcometothepasswordprotectedarea{$user}</p>";
echo"<imgsrc="{$avatar}"/>";
}
else{
//Loginfailed
echo"<pre><br/>Usernameand/orpasswordincorrect.</pre>";
}

mysql_close();
}

?>

# Command Injection

# CSRF

# File Inclusion

# File Upload

# Insecure CAPTCHA

# SQL Injection

# SQL Injection (Blind)

# Weak Session IDs

# XSS (DOM)

# XSS (Reflected)

# XSS (Stored)
