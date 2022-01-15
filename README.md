# crospin-docker
## Installation Guide
### Prerequisites

- Docker 20 or above
- Docker Compose 1.29 or above
- **DO NOT USE** root user for starting docker, and avoid using root user for pulling or handling docker configuration
- Create a symbolic link on folder crospin-dev using .env.dev file of folder **api** 
  - `ln -s ../../api/.env.dev .env`
- Create a symbolic link on folder crospin-test using .env.test file of folder **api** 
  - `ln -s ../../api/.env.test .env`

### Steps to follow

- Create an entry on **/etc/hosts** with these values: _127.0.0.1 host.docker.internal_,
  - `echo "127.0.0.1 localhost" >> /etc/hosts`<br />

- Run _docker_compose up_ on crospin-dev directory to start **Crospin** and crospin-test directory to run tests suite

### Verification

In order to verify backend started correctly, just open `http://localhost:3001/healthcheck`
In order to verify frontend started correctly, just open `http://localhost:3000`