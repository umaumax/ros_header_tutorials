# ros_header_tutorials

## 同一パッケージ内のinclude dirを利用したい場合
下記の`include`をコメントアウト
```
## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
```

## 他のパッケージでheaderを利用したい場合
これは外部パッケージがこのパッケージに依存する場合にパラメータ情報を渡すための設定
```
catkin_package(
  INCLUDE_DIRS include
#  LIBRARIES ros_header_tutorials
#  CATKIN_DEPENDS roscpp std_msgs
#  DEPENDS system_lib
)
```

e.g.
```
${ros_header_tutorials_INCLUDE_DIRS}=~/catkin_ws/src/ros_header_tutorials/include
```

----

## init command
```
catkin_create_pkg ros_header_tutorials std_msgs roscpp
```
