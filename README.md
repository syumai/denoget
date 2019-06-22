# DEPRECATED

* This command was added to `deno_std` as [`installer`](https://github.com/denoland/deno_std/tree/master/installer) and now `deno install` is available.
* Please use them instead of denoget.

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
# now you can use installed command!
denoinit
```

## Requirements for installing

- Deno
- wget

## Installing

### 1. Install denoget

denoget can be installed by using itself.

```sh
deno -A https://deno.land/x/denoget/denoget.ts https://deno.land/x/denoget/denoget.ts
```

### 2. Add `~/.deno/denoget/bin` to PATH

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
