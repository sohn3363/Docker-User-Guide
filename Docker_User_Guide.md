# Docker User Guide
- 2021.02.24 Updated
- source from: (https://leesungjae-git.github.io/).

---
### 1. Make Container
#### 1) Find docker image
   > docker search pytorch
#### 2) Download docker image
   > docker pull <image_name>
#### 3) Image check
   > docker images
#### 4) Make container 
   > docker run -itd --name <container_name> -v </root of local folder:/root of docker folder> -p <nnnn:nnnn> --gpus all
   > > -v : (Sharing) sharing local folder to docker folder
   > > 
   > > -p : (Connection) connect local port to docker port
   > > 
   > > --gpus all: allocate all gpus 
#### 5) Contatiner execution
   > docker exec -it <container_name> bash

---   
### 2. Jupyter Notebook in Docker
#### 1) Jupyter Notebook installation
   > conda install jupyter
#### 2) Jupyter Notebook excution
   > jupyter notebook --ip=0.0.0.0 --port=nnnn --allow-root
   > > --ip=0.0.0.0 : automatic IP allocate
   > > --port=nnnn : your docker port
   > > --allow-root : allow adnimistrator option
---
