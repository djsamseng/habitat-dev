## Installation
```bash
cd habitat-sim
git checkout stable
conda create -n 37 python=3.7 cmake=3.14.0
conda activate 37
pip3 install -r requirements.txt
sudo apt-get install -y --no-install-recommends libjpeg-dev libglm-dev libgl1-mesa-glx libegl1-mesa-dev mesa-utils xorg-dev freeglut3-dev
rm -rf ./build
python3 setup.py install --with-cuda --bullet
sudo apt install gstreamer1.0-libav
```


## Running
### Viewer
```bash
cd habitat-sim
./build/viewer --enable-physics --dataset ./data/replica_cad/replicaCAD.scene_dataset_config.json -- apt_1
```

### Asset viewer video python
```bash
cd habitat-sim
python3 examples/tutorials/nb_python/asset_viewer.py # Change object_to_view_path to asset to view
```

### Interactivity video python
```bash
cd habitat-sim
python3 examples/tutorials/nb_python/managed_rigid_object_tutorial.py
```