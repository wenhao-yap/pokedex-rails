# Pokedex Rails App (with Postgres SQL)

For this exercise, we'll create a Rails app with Postgres database. The end result we want is a CRUD app for pokemon with data saved into a database.

## Getting Started

1. Fork and clone this repository to your computer
1. In the project directory run:
```
rails new ./ -d postgresql
```
1. To install dependencies, run:
```
bundle install
```
1. Create a new Postgres database by running:
```
rails db:create
```
1. Generate a model for `pokemon`
1. Create the pokemons table in your database
1. Seed data into the newly created pokemons table by running:
```
rails db:migrate
```
1. Command when you want to start your server:
```
rails server
``` 

## Deliverables

The deliverable is an app that has CRUD functionality on pokemon.

* GET `/` should return HTML page showing all pokemons currently in database (specifically in the pokemon table within the database)
* GET `/:id` (eg. `/2`) should return HTML page showing information about pokemon with primary ID 2 (read: primary ID, not `num` property)
* GET `/new` should return HTML page showing a form to create a new pokemon - upon submit, it should send POST request to `/`
* POST `/` should create a new pokemon and insert a new entry in the pokemon table, and should redirect to the home page `/`
* GET `/:id/edit` (eg. `/2/edit`) should return HTML page showing a form pre-populated with that pokemon's data - upon submit, it should send PUT request to `/:id`
* The `/:id/edit` HTML page should also have a "Delete" button that when clicked, will send a DELETE request to `/:id` to delete the current pokemon
* PUT `/:id` should update the data of the pokemon with the specified ID, and should redirect to the pokemon detail page `/:id`
* DELETE `/:id` should delete the entry of the pokemon with the specified ID, and should redirect to the home page `/`

### HINT

Refer to the gitbook materials for relevant commands and examples: https://wdi-sg.github.io/gitbook-2018/06-ruby-rails/rails-intro/readme.html
