# cv_bridge for melodic

用于解决opencv版本与ros冲突的问题

- 下载编译
- 部署到所需要的ros包

## 下载编译

```
mkdir -p cv_bridge_ws/src
cd cv_bridge_ws/src
git clone https://gitee.com/bingobinlw/cv_bridge
cd ..
```

将opencv编译生成的build文件路径加入到[CMakeLists.txt](./CMakeList.txt)（详见此文件目录下的CMakeLists.txt文件）

```
set(OpenCV_DIR "your-path/opencv-x.x.x/build")
```

编译

```
catkin_make
```

## 部署到所需要的ros包

将所需的修改的ros包里的**CMakeLists.txt**文件中添加opencv路径以及cv_bridge路径

```
set(OpenCV_DIR "your-path/opencv-x.x.x/build")
set(cv_bridge_DIR your-path/cv_bridge_ws/devel/share/cv_bridge/cmake)
```



