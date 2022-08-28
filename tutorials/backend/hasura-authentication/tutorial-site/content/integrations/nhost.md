---
title: "Nhost"
metaTitle: "Nhost | Hasura Authentication Tutorial"
metaDescription: "Nhost is the open source GraphQL backend (Firebase Alternative) and a development platform. Nhost is doing for the backend, what Netlify and Vercel are doing for the frontend.
"
---

## What is Nhost

<!-- Nhost dashboard image  -->

Nhost is the open source GraphQL backend (Firebase Alternative) and a development platform. Nhost is doing for the backend, what Netlify and Vercel are doing for the frontend.

We provide a modern backend with the postgres database,
GraphQL, Authentication, Storage, and Serverless Functions.

Nhost Authentication is a ready-to-use authentication service that is integrated with the [GraphQL API](/platform/graphql) and its permission system from Hasura.

Nhost Authentication lets you authenticate users using different sign-in methods:

- [Email and Password](/platform/authentication/sign-in-with-email-and-password)
- [Magic Link](/platform/authentication/sign-in-with-magic-link)
- [Phone Number (SMS)](/platform/authentication/sign-in-with-phone-number-sms)
- [Google](/platform/authentication/sign-in-with-google)
- [Facebook](/platform/authentication/sign-in-with-facebook)
- [GitHub](/platform/authentication/sign-in-with-github)
- [LinkedIn](/platform/authentication/sign-in-with-linkedin)
- [Spotify](/platform/authentication/sign-in-with-spotify)

## How it works

1. When a user signs up or is created, the user's information is inserted into the `auth.users` table in your database.
2. Nhost returns an access token and a refresh token, together with the user's information.
3. The user sends requests to Nhost services (GraphQL API, Authentication, Storage, Functions) with the access token as a header.
4. The Nhost services use the user's access token to authorize the requests.

Nhost's authentication service is integrated with your database. All users are stored in the `users` table under the `auth` schema.

### Create a Nhost account

First things first, we need to create a new Nhost project.

So, log in to your Nhost dashboard and click the Create Your First Project button.

Next, give your new Nhost project a name, select a geographic region for your Nhost services and click Create Project.


We will be creating a basic Notes app.

### Open Hasura Console

We now need to create a table named notes. 
Create permissions so only users can read their own notes.