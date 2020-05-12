# ACCIDENTS INCIDENTS BY ZIPCODE IN PG COUNTY

This web application that visualizes the accident incidents that happened within zip code area on a map. When a zip code is selected by the user, we filter latitude and longitude within that zip code for it to be visualized on the map to be easily seen. Oftern, you might need to zoom out to clearly see all the datapoints on the map.

link to Heroku application: https://inst377accidentincident.herokuapp.com/
Target browsers: iOS, Android
link to user's manual:
link to developer's manual: developer manual is below
# Goal
We want commuters figuring out the safest and quickest path for their commute to work or school to be an safe proccess, so please open this application on a web browser from a desktop or laptop. Although you will be able to find the app functional on mobile iOs and Android devices, for your safety, we have built the plaftorm to run best from home, where you will have the best experience for mapping your next trip around town or for simply keeping an eye out for criminal hotspots. 

# DEVELOPER'S MANUAL

# How to install your application and all dependencies
To start working on this application from your local environment, you should start with downloading the source files from the github repository: bnwokele/Final_Project. This includes the code for the backend and frontend, and the dependencies required to make the application work. The core dependencies for this application are: babel/cli, babel/core, babel/node, babel/ preset-env,  node-fetch, nodemon, express, and eslint. A gitignore file is also required because once all these dependencies are installed, they come with a lot of files that would take a long time to push to github.

# How to run your application on a server
To run the application on a local server, you will need to open up a terminal and navigate to the folder that stores the source files on your local environment. Then in that folder you will install the dependencies with the command npm start. Once all the dependencies are installed and there are no errors or vulnerabilities, run the application on the server by typing in the command npm start on the terminal. This allows you to run the application locally. In the server.js file, the port was set to 3000 so to view the frontend of the application, you can navigate to localhost:3000. To run the application on heroku, you need to integrate github with a heroku server. When you deploy it, it builds an application that updates automatically with your commits. You also receive a link to the application where you can view it running on the server.

# How to run any tests you have written for your software
There are currently no tests for the application. This is a task that we hope to tackle in the future.

# The API for your server application - all GET, POST, PUT, etc endpoints, and what they each do
All requests have a /api endpoint.
GET - A get request is used to send data from the server to the frontend. In the backend, the data is processed into an object containing zipcodes as keys and arrays of corresponding latitude and longitude as the values. In the front end, the data is used to input the zipcodes into the dropdown menu and also to visualize the longitude and latitude as data points on the map.
POST - When a user decides to visualize accident data points within a zip code area on the map, they first have to select the desired zip code and click the check zip code button to visualize the data points. When the user clicks the button, the selected zip code is sent to the server using a post request
PUT - While using the application, users can plot the data points for multiple zip codes. A put request is used to send an array back to the server with an updated list of all the zipcodes the user has selected.

# A clear set of expectations around known bugs and a road-map for future development.
Currently, there is a bug on the application that requires you to reload the page after you initially get to the website to be able to view all the zipcodes from the drop-down menu. When you first get the website, only a few zip codes are available in the drop-down menu, but reloading/refreshing the page delivers the remaining zip codes. 

# Road-map for future development:
  - Insert another map so that users can select two zip codes at the same time and easily compare crime data between them.
  - Make use of the data that is sent back to the server from the post and put request. One idea might be to send back the streets where the  accidents happened in each zip code that is selected.
  - Write tests to make sure the code performs as intended.
