## Tool , Technologies and Version
    Python 3.6.8
    Django 2.2.8
    psycopg2-binary 2.8.3
    djangorestframework 3.9.4
    djangorestframework-jwt 1.11.0

## Installation
    Inside your root directory create VIRTUAL ENVIRONMENT :

    virtualenv env --python=python3 (If your Current version of Python is Python2)

    virtual env (If your Current default version of Python is Python3)

    After creating Virtual Environment you need to Activate that environment so that all the installed package will only available for this Specific Project not for the rest if any.

    source env/bin/activate

    After activating an environment we need to install all the required packages.

    pip install -r requirements.txt

## To dump data from postgres sql
    sudo pg_dump -h <HOSTNAME> -U <USERNAME> -f <FILENAME> <DB_Name from where you want to dump>
    sudo pg_dump -h 13.250.224.209 -U postgres -f ineed.sql INEEDWEBDEVELOPER

## To Load The Data into postgres sql
    sudo psql -h <HOSTNAME> -U <USERNAME> -d <DB_NAME where you want to load> -f <FILENAME>
    sudo psql -h 111.91.225.12 -U postgres -d INEEDWEBDEVELOPER -f ineed.sql

    
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


## How TO Run Celery
    At first we need to run redis using redis-server command than we need to run this command 
    celery -A cryptocurrency beat -l debug 
    and 
    celery -A cryptocurrency worker -l debug

## How to Setup scheduler
    Goto Admin pannel and Add  Intervals like in Every "1" and in Period "Minutes"
    and then Goto 
    Periodic tasks and add 
        Name = Task name
        Task = <appname.filename.function_name>
        Task = crypto_merchant.tasks.update_ethereum_tokens
        Interval = select interval
