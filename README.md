# zig-translate-c

This runs `zig translate-c` without having to create a temporary header file that includes the system header you want to use.

## Usage

```sh
bunx zig-translate-c netdb.h
bunx zig-translate-c sys/stat.h
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
