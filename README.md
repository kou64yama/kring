# kring

`kring` is a password manager written in Bash.

## Installation

```bash
curl -fsL -o kring https://github.com/kou64yama/kring/raw/main/kring
chmod +x kring
mv kring path/to/bin
```

## Usage

First, create a key to encrypt the password managed by `kring`.

```bash
kring init
```

`kring set` sets the password and `kring get` retrieves the
password. See `kring -h` for more detailed usage.

## FAQ

### How do I keep my encryptin key safe?

The path to the encryption key can be specified in the environment
variable `KRING_KEYFILE`. By settin this path to a different drive
than the password, e.g., a USB flash drive, the password can no longer
be used without the USB flash drive.

Alternatively, you can set `KRING_HOME` and `KRING_KEYFILE` to store
the password on a cloud drive and the encryption key on a local drive.
In this way, you can escurely share the password by sharing the
encryption key through another secure way.
