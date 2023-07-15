# Dockerizing a simple HTML site using Nginx as the base image

# Steps
1. Build the image
```docker build -t mini-project-3 .```

# Note
- The `CMD ["nginx", "-g", "daemon on;"] && tail -f /dev/null` in the Dockerfile
tells Docker to start the Nginx process with the `daemon on;` option, and then execute the `tail` command to keep the container running. The `tail` command will output nothing (because it's reading from `/dev/null`), but it will keep the container running until it's manually stopped.