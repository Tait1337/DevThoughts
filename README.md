- News
- Coding Best Practics
  - General
  - Configuration
  - Security
  - Communication
  - UI
  - Backend
  - Testing
  - Deployment
  - Monitoring
  - Frameworks
    - Spring
    - Angular
- Code Templates
  - General
  - Configuration
  - Security
  - Communication
  - UI
  - Backend
  - Testing
  - Deployment
  - Monitoring
  - Frameworks
    - Spring
    - Angular
- Architecture Pattern
  - Domain Driven Design (DDD)
  - Clean Code
  - arc42
- Design Pattern
  - Gang of four

# News
- Want to change some source code on GitHub but have no local IDE running? Simply use Gitpod to start an Visual Code based online IDE directly from the GitHub repository of interest: http://gitpod.io/#<GitHub repository url>


# Coding Best Practics
This Chapter focus on best practics about writing source code.

## General
-	Whenever possible use existing Pattern and Standards within your System Components. Note: This doesn't mean that you should use common Frameworks. Standards and Pattern should have a non Framework/Library focus.
- Try to achieve Clean Code with KISS, YAGNI and DRY. Always do a refactoring before completion of work.
- Don't use Developer Teams with more than 6 Persons.
-	Highly automate all your tasks e.g. builds, tests and deployments.
- Try to reduce complexity by building solutions that (a) focus on a low number of external dependencies and (b) solves only the existing requirements and not more predicted ones.
-	Document everything to the extent that each anyone can familiarize themselves with the topic shortly
- Cover 'Not Null' Design -> @NonNullByDefault @Nullable
- Never hide potential errors -> own exceptions, allow nulls, empty collections
- Use Modules -> Java and Maven for seperation
-	Use packages -> for unterstanding
- Cover aspects of non-blocking / multithreading: use only immutable objects and threadsafe classes

## Configuration
-	Externalize all your configuration f.e. via propertyfiles.
-	Make it possible to overwrite configurations after deployment.

## Security
-	Use proofen external libraries and applications for solving security requirements.
- Focus on security solutions that are transparent to the application e.g. Database internal encryption, Transportlayer security like HTTPS.
- Implement validation checks	always in backend. In frontend you can add them too but only for better usability. 

## Communication
- Abstract the communication protocol (e.g. http) within your application.
-	Reduce and Compress your communication data to reduce size and network latency.
-	Provide a version number in your external APIs.
-	Document your APIs precisely and provide a export that can be used for clients as a contract-first-approach.
- Don't require state. Stateless applications can be scaled much better.
-	Use Publish/Subscribe for notifications.

## UI
-	Make it sexy.
-	Make it fast.
-	Provide multilanguage support.
-	Create a User manual.

## Backend
-	Support Multitenancy.
- Respect the principle of data minimisation.

## Testing
- Run static code analyses e.g. find high complexity, redundant code and bugs.
- Run Unittests e.g. testing domain behaviour.
- Run Integrationtests e.g. testing API responses.
- Run Architecturetests e.g. correct naming of classes, no calls agains the application-layers.

## Deployment
- Make it easy to install.
- Make it easy to update.

## Monitoring
-	Make flows in the system tracable e.g. via unique ID or by using distributed tracing solutions.
-	Provide Healthchecks.

## Frameworks & Applications
### Spring
#### General
- Use dependency Injection always via Constructur and not via Annotation
#### Configuration
#### Controller
- RESTful API -> naming
- Return response codes and response details only on debug log-level in error cases
- Use Bean Validation for validating request data. If you need more use build your own Constaintvalidator.
- Use Annotations or Filters for authentication and identification
- Controller have to be stateless
- Controllers should not execute business logic but rely on delegation.
- Controllers should deal with the HTTP layer of the application. This should not be passed down to Services.
-	Controller should deal with Security
-	Use OpenAPI for documentation
#### Service
- Use Interfaces to describe the behaviour
- Contains the Business Logic – mostly DTO input and DTO output
- Must be so generic that it is simply reusable
#### Repository
- Use only the Query Interface to ensure DBMS neutrality
- Use Enums in Entities as String
- Use Pagable in the Repository Interfaces
- Use lombock @Data
### Angular
### Git
### IntelliJ
#### Hot Keys
- Auto help = Alt+Enter
- Show method signature = Strg+Q
- Search file = Shift+Shift
- Navigate between tabs = ???7
- Select block = Strg+W
- Format code = Strg+Alt+L
- Rename = Shift+F6
- Search & Replace = Strg+R
- New file = Strg+Alt+Insert
- Autogeneration = Alt + Insert
- Code templates = Strg+J
- git commit & push = Strg+K
- Debug step = F8
#### Refactoring

# Code Templates
This Chapter contains usefull source code examples for co
#### Service
#### Repositorymmon development problems.
## General
## Configuration
## Security
## Communication
## UI
## Backend
## Testing
## Deployment
## Monitoring
## Frameworks & Applications
### Spring
### Angular
### Git
### IntelliJ


# Architecture Pattern
This Chapter focus on pattern for whole software systems. Its focus is on a higher level of abstraction.
![architecture1](/architecture1.png)
![architecture2](/architecture2.png)
![architecture3](/architecture3.png)
- securing, tracing, health checking, scaling and downtime of services -> solution: use template project and/or use messaging
- creating doublicate DAOs in backend and frontend -> solution: use server-side rendering (vaadin) or non-typed json's => use contract first approach to make interface clear
- mapping from DAOs to Entity and back -> solution: create a helper-service for this
- validating forms and backend service -> solution: use validation in backend and show errors in frontend
- multi tanancy support -> solution: deploy environment for each tenant


# Design Pattern
This Chapter focus on pattern for common occurring problems while development.  It's focus is on a lower level of abstraction.
