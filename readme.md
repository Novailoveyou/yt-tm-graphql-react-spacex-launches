# GraphQL With React & Apollo

## About

This is me following Brad Traversy's youtube video series:

1. [Part One - Express GraphQL Server](https://youtu.be/SEMTj8w04Z8)
2. [Part Two - React & Apollo Setup](https://youtu.be/-XwkFm5a9lw)
3. [Part Three - Finishing The App](https://youtu.be/DKzprvzbS14)
4. [Part Four - Simple Heroku Deploy](https://youtu.be/ok6bu-3XRA8)

Year 2021

## Quick Start

```zsh
# Install dependencies (server & client)
npm install
cd client && npm install

# Run server & client (:3000 & :5000)
npm run dev

# Server only (:5000)
npm run server

# Client only (:3000)
npm run client

# Build for production (Builds into server ./public)
cd client && npm run build

# Graphiql - http://localhost:5000/graphql
```

## Graphql queries

Get some info on launches & rocket

```graphql
{
  launches {
    flight_number,
    mission_name,
    launch_year,
    launch_success,
    launch_date_local,
    rocket {
      rocket_id,
      rocket_name,
      rocket_type
    }
  }
}
```

Get launch of particular flight_number

```graphql
{
  launch(flight_number: 2) {
    mission_name,
    launch_year,
    launch_success,
    rocket{
      rocket_name
    }
  }
}
```
