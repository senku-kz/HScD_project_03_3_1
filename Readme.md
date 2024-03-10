### Get the up-to-date list of packages available for the installation by running the following command:
sudo apt update -y

### Run the following command to install the cross-compilation tools:
sudo apt install -y crossbuild-essential-armel



### Run CMake:
cd build && cmake ..

### Now, build the application by running the following:
make

### Get information about the resulting executable binary using the file command:
file hello


rm -rf ./*
cmake ..
make
file hello