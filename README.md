# zig-translate-c

This runs `zig translate-c` without having to create a temporary header file that includes the header you want to translate.

## Usage

```sh
bunx zig-translate-c netdb.h
bunx zig-translate-c sys/stat.h
bunx zig-translate-c sys/stat.h -I/usr/include/x86_64-linux-gnu
```

Previously, you had to do:

```bash
echo "#include <netdb.h>" > foo.h
zig translate-c -lc foo.h
```

Now you can do:

```bash
bunx zig-translate-c netdb.h
```

You will need `bun` installed:

```bash
curl https://bun.sh/install | bash
```
