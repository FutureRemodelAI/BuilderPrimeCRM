Leads Management API

--> Overview

The Leads Management API is a RESTful API built with Flask and SQLAlchemy for managing leads in a CRM system. It provides endpoints for creating, retrieving, updating, and deleting leads, along with Swagger documentation for easy testing and integration.

--> Features

- Create Lead: Add new leads to the system.
- List Leads: Retrieve a list of leads with optional filtering.
- Update Lead: Modify existing lead information.
- Delete Lead: Remove leads from the system.
- API Key Authentication: Secure access to the API using an API key.

--> Technologies Used

- Flask: A lightweight WSGI web application framework.
- Flask-SQLAlchemy: An extension for Flask that adds support for SQLAlchemy.
- Flask-Migrate: An extension that handles SQLAlchemy database migrations for Flask applications.
- Flask-RESTx: An extension for building REST APIs in Flask.
- PostgreSQL: A powerful, open-source object-relational database system.
- Python Dotenv: A module to load environment variables from a `.env` file.

--> Getting Started

--> Prerequisites

- Python 3.6 or higher
- PostgreSQL database
- pip (Python package installer)

--> Installation

1. Clone the repository:

   ```bash
   https://github.com/FutureRemodelAI/CrmIntegrationService.git

   ```

2. Create a virtual environment (optional but recommended):

   ```bash
   python -m venv venv
   source venv/bin/activate   On Windows use `venv\Scripts\activate`
   ```

3. Install the required packages:

   ```bash
   pip install -r requirements.txt
   ```

4. Set up the environment variables:
   Create a `.env` file in the root directory with the following content:

   ```plaintext
   FLASK_APP=run.py
   FLASK_ENV=development
   FLASK_DEBUG=True
   DB_USER=your_db_user
   DB_PASSWORD=your_db_password
   DB_HOST=localhost
   DB_NAME=leads_db
   SECRET_KEY=your-secret-key
   API_KEY=your-api-key
   ```

5. Initialize the database:
   ```bash
   flask db init
   flask db migrate -m "Initial migration"
   flask db upgrade
   ```

--> Running the Application

To start the application, run:

```bash
flask run
```

The API will be available at `http://127.0.0.1:5000/api`.

--> API Documentation

The API is documented using Swagger. You can access the documentation at:

```
http://127.0.0.1:5000/swagger
```

--> API Endpoints

- POST /api/clients/v1: Create a new lead
- GET /api/clients: Retrieve a list of leads
- PUT /api/clients/v1/{lead_id}: Update an existing lead
- DELETE /api/clients/v1/{lead_id}: Delete a lead

--> Authentication

To access the API, you need to provide an API key. Include the API key in the request headers as follows:

```
x-api-key: your-api-key
```