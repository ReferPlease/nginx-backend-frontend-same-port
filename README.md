# nginx-backend-frontend-same-port
Nginx Configuration to run the backend and frontend at the same port and hence to test service worker locally.
Actually backend 

## How to run
* Copy the frontend build folder to this folder
* In nginx.conf, replace the server ip address to your <local ip address>:<backend server port>
* docker build -t nginx . --no-cache
* docker run -dit -p 80:80 nginx
