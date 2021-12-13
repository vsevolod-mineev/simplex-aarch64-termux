Fix termux: ```pkg remove game-repo```

Fix termux_2: ```pkg remove science-repo```

Update: ```pkg update```

Update termux: ```apt-get update && apt-get upgrade -y```

Install wget: ```apt-get install wget -y```

Install proot: ```apt-get install proot -y```

Install git: ```apt-get install git -y```

Go to HOME folder: ```cd ~```

Download script: ```git clone https://github.com/MFDGaming/ubuntu-in-termux.git```

Go to script folder: ```cd ubuntu-in-termux```

Give execution permission: ```chmod +x ubuntu.sh```

Run the script: ```./ubuntu.sh -y```

Now just start ubuntu: ```./startubuntu.sh```

Update: ```apt update```

Install clang: ```apt install clang```

Install gcc: ```apt install gcc```

Install ghc: ```apt install ghc```

Install cabal: ```apt install cabal-install```

Install stack: ```apt install haskell-stack```

Install libtinfo5: ```apt install libtinfo5```


!You'll notice that ```/root/.stack/config.yaml``` is empty. You'll need to add something there for example: ```skip-ghc-check: false```

Clone simplex: ```git clone https://github.com/simplex-chat/simplex-chat```

Go to simplex: ```cd simplex-chat```

Install stack: ```stack install```