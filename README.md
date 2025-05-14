# sand-e
sudo apt-get install git
sudo apt-get install python3-rosdep

mkdir -p ~/sand_e_ws/src
git clone https://github.com/ros/ros_tutorials.git -b humble
cd ..
rosdep install -i --from-path src --rosdistro humble -y

