# Restaurant Backend API

This is a backend API for a restaurant management system, providing CRUD (Create, Read, Update, Delete) functionality for managing restaurant data.

## Features

- **Restaurant Management**: Add, view, update, and delete restaurant details.
- **Menu Management**: Add, view, update, and delete menu items for each restaurant.
- **Order Management**: Place and manage orders for restaurant items.

## Technologies Used

- Node.js
- Express.js
- MongoDB (with Mongoose)
- JSON Web Tokens (JWT) for authentication

## Getting Started

### Prerequisites

- Node.js and npm installed on your machine
- MongoDB installed and running locally or accessible via a remote connection

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/restaurant-backend.git
----------------------------------------------------------------------------------------------
Install dependencies
cd restaurant-backend
npm install
----------------------------------------------------------------------------------------------------
Set up environment variables
PORT=3000
MONGODB_URI=mongodb://localhost:27017/restaurant
JWT_SECRET=your_jwt_secret
------------------------------------------------------------------------------------------------------
Start server
npm start
-------------------------------------------------------------------------------------------------------


API Endpoints
Restaurants
GET /restaurants: Get all restaurants
GET /restaurants/:id: Get restaurant by ID
POST /restaurants: Create a new restaurant
PUT /restaurants/:id: Update restaurant details
DELETE /restaurants/:id: Delete a restaurant
Menu Items
GET /restaurants/:restaurantId/menu: Get menu items for a restaurant
GET /restaurants/:restaurantId/menu/:itemId: Get menu item by ID
POST /restaurants/:restaurantId/menu: Add a new menu item
PUT /restaurants/:restaurantId/menu/:itemId: Update a menu item
DELETE /restaurants/:restaurantId/menu/:itemId: Delete a menu item
Orders
GET /orders: Get all orders
GET /orders/:id: Get order by ID
POST /orders: Place a new order
PUT /orders/:id: Update order status
DELETE /orders/:id: Delete an order
Authentication
Authentication is required for creating, updating, and deleting restaurants, menu items, and orders.
Use JWT token obtained from the /login endpoint to authenticate requests.

---------------------------------------------------------------------------------------------------------------------------------

Sample User Authentication
POST /login: Authenticate user and generate JWT token
Request Body:
{
  "email": "user@example.com",
  "password": "password123"
}
Response:
{
  "token": "your_jwt_token"
}
:)
