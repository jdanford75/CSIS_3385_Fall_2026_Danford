# CSIS 3385 — Database & Web Security

## Project 1B — Docker Web App

**Jack Danford · Austin Community College**

I packaged a static HTML page in an Nginx container and verified that Firefox displayed the page at `localhost:8080`. The [Dockerfile](my-docker-webapp/Dockerfile) uses `nginx:alpine` and serves [index.html](my-docker-webapp/index.html) on container port 80.

### Run locally

From the repository root with Docker running:

```sh
docker build -t csis3385-webapp ./my-docker-webapp
docker run --rm -p 127.0.0.1:8080:80 csis3385-webapp
```

Open `http://localhost:8080`. The page should display **Hello from inside a Docker container!**

### Submission evidence

![Firefox displaying the Docker web app at localhost:8080](docs/project-1b-docker-browser.png)
