# Containerizing Nodejs Apps

--------------------
CREATE NETWORK
--------------------

docker create network app

--------------------
Run Mongodb app server
--------------------

docker run --name mongodb --rm --network app -d -v data:/data/db mongo

--------------------
Run backend app server
--------------------

docker run --name backend --rm --network app -v /root/projects/ContainerizeApps/multi-01-starting-setup/backend:/app -v /app/node_modules -v logs:/app/logs -d -p 80:80 backend 

--------------------
Run frontend app server
--------------------

docker run --name frontend -it -p 3000:3000 frontend

