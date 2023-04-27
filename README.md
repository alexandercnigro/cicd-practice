# cicd-practice

## Jenkins
https://www.jenkins.io/download/




## Concourse
https://concourse-ci.org/quick-start.html
^^^ left off at installing the Fly CLI

### Run Concourse Instance (local) Instructions
- run Docker
- `cd cicd-practice/concourse`
- if docker images not downloaded, `docker-compose pull`
- `docker-compose up`. This will run a local concourse instance on your machine which will be reachable at http://localhost:8080

### How to update your pipeline
- fly -t <targetInstance> set-pipeline -l <filepathToLoadVarsFrom> -c <filepathToPipelineConfig> -p <pipelineName>
- -t <targetName> in this case will be *tutorial* since the name of your local cocnourse instance is that
- -l <filepathToLoadVarsFrom> in this case will be `concourse/config.yml`
- -c <filepathToPipelineConfig> in this case will be `concourse/simple-microservices/simple-microservices-pipeline.yml`
- -p <pipelineName> in this case will be *simple-microservices*

### How to run a job
- Navigate to the home page (in this case http://localhost:8080)
- click on your pipeline
- click on the first task
- click the plus sign in the top right of the screen