Fix termux: ```pkg remove game-repo```

Fix termux number 2: ```pkg remove science-repo```

Update: ```pkg update```

Update termux: ```apt-get update && apt-get upgrade -y```

Install wget: ```apt-get install wget -y```

Install proot: ```apt-get install proot -y```

Install git: ```apt-get install git -y```

Go to HOME folder: ```cd ~```

Install Ubuntu on Proot: ```proot-distro install ubuntu```

Login to Ubuntu: ```proot-distro login ubuntu```

Update & Install Dependencies: ```apt update && apt install curl libnuma-dev git llvm-dev clang make zlib1g-dev```

Install ghcup: ```mkdir -p ~/.ghcup/bin && curl https://downloads.haskell.org/~ghcup/aarch64-linux-ghcup -o ~/.ghcup/bin/ghcup && chmod +x ~/.ghcup/bin/ghcup```

Add it to PATH: ```echo "export PATH=\"\$HOME/.cabal/bin:\$HOME/.ghcup/bin:\$PATH\"" >> ~/.bashrc && source ~/.bashrc```

Set GHC and Install Cabal: ```ghcup install ghc && ghcup set ghc && ghcup install cabal && ghcup set cabal```

Clone SimpleX & cd into it: ```git clone https://github.com/simplex-chat/simplex-chat && cd simplex-chat```

Update Cabal then Build: ```cabal update && cabal build```


Directory to simplex-chat will print in final linking stage. In my case it was: `/root/simplex-chat/dist-newstyle/build/aarch64-linux/ghc-8.10.7/simplex-chat-0.5.2/x/simplex-chat/build/simplex-chat/simplex-chat`

Grab the binary for simplex-chat located in the directory above place it somewhere, make it executable with ```chmod +x simplex-chat``` and add the location you placed the binary in to your PATH.

Finally enter ```simplex-chat``` to launch SimpleX.


