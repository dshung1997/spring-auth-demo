# This is a mini project which aims to test authentication and authorization implementation in Spring Security

After cloing the project, export the dumb.sql file in resources/database folder and make sure to change the username and password in the application.properties file.

---

Note: username and password of any already-defined user are the same.

# APIs

POST - http://localhost:8080/api/auth/signup
SIGN UP a new user

```json
{
	"username" : "",
	"password" : "",
	"name" : "",
	"role" : "ROLE_USER"
}
```

or a new admin

```json
{
	"username" : "",
	"password" : "",
	"name" : "",
	"role" : "ROLE_ADMIN"
}
```


POST - http://localhost:8080/api/auth/signin
SIGN IN and get the token

```json
{
	"username": "",
	"password": ""
}
```
After getting the token, remember that "Token " (removing the quotes) precedes the token in the Authorization header

GET - http://localhost:8080/api/users/me
GET the information of the current user

GET - http://localhost:8080/api/users/all
GET information of all users (of course - only admins can access)