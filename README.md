<h1 align="center">Practical Exercise - Container Registry</h1>


## TASK: 

Continuing with the above Node JS image, save your image with the following conditions. 

**CONDITIONS:**

1. You can save your image in docker hub or any other container registry you are familiar with.  
2. Image Should have proper name and tag 
3. Image must be private image 
4. Run your application using registry image 

## DOCKERHUB LINK:
<h5 align="center">https://hub.docker.com/repositories/jayrajmalamdi </h5>

## SOLUTION:

1. clone the nodejs application from github repository:
```
$ git clone git@github.com:Jayraj-Malamdi/docker-assignment_1.git 
```
2. Make image of the nodejs application: 
```
$ sudo docker build –t docker_prac_1:v1.0 .
```
3. Sign in to docker hub account 
```
$ sudo docker login
```
4. Creating private repository on docker hub.
5. Tagging my image with private repository name given in my docker hub repository. 
```
$ sudo docker tag jayrajmalamdi/docker_prac_1:v1.0 jayrajmalamdi/task3_private_repo:v1.0
```
6. Pushing the private repo image to docker hub private repository. 
```
$ sudo docker push jayrajmalamdi/task3_private_repo:v1.0
```
7. Verifying it by pulling the image and running it. 
```
$ sudo docker login 
$ sudo docker pull jayrajmalamdi/task3_private_repo:v1.0
$ docker run –name task3_private_cont –d –p 5000:3000 jayrajmalamdi/task3_private_repo:v1.0 
```
## OUTPUT:

![MicrosoftTeams-image (2)](https://user-images.githubusercontent.com/122361229/235102250-253d6460-6c00-46af-bf2e-8f091521b0c0.png )


 

 
