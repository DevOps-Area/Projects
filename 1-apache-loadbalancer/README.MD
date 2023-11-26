## Creating a single HAProxy and two Apache containers with Docker compose

- In this porject  we will create  two identical Apache servers and one HAProxy container. 

- When we want to access our website, we will be calling HAProxy, not the Apache servers. HAProxy will divert traffic to Apache servers in "round-robin" fashion.

1. HTTP Request goes to HAProxy container.

2. HAProxy container goes  either Apache container 1 or 2.

3. Response is served by Apache container 1 or 2.

- To test this use command 

 $ for in in {1..10} ; do echo "the working server is `curl -s http://127.0.0.1:90/`"; done

