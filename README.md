This is the reference code for [Worktips](https://worktips.info) cryptocurrency.

* Official homepage: [Worktips](http://worktips.info)
* Official repository: [Worktips GitHub](https://github.com/Vordas/worktips)
* Official Announcement thread: [Worktips BitcoinTalk](https://bitcointalk.org/index.php?topic=3086019.0)
* Official Discord: [Worktips Discord](https://discord.gg/UmZExyz)
* Official Facebook: [Worktips Facebook](https://www.facebook.com/worktipscoin)
* Official Twitter: [Worktips Twitter](https://twitter.com/wtipscoin)
* Official Telegram: [Worktips Telegram](https://t.me/joinchat/HOvygRE-6UnWOzoh72NVMA)
* Official Whitepaper: [Worktips Whitepaper](http://worktips.info/whitepaper_worktips.zip)
* Official Block explorer: [Worktips Block explorer](http://blockexplorer.worktips.info)

## Worktips Lite (GUI Wallet)

## How to compile

### Compile on Linux Ubuntu 16.04

- Dependencies

```
$ sudo apt-get update
$ sudo apt-get install -y build-essential python-dev gcc-4.9 g++-4.9 git cmake libboost-all-dev librocksdb-dev tmux qt5-default qttools5-dev-tools software-properties-common tk8.5 tcl8.5 zip unzip
```

- Clone the repository

```
$ git clone https://github.com/Vordas/worktips-lite.git worktipslite
```

- Unpack the rocksdb library

```
$ cd worktipslite/lib
$ unzip rocksdblib.zip
```
  
- Update core submodule

```
$ cd
$ cd worktipslite
$ git submodule update --init
$ git submodule foreach git pull origin master
```

- CHMOD

```
$ cd
$ cd worktipslite/cryptonote/external/rocksdb/build_tools
$ cd chmod +x build_detect_platform
$ chmod +x version.sh
```

- Build

```
$ cd
$ cd worktipslite
$ mkdir build
$ cd build
$ cmake -DSTATIC=ON -DCMAKE_BUILD_TYPE=RELEASE ..
$ make
```

_Your executables will be located in `build/src` folder._


### Compile on Windows

_Coming soon..._