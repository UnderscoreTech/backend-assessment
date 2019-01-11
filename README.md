# Lottery

You are building your own lottery.
You will build an API that can:
- allow a user to buy a lottery ticket
- draw a winner
- validate a ticket

## Endpoints

### Buying a ticket
Create an endpoint that allows a user to "buy" a lottery ticket.
When buying a ticket the user specifies how much he/she wants to pay for
the ticket. The api should return a non-guessable token that is unique
for the bought lottery.

### Drawing a winner
Create an endpoint that returns the token of the winning lottery ticket.
Once a winning lottery ticket has been chosen, the lottery should be
closed. I.e. no new tickets can be bought and no other tickets can win the
lottery.

The chance of a ticket winning the lottery should be proportional to the
price paid for that lottery. E.g. if $3.75 is paid for ticket-01 and
$5.25 is paid for ticket-02 (and no other tickets are sold), then the
chance of ticket-02 winning the lottery should be 5.25/9.

### Validating a ticket
Create an endpoint that accepts a ticket token and returns true if the
token corresponds to the winning lottery ticket, else false.

## Programming Language
The API can be written in any programming language.

## Storage
Use a database of your choice to store and retrieve the data used in your API.
Your documentation should be accompanied with an export of the database
schema.

## Documentation
### Instructions
Provide instructions on how to build and run your API.
Include a list of required dependencies.

#### API
The source code should be accompanied with documentation on how to use
your API.
For each endpoint provide:
- the request method
- the request url (including any route or query parameters)
- a list of request headers, if any
- the request body, if necessary
- the response body and status code. If there are multiple possible
responses explain when each response will occur

#### Database
Provide an export of your database schema.

## Extra credits
The sections below are optional extensions of the lottery API.

### Statistics
Add an endpoint that returns statistics about the tickets that have been bought.

### Listing tickets
Create an endpoint that returns the bought tickets.

### User & admin endpoints
Divide your endpoints in a group of user endpoints and a group of admin
endpoints.
The user endpoints should:
- allow a user to buy a lottery ticket
- validate a ticket

The admin endpoints should:
- draw a winner
- return statistics (if implemented)
- list the tickets (if implemented)

Protect your admin endpoints with _Basic access authentication_.

### Multiple lotteries
Extend your API such that it supports multiple lotteries.

### Docker
Add a Dockerfile that runs your API.
