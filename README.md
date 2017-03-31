# Torcs-Installation
How to Install TORCS in an hour

Tested on:

Ubuntu 14.04.5. Download from here

Make Directory:

    cd /usr/src/ 

    mkdir torcs 

Install Dependencies:

    sudo su (ALL COMMANDS UNDER ROOT)	

    apt-get install build-essential libxmu-dev libxmu6 libxi-dev libxine-dev libalut-dev freeglut3 freeglut3-dev cmake libogg-dev libvorbis-dev libxxf86dga-dev libxxf86vm-dev libxrender-dev libxrandr-dev zlib1g-dev libpng12-dev

    PLIB 1.8.5

    Download PLIB 1.8.5 from here 

    tar xfvz /path/plib-1.8.5...

    cd plib-1.8.5

    ./configure CFLAGS=”-fPIC” CXXFLAGS=”-fPIC” CPPFLAGS=”-fPIC” 

    make 

    make instal

    OpenAL

    Download OpenAL from here

    tar xfvj /path/openal-soft-1.17.2...

    cd openal-soft-1.17.2

    cd build

    cmake ..

    make

    make install

    FreeGlut

    Download FreeGlut from here

    tar xfvz /path/freeglut-3.0.0...

    cd freeglut-3.0.0

    cmake .

    make

    make install

 

Install TORCS:

    Download TORCS from here

    tar xfvj /path/torcs-1.3.7...

    cd torcs-1.3.7

    ./configure

    make

    make install

    make datainstall

Run TORCS:

    torcs

 

 

Permissions:

    cd /usr/src/

    chown -R uname:ugroup torcs

    cd /usr/local/share/games

    chown -R uname:ugroup torcs

    cd /usr/local/lib

    chown -R uname:ugroup torcs

Environment:

    cd /home/

    vi ~/.bashrc

    Copy the following on the end of the file: 

    export LD_LIBRARY_PATH=$LD_LIBRARY_PATH:/usr/local/lib

    export TORCS_BASE=/usr/src/torcs/torcs-1.3.7

    export MAKE_DEFAULT=$TORCS_BASE/Make-default.mk

    Put a newline after the last line in the file and save.

    Open a new terminal to check if successful:

    cd $TORCS_BASE

    ls

 

 

 

 

 

References:

    [1] TORCS PDF tutorial: http://www.berniw.org/aboutme/publications/torcs.pdf

    [2] TORCS web tutorial: http://www.berniw.org/tutorials/robot/tutorial.html
