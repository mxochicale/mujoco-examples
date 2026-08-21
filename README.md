# Mujoco examples

## Building from source
```bash
cd ~/repositories
git clone https://github.com/google-deepmind/mujoco.git
cd mujoco
mkdir -p build && cd build
cmake ..
cmake --build .
```

## Run examples

* Watch MuJoCo simulate tutorial: https://www.youtube.com/watch?v=P83tKA1iz2Y&t=22s

```bash
cd $HOME/repositories/mujoco/build/bin
./simulate ../model/humanoid.xml
./simulate ../model/22_humanoids.xml 
./simulate ../model/humanoid100.xml
```


## MuJoCo MPC (MJPC) 
```bash
git clone https://github.com/google-deepmind/mujoco_mpc
sudo apt-get update && sudo apt-get install cmake libgl1-mesa-dev libxinerama-dev libxcursor-dev libxrandr-dev libxi-dev ninja-build zlib1g-dev clang-12
cd mujoco_mpc
mkdir build && cd build
cmake .. -DCMAKE_BUILD_TYPE:STRING=Release -G Ninja -DCMAKE_C_COMPILER:STRING=gcc -DCMAKE_CXX_COMPILER:STRING=g++ -DMJPC_BUILD_GRPC_SERVICE:BOOL=ON -DCMAKE_SKIP_INSTALL_RULES=ON
#cmake .. -DCMAKE_BUILD_TYPE:STRING=Release -G Ninja -DCMAKE_C_COMPILER:STRING=clang-12 -DCMAKE_CXX_COMPILER:STRING=clang++-12 -DMJPC_BUILD_GRPC_SERVICE:BOOL=ON
cmake --build . --config=Release
#Run GUI application
cd bin
./mjpc
```

## References
* https://mujoco.org/
* https://mujoco.readthedocs.io/en/stable/programming/index.html#building-from-source


## Clone repo
```bash
git clone git@github.com:mxochicale/mujoco-examples.git
```

