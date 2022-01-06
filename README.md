![FlokoROM v5](https://raw.githubusercontent.com/FlokoROM/www/master/img/flokowall_v5_512px.png)

## How to build

### Basic

Read:

* [AOSP Guide](https://source.android.com/setup/build/requirements)
* [LineageOS wiki](https://wiki.lineageos.org/devices/kebab/build)

### Download the sources

Initialize repo:

```sh
repo init -u https://github.com/FlokoROM/manifesto.git -b 12.0
```

Sync(Download):

```sh
repo sync -j$(nproc) -c --no-clone-bundle --no-tags
```

### Build

```sh
export ALLOW_MISSING_DEPENDENCIES=true
```

```sh
. build/envsetup.sh
```

```sh
brunch <device> 2>&1 | tee ~/log/floko_$(date '+%Y%m%d_%H-%M-%S').log
```

## Contribute

To submit new features/patches, please send us a Pull Request on our GitHub. We will review and merge.
