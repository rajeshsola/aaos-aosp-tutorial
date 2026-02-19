# Prep the host
```
sudo apt-get install git-core gnupg flex bison build-essential zip curl zlib1g-dev libc6-dev-i386 x11proto-core-dev libx11-dev lib32z1-dev libgl1-mesa-dev libxml2-utils xsltproc unzip fontconfig

sudp apt install repo
```

> https://source.android.com/docs/setup/start/requirements

# Build Steps

Download source , Ref:- https://source.android.com/docs/setup/download

```
mkdir android-16.0.0_r4 && cd android-16.0.0_r4
repo init -u https://android.googlesource.com/platform/manifest -b android-16.0.0_r4 --max-depth=1
cat .repo/manifests/default.xml | grep revision
```

Build the source , Ref:- https://source.android.com/docs/setup/download
```
source build/envsetup.sh
lunch <target>
make -j8
```

# Kernel build
```
mkdir android16-6.12-kernel && cd android16-6.12-kernel
repo init -u https://android.googlesource.com/kernel/manifest -b common-android16-6.12
repo sync -c
```

# RUST
```
sudo apt install rustc rust-clippy rust-doc  rustfmt rust-gdb rust-lldb cargo rustc-1.88 cargo-1.88 rustup
```
