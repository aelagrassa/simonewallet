# Installing the GUI Wallet #

Simone GUI wallet is currently only available for Linux distributions. There are no premade packages and the GUI wallet must be compiled from source. The node software must be installed before attempting to install the GUI wallet. For directions on installing the node software please check [the simone readme](https://github.com/aelagrassa/simone).

## Installing the GUI Wallet on Ubuntu ##

The following steps have been tested and confirmed to work on the following Ubuntu distros:
- Ubuntu 16.04 LTS
- Ubuntu 18.04 LTS

Install the required software
```
sudo apt install qt5-default
```
In the **directory your simone install directory is in,** clone simonewallet. Example:
- /home
  - **/user**
    - /simone
    - /simonewallet
```
git clone https://github.com/aelagrassa/simonewallet
```
Change to the simonewallet directory
```
cd simonewallet
```
Create a symlink for sources to reference
```
ln -s ../simone cryptonote
```
Create a build directory and move to it
```
mkdir build
cd build
```
Run cmake and prepare to compile
```
cmake ..
```
Compile the wallet
```
make
```
The wallet is now compiled and ready for use
## Using the GUI Wallet on Ubuntu ##
Once you have finished compiling you may launch the wallet from your terminal in a GUI session. Navigate to 
```
simonewallet/build
```
Launch the GUI wallet
```
./Simone
