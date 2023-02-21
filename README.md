# LightBnB

LightBnb is a very simple website that lets you book your next vacation easily! With LightBnB you can search for places to stay that are in the location you are visiting! When searching you can also filter by your price range and how good of reviews each place has! 

This was a project mainly focused on buidling SQL skills and learning how to write propery queries. The front and back end of this website were forked and cloned while I wokred on just connecting the server and the database. 

## Finished Product

!["Screenshot of ERD Diagram"](https://github.com/marcuszcoding/LightBnB/blob/main/docs/erd-diagram.png)
!["Screenshot of Home Page"](https://github.com/marcuszcoding/LightBnB/blob/main/docs/home-page.png)
!["Screenshot of Reservations Page](https://github.com/marcuszcoding/LightBnB/blob/main/docs/my-reservations-page.png)
!["Screenshot of Create Listing Page"](https://github.com/marcuszcoding/LightBnB/blob/main/docs/create-listing.png)

## Project Structure


```
├── public
│   ├── index.html
│   ├── javascript
│   │   ├── components 
│   │   │   ├── header.js
│   │   │   ├── login_form.js
│   │   │   ├── new_property_form.js
│   │   │   ├── property_listing.js
│   │   │   ├── property_listings.js
│   │   │   ├── search_form.js
│   │   │   └── signup_form.js
│   │   ├── index.js
│   │   ├── libraries
│   │   ├── network.js
│   │   └── views_manager.js
│   └── styles
├── sass
└── server
  ├── apiRoutes.js
  ├── database.js
  ├── json
  ├── server.js
  └── userRoutes.js
```

* `public` contains all of the HTML, CSS, and client side JavaScript. 
  * `index.html` is the entry point to the application. It's the only html page because this is a single page application.
  * `javascript` contains all of the client side javascript files.
    * `index.js` starts up the application by rendering the listings.
    * `network.js` manages all ajax requests to the server.
    * `views_manager.js` manages which components appear on screen.
    * `components` contains all of the individual html components. They are all created using jQuery.
* `sass` contains all of the sass files. 
* `server` contains all of the server side and database code.
  * `server.js` is the entry point to the application. This connects the routes to the database.
  * `apiRoutes.js` and `userRoutes.js` are responsible for any HTTP requests to `/users/something` or `/api/something`. 
  * `json` is a directory that contains a bunch of dummy data in `.json` files.
  * `database.js` is responsible for all queries to the database. It doesn't currently connect to any database, all it does is return data from `.json` files.