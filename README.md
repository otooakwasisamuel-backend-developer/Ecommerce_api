# E-commerce API

This is a RESTful API for an e-commerce platform. It provides endpoints for managing products, categories, users, and orders.

## API Endpoints

### Products

*   **POST /api/products**
    *   Adds a new product.
    *   Requires authentication as a `manager`.
*   **GET /api/products**
    *   Gets a list of all products.
*   **GET /api/products/:id**
    *   Gets a single product by its ID.
*   **PUT /api/products/:id**
    *   Updates a product by its ID.
    *   Requires authentication.
*   **DELETE /api/products/:id**
    *   Deletes a product by its ID.
    *   Requires authentication.

### Categories

*   **POST /api/categories**
    *   Adds a new category.

### Users

*   **POST /api/users/register**
    *   Registers a new user.
*   **POST /api/users/login**
    *   Logs in a user.
*   **PATCH /api/users/:id**
    *   Updates a user by their ID.
*   **GET /api/users/me**
    *   Gets the authenticated user's profile.
    *   Requires authentication.

### Orders

*   **POST /api/orders**
    *   Creates a new order.
    *   Requires authentication.
*   **GET /api/orders**
    *   Gets a list of all orders.
    *   Requires authentication as a `manager`.
*   **GET /api/my-orders**
    *   Gets a list of the authenticated user's orders.
    *   Requires authentication.
*   **GET /api/orders/:id**
    *   Gets a single order by its ID.
    *   Requires authentication.
*   **PATCH /api/orders/:id/status**
    *   Updates the status of an order.
    *   Requires authentication as a `manager`.
*   **DELETE /api/orders/:id**
    *   Deletes an order by its ID.

## Setup and Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/faivich-api.git
    ```
2.  **Install dependencies:**
    ```bash
    npm install
    ```
3.  **Create a `.env` file** in the root of the project and add the following environment variables:
    ```
    MONGO_URL=<your-mongodb-connection-string>
    PORT=3000
    JWT_SECRET_KEY=<your-jwt-secret-key>
    ```

## Running the Application

*   **Development mode:**
    ```bash
    npm run dev
    ```
*   **Production mode:**
    ```bash
    npm start
    ```

## Technologies Used

*   **Node.js**
*   **Express**
*   **MongoDB**
*   **Mongoose**
*   **JSON Web Tokens (JWT)**
*   **Bcrypt**
*   **Joi**
*   **Multer**
*   **Cloudinary**
*   **Nodemailer**
