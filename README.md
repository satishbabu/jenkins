# Install Jenkins image on to Docker

Pull latest Jenkins docker image and run it..

```
docker run -p 8080:8080 -p 50000:50000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
```

-p --> expose the ports
-d --> run in the background
-v --> create persistence volume

Ensure Jenkins is running succesfully
```
docker ps
```

Jenkins server writes the password onto the log.  Get the password from the logs
```
docker logs <continerid>
```

Open Jenkins from the browser using `http://localhost:8080/` and follow the prompts to install common plug-ins and create a user.

# Create a pipeline and run it
Create a multibranch pipeline and provide the github url of this project.  Leave most of the other things on defaults.

Once the pipeline is created it connects to github and scans repository.  You can check the Logs from 'Scan Repository Log'.  It says 

    Checking branch main
      ‘Jenkinsfile’ not found
    Does not meet criteria




