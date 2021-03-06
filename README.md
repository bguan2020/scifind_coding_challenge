### Sci Find Coding Challenge ###

This is a coding challenge that will test your React.js and back-end abilities. You may use any back-end database for this (mongodb, firebase, etc.). This project should take approximately 4-5 hours, but you have 3 days to complete it.

![download](https://user-images.githubusercontent.com/43942774/82876787-32359980-9eee-11ea-8632-1e835a682014.png)


### Overview ###
Create a simple web app that has two pages: 
### 1 sign-in page that takes the following user information input:

  - username (string)
  - password (string)
  - service (string)
  
This should create a user and upload the data into a "user" collection to a Google Firebase server (or server of your choosing). You can use Firebase's authentication software to assist you with securing passwords and userID's, more info [here](https://firebase.google.com/docs/auth), or if you prefer other services like bcrypt feel free to use those as you please.

Upon completing sign-in, you should redirect them to:
### 1 profile page that displays all the relevant user data.
Username, serviceA, and serviceB should be connected to the database and dynamically rendered/updated upon any changes to the database. You must secure the profile page––Authenticated users should have an option to edit their username and services, while non-authenticated users should be able to view username, serviceA, serviceB, but not edit. In terms of accessing other user profiles, this can just be changing the ```const profile_uid = uid_of_someone_in_database``` in the javascript manually, saving, and having the profile page re-render with the new UID. No need to implement this functionality into the page/website. But you must also have something that tracks who is currently logged in, like ```const currentUser ``` (there are ways to do this in Firebase, more info [here](https://firebase.google.com/docs/auth/web/manage-users)), and this part must be done automatically, not manually. 
In other words, if I am logged in as "Brian" (the current user), I can manuever to other profiles by taking their UID from the database, manually changing the ```profile_uid``` then refreshing the page. And depending on if ```profile_uid == currentUser```, allow the ability to edit services and username. 

### Be careful!!! ###
Most errors regarding Firebase/firestore has to do with how data is uploaded asynchronously, so pay attention to your "useEffect", "async" and your ".then()" functions. Keep note of issues you encounter; we are especially interested to see how you overcame your mistakes! Mistakes make you who you are!

### Information ###
  - We suggest using [create-react-app](https://github.com/facebook/create-react-app) to quickly get a React project up and running quickly. 
  - Bonus points for a pretty and non-confusing UI as this website may be used by technically challenged scientists.
  - If you have any questions, email brian@scifind.net and I will try to get back to you in a timely manner.

### How to Submit Project: ###
The project is due 3 days from the receipt of this email. Please email brian@scifind.net with the following information to submit your project:

  1. A URL link to your web application (*Note: Feel free to host this however you like. Some free platforms that help you host your React apps include [Heroku](https://heroku.com/) and [Github](https://github.com/). Consult [this guide](https://medium.com/better-programming/how-to-deploy-your-react-app-to-heroku-aedc28b218ae) on how to deploy to Heroku.*)
  2. A URL link to the Github or Github equivalent with the source code of this project. (*Note: Remember to make it publicly accessible so we can see your awesome work :) *)
