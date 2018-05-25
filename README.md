# Ubuntu Docker Development Environment


Download the image from the repo (password required)
```
docker pull gjrdiesel/ubuntu-dev
```

Start a docker container and mount the host root directory to /host and call it ubuntu-dev (start it as a daemon too!).
```
docker run -p 8080:80 --name=dev -v C:\:/host -itd ubuntu-dev
```

Make any changes? Then save them via
```
docker commit dev ubuntu-dev && docker push gjrdiesel/ubuntu-dev:latest
```

Want to run a specific directory?
```
docker run -p 8080:80 --name=dev -v C:\:/host \ 
-v C:\Users\reaso\git\[dir]:/var/www/html -itd ubuntu-dev
```