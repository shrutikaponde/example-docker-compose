# Get started with Docker Compose
This is example of simple Python web application running on Docker Compose. The application uses the Flask framework and maintains a hit counter in Redis. While the sample uses Python, the concepts demonstrated here should be understandable even if you’re not familiar with it.

## Prerequisites
Make sure you have already installed both [Docker Engine][1] and [Docker Compose][2]. You don’t need to install Python or Redis, as both are provided by Docker images.

## Step 1: Setup
```
git clone https://github.com/shrutikaponde/example-docker-compose.git
cd example-docker-compose
```

## Step 2: Build and run your app with Compose

1. From your project directory, start up your application by running `docker-compose up -d`.
2. Enter `http://localhost:5000/` in a browser to see the application running.

    You should see a message in your browser saying:
    ```
    Hello World! I have been seen 1 times.
    ```

3. Refresh the page.

    The number should increment.
    ```
    Hello World! I have been seen 2 times.
    ```

## Step 3: Stop services
1. Stop your services once you’ve finished with them by running:
    ```
    docker-compose stop
    ```
2. You can bring everything down, removing the containers entirely, with the `down` command. Pass `--volumes` to also remove the data volume used by the Redis container:
    ```
    docker-compose down --volumes
    ```

For detailed explanation of all steps refer [official docker compose documentation][3]

[1]:https://docs.docker.com/get-docker/
[2]:https://docs.docker.com/compose/install/
[3]:https://docs.docker.com/compose/gettingstarted/