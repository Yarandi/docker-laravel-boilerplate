# docker-laravel-boilerplate

The beauty of Docker for Laravel Project development ,
Set up and configured a docker-compose file to create a LEMP stack of three containers wrapped in a single network, have exposed ports on that network that let us access our app and database, and have even run cli commands through docker-compose’s exec method.

The first thing you should do is installing or cloning laravel in your local 

`git clone https://github.com/laravel/laravel.git laravel-app`

OR if you have already installed composer on your local system

`composer create-project --prefer-dist laravel/laravel laravel-app`


Then pulling this repository codes in the same directory that installed laravel in previous ,

Edit `docker-compose.yaml` and set your `MYSQL_DATABASE`, `MYSQL_USER`, `MYSQL_PASSWORD`, `MYSQL_ROOT_PASSWORD` environments.

Then the thing we need to do is run the build command to generate the image data:

`docker-compose build`

You can then proceed with actually starting up the containers using:

`docker-compose up -d`

In your browser, navigate to http://localhost:8080 where 8080 is the first port that you specified under the nginx service in your docker-compose.yml file.

# How connect to the mysql: 
If you have issue with database connection in laravel , change `DB_HOST=127.0.0.1` to `DB_HOST=mysql` actually its the name of service that we defined in `docker-compose.yaml`

How connect to the mysql:  
first run `docker ps -a` to see container Id's then use below command to execute the container 
`docker exec -it CONTAINERID bash`

Then you can run this command `mysql --user=USER --password`
after then you need to enter the password of this user that you defined in docker-compose.yaml


