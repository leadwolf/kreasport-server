# Kreasport-server

Servers for the [Kreasport](https://github.com/Christopher-Caroni/KreaSport) project. This repository will be used as a subproject to seperate the app and the server. Created as part of an Erasmus project work. Read the [project report](https://github.com/Christopher-Caroni/KreaSport/blob/41698bede1d36e6a5800d7386fc56d343fa991ee/doc/Kreasport%20Report.pdf) to learn more.

## Built With

* [Spring](https://spring.io/) - The web framework used for security, data and authentication.
* [Maven](https://maven.apache.org/) - Dependency Management.
* [Auth0](https://auth0.com/) - Used to authenticate users.
* [MongoDB](https://www.mongodb.com/) - Document based database structure.
* [Heroku](https://www.heroku.com/) - Used to deploy the servers.

## Authors

* **Christopher Caroni** - *Idea and project maintainer* - [Github](https://github.com/Christopher-Caroni)

## License

This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](LICENSE) file for details

## Project structure

 - **parent**: This is the top level Maven project that contains the servers and common submodules.
 
The submodules are as follows:
 - **common**: the common classes necessary to both servers
 - **kreasport-backend**: the server handling request with JWTs for trusted clients such as the Android app. Interacts directly with the database. 
 - **kreasport-frontend**: the server handling request authenticated by the user session. Used by the admin to manage the database.

The two servers are because of a Maven conflict with Auth0 dependencies.