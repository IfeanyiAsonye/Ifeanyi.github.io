Passbolt deployemnet on docker, connected to a mariadb and a mailserver

Here's how:

For Passbolt, run

- docker run --name Pass-bolt -d -p 7000:80 passbolt/passbolt

Create a network using

docker network create <whatevernameyouwant>

or 

docker network connect <whatevernetworkyouhavecreated> mariadb or Pass-bolt container created earlier

I used a mailpit smtp server i created earlier in a container just for the fun of it 
here's the 



docker run -d \
  --name mariadb \
  --network Passbolt_net \
  -e MYSQL_ROOT_PASSWORD=yourpick \
  -e MYSQL_DATABASE=passboltdb \
  -e MYSQL_USER=youruser \
  -e MYSQL_PASSWORD=yourpassword \
  mariadb



openpgb for email encription standard



i later found that you could actuallu pass by creating
- the network first 
docker network create <e.g passbolt_net>
- for the database 
docker run -d \
  --name mariadb \
  --network passbolt_net \
  -e MYSQL_ROOT_PASSWORD=secret \
  -e MYSQL_DATABASE=passbolt \
  -e MYSQL_USER=passboltuser \
  -e MYSQL_PASSWORD=passboltpassword \
  mariadb

- for passbolt
docker run -d \
  --name passbolt \
  --network passbolt_net \
  -e DATASOURCES_DEFAULT_HOST=mariadb \
  -e DATASOURCES_DEFAULT_USERNAME=passboltuser \
  -e DATASOURCES_DEFAULT_PASSWORD=passboltpassword \
  -e DATASOURCES_DEFAULT_DATABASE=passbolt \
  passbolt/passbolt


Head to browser type 
localhost:7000 or whatever port you have bound it to. 

You'll firefox will require you to download the passbolt extension 


What i learned
you can't change or bind ports for running containers 
When a container starts, Docker sets up iptables rules to map host ports to container ports. These rules can’t be modified dynamically without restarting the container.
i learned that openpgp(pretty Good Privacy) keys are primarily used for email encryption and digital signatures. 