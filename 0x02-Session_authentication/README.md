# Simple API

A lightweight HTTP API designed for interacting with the `User` model.

## Project Structure

### `models/`
- **`base.py`**: Base class for all models, managing serialization to files.
- **`user.py`**: User model implementation.

### `api/v1`
- **`app.py`**: Main entry point of the API.
- **`views/index.py`**: Contains basic API endpoints (`/status` and `/stats`).
- **`views/users.py`**: Manages user-related endpoints.

## Setup Instructions

To install the required dependencies, run:
```bash
pip3 install -r requirements.txt
```

## Running the API

To start the API, use:
```bash
API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```

## Available Endpoints

- **`GET /api/v1/status`**: Checks the API status.
- **`GET /api/v1/stats`**: Provides statistics about the API.
- **`GET /api/v1/users`**: Retrieves a list of all users.
- **`GET /api/v1/users/:id`**: Fetches details of a specific user by ID.
- **`DELETE /api/v1/users/:id`**: Deletes a user by ID.
- **`POST /api/v1/users`**: Creates a new user. Accepts JSON parameters:
  - `email` (required)
  - `password` (required)
  - `last_name` (optional)
  - `first_name` (optional)
- **`PUT /api/v1/users/:id`**: Updates a user's `last_name` or `first_name` by ID.
