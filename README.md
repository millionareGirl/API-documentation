# API-documentation
# Method Shop
***
Documentation of an API project by Group #4

  * **URL**: http://localhost:3000/api/

## Microservices
 ----
 ### CATEGORIES
 
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
 ### PRODUCTS
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
 ### USER
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
