This is the reference code for [Worktips](https://worktips.info) cryptocurrency.

* Official homepage: [Worktips](http://worktips.info)
* Official repository: [Worktips GitHub](https://github.com/worktips/worktips)
* Official Announcement thread: [Worktips BitcoinTalk](https://bitcointalk.org/index.php?topic=3086019.0)
* Official Discord: [Worktips Discord](https://discord.gg/UmZExyz)
* Official Facebook: [Worktips Facebook](https://www.facebook.com/worktipscoin)
* Official Twitter: [Worktips Twitter](https://twitter.com/wtipscoin)
* Official Telegram: [Worktips Telegram](https://t.me/joinchat/HOvygRE-6UnWOzoh72NVMA)
* Official Whitepaper: [Worktips Whitepaper](http://worktips.info/whitepaper_worktips.zip)
* Official Block explorer: [Worktips Block explorer](http://blockexplorer.worktips.info)


## Worktips Cryptocurrency

Worktips [WTIP] is an ASIC resistant CryptoNightLite V1 algorithm based cryptocurrency. Fast transactions & privacy make this coin perfect for rewarding your workers, co-workers and colleagues for a job well done.

- Algorithm: CryptoNightLite V1
- Max. supply: 184,467,440,735.0
- CryptoNote name: worktips
- Decimal points: 8
- Block time: 120
- Ticker: WTIP
- Emission speed factor: 18
- P2P port: 17239
- RPC port: 18238

## How to compile

### Compile on Linux Ubuntu 16

**1. Install dependencies**

- run an update

``
sudo apt-get update
``

- get all dependencies

``
sudo apt-get install -y build-essential python-dev gcc g++ git cmake librocksdb-dev libboost-all-dev
``

**2. Get the coin**

``
git clone https://github.com/worktips/worktips.git worktips
``

**3. CHMOD**

- navigate to:

``
cd worktips/external/rocksdb/build_tools
``

- execute the following commands:

``
chmod +x build_detect_platform
``

``
chmod +x version.sh
``

**4. Build executables**

- Navigate back to repo folder 

``
cd
``

``
cd worktips
``

- prepare the build

``
mkdir build && cd $_
``

``
cmake ..
``

- Export flags

``
export CXXFLAGS="-std=gnu++11"
``

- Make/Build

``
make
``

_Your executables will be located in `build/src` folder._


### Compile on Linux Ubuntu 14

**1. Install dependencies**

- run an update

``
sudo apt-get update
``

- get all dependencies

``
sudo apt-get install -y build-essential python-dev git cmake libboost1.55-all-dev libgflags-dev libsnappy-dev zlib1g-dev libbz2-dev libgflags-dev libgflags2 gcc-4.8 g++-4.8
``

**2. Install RocksDB database (long compilation)**

``
git clone https://github.com/facebook/rocksdb.git
``

``
cd rocksdb
``

``
make all
``

**3. Get the coin**

``
cd
``

``
git clone https://github.com/worktips/worktips.git worktips
``

**4. CHMOD**

- navigate to:

``
cd worktips/external/rocksdb/build_tools
``

- execute the following commands:

``
chmod +x build_detect_platform
``

``
chmod +x version.sh
``

**5. Build executables (long compilation)**

- Navigate back to repo folder 

``
cd
``

``
cd worktips
``

- prepare the build

``
mkdir build && cd $_
``

``
cmake ..
``

- Export flags

``
export CXXFLAGS="-std=gnu++11"
``

- Make/Build

``
make
``

### Compile on Windows 7/8/10

**1. Environment**

- Visual Studio 2017 Community Edition with desktop development with C++ and the VC++ v140 toolchain features selected
- Boost 1.59.0, with the installer for MSVC 14

**2. Build**

- From the start menu, open 'x64 Native Tools Command Prompt for vs2017'


``
cd <worktips_directory>
``

``
mkdir build
``

``
cd build
``


-  Set the PATH for Cmake:

``
set PATH="C:\Program Files (x86)\Microsoft Visual Studio\2017\Community\Common7\IDE\CommonExtensions\Microsoft\CMake\CMake\bin";%PATH%
``

- Run Cmake:

``
cmake -G "Visual Studio 14 Win64" .. -DBOOST_ROOT=C:/local/boost_1_59_0
``

- Build:

``
MSBuild Worktips.sln /p:Configuration=Release /m
``

_Your binaries  will be located in `..\build\src\Release` folder._


### Compile on macOS High Sierra

**1. Dependencies**

- Download and install Xcode from App Store
- Open Xcode and download additional contents
- Download CMAKE for OSX: https://cmake.org/files/v3.10/cmake-3.10.3-Darwin-x86_64.dmg
- Copy the CMAKE app to Application folder
- Open CMAKE GUI first time, and close it afterwards
- Run this command in terminal for CMD tools:

- on newer devices

``
sudo "/Applications/CMake.app/Contents/bin/cmake-gui" --install
``

- older than 4 years

``
sudo "/Applications/CMake.app/Contents/bin/cmake-gui" --install=/path/to/bin
``

- install Homebrew if you haven’t already

``
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
``

- install xCode CMD tools and install Xcode from app store:

``
xcode-select --install
``

- accept Xcode license

``
sudo xcode-select -s /Applications/Xcode.app/Contents/Developer
``

``
sudo xcodebuild -license accept
``

- install rocksdb

``
brew install rocksdb
``

- install boost

``
brew install boost
``

**2. Build**

``
cd
``

- get the source code

``
git clone https://github.com/worktips/worktips.git worktips
``

- CHMOD

``
cd worktips/external/rocksdb/build_tools
``

``
sudo chmod +x build_detectplatform
``

``
sudo chmod +x version.sh
``

- navigate back to source folder and run

``
mkdir build && cd $
``

``
sudo cmake -DBOOST_ROOT=/usr/local/include/boost ..
``

``
sudo make
``

_Your binaries  will be located in `..\build\src\Release` folder._

### Credits
Cryptonote Developers, Bytecoin Developers, Monero Developers, Forknote Project, TurtleCoin Developers