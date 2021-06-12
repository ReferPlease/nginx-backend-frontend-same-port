# nginx-backend-frontend-same-port
Nginx Configuration to run the backend and frontend at the same port and hence to test service worker locally.
Actually backend runs at different port but request are routed to it based on context path when they hit the nginx(in this case it is /api) and the frontend is served through nginx.

## How to run
* Copy the frontend build folder to this folder
* All backend api should start with /api. In simple words set context path as /api
* In nginx.conf, replace the server ip address to your [local ip address]:[backend server port]. It is currently set to 192.168.1.6:8080
* docker build -t nginx . --no-cache
* docker run -dit -p 80:80 nginx
