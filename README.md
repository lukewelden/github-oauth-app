# Github OAuth App
This application is a simple web app that uses GitHub as an authentication service and displays the user's
github profile on a web page. 

This project has been created as part of the OAuth 2.0 lesson in the module *User Authentication and Authorization* which is part of the Backend Engineer Career Path provided by Codecademy. 

This application demonstrates my knowledge of the following tools and technology
- OAuth 2.0 
- [GitHub Authentication and Authorisation](https://www.passportjs.org/packages/passport-github/) with `passport-github` 
- Session authenticaion 
- [express sessions](https://www.npmjs.com/package/express-session)
- [Passport.js](https://www.passportjs.org/) 
- [bycrypt](https://www.npmjs.com/package/bcrypt)

## Running Locally 
To run this app locally follow the steps below. 
1. Clone the repo with `git clone https://github.com/lukewelden/github-oauth-app`
2. At the root level install the project dependencies with `npm install`
3. Setup a GitHub OAuth App by following [GitHub's Documentation](https://docs.github.com/en/apps/oauth-apps/building-oauth-apps/creating-an-oauth-app). Use the following configuration
    i. Application Name: OAuth Project (or any name for your project)
    ii. Homepage URL: http://localhost:3000
    iii. Authorization Callback URL: http://localhost:3000/auth/github/callback
4. Create a `.env` file and set the following environment variables 
```
GITHUB_CLIENT_ID=<Your GitHub Client ID>
GITHUB_CLIENT_SECRET=<Your Github Client Secret>
SESSION_SECRET=<A random secret string> 
```
5. Finally, run the application with `node app.js`