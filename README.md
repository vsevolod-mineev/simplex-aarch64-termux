We got Haskell to compile on aarch64 architecture. This was done from an Android phone with Termux running a virtual Ubuntu shell courtesy of PRoot alongside our larger effort to port SimpleX for [iOS and Android.](https://www.reddit.com/r/haskell/comments/r82ji7/christmas_of_code_haskell_for_mobile_a_3000_grant/) This recipe assumes a fresh Termux installation.

If you'd like to skip the compilation process and just [grab the binary](https://github.com/vsevolod-mineev/simplex-aarch64-termux/releases) it is available in releases.

[SimpleX](https://github.com/simplex-chat/simplex-chat) is a thin terminal UI message broker that uses [SMP protocols](https://github.com/simplex-chat/simplexmq/blob/master/protocol). The motivation for SimpleX chat is [presented here](./simplex.md).

Fix termux: ```pkg remove game-repo```

Fix termux number 2: ```pkg remove science-repo```

Update: ```pkg update```

Update termux: ```apt-get update && apt-get upgrade -y```

Install Dependencies: ```apt-get install wget proot proot-distro git -y```

Go to HOME folder: ```cd ~```

Install Ubuntu on PRoot: ```proot-distro install ubuntu```

Login to Ubuntu: ```proot-distro login ubuntu```

Update & Install Dependencies: ```apt update && apt install curl libnuma-dev git llvm-dev clang make zlib1g-dev```

Install ghcup: ```mkdir -p ~/.ghcup/bin && curl https://downloads.haskell.org/~ghcup/aarch64-linux-ghcup -o ~/.ghcup/bin/ghcup && chmod +x ~/.ghcup/bin/ghcup```

Add it to PATH: ```echo "export PATH=\"\$HOME/.cabal/bin:\$HOME/.ghcup/bin:\$PATH\"" >> ~/.bashrc && source ~/.bashrc```

Set GHC and Install Cabal: ```ghcup install ghc && ghcup set ghc && ghcup install cabal && ghcup set cabal```

Clone SimpleX & cd into it: ```git clone https://github.com/simplex-chat/simplex-chat && cd simplex-chat```

To avoid Android killing the compiler enable power mode, put phone on charge, and remove Termux from tracking by "Memory" within "Device care" of "Settings".

Update Cabal then Build: ```cabal update && cabal build```

Directory to simplex-chat will print in final linking stage. In my case it was: `/root/simplex-chat/dist-newstyle/build/aarch64-linux/ghc-8.10.7/simplex-chat-0.5.2/x/simplex-chat/build/simplex-chat/simplex-chat`

Grab the binary for simplex-chat located in the directory above -> place it somewhere -> make it executable with ```chmod +x simplex-chat``` -> add the location you placed the binary in to your PATH.

Finally enter ```simplex-chat``` to launch SimpleX.


