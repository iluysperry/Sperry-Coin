Sperry Coin
================================

http://www.sperrytecnologia.com.br

Copyright (c) 2015-2018 Sperry Tecnologia 

What is Sperry Coin?
----------------

Sperry Coin is more than a coin is an secure and customizable blockchain using cryptographical kabbalistic numerology provides new features in blockchain source using scrypt as a proof-of-work algorithm.

Using a fork of Bitcoin and Litcoin building a exclusive updated blockchain full of features and novelties based on cabalistic numerology.

 - 2 minute block targets
 - subsidy halves in 333k blocks (~3 years)
 - ~33 million total coins
 - 33 coins per block
 - 1033 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the Sperry client sofware, see http://www.sperrytecnologia.com.br

License
-------

Sperry is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the Sperry
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/sperry-project/sperry/tags) are created
regularly to indicate new official, stable release versions of Sperry.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing
---------------------

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them: 

    qmake BITCOIN_QT_TEST=1 -o Makefile.test bitcoin-qt.pro
    make -f Makefile.test
    ./sperry-qt_test
    
### How to install?
-------------------

Follow the correct recipe order for installation of dependencies and compilation on Ubuntu 16.04. 
    
    apt-get install git -y 
    apt-get install build-essential libtool autotools-dev automake pkg-config libssl-dev libevent-dev bsdmainutils -y
    apt-get install libboost-system-dev libboost-chrono-dev libboost-program-options-dev libboost-test-dev libboost-thread-dev -y
    apt-get install libboost-filesystem-dev libboost-all-dev -y
    apt-get install software-properties-common -y
    add-apt-repository ppa:bitcoin/bitcoin
    apt-get update
    apt-get install libdb4.8-dev libdb4.8++-dev -y
    apt-get install libminiupnpc-dev -y
    apt-get install libzmq3-dev -y
    apt-get install libqt5gui5 libqt5core5a libqt5dbus5 qttools5-dev qttools5-dev-tools libprotobuf-dev protobuf-compiler -y
    apt-get install libqt4-dev libprotobuf-dev protobuf-compiler -y
        
Clone Sperry Coin source code from github
    
    git clone https://github.com/iluysperry/Sperry-Coin.git && mv Sperry-Coin/ sperry
    
Compile source code and wallet  
    
    cd /root/sperry/src && make -f makefile.unix      -----> Core
    cd /root/sperry/ && qmake && make                 -----> Grafical Wallet

### How to use?
-------------------
## GUI WALLET
Run this commands in path directory of installation /sperry/ 
    
    ./sperry-qt  -------> Grafical wallet
    
### CORE FULL NODE
Run this commands in path directory of installation /sperry/src
    
    ./sperryd -daemon            -------> Start server  
    ./sperryd getinfo            -------> General info
    ./sperryd setgenerate true   -------> Start solo mining 
    ./sperryd gethashespersec    -------> Current mining hashrate 
    ./sperryd getbalance         -------> Balance
    
List all commands 
    
    ./sperryd help 
    
### Block explorer
-------------------  
http://explorer.sperrytecnologia.com.br
    
