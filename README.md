# denoget

- denoget installs executable deno script.

## Features

- Install executable script into ~/.deno/denoget/bin

## Supported Environments

- macOS
- Linux

## Usage

```sh
denoget https://denopkg.com/syumai/deno-libs/denoinit/denoinit.ts
denoinit # now you can use installed command!
```

## Requirements for installing

- deno
- wget

## Installing

### Install denoget

- denoget can be installed using the command itself.

```sh
deno -A https://denopkg.com/syumai/denoget/denoget.ts https://denopkg.com/syumai/denoget/denoget.ts
```

### Add `~/.deno/denoget/bin` to PATH

```
echo 'export PATH="$HOME/.deno/denoget/bin:$PATH"' >> ~/.bashrc # change this to your shell
```

## Create Executable Script

- Add shebang to top of your deno script.
  - This defines what permissions are needed.

```sh
#!/usr/bin/env deno --allow-read --allow-write --allow-env --allow-run
```

- Host script on the web.
- Install script using denoget.
