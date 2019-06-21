# API-documentation
# Method Shop
***
Documentation of an API project by Group #4

  * **URL**: http://localhost:3000/api/

### Microservices
 ----
 ##### Categories
  `GET` | `POST` | `DELETE` | `PATCH`
  > `GET`
 - [/categories](<>)
    - lists information about all users
 - [/categories/:id](<>) 
    - information about a user with the id<string> entered

  > `POST`
   - [/categories/create](<>)
        - creates a category by recieving `name: <String>`
 > `DELETE`
   - [/categories/:id](<>)
       - deletes the user with an id<string>
 > `PATCH`
   - [/categories/:id](<>)
       - recieves from the user: 
            ```sh    
           propname: <string> 
           value: <string>
            ```
            submits the modification to a resource
 ----
 ##### PRODUCTS
  `GET` | `POST` | `DELETE` | `PATCH`
  > `GET`
   - [/products](<>)
        - recieves all the products
   - [/products/:productId](<>) 
       - recieves the product with the `productsId<string>` entered
  > `POST`
   - [/products/create](<>)
       - recieves from the user:
            ```sh
            categoryID: <string> 
            title: <string> !Required!
            description: <string>
            price: <number>
            ```
 > `DELETE`
   * [/products/:productId](<>)
        - deletes the product with an id<string> entered
 > `PATCH`
   * [/products/:productId](<>)
        - changes the product with an `productsId<string>` entered
 ----
 ##### USER
  `GET` | `POST` | `PATCH`
  > `GET`
   - [/user/list](<>)
       - shows all the users
   - [/user/:userId](<>) 
       - show the user by Id<string>
  > `POST`
   - [/user/signup](<>)
        - recieves from the user !All Required!:
            ```sh
            username: <string>
            email: email<string>
            password: <string>
            ```
 - [/user/signin](<>)
     - recieves from the user *!All Required!*:
        ```sh 
        email: email<string>
        password: <string>
        ```
 > `PATCH`
 * [/user/:userId](<>)
        edits user information

---

* **Data Params**

  <_If making a post request, what should the body payload look like? URL Params rules apply here too._>

* **Success Response:**
  
  <_What should the status code be on success and is there any returned data? This is useful when people need to to know what their callbacks should expect!_>

* **Code:** 200 <br />
    **Content:** `{ id : 12 }`
 
* **Error Response:**

  <_Most endpoints will have many ways they can fail. From unauthorized access, to wrongful parameters etc. All of those should be liste d here. It might seem repetitive, but it helps prevent assumptions from being made where they should be._>

  * **Code:** 401 UNAUTHORIZED <br />
    **Content:** `{ error : "Log in" }`

  OR

  * **Code:** 422 UNPROCESSABLE ENTRY <br />
    **Content:** `{ error : "Email Invalid" }`

* **Sample Call:**

  <_Just a sample call to your endpoint in a runnable format ($.ajax call or a curl request) - this makes life easier and more predictable._> 

* **Notes:**

  <_This is where all uncertainties, commentary, discussion etc. can go. I recommend timestamping and identifying oneself when leaving comments here._> - Type some Markdown on the left
  - See HTML in the right
  - Magic
