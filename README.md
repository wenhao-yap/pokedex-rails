# Pokedex Rails App (with Postgres SQL)

For this exercise, we'll create a Rails app with Postgres database. The end result we want is a CRUD app for pokemon with data saved into a database.

## Getting Started

1. Fork and clone this repository to your computer

2. To generate a new Rails application, in the project directory run:
```
rails new ./ -d postgresql
```
3. To install dependencies, run:
```
bundle install
```
4. Create a new Postgres database by running:
```
rails db:create
```
5. Generate a model for `pokemon` and specify the table attributes
```
rails g model pokemon
```
6. To create your pokemons table in your database:
```
rails db:migrate
```
7. Seed data into the newly created pokemons table by running:
```
rails db:seed
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

### Bonus:
- Change your data model by adding a migration. (Look up the rails docs for running a `change table` migration.)
- Add a pokemon master who will `have many` pokemon. (This is different from a logged in user / you won't need login capability)
You can change the seed file as well to have a seed master who has pokemon, or you can start with an empty db.
Use nested routes to refer to the pokemons and their masters.

