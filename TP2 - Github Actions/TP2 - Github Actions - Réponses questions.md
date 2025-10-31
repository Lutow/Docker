Question 2-1: What are testcontainers?

Testcontainers is a testing library in java that allows you to run real services (like databases) inside Docker containers during integration tests. In a Maven pom.xml, Testcontainers dependencies are added under the <dependencies> section with <scope>test</scope>.

Question 2-2: For what purpose do we need to use secured variables?

Secrets are used to protect sensitive information such as passwords, tokens or API keys that are needed by the workflows to run. Instead of hardcoding them, we store them in GitHub's Secrets storage.

Question 2-3: Why did we put needs: build-and-test-backend on this job?

The `needs` section defines job dependencies and execution order. It tells GitHub Actions that the `build-and-push-docker-image` job has to wait for `test-backend` to finish successfully before it can start.

Question 2-4: For what purpose do we need to push docker images?

We push Docker images to a registry (like Docker Hub) so they can be pulled and deployed across different environments or servers. 
