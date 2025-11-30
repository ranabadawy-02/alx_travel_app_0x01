# alx_travel_app_0x01

This project extends the original `alx_travel_app_0x00` by adding fully functional CRUD API endpoints for Listings and Bookings using Django REST Framework. All endpoints are implemented using DRF ViewSets and registered through a router under the `/api/` base path. The project also includes Swagger documentation for interactive API testing.

## Features
- CRUD API for Listings and Bookings
- Implemented using Django REST Framework ModelViewSet
- Router-based endpoint registration
- RESTful API structure under /api/
- Supports Swagger UI API documentation
- Endpoints tested with Postman

## API Endpoints

### Listings Endpoints
- GET /api/listings/ — List all listings
- POST /api/listings/ — Create a new listing
- GET /api/listings/<id>/ — Retrieve a listing
- PUT /api/listings/<id>/ — Update a listing
- PATCH /api/listings/<id>/ — Partially update a listing
- DELETE /api/listings/<id>/ — Delete a listing

### Bookings Endpoints
- GET /api/bookings/ — List all bookings
- POST /api/bookings/ — Create a new booking
- GET /api/bookings/<id>/ — Retrieve a booking
- PUT /api/bookings/<id>/ — Update a booking
- PATCH /api/bookings/<id>/ — Partially update a booking
- DELETE /api/bookings/<id>/ — Delete a booking

## Running the Project

1. Install dependencies:
   pip install -r requirements.txt

2. Apply migrations:
   python manage.py migrate

3. Start the server:
   python manage.py runserver

The API will be available at:
http://localhost:8000/api/

Swagger documentation will be available at:
http://localhost:8000/swagger/

## Testing the API with Postman

### Example: Create a Listing
POST /api/listings/

{
  "title": "Modern Apartment",
  "description": "A clean and sunny apartment in the city center.",
  "price": 150
}

### Example: Create a Booking
POST /api/bookings/

{
  "listing": 1,
  "name": "John Doe",
  "email": "john@example.com",
  "check_in": "2025-05-20",
  "check_out": "2025-05-25"
}

## Project Structure

alx_travel_app/
    listings/
        views.py
        urls.py
        serializers.py
        models.py
    alx_travel_app/
        settings.py

## Notes
- All endpoints follow REST conventions.
- ViewSets eliminate boilerplate and allow clean, reusable API logic.
- Swagger ensures easy documentation and endpoint exploration.
