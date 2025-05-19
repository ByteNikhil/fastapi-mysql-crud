# FastAPI CRUD Application

A simple CRUD application built with FastAPI and MySQL for managing users and items.

## Setup & Installation

1. **Clone the repository**
```bash
git clone <repository-url>
cd CRUD
```

2. **Create virtual environment**
```bash
python -m venv venv
.\venv\Scripts\activate
```

3. **Install dependencies**
```bash
pip install -r requirements.txt
```

4. **Configure MySQL**
- Create a database named `crud_db`
- Update database connection string in `app/database.py`

## Project Structure
```
CRUD/
├── app/
│   ├── main.py         # FastAPI app and routes
│   ├── database.py     # Database configuration
│   ├── models.py       # SQLAlchemy models
│   ├── schemas.py      # Pydantic schemas
│   └── crud.py        # CRUD operations
└── requirements.txt
```

## API Endpoints

### Users
- `POST /users/` - Create user
- `GET /users/` - Get all users
- `GET /users/{id}` - Get user by ID
- `PUT /users/{id}` - Update user
- `DELETE /users/{id}` - Delete user

### Items
- `POST /users/{user_id}/items/` - Create item
- `GET /items/` - Get all items
- `GET /items/{id}` - Get item by ID
- `PUT /items/{id}` - Update item
- `DELETE /items/{id}` - Delete item

## Running the Application

```bash
uvicorn app.main:app --reload
```

Access the API documentation at: http://localhost:8000/docs

## Dependencies
- FastAPI
- SQLAlchemy
- PyMySQL
- Pydantic
- uvicorn