# Dhrystone

<!-- vim-markdown-toc GFM -->

* [參數](#參數)
    - [系統](#系統)
    - [目標](#目標)
* [環境](#環境)
    - [cross compiler](#cross-compiler)
* [Dhrystone](#dhrystone)
    - [下載](#下載)
    - [構建](#構建)
    - [執行](#執行)

<!-- vim-markdown-toc -->

---

## 參數

### 系統

-   Ubuntu 18.04（WSL）

### 目標

-   arm64

## 環境

### cross compiler

```zsh
sudo apt install -y gcc-aarch64-linux-gnu
```

## Dhrystone

### 下載

```zsh
git clone --no-tags --depth 1 https://github.com/Keith-S-Thompson/dhrystone.git
cd dhrystone/v2.2

aarch64-linux-gnu-gcc -c dry.c -o dry.o
aarch64-linux-gnu-gcc -DPASS2 dry.c dry.o -o dry -static

adb push dhrystone/v2.2/dry /data/local/tmp/Dhrystone/dry
```

### 構建

```zsh
cd dhrystone/v2.2

aarch64-linux-gnu-gcc -c dry.c -o dry.o
aarch64-linux-gnu-gcc -DPASS2 dry.c dry.o -o dry -static
```

### 執行

```
./dry
```
