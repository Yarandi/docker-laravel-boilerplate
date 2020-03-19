# docker-laravel-boilerplate

The beauty of Docker for Laravel Project development ,
Set up and configured a docker-compose file to create a LEMP stack of three containers wrapped in a single network, have exposed ports on that network that let us access our app and database, and have even run cli commands through docker-compose’s exec method.

The first thing you should do is installing or cloning laravel in your local 

`git clone https://github.com/laravel/laravel.git laravel-app`

OR if you have already installed composer on your local system

`composer create-project --prefer-dist laravel/laravel laravel-app`


Then pulling thisrepository codes in the same directory that installed laravel in previous ,Then the thing we need to do is run the build command to generate the image data:

`docker-compose build`

You can then proceed with actually starting up the containers using:

`docker-compose up -d`

In your browser, navigate to http://localhost:8080 where 8080 is the first port that you specified under the nginx service in your docker-compose.yml file.

