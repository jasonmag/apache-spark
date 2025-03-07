# Starting Apache Spark

by jasonmag

## Using docker

`docker run -it --rm spark:python3 /opt/spark/bin/pyspark`

## User Docker Compose

    - start: `docker-compose up -d`
        - running as detached
    - view logs: `docker-compose logs -f`
        - you can see the links,
            - e.g. http://127.0.0.1:8888 (Jupyter) | http://127.0.0.1:4040 (Spark UI)
    - If it asks for a token, get it from the logs
        - `docker logs pyspark_container | grep "http"`
    - stop: `docker-compose down`

## Setup in VSCode

    - Create new Jupyter Notebook
        - Command/Ctrl + Shift + p
        - `> Create: New Jupyter Notebook`
    - Select Kernel, on this setup is docker
        - Command/Ctrl + Shift + p
        - `Jupyter: Manage Access To Jupyter Kernel`
        - Input e.g. `http://127.0.0.1:8888/lab?token=<tokenValue>`
        