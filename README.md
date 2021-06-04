Simple Web Server with reverse proxy in front of it

For simplicity it uses Traefik as ReverseProxy (due to easyness on configuration) and Apache as Web Server.

the way to use it is to clone all the repo and just run: "docker-compose up -d"; the docker compose is instructed to build the container locally from the paths proxy and webserver, when stop the test you can run: "docker-compose down --rmi all" in order to stop the containers and prune the unused images.

The proxy accepts only request with Host information in the header, the host should be "techtask.demo.cf", also it uses basic authentication User/Pass combination is "techtask:techtask"

