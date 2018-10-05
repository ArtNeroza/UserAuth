# UserAuth
NodeJS Authentication API

Endpoint
`https://userauth-218420.appspot.com/`


**Add User**
----
  Add User

* **URL**

  /api/User

* **Method:**

  `POST`

* **Body**

  `{Username: "<username>", Password:"<password>" }`

* **Success Response:**
    **Content:** `"Registration Sucessfuly"`
 
* **Error Response:**

    **Content:** `"User already exist"`

    **Content:** `"Password does not meet the requirements"`
    
    **Content:** `"Invalid Username"`
   
* **Requirements:**

    **Username:** `"Combination of lowercase and uppercase alphabet, numbers and minimum of 3 to maximum of 20 characters"`
    
    **Password:** `"Combination of lowercase and uppercase alphabet, numbers and mininum of 8 characters. No spaces allowed"`


**Login User**
----
   Login user returns Token

* **URL**

  /api/Auth

* **Method:**

  `POST`

* **Body**

  `{Username: "<username>", Password:"<password>" }`

* **Success Response:**
    **Content:** `"{token: <token>}"`
 
* **Error Response:**

    **Content:** `"Authentication Error"`
    
    

**Token Auth**
----
  Checks if token is valid returns Username

* **URL**

  /api/TokenAuth

* **Method:**

  `POST`

* **Body**

  `{token:"<token>" }`

* **Success Response:**
    **Content:** `<username>`
 
* **Error Response:**

    **Content:** `"Token Expired"`

