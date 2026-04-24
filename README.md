Test Case 4 — Docker & Containerization
Scenario: The Node.js API from Test Case 3 must be packaged into a Docker container for consistent deployment.

Tasks
Write a Dockerfile in the project root that:
Uses node:18-alpine as the base image.
Sets /app as the working directory.
Copies and installs dependencies.
Exposes port 8080.
Starts the application using node index.js.
Build a Docker image named nodejs-api.
Run the container and verify the /health endpoint responds correctly on http://localhost:8080/health.
Write a docker-compose.yml file to run the application as a background service on the same port.
Expected Outcome
docker build completes with no errors and the image appears in docker images.
The container starts successfully and GET http://localhost:8080/health returns:
{ "status": "OK" }
docker compose up -d starts the service in detached mode with no errors.
