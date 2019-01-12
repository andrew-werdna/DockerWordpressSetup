# Installation Instructions

1. Clone *this* repo `git clone git@github.com:andrew-werdna/DockerWordpressSetup.git <your-project-name>`
1. Change directory `cd <your-project-name>/docker`
1. Add a `.env` with the values:
* dbname=\<database-name>
* dbrootpass=\<mysql-root-password>
* dbpass=\<mysql-user-password>
* dbhost=database:3306
* dbuser=\<mysql-username>
1. Build and start containers `docker-compose up -d`
1. Navigate to `http://localhost/` after the build is complete to complete your installation and set your admin credentials
