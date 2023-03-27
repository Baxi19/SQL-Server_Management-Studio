# Docker Compose for SQL Server & SQL Management Studio
Docker Compose to create SQL Server & SQL Server Management Studio

### In this example, we have two services: sql-server and sql-management-studio.

### The sql-server service is based on the official SQL Server 2019 Docker image and exposes port 1433 for SQL Server connections. It also sets environment variables for the sa user password, EULA acceptance, and the product ID.

### The sql-management-studio service is based on the official Microsoft SQL Server Tools image and depends on the sql-server service. It sets environment variables for the SQL Server hostname (sql-server), the sa user credentials, and connects to the db-network network.

### Finally, we define a network called db-network using the bridge driver.

### To start the services defined in the Docker Compose file, navigate to the directory containing the Docker Compose file and run the following command:

### Run
```docker
docker-compose up -d
```
### This will start the containers in the background (detached mode). To stop the containers, run the following command:

### Stop
```docker
docker-compose down
```

### Note that if you make changes to the Docker Compose file or the environment variables in the .env file, you'll need to rebuild the Docker images and restart the containers using the `docker-compose up` command.
