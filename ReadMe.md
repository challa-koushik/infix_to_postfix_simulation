
** we created infix to postfix simulation using stack operations like pop, push , Here we also created gui in c++ to simulation of stack **




step 1:

open terminal in windows
"wsl --install " run this comand

//after installation
step-2:

sudo apt update
sudo apt upgrade -y

step 3:

"sudo apt install -y build-essential"

step 4:

"sudo apt install -y cmake "

step-5:

"cmake --version "
You should see something like:
"cmake version 3.xx.x"

step-6:

"sudo apt install -y qtbase5-dev qt5-qmake qttools5-dev-tools"

step 7:

open vs code of the project folder and (ctrl + shift + p)
then
u will see wsl reload/reopen

step-8:



mkdir build
cd build
cmake ..
make
./infix-postfix-sim