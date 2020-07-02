## Dev Image

Build:

```bash
docker build -t sgkit-dev .
```

Run:

```bash
WORK_DIR=/home/jovyan/work
docker run --rm -ti \
-e GRANT_SUDO=yes --user=root \
-p 8898:8888 -p 8897:8887 \
-e JUPYTER_TOKEN=ItORmEnSTaTeNloRADHonisi \
-e VSCODE_TOKEN=ItORmEnSTaTeNloRADHonisi \
-e SPARK_DRIVER_MEMORY=64g \
-e JUPYTER_ENABLE_LAB=yes \
-v $HOME/.ssh:/home/jovyan/.ssh \
-v /data/disk1/dev:$WORK_DIR/data \
sgkit-dev
```