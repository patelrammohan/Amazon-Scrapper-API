# Amazon Scraper API

Amazon Scraper API is a simple and powerful API to fetch product details, search results, reviews, and offers from Amazon using Node.js and Express.

## Features

- Fetch product details by product ID
- Get search results for a given query
- Retrieve product reviews
- Obtain offers for a specific product

## RapidAPI Deployment

This API is also available on the RapidAPI marketplace, allowing easy integration and usage by developers.
You can find it here- https://rapidapi.com/mram41614/api/amazon-scrapper-api3 on RapidAPI.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/amazon-scraper-api.git
    cd amazon-scraper-api
    ```

2. Install dependencies:
    ```bash
    npm install
    ```

3. Create a `.env` file to set your API key (if using environment variables):
    ```env
    PORT=5000
    ```

## Usage

1. Start the server:
    ```bash
    npm start
    ```

2. The API will be running on `http://localhost:5000`

## API Endpoints

### Welcome Message

- **GET /**

    Returns a welcome message.

    **Response:**
    ```json
    "Welcome to Amazon-Scrapper-API"
    ```

### Get Product Details

- **GET /products/:productId**

    Fetches details for a specific product by its ID.

    **Parameters:**
    - `productId` (required): The ID of the product.
    - `api_key` (required): Your ScraperAPI key.

    **Example:**
    ```bash
    GET /products/B08N5WRWNW?api_key=YOUR_API_KEY
    ```

### Get Search Results

- **GET /search/:searchQuery**

    Retrieves search results for a given query.

    **Parameters:**
    - `searchQuery` (required): The search query.
    - `api_key` (required): Your ScraperAPI key.

    **Example:**
    ```bash
    GET /search/laptop?api_key=YOUR_API_KEY
    ```

### Get Product Reviews

- **GET /products/:productId/reviews**

    Fetches reviews for a specific product by its ID.

    **Parameters:**
    - `productId` (required): The ID of the product.
    - `api_key` (required): Your ScraperAPI key.

    **Example:**
    ```bash
    GET /products/B08N5WRWNW/reviews?api_key=YOUR_API_KEY
    ```

### Get Product Offers

- **GET /products/:productId/offers**

    Retrieves offers for a specific product by its ID.

    **Parameters:**
    - `productId` (required): The ID of the product.
    - `api_key` (required): Your ScraperAPI key.

    **Example:**
    ```bash
    GET /products/B08N5WRWNW/offers?api_key=YOUR_API_KEY
    ```

## Error Handling

Errors are returned in JSON format. If an error occurs during the request, the response will contain the error details.

**Example:**
```json
{
    "message": "Error message here"
}
