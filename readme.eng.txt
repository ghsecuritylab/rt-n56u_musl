* BUILD INSTRUCTION *

1) You need Linux environment to build the firmware. Ubuntu 16.04.4 LTS
   has been tested and recommended.
2) Build cross-toolchain for MIPS32_R2 CPU (binutils-2.25.1, gcc-540, musl-1.1.16)
   from external package toolchain-mipsel.
3) Configure firmware content via .config file. Use comment mark # for
   disable features. Change "CONFIG_TOOLCHAIN_DIR=" param to target cross-toolchain
   directory.
4) LPR printer daemon is not support right now. 
   Please disable CONFIG_FIRMWARE_INCLUDE_LPRD feature.
5) Default source code path is /opt/rt-n56u_musl. If you change this, 
   some libraries or apps need to run cmake or autogen again.
6) Build firmware via "build_firmware" script. After the build is finished,
   the firmware file (*.trx) will be placed to directory "images".



* NOTE *

You need following packages to build the firmware under Debian 8.x 'Jessie':
- autoconf
- automake
- bison
- build-essential
- cmake
- flex
- gawk
- gettext
- gperf
- libtool
- pkg-config
- python-docutils
- sudo
- zlib1g-dev

You need additional packages to build cross-toolchain:
- libgmp3-dev
- libmpc-dev
- libmpfr-dev
- texinfo




-
08/26/2016 Padavan
04/16/2018 ZXP