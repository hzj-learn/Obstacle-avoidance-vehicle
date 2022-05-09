# R150 NDT建图
roslaunch r150_simulation r150_ndt_mapping.launch

# 保存地图
rosrun pcl_ros pointcloud_to_pcd input:=/ndt_map prefix:=map

## 录制移动轨迹
roslaunch waypoint_saver waypoint_saver.launch

## 读取轨迹
roslaunch waypoint_loader waypoint_loader.launch

# R150动态避障整体演示
roslaunch r150_simulation r150_ndt_planning.launch

## package依赖

## 参数配置说明

## 启动说明

[R150驱动程序](src/r150-chassis-driver/README.md)
