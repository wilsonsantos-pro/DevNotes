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

## Benchmark any command

[hyperfine](https://github.com/sharkdp/hyperfine)

### Install

```sh
wget https://github.com/sharkdp/hyperfine/releases/download/v1.15.0/hyperfine_1.15.0_amd64.deb
sudo dpkg -i hyperfine_1.15.0_amd64.deb
```

### Example

```sh
hyperfine --runs 5 --warmup 3 'sleep 0.3'
```
