# Ghost Setup on Docker

How to set up Ghost on Docker using external volumes.

## Volumes

Copy the directory in [sample-volumes](sample-volumes/) to e.g. `~/Desktop`. This is where Ghost's data, images, themes and apps will be kept (out of the Docker container).

## Docker

As indicated by the [official repository](https://hub.docker.com/_/ghost/):

```bash
docker run --name ghost -d -p 8080:2368 -v ~/Desktop/sample-volumes/:/var/lib/ghost ghost
```

Open `http://<host>` for the blog or `http://<host>/ghost` for the admin page. If you're running Docker on OS X, `<host>` will be `192.168.99.100`.
