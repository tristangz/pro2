# Bitcoin Miner
### What is a Bitcoin?
A Bitcoin is a virtual currency that was established in 2009. You can earn Bitcoin by buying, exchanging or mining them. Every Bitcoin transaction is publicly viewable, and each transaction is stored in something called the blockchain. 
### Requirements
To mine Bitcoin I needed the following:
##### A Raspberry Pi
##### A Bitcoin wallet
##### A pool account
##### A USB Bitcoin miner
### Getting Started
I bought a Raspberry Pi 3 Model B Plus and downloaded the NOOBS operating system to it. I then downloaded a Bitcoin wallet to my computer called Bitcore. The wallet is what will give me unique addresses to receive Bitcoin. To use this wallet, I had to sync it to the blockchain. Since this blockchain has been building since 2009 it was over 200 Gigabytes of text file. Due to a bad internet connection, it took me over a week to sync my wallet. Once my wallet was synced, I backed it up in a file named “wallet.dat.” 
#### https://imgur.com/a/mfhMuHS
Since mining Bitcoin has become to complex to mine alone, mining is done is groups called pools. Mining Bitcoin as a pool gives everyone a chance to earn a little. I used a pool called Slush’s Pool. 
#### https://imgur.com/a/b0JYysf
After I created an account, I had to set it up so the payout went to my wallet. To do this I had to go to my wallet and create a receiving address. After I created the address and gave it a name, it gave me the unique code that I used for my pool.
#### https://imgur.com/a/1fvCgAn
#### https://imgur.com/a/iwf4SGF
### Finishing Touches
Once I had finished all of that I was almost ready to begin mining, or so I thought. Right before I started downloading the required files onto my Raspberry Pi, I realized that I had forgotten to buy the USB Bitcoin miner. This piece is essential because it is what does the actual mining. I bought one for about $65 dollars online. After it had arrived I was able to start setting my Raspberry Pi up for mining. 
I used software called BFG Miner for my Raspberry Pi. For BFG Miner to run I needed to download some other software to make BFG Miner compile properly. After making sure my Raspberry Pi was updated, with the USB miner in I typed:
##### “Sudo apt-get install autoconf autogen libtool uthash-dev libjansson-dev libcurl4-openssl-dev libusb-dev libcurses-dev git-core -y” 
into the terminal. Once that installed, the next command I typed into the terminal was:
##### “git clone https://github.com/luke-jr/bfgminer.git”
After that I typed in:
##### “cd bfgminer”
followed by:
##### “./autogen.sh”
and then:
##### “./ configure”
and finally:
##### “make.”
I was met with the following screen.
#### https://imgur.com/a/iaEoOpM
On this screen I connected this miner to my pool by typing:
##### “./bfgminer -o stratum.bitcoin.cz:3333 -O username.worker:password -S all”
into the pool section. However, instead of:
##### “username.worker:password”
I used my pool accounts information. First of all, I used my username:
##### “tjg2601”
and then I put my workers name:
##### “worker1”
you can change the workers name but I decided to just use the set name. Lastly it doesn’t matter what you put the password as because if anyone ever used tried to use this worker they would just be making you money, so I put the password as anything. So I used:
##### “tjg2601.worker1:anything”
After this my miner was ready to go! I mined only for a few minutes to make sure it was working and was able to monitor it on the slush pool website. 
