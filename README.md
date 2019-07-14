![](https://i.ytimg.com/vi/NIEKB5iRcOs/maxresdefault.jpg)
## Setting up Symfony 4 Application with Docker
The Docker will be used to run all the services such as Nginx, PostgreSQL and PHP-FPM(7.3). Note: The Symfony 4 application's code should be located on your local machine.
#### How to run
###### Let's start!

- Create a "docker" folder inside your Symfony application root directory
- Copy all this files in your docker folder (created at first step)
- Right now, if we have all the configuration files in place, it is a time to build the images.
- To do that, inside "docker" directory run the following command in your terminal:
`docker-compose build`
- Docker will download all needed files and will build PHP-FPM, Nginx, PostgreSQL images which you will be able to run later on.
- To run the application, inside docker directory run the command in your terminal:
`docker-compose up -d`
- The Docker containers will start based on the previously built images. In the terminal you should see something like that:

![](https://blog.rafalmuszynski.pl/assets/images/posts/2018-02-12-img4.png)

- Success! Your application located on your local machine is now running inside the Docker using the configured Nginx, PostgreSQL and PHP-FPM images.
##### How to Access Symfony 4 App from inside the Docker?
- The web server is exposed on port 8080 on your local machine. So to access it you have to go to the url: http://127.0.0.1:8080 in your browser on MacOS(on Windows you should use localhost instead of 127.0.0.1).
