# Install Jenkins image on to Docker

Pull latest Jenkins docker image and run it

```
docker run -p 8080:8080 -p 5000:5000 -d -v jenkins_home:/var/jenkins_home jenkins/jenkins:lts
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

