# Project Webshop
Project Webshop is a simple webshop application based on the wideline known MERN-stack (MongoDB, Express, React, NodeJS).
React interacts with our own REST API to gather the required data like products, product categories, orders, customers... and give a clean visual representation of this data.

*The features of the webshop are aligned with the requirements I got from University College, user authentication not being on of them.*

## Deploy
Project Webshop is currently hosted on [Heroku](https://projectwebshop.herokuapp.com/).
*Note: The root of the project had to contain an additional package.json to be able to harmlessly deploy it to Heroku.*
*For some bizar reason the '+' sign in the shopping cart view doesn't want to work, although the code being 100% correct.*

## Project overview
### Backend
- Database running on MongoDB's cloud solution Atlas
- REST API **GET** routes
    - '/product': returns an array of all Product objects in JSON format
    - '/order/(id)': returns an Order object for specified order id in JSON format
    - '/order/(id)/products': returns an array of Product objects for specified order id in JSON format
    - '/user/(id)': returns a User object for specified user id in JSON format
    - '/categories/:id': returns a Category object for specified category id in JSON format
- REST API **POST** routes
    - '/order': Creates a new Order in database + appropriate Order Lines and returns the new order_id in JSON format
    - '/user/new': Creates a new User/Customer in database and returns new customer_id in JSON format

### Frontend
- React in combination with React-Bootstrap ensures a simple but clean design
- Some of the possibilities for the user:
    - Get detailed product specifications
    - Add / Remove products to wishlist
    - Add / Remove products to shopping cart
    - Confirm a (virtual) order by providing relevant details
    - Get a (virtual) order overview after confirming an order