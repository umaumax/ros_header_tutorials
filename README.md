# ros_header_tutorials

## 同一パッケージ内のincludeを利用したい場合
下記の`include`をコメントアウト
```
## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)
```

----

## init command
```
catkin_create_pkg ros_header_tutorials std_msgs roscpp
```
