# Engineering Interview

## Summary

This assessment will gauge the candidates technical aptitude for building frontend
view layers that have the ability to interact with third-party API's.

In this assessment we will be interacting with the NASA API which can be found here:
[NASA APIs](https://api.nasa.gov/)

To obtain access to a free API key please follow the instructions for generating an API key
by clicking the "Generate API Key" tab in the naviation bar. It will ask for basic input
such as "First Name", "Last Name", and "Email"

Once you have recieved your API key you can start interacting with the NASA API.
In this Assessment we will be interacting with the Mars Rover API which can be found further
down the [NASA APIs](https://api.nasa.gov/) page. I have also included a link to the Mars Rover API here: [Rover Photos API](https://github.com/chrisccerami/mars-photo-api)

If full feature set cannot be implemented in the time given try not to give "full featured"
which only halfway works, rather give time to the features you know you can make 100% functional

User interface and user experience is not a major priority we are leaving design and 
creativity up to the user implementing the test. However it should feel intuitive to find 
the search parameters on the page and view the images in a reasonable frame.

Image Viewer should be either a carosel or grid view

### Technology Expectation for Assessment

We would like you to use **Vue.js** as the frontend framework of choice. 
Documentation and Framework information can be found at:
[vue.js](https://vuejs.org/)

## Assessment Requirements

DATE Format for API: "YYYY-MM-DD"

1. When arriving at landing page show photo data associated for the current date
    a. Use photos from a "default" rover of your choosing
    b. If no photos exist for day in question, generate a random date in which to display images

2. On the page we should also have a choice to select which rover images we would like to view.
    a. Rover choices include: "Curiosity", "Opportunity", "Spirit", or "All"

3. On the page we should also be able to choose which camera we would like to view data from
    a. Each rover only has a certain cameras in which they can use, the array of camera options and which rover is able to interact with them is listed within the API documentation. This means if a rover is chosen you should not be able to choose a camera that the rover does not have access to.

4. On the page we should have some way to chose a date in which to populate data from
    a. This can be a datepicker, calendar popup, or datetime field in which you can type
    b. Dates for the API are in "YYYY-MM-DD"
    c. If no date is selected, generate a random date in which to display photos
    d. Use "Querying by Earth date" **NOT** "Querying by Martian sol"

5. Additional data to pull in with your query's are "Rover status" and "Total photos" From mission manifest

### Bonus Points
- Written in TypeScript over JavaScript
- Has it been hosted? (heroku, aws, gcp, azure, blah blah)
- Add some kind of authentication to view the site (sign up / sign in)
    - AWS cognito
    - Azure AD B2C
    - Googles Firebase Auth
       - federated identity providers (facebook, gmail, amazon, etc..)
    - SSO (OAuth, Okta, etc..)
