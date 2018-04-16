#############################################################################
sudo apt-get install libglfw3-dev;
sudo apt-get install libosmesa6-dev;
cd /usr/lib/; sudo ln -s libGL.so.1 libGL.so; cd -;
#############################################################################
git clone https://github.com/openai/mujoco-py;
cd mujoco-py; 
pip install -e .;
#############################################################################
wget https://www.roboti.us/download/mjpro150_linux.zip;
mkdir ~/.mujoco;
unzip mjpro150_linux.zip -d ~/.mujoco;
#############################################################################
wget https://www.roboti.us/getid/getid_linux;
chmod 755 ./getid_linux;
./getid_linux;
#############################################################################
cp mjkey_158.txt  ~/.mujoco/mjkey.txt
ls ~/.mujoco/mjkey.txt;
#############################################################################
echo 'export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/home/danny/.mujoco/mjpro150/bin' >> ~/.bashrc; source ~/.bashrc;
python; import mujoco_py
#############################################################################



