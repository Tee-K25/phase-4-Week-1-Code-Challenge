# Superheroes Web Application

## Description

Superheroes is a web application that showcases superheroes and their various powers. A front end with react lets users interact with the application backend built using Flask. Users can view all the heroes and powers, edit the description of powers and even add new associations between a hero and a power.

## Prerequisites

You need to have the following installed:
- Python 3.10 or later.
- Visual Studio Code or an IDE of your choice.
- Web Browser of your choice.
- Postman or Insomnia

## Setup

Instructions on how to get the project up and running.

```bash
# Clone the repository
git clone git@github.com:Tee-K25/phase-4-Week-1-Code-Challenge.git

# Navigate to the directory
cd Phase-4-Week-1-Code-Challenge

# Install Python dependencies, activate the virtual environment and run the server
pipenv install && pipenv shell
cd server
python app.py

# Install react dependencies and start the server
cd client
nvm use 16.20.2
npm install
npm start
```

## API Endpoints

* Use Postman or Insomnia to test out the endpoints.

### GET /heroes

* Url: http://127.0.0.1:5555/heroes

Returns JSON data in the format below:

```json
[
  { "id": 1, "name": "Kamala Khan", "super_name": "Ms. Marvel" },
  { "id": 2, "name": "Doreen Green", "super_name": "Squirrel Girl" },
  { "id": 3, "name": "Gwen Stacy", "super_name": "Spider-Gwen" }
]
```

### GET /heroes/:id

* Url: http://127.0.0.1:5555/heroes/1

If the `Hero` exists, it returns JSON data in the format below:

```json
{
  "id": 1,
  "name": "Kamala Khan",
  "super_name": "Ms. Marvel",
  "powers": [
    {
      "id": 1,
      "name": "super strength",
      "description": "gives the wielder super-human strengths"
    },
    {
      "id": 2,
      "name": "flight",
      "description": "gives the wielder the ability to fly through the skies at supersonic speed"
    }
  ]
}
```

### GET /powers

* Url: http://127.0.0.1:5555/powers

Returns JSON data in the format below:

```json
  {
    "id": 1,
    "name": "super strength",
    "description": "gives the wielder super-human strengths"
  }
```

### GET /powers/:id

* Url: http://127.0.0.1:5555/powers/1

Returns JSON data in the format below:

```json
{
  "id": 1,
  "name": "super strength",
  "description": "gives the wielder super-human strengths"
}
```

### PATCH /powers/:id
* Url: http://127.0.0.1:5555/powers/1
* Use the patch method in Postman to edit powers' descriptions. 

```json
{
  "description": "Updated description"
}
```

### POST /hero_powers
* Url: http://127.0.0.1:5555/hero_powers
* Use the post method in Postman to add a new hero_power object.

Create a new `HeroPower` that is associated with an
existing `Power` and `Hero`.

```json
{
  "strength": "Average",
  "power_id": 1,
  "hero_id": 3
}
```

## Browser Interaction (Front-End)

After running npm start to begin the react app, you will be redirected to your web browser where you can test out the client side of the 
application. All the routes are included and you can manipulate the API with various methods and interactions.

## Authors
Tony Kiplagat- tony.kiplagat@moringaschool.com



