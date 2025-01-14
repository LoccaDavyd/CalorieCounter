# Calorie Counter with Diet Tracker

### Distinctiveness and Complexity

This project is for keeping track of the diet throughout the day and throughout the months.  
It contains **three** applications:

**Foods**: the app for building food, date, recommended calorie intake APIs using viewsets, router and filters of the **Django REST framework**.

**Users**: the app for building user authentication API using viewsets and routers of the **Django REST framework**. 
Authentication and storing user sessions are provided with token generated by **knox**.

**Frontend**: the single-page application implemented on **JavaScript** (**React** with hooks) using **Redux** as a state manager. 
Layout and design are made with **SASS**. Responsiveness is provided with CSS Media Queries. 
In order for all of this to work together, **Webpack** is used. It has a calendar made using JavaScript and CSS grid. The calendar and food basket are synchronized.

Front-end and back-end are connected through **REST API**.

### Functionality

**Authorized and unauthorized users** can find out calorie and nutrient content of foods which can be found by taping in search input or by category. 
They also may collect food basket in which the calorie content is summed up. And the last thing is opportunity to find out their recommended calorie intake. 

**Authorized users** can collect and save their food baskets binding a specific day. They can change day basket content any time. 
For example, during a day and watch what they have already eaten to keep track of the diet throughout the day. 
After saving they get the opportunity to watch a food diary as calendar. Every day is colored depending on the ratio of daily calories consumed to the recommended intake. 
Clicking on a day in calendar opens this day basket. 
And finally in order to have the opportunity to get the calorie ratio, users should count and save their recommended calorie intake. 
Which they always can update in case of changes in weight or physical activity.

### The Structure

**Foods** app contains *urls* file with documentation url and API routes, *models* file with models for category, food, day, food item and calorie intake. 
There are also *api* and *serializers* files for creating and configuring API. The documentation is in the *index* template.

**Users** app includes *urls*, *api* and *serializers* files for creating and managing the authentication API using the built-in User model.

**Frontend** app contains *src* directory, which also has several folders:
* *components* directory contains *.jsx* files, which are components of the application interface
* *reducers* folder has several reducers for managing app state, including thunks which send HTTP requests
* *style* folder has several *.scss* files providing layout, style and responsiveness

For correct working of the front-end created *.babelrc* and *webpack.config*.
The last bundles all files in *main.js* (in *static* folder) which is linked as a script in *index.html* (in *templates* folder).

### How to run

**Although it's not necessary because it's deployed.**  
In the root folder  
activate (create) virtual environment
```
    pipenv shell  
```
install the packages according to *requirements.txt* 
```
    pip install -r requirements.txt  
```
start the project by running
```
    python manage.py runserver 
```
This should be enought, if not:  
in another terminal in the root folder to create node_modules type in:  
```
    npm install  
```
and start the app:  
```
    npm run dev  
```
Frontend app should be available on *localhost:8000*  

Registration is available  
Or  
Here are my credentials to log in:  
login – dami  
password – Vovasik3%  

**Although it's not necessary because it's deployed.**

### Deploy And Separation

There were some problems (most likely with the integration of the Webpack and Django) during the deployment, so I have decided to divide the project into 
front-end and back-end parts for deployment purpose.

Front-end is hosted on [netlify](https://canthin.netlify.app)  
Back-end with documentation is hosted on [heroku]( https://caloriecounterapi.herokuapp.com) 

Repositories used for deployment:  
Front-end Repository: <https://github.com/DamiDavy/diet-tracker-frontend>  
Back-end Repository: <https://github.com/DamiDavy/diet-tracker-backend>  

Registration is available [here](https://canthin.netlify.app/app/register).  
Or.  
Here are my credentials [to log in](https://canthin.netlify.app/app/login):  
login – dami  
password - MrPresident14?6 

### Technologies

Frontend: React, Redux, Webpack, SASS  
Backend: Django REST framework, knox

### Demo
![App Promo Gif](gif-for-github.gif)
