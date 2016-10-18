[![Build Status](https://travis-ci.org/JoinMarket-Org/joinmarket.svg?branch=develop)](https://travis-ci.org/JoinMarket-Org/joinmarket.svg?branch=develop)
2
​
3
[![Coverage Status](https://coveralls.io/repos/github/JoinMarket-Org/joinmarket/badge.svg?branch=develop)](https://coveralls.io/github/JoinMarket-Org/joinmarket?branch=develop)
4
​
5
##What is JoinMarket ?
6
​
7
The idea behind JoinMarket is to help create a special kind of bitcoin transaction called a CoinJoin transaction. It's aim is to improve the confidentiality and privacy of bitcoin transactions, as well as improve the capacity of the blockchain therefore reduce costs. The concept has enormous potential, but had not seen much usage despite the multiple projects that implement it. This is probably because the incentive structure was not right.
8
​
9
A CoinJoin transaction requires other people to take part. The right resources (coins) have to be in the right place, at the right time, in the right quantity. This isn't a software or tech problem, its an economic problem. JoinMarket works by creating a new kind of market that would allocate these resources in the best way.
10
​
11
One group of participants (called market makers) will always be available to take part in CoinJoins at any time. Other participants (called market takers) can create a CoinJoin at any time. The takers pay a fee which incentivizes the makers. A form of smart contract is created, meaning the private keys will never be broadcasted outside of your computer, resulting in virtually zero risk of loss (aside from malware or bugs). As a result of free-market forces the fees will eventually be next to nothing. 
12
​
13
Widespread use of JoinMarket could improve bitcoin's fungibility as a commodity. The privacy aspect has many applications. For example, some users of bitcoin exchanges have a problem of being front-run. As all bitcoin transactions are public, when a seller sends a large amount of coins to an exchange it will be public knowledge and the price will move downwards accordingly.
14
​
15
##Installation
16
​
17
#####A NOTE ON UPDATING FROM PRE-0.2 VERSIONS
18
The installation is slightly changed, with the secp256k1 python binding no longer being optional, and libnacl now being installed via pip, not locally. The short version is: do follow the below process, for example the secp256k1 binding must be the latest version else you'll get errors. Of course if you already have libsodium you don't need to re-install it. Be sure to read the [release notes](https://github.com/JoinMarket-Org/joinmarket/blob/develop/doc/release-notes-0.2.1.md).
19
​
20
#####REQUIRED INSTALLATION DEPENDENCIES (for Linux)
21
​
22
+ You will need python 2.7
23
​
24
+ You will need libsodium installed
25
​
26
 - Debian/Ubuntu, apt-get install libsodium-dev
27
 - Arch, pacman -S libsodium
28
 - or build:
29
​
30
    ```
31
    git clone git://github.com/jedisct1/libsodium.git
32
    cd libsodium
33
    git checkout tags/1.0.3
34
    ./autogen.sh
