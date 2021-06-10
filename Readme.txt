This repository was made as part of Jose Salvatierra's "REST APIs with Flask and Python" course on Udemy.

Utilizing and testing the API was done through Postman.

The API can be accessed through https://smn48-restful-api.herokuapp.com/, though the home endpoint does not return any resources.

By sending a POST request to https:/register with a JSON containing a username and password, you will be registered as a user into the Postgresql database.

Sending the same username and password to /auth, you will obtain an JWT key that will allow for accessing individual items, assuming your information is found in the database.

Sending a GET request to /items or /stores will return a list of all of the resources of that type.

Sending a GET request to /item/<name> or /store/<name> will return a JSON regarding that resource.
*Sending a GET request to /item/<name> requires valid JWT authorization.

Sending a PUT request with a JSON containing a price and store_id to /item/<name> will update the values for that item, or create the item if it is not found.