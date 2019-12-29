# build

```
docker build -t pyvino_image .
```

# run

```
docker run -it \
--name pyvino \
-e DISPLAY=$DISPLAY \
-v /tmp/.X11-unix:/tmp/.X11-unix \
-v /Users/yuya/src:/home/ubuntu/src \
-p 8888:8888 \
pyvino_image \
/bin/bash
```

# start
```
docker start pyvino
```

# exec
```
docker exec -it pyvino bash
```

# env
path to pose extractor module for 3d pose estimation
```
export PYTHONPATH=/home/ubuntu/src/pyvino/pyvino/model/human_pose_estimation/human_3d_pose_estimator/pose_extractor/build/
```

setupvars for openvino
```
source /opt/intel/openvino/bin/setupvars.sh 
```

# jupyter notebook
```
jupyter notebook --port 8888 --ip=0.0.0.0 --allow-root
```