# Scorpion LMS

## Requirements

Install all listed applications below.

1. [Git](https://git-scm.com)
2. [Git Large File Storage (LFS)](https://git-lfs.github.com)
3. [Docker](https://www.docker.com/products/docker-desktop)
4. [Node.js (LTS)](https://nodejs.org/en/)
5. [Yarn (Global Install)](https://yarnpkg.com) `npm install -g yarn`
6. [Gatsby CLI (Global Install)](https://www.apollographql.com/docs/react/get-started/) `npm install -g gatsby-cli`
7. [Rust](https://www.rust-lang.org)
8. [Scorpion](https://crates.io/crates/scorpion) `cargo install scorpion`

## Documentation

## URL's

## App Setup

1. Dreate `Dev` folder under your home directory and clone repository. (https://desktop.github.com)
2. Ensure required applications listed above are installed.
3. Copy contents of `.env.example` into `.env` and modify per needs.

## Docker

```dockerfile
docker-compose up -d --build
```

### RabbitMQ

Ensure .env.example RabbitMQ environment variables are copied and required fields filled out.

> UI: <http://localhost:15672>
> Use the username/pass entered in your .env file.

RabbitMQ TCP listener available on port `5672`.

> Port: <http://localhost:5672>

### LMS Client (Future Development)

> <http://localhost>

### Connect to Frontend (Future Development)

> Run `yarn start` from project root.

> <http://localhost:8000>

> <http://localhost:8000/___graphql>

### Command Breakdown

|                  |                                                                                                                            |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------- |
| `docker-compose` | [Docker Compose](https://docs.docker.com/compose/) is a tool for defining and running multi-container Docker applications. |
| `up`             | The [up](https://docs.docker.com/compose/reference/up/) command aggregates the output of each container.                   |
| `-d`             | Detached mode: Run containers in the background, print new container names.                                                |
| `--build`        | Build images before starting containers.                                                                                   |

> Builds, (re)creates, starts, and attaches to containers for a service.
>
> Unless they are already running, this command also starts any linked services.
>
> The `docker-compose up` command aggregates the output of each container (essentially running `docker-compose logs -f`). When
> the command exits, all containers are stopped. Running `docker-compose up -d`
> starts the containers in the background and leaves them running.
>
> If there are existing containers for a service, and the service's configuration
> or image was changed after the container's creation, `docker-compose up` picks
> up the changes by stopping and recreating the containers (preserving mounted
> volumes). To prevent Compose from picking up changes, use the `--no-recreate`
> flag.
>
> If you want to force Compose to stop and recreate all containers, use the
> `--force-recreate` flag.
>
> If the process encounters an error, the exit code for this command is `1`.  
> If the process is interrupted using `SIGINT` (`ctrl` + `C`) or `SIGTERM`, the containers are stopped, and the > exit code is `0`.  
> If `SIGINT` or `SIGTERM` is sent again during this shutdown phase, the running containers are killed, and the exit code is `2`.
