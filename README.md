# Full-stack web developer challenge

In this test, you are expected to write a small web application to manage a list of Movies. Each movie has a name, release year and director. The test consists of two parts, a RESTful API as the **backend** and the Javascript based **frontend** application.

There is no need to create a PR back to this repository once completed, please provide a link to your project repository for review.

## Backend implementation

Use the following structure to model the data

```
class Director(Model):
    first_name = models.TextField()
    last_name = models.TextField()
```

```
class Movie(Model):
    name = models.TextField()
    release_year = models.IntegerField()
    director = models.ForeignKey(Director)
```

Implement the following API endpoints:

* **GET /movies/** - Returns a list of movies in the database in JSON format
* **GET /movies/{{id}}/** - Returns a detail view of the specified movie id. Nest director details in JSON format
* **GET /directors/** - Returns a list of directors in the database in JSON format
* **GET /director/{{id}}/** - Returns a detail view of the specified author id
* **POST /director/** - Creates a new director with the specified details - Expects a JSON body
* **POST /movie/** - Creates a new movie with the specified details - Expects a JSON body

_Optional_: You can go a step further by implementing API endpoints to update existing records if you like.

eg:
* **PUT /director/{{id}}** - Updates an existing director - Expects a JSON body
* **PUT /movie/{{id}}** - Updates an existing movie - Expects a JSON body

You are recommended to use **Python/Django** along with [**Django REST Framework**](http://www.django-rest-framework.org/) to implement your backend and API layer, but you are free to use a different language/framework/libraries you are comfortable with.


## Frontend implementation

Implement a small frontend application to consume the API you developed above.

The frontend should be able to show a list of names of the movies available in the database. Upon clicking the name of a movie on the list, the user should be navigated to a more detailed view of the selected movie, where they are presented with the year of release and the director details. You should also implement two forms where the user is able to create/update director and movies (using the POST and PUT endpoints)
You are recommended to use **ReactJS** to create the frontend, but you are free to use a different Javascript framework.

### Notes and recommendations

* The languages, frameworks and libraries mentioned are recommendations only, you are free to use whatever you are comfortable with.
* The project structure is up to you to decide
* You are recommended to use git commits in a logical manner to demonstrate the development progress
* Writing tests and adhering to development standards/conventions will let you gain extra points :)
