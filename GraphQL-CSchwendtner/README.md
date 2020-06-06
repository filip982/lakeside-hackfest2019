# lakeside-hackfest2019
DevOps conference in Klagenfurt, Lakeside Spitz am Wörthersee, organised by Dynatrace.

## Christian Schwendtner Links
* https://github.com/cschwendtner
* https://twitter.com/CSchwendtner

## GraphQL – forget (the) REST? A query language for your API - Christian Schwendtner
*Trainer & Consultant, devinitive*

**Slides:** [GraphQL – forget (the) REST? - Slides](GraphQL-CSchwendtner-slides.pdf)

Christian Schwendtner is a passionate software architect and developer. He is an expert with longstanding experience in web development and Microsoft technologies. GraphQL is a query language for your API and is used by Facebook, GitHub and others as an alternative to RESTful web services. 

### GraphQL
* A query language for your API
* is NOT A query language for graph databases
* Specification
* Schema (domain specific)
* GraphQL Operations
	* Query -> Read
	* Mutation -> Write
	* Subscription -> Notification (“Event”)
* Talked about
	* Fields - how to structure your requests using fields
	* Arguments - additional data for fields
	* Aliases - prettify your code
	* Fragments - group and name your repetitive code for request 
	* Variables - we can put variables into our requests, when defining it
	* Validation / Errors - all errors are grouped into one list and location is inside error object
	* Introspection - Apollo client does it, cool thing to verify all requests

### Schema
* we define our own schema and that is the core of GraphQL where everything starts
* Cheat sheet: [GitHub - sogko/graphql-schema-language-cheat-sheet: GraphQL Shorthand Notation Cheat Sheet](https://github.com/sogko/graphql-schema-language-cheat-sheet)

### Resolvers
* every field has it’s own resolver
* if it’s not provided for every field then it’s auto-generated by the system
* resolvers are just functions

### Apollo Server
* Start: https://www.apollographql.com/docs/apollo-ser 
* Terminal: `npm install apollo-server graphql`

### DataLoader
* fetching layer to provide a simplified and consistent API over various remote data sources
* It works like Caching & Batching but not in original way like we use to 

### Pro’s
* much simpler to implement than REST
* could handle multiple sources of any kind
* it’s an abstraction layer
* works great with Microservices and components
* Apollo is a great addition and it’s always recommended

### Con’s
* Caching is not working like with REST
* Best use is for “Facebook” apps like usage, so when partial response are enough
* It’s not for simple usage and it’s not the quickest solution
---

## Instructions
* do `npm install`
* go to 010-graphql-server
* edit server.js
* start it with: ` npx nodemon server.js`
* now it will watch continuosly for changes and update the playground
* open in Chrome GraphQL at address: `localhost:4000`