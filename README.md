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

# Coding Best Practics
This Chapter focus on best practics about writing source code.

## General
-	Whenever possible use existing Pattern and Standards within your System Components. Note: This doesn't mean that you should use common Frameworks. Standards and Pattern should have a non Framework/Library focus.
- Don't use Developer Teams with more than 6 Persons.
-	Highly automate all your tasks e.g. builds, tests and deployments.
- Try to reduce complexity by building solutions that (a) focus on a low number of external dependencies and (b) solves only the existing requirements and not more predicted ones.

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
#### Configuration
#### Controller
- RESTful API -> naming
- Return response codes and response details only on debug log-level in error cases
- Use Bean Validation for validating request data
- Use Annotations or Filters for authentication and identification
#### Service
#### Repository
- Use only the Query Interface to ensure DBMS neutrality
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


# Design Pattern
This Chapter focus on pattern for common occurring problems while development.  It's focus is on a lower level of abstraction.
