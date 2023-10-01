# SuperHeroesNew
## Description

# Flask Code Challenge - Superheroes

For this assessment, you'll be working on an API for tracking heroes and their
superpowers.

In this repo, there is a Flask application with some features built out. There
is also a fully built React frontend application, so you can test if your API is
working.

Your job is to build out the Flask API to add the functionality described in the
deliverables below.

## Setup

To download the dependencies for the frontend and backend, run:

```sh
pipenv install
npm install --prefix client
```

There is some starter code in the `app/seed.py` file so that once you've
generated the models, you'll be able to create data to test your application.

You can run your Flask API on [`localhost:5555`](http://localhost:5555) by running:

```sh
python app.py
```

You can run your React app on [`localhost:4000`](http://localhost:4000) by running:

```sh
npm start --prefix client
```

You are not being assessed on React, and you don't have to update any of the React
code; the frontend code is available just so that you can test out the behavior
of your API in a realistic setting.

There are also tests included which you can run using `pytest -x` to check your work.

Depending on your preference, you can either check your progress by:

- Running `pytest -x` and seeing if your code passes the tests
- Running the React application in the browser and interacting with the API via
  the frontend
- Running the Flask server and using Postman to make requests

## Models

You need to create the following relationships:

- A `Hero` has many `Power`s through `HeroPower`
- A `Power` has many `Hero`s through `HeroPower`
- A `HeroPower` belongs to a `Hero` and belongs to a `Power`

Start by creating the models and migrations for the following database tables:

![domain diagram](domain.png)

Add any code needed in the model files to establish the relationships.

Then, run the migrations and seed file:

```sh
flask db upgrade
python app/seed.py
```

> If you aren't able to get the provided seed file working, you are welcome to
> generate your own seed data to test the application.
