# Docker Technology Basics

You need to clone a FastAPI application, configure it, and run it in a Docker container. After that, verify the application's functionality and ensure successful connection to the database.

## Technical Description of the Task

1.  Use the `git clone` command to clone the repository from [repository](https://github.com/GoIT-Python-Web/FullStack-Web-Development-hw2). Navigate to the cloned directory.

2.  Create a `Dockerfile` with instructions for building the Docker image of the application.

3.  Write a `docker-compose.yaml` file with configurations for the application and PostgreSQL.

4.  Use Docker Compose to build the environment and the `docker-compose up` command to launch the environment.

> [!TIP]💡 Hint:

Modify the database connection string `SQLALCHEMY_DATABASE_URL`, located in the `\\conf\\db.py` file. Replace `localhost` with the name of the PostgreSQL service from your `docker-compose.yaml` file.

```python
  SQLALCHEMY_DATABASE_URL = f"postgresql+psycopg2://postgres:567234@localhost:5432/hw02"
```

When using Docker Compose, each service (container) operates within its own network, and they typically cannot refer to each other using localhost. Instead, you should use the service name as the hostname.

Test the application's functionality and database availability.
💡 Hint:

After starting the application container, the browser view should look as follows:

![01](./screenshot/01.png)

If everything is correctly configured in the `docker-compose.yaml` file, clicking the `Check DB` button should show the following:

![02](./screenshot/02.png)

#### Acceptance Criteria

- The repository has been cloned, and a `Dockerfile` for building the application's Docker image has been created.
- A `docker-compose.yaml` file with configurations for the application and PostgreSQL has been written.
- Docker Compose has been used, and the environment has been built and launched using the docker-compose up command.
- The application is functional, and the database is accessible, confirmed by clicking the Check DB button.
