# Build Sonic Kart from Ubuntu 64bit from original repo
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; git clone https://github.com/STJr/Kart-Public.git ; cd Sonic-Kart ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1
```

# Build Sonic Robo Blast 2 64bit from Ubuntu 64bit

First you have to download the windows exe file who contain the gamefiles, but don't work with wget (idkw), here is to wget an archive from a forked repo (mine)
```
wget http://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/srb2files.tar.gz
```
Extract and delete archive :
```
tar xvzf srb2files.tar.gz ; rm srb2files.tar.gz
```
Dependencies :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git
```
Download Source code :
```
git clone https://github.com/B4rabbas/SRB2.git
```
Go in to the folder :
```
cd SRB2
```
Start Compiling
```
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
make -C src/ LINUX64=1
```
You executable is in ~/SRB2/bin/Linux64/Release/

If you want to install it, continue with

Copy game executable in your files folder and delete source folder &
```
cd /..
cp ~/SRB2/bin/Linux64/Release//lsdl2srb2 ~/srb2files/
sudo rm -rf ~/SRB2/
```
Rename and copy in /usr/games
```
sudo mv ~/srb2files/ /usr/games/SRB2/
```
Launch with :
```
/usr/games/SRB2/lsdl2srb2
```
One line copy past to build :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git ; git clone https://github.com/B4rabbas/SRB2.git ; cd SRB2 ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1
```
Your compiled executable is 
~/SRB2/bin/Linux64/Release/lsdl2srb2

One line copy past to build and install :
```
sudo apt install -y libgme-dev libsdl2-mixer-dev libsdl2-dev zlib1g-dev libpng-dev nasm build-essential git
wget http://github.com/B4rabbas/Sonic-Kart/releases/download/1.0.0.0.0.0.1/srb2files.tar.gz ; tar xvzf srb2files.tar.gz ; rm srb2files.tar.gz ; git clone https://github.com/B4rabbas/SRB2.git ; cd SRB2 ; export LIBGME_CFLAGS= ; export LIBGME_LDFLAGS=-lgme ; make -C src/ LINUX64=1 ; cd /.. ; cp ~/SRB2/bin/Linux64/Release//lsdl2srb2 ~/srb2files/ ; sudo rm -rf ~/SRB2/ ; sudo mv ~/srb2files/ /usr/games/SRB2/
```
Launch with :
```
/usr/games/SRB2/lsdl2srb2
```

## Cross compilation Not tested
Compile 32 bit linux executable
```
git clone https://github.com/B4rabbas/SRB2.git
cd SBR2
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
set CC=gcc -m32 
make -C LINUX=1 
```

Compile 64 windows executable :
```
git clone https://github.com/B4rabbas/SRB2.git
cd SBR2
export LIBGME_CFLAGS=
export LIBGME_LDFLAGS=-lgme
set PREFIX=i686-w64-mingw32
make -C src/ MINGW=1
```


