# Hi,<img src="Hi.gif" height="48" width="48" >  I’m @JackThanawat !
👀 I’m interested in Web Developer <br>
🌱 I’m currently learning Java, JavaScript, SQL, R <br>
💞️ I’m looking to collaborate on ...Who collaborate study same to me. <br>

## 📫 How to reach me 
👉 [Facebook](https://www.facebook.com/tnw.jack/)<br>
👉 [Page: ส่องโปร - SongPro](https://www.facebook.com/songpro.online) <br>
👉 [Instagram](https://www.instagram.com/jack.tnw/)<br><br>



## GitHub Stats
[![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=jacktnw&layout=demo&theme=radical)](https://github.com/anuraghazra/github-readme-stats) 
![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=jacktnw&show_icons=true&theme=radical)


<!--


Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->

# Docker Workshop

## Prerequisites

* Linux Terminal, Google Cloud Shell, MacOS Terminal, or WSL2 on Windows
* Docker
* Your own text editor such as Vim or VSCode

## Docker Image

```bash
# To show Docker Image on your machine
docker images
# To pull ubuntu image with tag latest from Docker Hub
docker pull ubuntu
# To show your newly pull ubuntu image on your machine
docker images
```

## Docker Image Name and Tag

```bash
# Pull Ubuntu 18.04
docker pull ubuntu:18.04
# To show Docker Image on your machine
docker images
# Pull Ubuntu 20.04
docker pull ubuntu:20.04
# See the Image ID
docker images
```

## Docker Container

```bash
# Run first ubuntu container
docker run ubuntu echo "Hello World"
# Run container with bash command
docker run -i -t ubuntu bash
# Below command are run inside container
whoami
hostname
cat /etc/*release*
exit
```

## Docker Container Basic Operation

```bash
# Show running containers
docker ps
# Show running and stopped containers
docker ps -a
# Run container with specify name
docker run --name ubuntu-universe ubuntu echo "Hello Universe"
docker ps -a
# Delete container by name
docker rm ubuntu-universe
docker ps -a
# Delete container by part of container id
docker rm 07f
docker ps -a
```

## Run Docker as daemon and expose port

```bash
# Run Nginx
docker run nginx:alpine
docker ps -a
# Run Nginx in background
docker run -d nginx:alpine
docker ps
# Export 8080 port from outside forward to port 80 on container
docker run -d -p 8080:80 nginx:alpine
```

* Click on icon `Web preview` and `Preview on port 8080` on the top right of Cloud Shell to access to nginx container

```bash
# What happen if try to expose same port again
docker run -d -p 8080:80 nginx:alpine
# What happen if we expose difference outside port
docker run -d -p 8888:80 nginx:alpine
# You can try Web preview again
docker ps
```

### Docker Exercise

* Try to run Apache Server 2.4.33 on Alpine Linux and expose to port 8083

> Hint: <https://hub.docker.com> and search for apache

## Docker Utilities Commands

```bash
# Rename container name
docker rename vigorous_sammet nginx
# To go inside running container
docker exec -it nginx sh
ls -l
ps -ef
exit
# Show container processes
docker top nginx
# Show logs
docker logs nginx
# Follow logs
docker logs nginx -f
# Try Web preview to see log running
# Show container resource consumes
docker stats
# Show container all metadatas
docker inspect nginx
```

* Delete all the containers

```bash
docker rm -f $(docker ps -aq)
```

