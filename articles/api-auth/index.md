---
sitemap: false
title: API Authentication and Authorization
url: /api-auth
---

# API Authentication and Authorization

At some point in time the APIs you are building will need to give users, servers, or servers on behalf of users limited access to these APIs. This is where API authentication/authorization will play an important role and this is one of Auth0's core features.

This would allow you to cover different requirements going from user consent to server to server applications.

## Example Scenarios

### User Consent: Organizer

![](/media/articles/api-auth/user-delegation.png)

Organizer is a company that allows users to manage their appointments, contacts and tasks. They are now planning to open up their API and allow third party applications to integrate with it.

The following applications have already integrated Organizer within their Apps:

- **CalendarApp**: This application allows users to manage appointments from different sources, including appointments you have in your Organizer account. In addition to that it can also invite your contacts when you create new appointments.
- **MyTodos.io**: This application allows users to manage their tasks in different platforms including the Organizer platform.
- **TextApp.io**: A next generation messaging platform allowing you to easily communicate with your friends (including your contacts in Organizer).

Organizer decided to use a standards based approach instead of rolling their own authentication for their API. Using OAuth 2.0, their services are represented as Resource Servers and their consumers are the Clients. The main goal is that Users have to give explicit consent before the Clients can do anything. After giving consent, the Clients will interact with Auth0 (the Authorization Server) to get an `access_token` which can be use to talk to the Organizer API on behalf of the users.

### Server to Server Applications: World Mappers

World Mappers is a company that has been collecting geospatial data for many years and they have started building a new API that offers geocoding and route planning.

Their customers will be able sign up for their service in order to access one or more of its features. The customers will for example use these services to find the closest restaurant to your current location, to find a taxi or even for route planning in an application managing drivers and deliveries.

World Mappers decided to use a standards based approach instead of rolling their own authentication for their API. Using OAuth 2.0, their services are represented as Resource Owners and their consumers are the Clients. These Clients will interact with Auth0, the Authorization Server to get an access token which they can use to talk to the World Mapper API.

![](/media/articles/api-auth/server-to-server.png)

## API Authorization

By using the OAuth 2.0 authorization framework you can give your own applications or third-party applications limited access to your own APIs, either on behalf of a user (using a consent flow) or on behalf of the application itself. This standard way of handling API authorization has been accepted by large social platforms like Facebook, Google, ... but also by large enterprise platforms like Azure AD.

Using Auth0 you can easily support the different flows in your own APIs without having to worry about the OAuth 2.0/OpenID Connect specification, user consent and many other technical aspects of API authorization.

### High Level Overview

When we look at the OAuth 2.0 specification we can identify a few actors:

 - The Authorization Server (Auth0 in this case)
 - The Resource Servers (your APIs)
 - The Clients (the consumers of your APIs, which can be your own or third-party applications)
 - The Resource Owner (the user of your APIs and of the applications)
 - The User Agent (the user's browser or mobile application)

Using different grants (flows) these actors will start interacting with the final goal of giving the Clients limited access to the Resource Servers you are building. The end result will always be the same, the Client will end up with an `access_token` which can be used to call the Resource Server (on behalf of the user or of the Client itself).

Supported flows:

 - Tradition Web Applications: [Authorization Code Grant](/api-auth/grant/authorization-code)
 - Single Page Applications/Mobile Applications: [Implicit Grant](/api-auth/grant/implicit)
 - Server to Server Applications: [Client Credentials Grant](/api-auth/grant/client-credentials)

## API Authentication

- [Using the Auth0 Dashboard](/api-auth/using-the-auth0-dashboard)
- [Using Auth0's Management API](/api-auth/using-the-management-api)
- [How to ask for an access token](/api-auth/asking-for-access-tokens)
- [How to define custom scopes](/api-auth/adding-scopes)


## Tutorials

See the following tutorials for a step-by-step guide on how to implement the OAuth 2.0 authorization framework within your applications using Auth0:

### Configuration

 - [Configuring the Resource Servers](/api-auth/config/resource-servers)
 - [Configuring the Clients](/api-auth/config/clients)

### Resource Server

 - [Creating a Resource Server in Node.js](/api-auth/resource-servers/node-js)
 - [Creating a Resource Server using the ASP.NET Web API](/api-auth/resource-servers/asp-net)

### Authorization Code Grant

 - [Using the Authorization Code Grant from a Node.js application](/api-auth/authorization-code-grant/node-js)
 - [Using the Authorization Code Grant from an ASP.NET MVC application](/api-auth/authorization-code-grant/asp-net)

### Implicit Grant

 - [Using the Implicit Grant from a Single Page application](/api-auth/implicit-grant/single-page)
 - [Using the Implicit Grant from an iOS application](/api-auth/implicit-grant/ios)

### Client Credentials Grant

 - [Example use case: 'Foo'](/api-auth/client-credentials-grant/use-case-foo)

## Have Questions?

You may find the answers on the [API Auth FAQ](/api-auth/faq).
