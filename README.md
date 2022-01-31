# user-auth-api
A simple API with basic authentication features

### ✅ The following API calls can be made with this project

***

#### POST Requests

* > __/register__

  It will register the user and return the registered user details for future reference.
  <br>
  Required body parameters:
  ```json
  {
    "user_name": "Some User Name",
    "user_email": "user@email.com",
    "user_password": "supersecretpassword"
  }
  ```

* > __/login__

  It will login the user and will return a generated jwt token for future reference. The details will be stored in the browser's session.
  <br>
  Required body parameters:
  ```json
  {
    "user_name_or_email": "Some User Name or user@email.com",
    "user_password": "supersecretpassword"
  }
  ```
<br>

#### GET Requests

* > __/welcome__

  It will return the details of the user based on the jwt token stored in sessions of the browser. An error will be generated if the user isn't logged in.

<br>

#### DELETE Requests

* > __/logout__

  It will logout the user and destroy the current session.

<br>


### ⚙️ Setting Up the Project

1. Clone the repo
   ```sh
   git clone https://github.com/savi-1311/user-auth-api
   ```
2. Install NPM packages
   ```sh
   cd user-auth-api
   npm install
   ```
3. Create a .env file and add values accordingly.
   ```sh
   touch .env
   ```
   
   Sample .env file:
   ```env
   PORT=3000
   ACCESS_TOKEN_SECRET=supersecret
   ```
4. Configure the ```server.js``` line no. 25 and 26 with correct MySQL configurations.

### ▶️ Usage 
1. Setting up MySQL environment
    ```sql
    CREATE DATABASE userdb;
    CREATE TABLE userinfo (
    user_id int primary key auto_increment,
    user_name varchar(255),
    user_email varchar(255),
    user_password varchar(255));
    ```

2.  To run the server
    ```node 
    npm start 
    ```
***

