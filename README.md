
# SincNet
This is a still under development adaptation of the [SincNet](https://github.com/mravanelli/SincNet).

## Prerequisites
- Python 3.6
- Pytorch
- Soundfile

## How to run
Update the permissions for .sh files in SincNet folder.
```bash
chmod +x *.sh
```

Update TIMIT_PATH on prepare.sh and run it.
```bash
./prepare
```

Check if cfg/SincNet_TIMIT.cfg is using the desired configs, then run train.sh.
```bash
./train
```
