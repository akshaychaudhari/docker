docker
=======

Basic commands:
--------------
>>docker --version
>>docker info

* Check present docker images:
>>docker images

>>docker hello-world

* To run linux container and run bash in it:
>> docker run -ti ubuntu:latest  bash
 (ti stands for terminal interface)

* To see running images:
docker ps --format $FORMAT

```BASH
*Putting/Check format variable:
echo $FORMAT
>>\nID\t{{.Id}}\nIMAGE\t{{Image}}
```
* Check the last container:
>> docker ps -l 

* Make docker images out of container, return image_id:
>> docker commit container_id

* To give image a name:
>> docker tag image_id my-image

* Short-hand to commit and give image a name:
>>docker commit container_name my-image2

* Test my-image by running process 'bash' in it
>> docker run ti my-image bash

* Run container for 5 sec
> docker run --rm ti ubuntu sleep 5

- Run container with bash commands
> docker run ti ubuntu bash -c "sleep 3; echo all done"
> docker run --name my_container

- Run and detach the container
> docker run -d -ti ubuntu bash

- attach the container 
> docker attach container_name

- detach container
> ctrl P ctrl Q 

- use same container parallely and start bash
> docker exec -ti container_name bash

- To exit container
> ctrl D

- Logs
> docker logs container_name

- Killing and removing docker container
> docker kill container_name
> docker rm container_name

- We can add memory constraints, CPU limits and various orchestrations to docker container

* Building the container
> docker build -t container_build01

* Running the image:
> docker run -d -p 80:80 \ --name docker_img01 container_build01

* Pushing image to docker hub
> docker tag docker_img01 akshaychaudhari/my-image01
> docker push akshaychaudhari/my-image01


