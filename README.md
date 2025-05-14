# sand-e
echo "source /opt/ros/humble/setup.bash" >> ~/.bashrc

sudo apt-get install git
sudo apt-get install python3-rosdep
sudo apt install python3-colcon-common-extensions

mkdir -p ~/sand_e_ws/src
git clone https://github.com/ros/ros_tutorials.git -b humble
cd ..
rosdep install -i --from-path src --rosdistro humble -y
colcon build --symlink-install
cd
ros2 pkg executables turtlesim


