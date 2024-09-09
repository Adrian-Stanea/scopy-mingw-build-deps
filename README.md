# scopy-mingw-build-deps

Script that build staging environment with dependencies to build scopy. MSYS2 - https://www.msys2.org/ is required for development. To initialize the development environment, from the mingw64 shell

git clone https://github.com/analogdevicesinc/scopy-mingw-build-deps
cd scopy-mingw-build-deps
./init_staging x86_64
source ./build.sh
install_tools
install_deps
build_deps


## Build the Docker image
To build docker image execute the command from the ```scopy-mingw-build-deps/docker``` directory:
### x86_64:
```bash
docker build --progress=plain --tag scopy-build:mingw64 --build-arg BUILD_TARGET=x86_64 --isolation=hyperv --memory=16GB .
```
### i686:
```bash
docker build --progress=plain --tag scopy-build:mingw32 --build-arg BUILD_TARGET=i686 --isolation=hyperv --memory=16GB .
```
