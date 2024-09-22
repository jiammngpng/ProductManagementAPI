# Product Management API

## Overview
This is a simple .NET 8 Web API for managing products. It supports basic CRUD (Create, Read, Update, Delete) operations and is built using ASP.NET Core and Entity Framework Core.

## Features
- **GET /api/products**: Retrieve a list of all products.
- **GET /api/products/{id}**: Retrieve a single product by ID.
- **POST /api/products**: Create a new product.
- **PUT /api/products/{id}**: Update an existing product by ID.
- **DELETE /api/products/{id}**: Delete a product by ID.

## Getting Started

### Prerequisites
- [.NET 8 SDK](https://dotnet.microsoft.com/download/dotnet/8.0)
- [Postman](https://www.postman.com/downloads/) (for testing the API)
- SQL Server or SQLite for the database

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/jiammngpng/ProductManagementAPI.git
2. Navigate to the project directory:
   ```bash
   cd ProductManagementAPI
3. Update the database connection string in `appsettings.json` if necessary.

4. Run database migrations:
   ```bash
   dotnet ef database update
5. Start the application:
   ```bash
   dotnet run
After running the application, you will see the endpoint URL in the Git Bash console. Use this URL to access the API.

### Testing the API
You can use Postman to test the API endpoints. Here are some example requests:

#### Get All Products
- **Endpoint:** `GET <URL>/api/products`
- **Response:** A list of products in JSON format.

#### Get Product by ID
- **Endpoint:** `GET <URL>/api/products/{id}`
- **Response:** Details of the specified product.

#### Create a New Product
- **Endpoint:** `POST <URL>/api/products`
- **Body (JSON):**
    ```json
    {
    "name": "Product Name",
    "description": "Product Description",
    "price": 29.99,
    "image": "image_url_here"
    }
- **Response:** The created product with its ID.
#### Update an Existing Product
- **Endpoint:** `PUT <URL>/api/products/{id}`
- **Body (JSON):**
    ```json
    {
    "name": "Updated Product Name",
    "description": "Updated Description",
    "price": 39.99,
    "image": "updated_image_url_here"
    }
- **Response:** The updated product.

#### Delete a Product
- **Endpoint:** `DELETE <URL>/api/products/{id}`
- **Response:** Confirmation of deletion.

## Error Handling
The API provides appropriate HTTP status codes for various scenarios (e.g., 200 OK, 201 Created, 404 Not Found, 500 Internal Server Error).

## Contributing
Contributions are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the MIT License - see the [LICENSE](https://github.com/jiammngpng/ProductManagementAPI/blob/master/LICENSE.txt) file for details.
