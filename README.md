# Firebase-Hosting-for-Angular

Below is step by step process to host angular6.0 app on firebase

1] `npm install -g firebase-tool`  Install firebase tool 

2] `firebase login` Use the CLI tools to login in Firebase.

After connecting to our account/Gmail-account, we will get the **firebase CLI Login Successfull** message in browser

3] `firebase-init`

*Here are the answers to the questions Firebase tools will ask:*

> ? Are you ready to proceed? **Yes**  
>? Which Firebase CLI features do you
> want to setup for this folder? Press Space to select features, then
> Enter to confirm your choices. **Hosting: Configure and deploy Firebase
> Hosting sites**

>? What do you want to use as your public directory? **dist** `(This is important! Angular creates the dist folder.)`

>? Configure as a single-page app (rewrite all urls to /index.
html)? **Yes**

4] `ng build --prod`

> This will create a brand new dist/ folder in our project with the
> files necessary to launch our app.

5] Before deploying the app, go to firebase.json file and specify your project public field like this

    "public": "dist/your_project_name",
6] Now deploy the project in firebase using below command

> firebase deploy


After depolying you will get the below message

> +  Deploy complete!
> 
> Project Console: https://************ [you will get the actual url
> name rather than stars]
> 
> Hosting URL: https://*************  [you will get the actual url name
> rather than stars]
> 
> you can access the website by the URL given in Hosting URL

