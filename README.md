Requirements:
-------------------------
Generic:
* Strayacoind > 1.0
* Python >=2.6
* Twisted >=10.0.0
* ltc_scrypt >= 1.0

Linux:
* sudo pip install twisted ltc_scrypt
* sudo pip install python-argparse # if on Python 2.6

Windows:
Use precompiled binaries in [releases](https://github.com/MxBlu/zen2pool/releases) or:

* Install [Python 2.7](http://www.python.org/getit/)
* Install [Twisted](http://twistedmatrix.com/trac/wiki/Downloads)
* Install [Zope.Interface](http://pypi.python.org/pypi/zope.interface/3.8.0)
* Install [python win32 api](http://sourceforge.net/projects/pywin32/files/pywin32/Build%20218/)
* Install [python win32 api wmi wrapper](https://pypi.python.org/pypi/WMI/#downloads)
* Unzip the files into C:\Python27\Lib\site-packages

Running P2Pool:
-------------------------
To use P2Pool, you must be running your own local strayacoind instance with 
the RPC port open to localhost/127.0.0.1. Ensure that the configuratation file (strayacoin.conf) 
is located in its default location (~/.strayacoin/strayacoin.conf OR %appdata%/strayacoin/strayacoin.conf).

For standard configurations, using P2Pool should be as simple as:

    python run_p2pool.py --net strayacoin
	
or on Windows:
	
	run_p2pool.exe --net strayacoin

Then run your miner program, connecting to 127.0.0.1 on port 9444 with any
username and password.

If you are behind a NAT, you should enable TCP port forwarding on your
router. Forward port 8444 to the host running P2Pool.

Fees can be added with the -f switch, for example:

	run_p2pool.exe --net strayacoin -f 2
	
will run p2pool with a fee of 2%.

Run for additional options.

    python run_p2pool.py --help
	
Changing bootstrap nodes and bootstrapping:
-------------------------
If you want to change the bootstrap nodes you connect to and/or want to 
bootstrap the network (not recommended for a network that is already running), 
this can be done in p2pool/networks/strayacoin.py. 

Changing PERSIST to False will cause you to build your own sharechain if it is 
unavailable, please do not do this if the network is running as it will fork the network.

Donations towards further development:
-------------------------
    SiysxnAXZS3cWdJwdwyUENQXW2KRSJGbVY

Official wiki:
-------------------------
https://en.bitcoin.it/wiki/P2Pool

Alternate web frontend:
-------------------------
* https://github.com/justino/p2pool-ui-punchy

Sponsors:
-------------------------

Thanks to:
* The Bitcoin Foundation for its generous support of P2Pool
* The Litecoin Project for its generous donations to P2Pool
 
License:
-------------------------

[Available here](COPYING)


