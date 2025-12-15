# CI/CD Practice Repository

This is a tiny Node.js project you can use to practice CI/CD pipelines.

Contents:
- index.js — tiny HTTP server + exported helper
- package.json — scripts and deps
- test/app.test.js — Jest test
- Dockerfile — build image
- .github/workflows/ci.yml — GitHub Actions pipeline
- .gitlab-ci.yml — GitLab CI example
- Jenkinsfile — Jenkins Declarative pipeline

Quick start (locally)
1. Install dependencies:
   npm ci
2. Run tests:
   npm test
3. Run app:
   npm start
   then open http://localhost:3000

Practice exercises
1. GitHub Actions:
   - Push this repo to GitHub and observe the `CI` workflow run on push/PR.
   - Modify the test to fail and push — observe the pipeline failing.
   - Add a job to build a Docker image and push to Docker Hub (set secrets DOCKERHUB_USERNAME and DOCKERHUB_TOKEN).
2. GitLab CI:
   - Import repo into GitLab and enable CI. Try enabling Docker-in-Docker to build images.
3. Jenkins:
   - Create a Jenkins pipeline using the provided `Jenkinsfile`. Try running on a self-hosted agent.
4. Add more checks:
   - Add ESLint and a lint job.
   - Add integration tests (use supertest) and run them in CI.
5. Deployment:
   - Add a deploy stage: push image to a registry and deploy to a Kubernetes cluster or a simple VPS via SSH.

Notes about secrets
- Docker pushes and deploys require credentials. On GitHub Actions use repository Secrets. On GitLab use CI/CD variables. In Jenkins configure credentials and reference them in the pipeline.

Have fun experimenting — if you want I can:
- Create a GitHub repository with these files,
- Add an example that publishes images to Docker Hub,
- Or convert the example to another language or framework.
