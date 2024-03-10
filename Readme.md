### Get the up-to-date list of packages available for the installation by running the following command:
sudo apt update -y

### Run the following command to install the cross-compilation tools:
sudo apt install -y crossbuild-essential-armel

### go to the build directory
mkdir build
cd build


# Compile for x86 architecture
## Commit 16-21 lines in CMakeLists.txt
### Run CMake:
cmake ..

### Now, build the application by running the following:
make

### Get information about the resulting executable binary using the file command:
file hello


# Compile for ARM architecture
## UnCommit 16-21 lines in CMakeLists.txt
### Remove files in folder
rm -rf ./*

### Run CMake:
cmake ..

### Now, build the application by running the following:
make

### Get information about the resulting executable binary using the file command:
file hello
