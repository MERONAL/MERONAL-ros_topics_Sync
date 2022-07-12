# MERONAL-ros_topics_Sync

### 1. 代码拷贝
cd 
mkdir -p SensorTimeSync_ws/src
cd SensorTimeSync_ws/src
git clone https://github.com/MERONAL/MERONAL-ros_topics_Sync.git
cd SensorTimeSync 
mkdir include
cd ../../
(修改代码：topic、数据类型、callback内容等)
catkin_make
# 显示 [100%] Built target data_tb 完成代码拷贝

### 2. 代码使用
source devel/setup.bash
rosrun data_tb data_tb  # 记得启动 ros master
rosbag play ***  # 播放你想要同步的bag
rosbag record -a  # 记录同步好的bag  
