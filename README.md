## Install Solidity Compiler in MAC
    https://github.com/crytic/solc-select
    brew update
    brew upgrade
    brew tap ethereum/ethereum
    brew install solidity
    docker pull trailofbits/solc-select
    docker run --read-only -i --rm --entrypoint='/bin/sh' trailofbits/solc-select:latest -c 'cat /usr/bin/install.sh' | bash -e


## Install Solidity Compiler in UBUNTU
    sudo add-apt-repository ppa:ethereum/ethereum
    sudo apt-get update
    sudo apt-get install solc
    git clone https://github.com/crytic/solc-select.git
    ./solc-select/scripts/install.sh
    export PATH=/home/<USERNAME>/.solc-select:$PATH
    $ solc --version
    solc, the solidity compiler commandline interface
    Version: 0.5.2+commit.1df8f40c.Linux.g++
    $ solc use 0.4.24
    solc, the solidity compiler commandline interface
    Version: 0.4.24+commit.e67f0147.Linux.g++

    In special scenarios the current version can also be overwritten with the SOLC_VERSION environment variable.
    $ solc --version
    solc, the solidity compiler commandline interface
    Version: 0.4.24+commit.e67f0147.Linux.g++
    $ SOLC_VERSION=0.5.2 solc --version
    solc, the solidity compiler commandline interface
    Version: 0.5.2+commit.1df8f40c.Linux.g++

   

    You can list all available versions with the special --versions argument:
    $ solc --versions
    0.4.11
    0.4.12
    0.4.13
    0.4.14
    0.4.15
    0.4.16
    0.4.17
    0.4.18
    0.4.19
    0.4.20
    0.4.21
    0.4.22
    0.4.23
    0.4.24
    0.4.25
    0.5.0
    0.5.1
    0.5.2
    0.5.3
    0.5.4
    0.5.5
    nightly


## Install Tumx Server In Linux:
    sudo apt-get install tmux

## Creating Tmux sessions
    tmux new -s <session_name>

## Kill Tmux sessions
    tmux kill-session -t <session_name>

