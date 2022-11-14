## Link for the article https://sweetcode.io/deploying-express-node-js-backend-heroku/
Step 1: Preparing the codebase for Heroku
Now that we have the base code for the application, we need to make a few changes to the package.json file to enable deployment to Heroku.

1. Run the node –version command to get your version of Node.js.
2. Add the engines key to your package.json, specifying your node version.

```package.json

{
  "name": "hero",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
      "start": "node index.js",
      "test": "echo \"Error: no test specified\" && exit 1"
  },
  "author": "",
  "license": "ISC",
  "dependencies": {
      "express": "^4.16.4"
  },
  "engines": {
        "node": "v11.3.0"
  }
}
```
Step 2: Testing Heroku locally
1. Initialize the Git repository and commit the changes we just made.
`git init`
`git add .`
`git commit -m “First deploy to Heroku”

2. Log in to Heroku (one-time command) by running heroku login



3. Run heroku local web



4. Open up localhost:5000 in your browser to see the result:
<img width="448" alt="image" src="https://user-images.githubusercontent.com/88828825/201579869-c5074024-1d42-4489-b80b-f01214b0486a.png">



Step 3: Deploying to Heroku
1. Run heroku create [chosen name of your project] to create the Heroku app.
2. Run git push heroku master to push the code to the Heroku servers.
<img width="320" alt="image" src="https://user-images.githubusercontent.com/88828825/201579998-f34d104a-8bf0-4959-8348-fc7eebe38d75.png">



After the process is complete, visit the Heroku link for your newly deployed app (which should be printed near the bottom of the output).
<img width="364" alt="image" src="https://user-images.githubusercontent.com/88828825/201580052-8b835f14-b808-4ec6-8d0e-83ce65be2d84.png">



Great Job! You’ve just deployed your Node.js application to Heroku. To make changes after deploying, simply

```git commit```
your changes and run

```git push heroku master```
once again.
