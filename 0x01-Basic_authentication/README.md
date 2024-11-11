# Simple API

A straightforward HTTP API designed for interacting with the `User` model.

## Project Structure

### `models/`

- **`base.py`**: The foundational class for all API models, managing serialization to file.
- **`user.py`**: Represents the user model.

### `api/v1`

- **`app.py`**: Main entry point for the API.
- **`views/index.py`**: Contains basic endpoints: `/status` and `/stats`.
- **`views/users.py`**: Manages all user-related endpoints.

## Installation

Ensure all required packages are installed by running:
```bash
pip3 install -r requirements.txt
```

## Running the API

Start the API server with:
```bash
API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
```

## Available Routes

- **`GET /api/v1/status`**: Checks the API's status.
- **`GET /api/v1/stats`**: Provides statistical information about the API.
- **`GET /api/v1/users`**: Retrieves a list of users.
- **`GET /api/v1/users/:id`**: Fetches a specific user by ID.
- **`DELETE /api/v1/users/:id`**: Deletes a user by ID.
- **`POST /api/v1/users`**: Creates a new user with JSON parameters:
  - `email` (required)
  - `password` (required)
  - `first_name` (optional)
  - `last_name` (optional)
- **`PUT /api/v1/users/:id`**: Updates a user by ID with JSON parameters:
  - `first_name`
  - `last_name`

