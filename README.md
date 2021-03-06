RubleBit integration/staging tree
================================

http://www.rublebit.info

Copyright (c) 2009-2014 Bitcoin Developers

Copyright (c) 2011-2014 Litecoin Developers

Copyright (c) 2011-2016 RubleBit Developers

What is RubleBit?
----------------

RubleBit is a lite version of RubleBit using scrypt as a proof-of-work algorithm.
 - 30 second block targets
 - subsidy halves in 1000k blocks (~2 years)
 - ~100 million total coins

The rest is the same as RubleBit.
 - 40 coins per block
 - 5 blocks to retarget difficulty

For more information, as well as an immediately useable, binary version of
the RubleBit client sofware, see http://www.rublebit.info.

License
-------

RubleBit is released under the terms of the MIT license. See `COPYING` for more
information or see http://opensource.org/licenses/MIT.

Development process
-------------------

Developers work in their own trees, then submit pull requests when they think
their feature or bug fix is ready.

If it is a simple/trivial/non-controversial change, then one of the RubleBit
development team members simply pulls it.

If it is a *more complicated or potentially controversial* change, then the patch
submitter will be asked to start a discussion with the devs and community.

The patch will be accepted if there is broad consensus that it is a good thing.
Developers should expect to rework and resubmit patches if the code doesn't
match the project's coding conventions (see `doc/coding.txt`) or are
controversial.

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/rublebit-project/rublebit/tags) are created
regularly to indicate new official, stable release versions of RubleBit.

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test. Please be patient and help out, and
remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write unit tests for new code, and to
submit new unit tests for old code.

Unit tests for the core code are in `src/test/`. To compile and run them:

    cd src; make -f makefile.unix test

Unit tests for the GUI code are in `src/qt/test/`. To compile and run them:

    qmake RUBLEBIT_QT_TEST=1 -o Makefile.test rublebit-qt.pro
    make -f Makefile.test
    ./rublebit-qt_test

    apt-get install build-essential libssl-dev libdb-dev libdb++-dev libboost-all-dev git libssl1.0.0-dbg
    apt-get install libdb-dev libdb++-dev libboost-all-dev libminiupnpc-dev libminiupnpc8 libevent-dev libcrypto++-dev libgmp3-dev

