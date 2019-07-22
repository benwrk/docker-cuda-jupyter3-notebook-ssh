Create container

docker run --name $CONTAINERNAME -it -v host-vol:container-vol $IMAGENAME bash

Run with GPU add flag --runtime=nvidia
ex. docker run --runtime=nvidia -it $IMAGE bash

## Tensorflow, Jupyter, Miniconda3
1. cd ~
2. export JUPYTER_PORT=888X
3. export SSH_PORT=222X
2. docker run -dt --runtime=nvidia --name test --restart always -p $JUPYTER_PORT:8888 -p SSH_PORT:22 -v $PWD:/home gpu-conda-tf-jupyter-ssh:1.0.0

Access to container: ssh root@SERVER_IP -p SSH_PORT
