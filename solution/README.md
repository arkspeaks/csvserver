DOCKER PART1 Commands:

1.  Installed the Docker on ubuntu server
2.  docker pull infracloudio/csvserver:latest
3.  docker pull prom/prometheus:v2.22.0
4   docker run -i -t infracloudio/csvserver   Got an error 2021/12/12 07:45:00 error while reading the file "/csvserver/inputdata": open /csvserver/inputdata
5.  mkdir /home/assignement
6.  vi gencsv.sh
7.  chmod 755 gencsv.sh
8.  bash  gencsv.sh
9.  docker -it infracloudio/csvserver /bin/bash
10. Quit the container and run: docker ps -a
a4944758867c   infracloudio/csvserver   "/bin/bash"              About a minute ago   Up About a minute           9300/tcp   bold_bartik
Container was running on the port 9300.
11. Removed the container using command:  docker rm ID
12. docker run -p 9393:9300 --name csv -e CSVSERVER_BORDER=Orange -v /home/assignment/inputFile:/csvserver/inputdata -itd infracloudio/csvserver
