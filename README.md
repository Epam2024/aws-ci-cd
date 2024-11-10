# aws-ci-cd

For code compliation in Sprint boot project we have to run the below code 

mvn clean package 

For Gradle :-
gradle build ensures .jar & .war file in the build/libs directory 


<!-- ##Step 3: Automate Steps 1 and 2 with AWS CodeBuild## -->
Define the steps in the buildspec.yaml file, which has three phases:
1. Pre-build:

Commands for Maven clean, generating the JAR file, ECR repository URI, login credentials, CodeBuild commits, and image tags.

2. Build:

Commands for building and tagging the Docker image.

3. Post-build:

Commands for pushing the image to ECR with the registry name.

Provide the buildspec.yaml file to AWS CodeBuild to execute the defined steps.