# Bookstore API

This is the Bookstore API, a Django-based web API for managing books, authors, and categories. It provides various endpoints for interacting with the bookstore's data.

## Table of Contents

- [Overview](#overview)
- [Bookstore API Documentation](#bookstore-api-documentation)
- [Setup Instructions](#setup-instructions)
- [Contributing](#contributing)
- [License](#license)

## Overview

The Bookstore API allows you to perform CRUD (Create, Read, Update, Delete) operations on books, authors, and categories. It also includes user registration and authentication features. You can use this API to build applications like online bookstores, library management systems, and more.

## Bookstore API Documentation

For detailed information on how to use the API, refer to the [API Documentation](#bookstore-api-documentation) section in the [API.md](API.md) file.

## Setup Instructions

Follow these instructions to set up and run the Bookstore API locally.

### Prerequisites

Before you begin, ensure you have met the following requirements:

- Python 3.6+
- Django and Django REST framework installed. You can install them using pip:

```bash
pip install django djangorestframework





 # Bookstore API Documentation

This API documentation provides details about the endpoints, request methods, authentication, and usage of the Bookstore API.

## Authentication

To access certain endpoints, you need to be authenticated. Use the following endpoint to log in and obtain an authentication token:

- **UserLoginView**
  - `POST /login/`: Log in and obtain an authentication token.

### Endpoints

#### Author Endpoints

- **AuthorViewSet**
  - `GET /authors/`: List all authors.
  - `POST /authors/`: Create a new author.
  - `GET /authors/{id}/`: Retrieve an author by ID.
  - `PUT /authors/{id}/`: Update an author by ID.
  - `DELETE /authors/{id}/`: Delete an author by ID.

#### Category Endpoints

- **CategoryViewSet**
  - `GET /categories/`: List all categories.
  - `POST /categories/`: Create a new category.
  - `GET /categories/{id}/`: Retrieve a category by ID.
  - `PUT /categories/{id}/`: Update a category by ID.
  - `DELETE /categories/{id}/`: Delete a category by ID.

#### Book Endpoints

- **BookViewSet**
  - `GET /books/`: List all books with pagination and filtering.
  - `POST /books/`: Create a new book.
  - `GET /books/{id}/`: Retrieve a book by ID.
  - `PUT /books/{id}/`: Update a book by ID.
  - `DELETE /books/{id}/`: Delete a book by ID.

- **BookDetailView**
  - `GET /books/{id}/detail/`: Retrieve a book by ID.

- **BookCreateView**
  - `POST /books/create/`: Create a new book.

- **BookListView**
  - `GET /books/list/`: List all books with authors and categories.

#### User Endpoints

- **UserRegistrationView**
  - `POST /registration/`: Register a new user.

### Pagination and Filtering

- Pagination is applied to the `GET /books/` endpoint with a default page size of 10.
- Filtering is available based on the book's category and author's name.

### Swagger Auto Schema

- The `@swagger_auto_schema` decorator is used to provide detailed descriptions for each endpoint, including request/response formats and operation descriptions.

### Error Handling

- The code handles validation errors and returns appropriate error responses.

To access authenticated endpoints, include the obtained authentication token in your request headers.

## Usage

To use the API, follow the authentication process and make requests to the relevant endpoints based on your requirements. Be sure to check the Swagger or drf-yasg-generated documentation for detailed request/response formats and examples.
