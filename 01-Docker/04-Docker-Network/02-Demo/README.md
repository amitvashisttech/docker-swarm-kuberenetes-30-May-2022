```
  155  docker kill $(docker ps -qa ) 
  156  docker rm $(docker ps -qa ) 
  157  ls
  158  docker network ls 
  159  docker network create mynet
  160  docker network ls 
  161  docker network inspect mynet
  162  ip addr 
  163  ls
  164  docker run -it --name test-network-1 --network mynet ubuntu:16.04 
  165  docker ps 
  166  docker commit -p -m "NetTools Installed" 0200fa7b97da ubuntu-nettools:16.04
  167  docker ps 
  168  docker images 
  169  docker run -it --name test-network-2 --network mynet ubuntu-netools:16.04 
  170  docker run -it --name test-network-2 --network mynet ubuntu-nettools:16.04 
  171  docker run -it --name test-network-3  ubuntu-nettools:16.04 
  172  docker ps 
  173  docker exec -it test-network-1 -- ifconfig 
  174  docker exec -it test-network-1  ifconfig 
  175  docker exec -it test-network-2  ifconfig 
  176  docker exec -it test-network-3  ifconfig 
  177  ls
  178  docker network create mybr0 --help
  179  docker network create mybr0 --driver=bridge --subnet=172.28.0.0/16 --ip-range=172.28.5.0/24 --gateway=172.28.5.1
  180  docker network ls 
  181  docker network inspect mybr0
  182  ip addr 
  183  ls
  184  docker run -it --name test-network-2 --network mybr0 ubuntu-nettools:16.04 
  185  docker run -it --name test-network-5 --network mybr0 ubuntu-nettools:16.04 
  186  docker run -itd --name test-network-6 --network mybr0 ubuntu-nettools:16.04 
  187  docker exec -it test-network-5  ifconfig 
  188  ping 172.28.5.0
  189  docker exec -it test-network-6  ifconfig 
  190  ls
  191  docker network ls 
  192  netstat -tulnp 
  193  docker run -itd --name test-network-7 --network host ubuntu-nettools:16.04 
  194  docker ps 
  195  docker exec -it test-network-6  ifconfig 
  196  docker exec -it test-network-7  ifconfig 
  197  docker images 
  198  netstat -tulnp 
  199  docker run -itd --name test-network-8 --network host python-web-app:v2
  200  netstat -tulnp 
  201  docker ps 
  202  curl localhost:8081
  203  docker run -itd --name test-network-9 --network none ubuntu-nettools:16.04 
  204  docker exec -it test-network-9  ifconfig 
  205  ls
  206  cd 01-Docker/
  207  ls
  208  cd 04-Docker-Network/
  209  ls
  210  mkdir 02-Demo
  211  cd 02-Demo/
  212  ls
  213  history > README.md
```
