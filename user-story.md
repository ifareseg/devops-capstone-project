# User Story

As a developer  
I need to automate the deployment process using a Continuous Delivery pipeline  
So that I can ensure that code changes are automatically tested, built, and deployed to OpenShift without manual intervention  

# Acceptance Criteria

Given that code is pushed to the repository  
When the Tekton pipeline is triggered  
Then the pipeline should run linting, unit tests, build the container image, and deploy the application successfully  

Given that the pipeline runs successfully  
When the deployment step is executed  
Then the application should be updated with the latest image and be accessible via the OpenShift route  

Given that unit tests are executed  
When tests fail  
Then the pipeline should stop and not proceed to the build and deployment steps  

# Notes

- The pipeline uses Tekton for automation  
- SQLite is used for testing instead of PostgreSQL  
- Buildah is used to build and push container images  
- Kubernetes manifests are applied using kubectl  
