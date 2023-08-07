Hybrid Sysmmetric Scheme
=====

***

Implementation based on HElib v2.2.1

# Build and Run
Our implementation relies on [HElib v2.2.1](https://github.com/homenc/HElib/tree/v2.2.1), which is a famous homomomorphic encryption scheme library and `v2.2.1` is now (July, 2022) the newest release version. Therefore, you firstly need to install HElib. The HElib iteratively relies on [NTL](https://libntl.org/), [GMP](https://gmplib.org) and M4 libraries. We suggest that install them to your default user's program path `/usr/local`, and the suggeted version of them are showed in following table. What's more, using `./configure SHARED=on` to get a shared library when compile NTL is also suggested.

| Libraries | Version | Website |
| ---- | ---- | ---- |
| M4  | v1.4.18 | http://mirrors.kernel.org/gnu/m4 |
| GMP | v6.2.1  | https://gmplib.org |
| NTL | v11.4.3 | https://libntl.org
| HElib | v2.2.1 | https://github.com/homenc/HElib

We suggest that follow the command below to install HElib. You can also refer to the website https://github.com/homenc/HElib.

```
git clone https://github.com/homenc/HElib.git -b v2.2.1 --single-branch 
cd HElib
mkdir build
cd build
cmake ..
make
sudo make install
```

After install [HElib](https://github.com/homenc/HElib), you can run our tests by

```
mkdir build
cd build
cmake ..
make
./test/test-trans-Yu2x-8-C16

```
Symmetic test:
g++ test-Yu2x-8.cpp -Iinclude ../Yux/Yu2x-8.cpp -o test-Yu2x-8 