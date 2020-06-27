docker
------

Basic commands:

>>docker --version
>>docker info

*Check present docker images:
>>docker images

>>docker hello-world

* To run linux container and run bash in it:
>> docker run -ti ubuntu:latest  bash
 (ti stands for terminal interface)

* To see running images:
docker ps --format $FORMAT

*Putting/Check format variable:
echo $FORMAT
>>\nID\t{{.Id}}\nIMAGE\t{{Image}}

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

* Run image 


