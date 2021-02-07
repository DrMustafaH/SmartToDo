LHL Node Skeleton
=========

## Project Setup

The following steps are only for _one_ of the group members to perform.

1. Create your own copy of this repo using the `Use This Template` button, ideally using the name of your project. The repo should be marked Public
2. Verify that the skeleton code now shows up in your repo on GitHub, you should be automatically redirected
3. Clone your copy of the repo to your dev machine
4. Add your team members as collaborators to the project so that they can push to this repo
5. Let your team members know the repo URL so that they use the same repo (they should _not_ create a copy/fork of this repo since that will add additional workflow complexity to the project)


## Getting Started

1. Create the `.env` by using `.env.example` as a reference: `cp .env.example .env`
2. Update the .env file with your correct local information 
  - username: `labber` 
  - password: `labber` 
  - database: `midterm`
3. Install dependencies: `npm i`
4. Fix to binaries for sass: `npm rebuild node-sass`
5. Reset database: `npm run db:reset`
  - Check the db folder to see what gets created and seeded in the SDB
7. Run the server: `npm run local`
  - Note: nodemon is used, so you should not have to restart your server
8. Visit `http://localhost:8080/`

## Warnings & Tips

- Do not edit the `layout.css` file directly, it is auto-generated by `layout.scss`
- Split routes into their own resource-based file names, as demonstrated with `users.js` and `widgets.js`
- Split database schema (table definitions) and seeds (inserts) into separate files, one per table. See `db` folder for pre-populated examples. 
- Use the `npm run db:reset` command each time there is a change to the database schema or seeds. 
  - It runs through each of the files, in order, and executes them against the database. 
  - Note: you will lose all newly created (test) data each time this is run, since the schema files will tend to `DROP` the tables and recreate them.

## Dependencies

- Node 10.x or above
- NPM 5.x or above
- PG 6.x

## USER STORIES
They have the form: As a ___, I want to _, because ____.

As a user, I want to be able to create a todo list which categorizes my selections based on one of 4 categories because I thrive on being organized.
As a user, I want to be able to see each individual list on its own, or a combination of lists together because sometimes I want to focus on specific tasks.
As a user, I want to be able to change the category of a submission if it is incorrect because technology isn't perfect
As a user, I want to be able to log in, log out, and change my profile because I want to customize my space.
As a user, I shouldn't be able to access other user's lists because I do not own those todo lists.
As a user, I shouldn't be able to change someone else's profile or log in as them because I do not own their user profile.
If I am not logged in, I should not be able to do much at all because I need to be logged in for the app to work.

## ROUTES

/todos | GET
/todos | POST
/todos:id | GET 
/todos:id/edit | GET
/todos:id | DELETE




















