Create container

docker run --name $CONTAINERNAME -it -v host-vol:container-vol $IMAGENAME bash

Run with GPU add flag --runtime=nvidia
ex. docker run --runtime=nvidia -it $IMAGE bash



