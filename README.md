# Docker-Entrypoint

Provide a single file `docker-entrypoint.sh`, intended to be set as a Dockerfile's `ENTRYPOINT`.

At the container's launche, this script will, in order:

* Source the `/dockerconfig.env` file, if it exists
* Execute custom scripts in `/docker-entrypoint.d/` folder
* `exec` its arguments (essentially, executing the Dockerfile's `CMD`)
