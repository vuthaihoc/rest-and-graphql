# Scalable API Architecture

[![Codacy Badge](https://api.codacy.com/project/badge/Grade/bef9e90ff8d340a58bd307db645ce715)](https://app.codacy.com/app/ashokdey/rest-and-graphql?utm_source=github.com&utm_medium=referral&utm_content=knaxus/rest-and-graphql&utm_campaign=Badge_Grade_Dashboard)

This repository is a demostration of highly scalable & easily maintainable codebase architecture for both **REST & GraphQL API** interface.

![Banner](./__assets/banner.png)

## Tech Stack

- Node.js
- GraphQL
- MySQL

## Work Progress

- Upcoming APIs in this repo
  - User Registration
  - ACL
  - Admin Portal
  - Seller Portal
- Unit Testing
  - REST endpoints
  - GraphQL endpoints
- CI and CD

## Run locally

- Clone the repo
- `npm install`
- Setup a `.env` file at the root of the repo
- `npm run dev`
- GraphQL endpoint will be http://localhost:PORT/graphql

## Notes

- Contents of `.env` file

```env
PORT=8080
NODE_ENV = development
READ_DB_HOST = localhost
READ_DB_USER = root
READ_DB_PASSWORD = password
READ_DB_NAME = awesome_products
READ_DB_PORT = 3306
READ_DB_CONNECTION_LIMIT = 10
WRITE_DB_HOST = localhost
WRITE_DB_USER = root
WRITE_DB_PASSWORD = password
WRITE_DB_NAME = awesome_products
WRITE_DB_PORT = 3306
WRITE_DB_CONNECTION_LIMIT = 10
```

- Use the `SQL` file located in `resources` folder to create the database

- The source files are inside the /src folder. Let's define the roles of the folders inside /src

  - config: contains the .env files
  - controllers: contains the route handlers using methods inside ro  utes
  - db: contains the database connection logic
  - graphql: contains the resolvers and definitions
  - routes: contains the definition of the routes using services
  - services: contains the logic to fetch data from DB
  - utils: contains the globally used util functions

- As you can see, the codebase is organized as per the entities. What really helped me to scale here is the services folder, it is the real gem here
