# INSTRUCTIONS

1- once in this directory run this to start postgres container in port 5433(you can configure the port in docker-compose.yml in the ports section, the first number is the port [host]:5432). The -d is for background mode<br />

**docker-compose up -d**<br />

A pgdata folder should be created in the same folder to persist the data across container recreations and restarts<br />

2- If you want to connect to the database with a GUI client like pgadmin 4 use<br />

**host**: 127.0.0.1<br />
**port**: 5433<br />
**user**: postgres<br />
**password**: postgres<br />

if you want to connect from the command line to the postgres container run<br />

**docker exec -it pg-container psql -U postgres**<br />

once in you can interact with the database. Enter \q to quit the container and get back to your host machine<br />

# OTHER USEFUL COMMANDS

-> To list running services<br />
**docker-compose ps**<br />

-> restart service<br />
**docker-compose restart pg-container**<br />

-> To stop postgres service<br />
**docker stop pg-container**<br />

->To remove postgres container(stop the service first with the previous command)<br />
**docker rm pg-container**<br />

-> To check the logs:<br />
**docker-compose logs**<br />
