# Benchmarking

```sh
sudo apt install sysbench
```

## CPU

```sh
sysbench --threads=16 --test=cpu run
```

## RAM

```sh
sysbench --threads=16 --test=memory run
```

## IO

```sh
dd if=/dev/zero of=testfile bs=1G count=5 oflag=dsync

rm testfile
```
