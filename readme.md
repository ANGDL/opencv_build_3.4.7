directories tree:
```
opencv_build_3.4.7
    ├── opencv
    └── opencv_contrib
    └── .cache
```

shell
```shell
mkdir opencv/build
cp -r .cache opencv/build
cd build

cmake \
    -DENABLE_CXX11=ON \
    -DCMAKE_BUILD_TYPE=Release \
    -DCMAKE_INSTALL_PREFIX=../bin \
    -DBUILD_IPPICV=OFF \
    -DBUILD_PNG=ON \
    -DBUILD_TIFF=ON \
    -DBUILD_TBB=OFF \
    -DBUILD_JPEG=ON \
    -DBUILD_JASPER=OFF \
    -DBUILD_ZLIB=OFF \
    -DBUILD_EXAMPLES=ON \
    -DBUILD_opencv_java=OFF \
    -DBUILD_opencv_python2=OFF \
    -DBUILD_opencv_python3=OFF \
    -DWITH_OPENCL=ON \
    -DWITH_OPENMP=OFF \
    -DWITH_FFMPEG=OFF \
    -DWITH_GSTREAMER=OFF \
    -DWITH_GSTREAMER_0_10=OFF \
    -DWITH_CUDA=OFF \
    -DBUILD_opencv_cudacodec=OFF \
    -DWITH_GTK=ON \
    -DWITH_VTK=OFF \
    -DWITH_TBB=ON \
    -DWITH_1394=OFF \
    -DWITH_OPENEXR=ON \
    -DCUDA_TOOLKIT_ROOT_DIR=/usr/local/cuda \
    -DCUDA_ARCH_BIN=7.5 \
    -DCUDA_ARCH_PTX="" \
    -DINSTALL_C_EXAMPLES=ON \
    -DINSTALL_TESTS=OFF \
    -DOPENCV_ENABLE_NONFREE=ON \
    -DBUILD_opencv_world=ON\
    -DBUILD_LIBPROTOBUF_FROM_SOURCES=ON \
    -D CUDA_NVCC_FLAGS="-std=c++11 --expt-relaxed-constexpr" \
    ..
```
