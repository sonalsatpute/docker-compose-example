# Basic Docker commands

## Build using docker file

$ docker build -t sonalsatpute/example-01 .

## View images

$ docker images

REPOSITORY                TAG                 IMAGE ID            CREATED             SIZE
sonalsatpute/example-01   latest              0c51c2bbb56a        4 seconds ago       94.6MB
redis                     alpine              98bd7cfc43b8        10 days ago         27.8MB
python                    3.4-alpine          6610ae9fa51a        2 weeks ago         83.6MB

## Run

$ docker run -it -p "8080:80" --rm --name example-01 sonalsatpute/example-01

* Running on http://0.0.0.0:5000/ (Press CTRL+C to quit)
* Restarting with stat
* Debugger is active!
* Debugger PIN: XX-XXX-XXX


## Get long container ID

$ docker container ls

CONTAINER ID        IMAGE                     COMMAND             CREATED             STATUS              PORTS                  NAMES
d2d27c8b3e91        sonalsatpute/example-01   "python app.py"     39 seconds ago      Up 38 seconds       0.0.0.0:5000->80/tcp   example-01

## View container IP

$ docker exec ac06500697ae ifconfig

# Share your image

## Log in with your Docker ID

$ docker login

- enter username and password

## Publish the image

$ docker push sonalsatpute/example-01

## Pull and run the image from the remote repository

$ docker run -p sonalsatpute/example-01

