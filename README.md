# docker images
this repository has made for my custom docker images


## build a dokcer image 

- Navigate to the directory containing your Dockerfile and build the image

'''
docker build -t alpine-awscli .
'''

## run docker image as a new container
'''
docker run -v /path/to/your/repo:/data -it alpine-awscli
'''