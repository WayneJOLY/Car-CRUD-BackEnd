# Car  API

## Description
This API allows for the management of cars, including the creation, reading, updating, and deletion (CRUD) of car records. It uses Sequelize as an ORM to interact with the database.

## Data Model
The Car model represents a car and has the following properties:
- **brand** (String, required): The brand of the car.
- **model** (String, required): The model of the car.
- **color** (String, required): The color of the car.
- **year** (Integer, required): The manufacturing year of the car.
- **price** (Float, required): The price of the car.
- **image** (String, optional): A URL or path to an image of the car.

- const Car = sequelize.define('Car', {
  brand: {
    type: Sequelize.STRING,
    allowNull: false
  },
  model: {
    type: Sequelize.STRING,
    allowNull: false
  },
  color: {
    type: Sequelize.STRING,
    allowNull: false
  },
  year: {
    type: Sequelize.INTEGER,
    allowNull: false
  },
  price: {
    type: Sequelize.FLOAT,
    allowNull: false
  },
  image: {
    type: Sequelize.STRING,
    allowNull: true
  }
});



# Endpoints

1. **Get All Cars**
   - **Method**: `GET`
   - **Route**: `/api/cars`
   - **Description**: Returns a list of all cars.

2. **Get Car by ID**
   - **Method**: `GET`
   - **Route**: `/api/cars/:id`
   - **Description**: Returns a specific car by its ID.

3. **Create a New Car**
   - **Method**: `POST`
   - **Route**: `/api/cars`
   - **Description**: Creates a new car record.
   - **Request Body**:
     ```json
     {
       "brand": "Car Brand",
       "model": "Car Model",
       "color": "Car Color",
       "year": 2023,
       "price": 25000.00,
       "image": "http://example.com/image.jpg"
     }
     ```



4. **Update an Existing Car**
   - **Method**: `PUT`
   - **Route**: `/api/cars/:id`
   - **Description**: Updates an existing car record by its ID.
   - **Request Body**:
     ```json
     {
       "brand": "string",
       "model": "string",
       "color": "string",
       "year": integer,
       "price": float,
       "image": "string" // optional
     }
     ```

5. **Delete a Car**
   - **Method**: `DELETE`
   - **Route**: `/api/cars/:id`
   - **Description**: Deletes a car record by its ID.

## Example Response

## Frontend Repository and Video Demostration

For those interested in exploring the frontend of this Car Management API project, you can find the source code in a separate repository. This frontend application provides a user-friendly interface to interact with the API, allowing users to manage car records seamlessly.

You can access the frontend repository ![here](www.github.com/WayneJOLY/Car-CRUD-FrontEnd).

Additionally, we have created a video tutorial that walks you through the setup and usage of both the API and the frontend application. Check it out 
[![VIDEO](./Car%20CRUD.mp4)]. Enjoy!

**Get All Cars**

```json
[
  {
    "id": 1,
    "brand": "Toyota",
    "model": "Corolla",
    "color": "Red",
    "year": 2020,
    "price": 20000.00,
    "image": "http://example.com/image1.jpg"
  },
  {
    "id": 2,
    "brand": "Honda",
    "model": "Civic",
    "color": "Blue",
    "year": 2021,
    "price": 22000.00,
    "image": null
  }
]
````


