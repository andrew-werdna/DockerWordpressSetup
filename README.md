# Installation Instructions

1. Create your project folder `mkdir <project-folder-name>`
1. Change directory `cd <project-folder-name>`
    <br />^ **Please Note** there will be *two* repository folders living inside this parent project folder. One is the Docker setup, and the other is the WordPress filesystem. They both should live inside your <project-folder-name> directory (unless you want to edit the `docker-compose.yml`)
1. Clone *this* repo `git clone git@github.com:andrew-werdna/DockerWordpressSetup.git docker`
1. Download the **WordPress file system** `curl https://wordpress.org/latest.tar.gz -o -s wordpress.tar.gz && tar -xzf wordpress.tar.gz && mv wordpress application && rm -rf wordpress.tar.gz`
    <br />^ **Please Note** the WordPress filesystem folder *must* be named `application` (unless you wish to edit the `docker-compose.yml`)
1. Change directory `cd docker`
1. Build and start containers `docker-compose up -d`
1. Navigate to http://localhost/ after the build is complete to complete your installation and set your admin credentials

### Simple Example

```
myProject="wordpress_docker_setup";
myDocker="docker";
myApp="wordpress";

mkdir --parents $myProject
cd $myProject
git clone git@github.com:andrew-werdna/DockerWordpressSetup.git $myDocker

curl https://wordpress.org/latest.tar.gz -o -s wordpress.tar.gz
tar -xzf wordpress.tar.gz
mv wordpress $myApp
rm -rf wordpress.tar.gz

cd $myDocker
docker-compose up -d

echo -e "\n COMPLETED \n"
```
