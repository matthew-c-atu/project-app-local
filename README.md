# project-app-local
Repo for running the final project music player app locally. Requires Docker compose.

### USAGE
- Install docker (https://docs.docker.com/get-docker/)
- Ensure docker compose is installed (https://docs.docker.com/compose/install/)
- Run `docker compose up` from this repo's directory.
  
# IMPORTANT
Running the project with this repo DOES NOT WORK.
The networking between services has not been implemented correctly between the Docker compose file and in the source code of the microservices themselves.
Specifically, the database services fails to connect to the audio-streamer service on port 9001, and the frontend fails to connect to the database on port 9002.

This repo exists to show how a runtime environment was planned, and to show that the CI pipeline setup for each repo above does indeed work and publish automatically and successfully to DockerHub.

Pulls images from the following DockerHub repos:
- https://hub.docker.com/repository/docker/matthewatu/project-react-frontend/general
- https://hub.docker.com/repository/docker/matthewatu/project-audio-streamer/general
- https://hub.docker.com/repository/docker/matthewatu/project-database/general
