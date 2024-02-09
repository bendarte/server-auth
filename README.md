# Bendarte - Authentication Server.

![project_structure](https://github-production-user-asset-6210df.s3.amazonaws.com/143492796/302132306-6f99bb24-35a0-4735-8b85-c9d9cb7575f9.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240209%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240209T171901Z&X-Amz-Expires=300&X-Amz-Signature=9db0c5481276c6cbbb10d360c079fd433a75a049daa5e2f0d82bf88cea7df245&X-Amz-SignedHeaders=host&actor_id=143505763&key_id=0&repo_id=743937813)

## Run Complete Project:

### `Backend and Frontend Servers:`
- You can find the Backend Server here:
```Backend
https://github.com/bendarte/server-backend.git
```

- You can find the Frontend Server here:
```
https://github.com/bendarte/server-frontend.git
```

```NOTES
HOW TO RUN COMPLETE PROJECT:
You will have to add the same JWT_SECRET in .env file of the Backend Server.
So the Backend Server can verify the users token and fetch secret data depending on user role.
```

## TTFHW Auth Server - 5min

### `Auth Setup:`
- Git clone https://github.com/bendarte/server-auth.git
- Go to the root folder of the project and run "npm install" in the terminal to get all correct node_modules.
- Create .env file in root folder of project, add a cryptokey to JWT_SECRET & PORT to .env config file.

```CREATEJWT
CREATE JWT SECRET IN TERMINAL:
node -e "console.log(require('crypto').randomBytes(256).toString('base64'));"
```
  
```.ENV
ADD FOLLOWING BELOW TO AUTHSERVER'S .ENV FILE:
JWT_SECRET=ADDCRYPTOKEY
PORT=3001
```

### `How to start the Auth Server:`
- You can now run "npm start" in the root folder of auth server to start the Authentication Server.

#### `Run Complete Project:`
- You will need to add both Backend and Frontend Servers to run the complete project.
- Run Frontend Server on PORT=3000
- Run Auth Server on PORT=3001
- Run Backend Server on PORT=3002
- .ENV file in both Auth & Backend Server, both containing the same JWT_SECRET.

## Functions - Auth Server
`1. Jsonwebtoken - authentication and authoriziation:`
- JWT is used to verify users and to determine user roles.
- Users token is stored in httpOnly cookie.
  
`2. Helmet - To protect from multiple attacks such as:`
- Cross-Site Scripting (XSS) 
- Clickjacking 
- Man-in-the-middle 
- Cross-site Request Forgery
- DNS Prefetch Control
- Content-Type Sniffin

`3. CORS - Resource Sharing:`
- Cors is used to control and restrict cross-origin requests.
- Cors allows applications on one domain to make request for resources from a different origin / domain.
- Cors also prevents CSRF and XSS attacks.

`4. DOTENV - Environment Variables:`
- dotenv is used to store and access sensitive information.
- dotenv is used to avoid storing configuration details inside of source code.
- JWT Secret is stored inside of .ENV file.
