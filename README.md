# Ringworld Tags
Tag overrides for Ringworld, applied on top of the
[Halo CE Restored](https://github.com/Aerocatia/halopc-restored) tagset.

This is not a standalone tagset. It only holds the tags that Ringworld changes or adds, so every
tag missing here is taken from `halopc-restored`. Nothing from that repository is duplicated here.

## Requirements
- A checkout of [halopc-restored](https://github.com/Aerocatia/halopc-restored).
- [Ringworld Invader](https://github.com/MangoFizz/ringworld-invader), since some tags use fields
  and tag groups that stock Invader does not know.
- The Ringworld engine. Maps built from these tags target the `ringworld` engine only.

## Building
Pass this tags directory first so it takes priority over the base tagset:

```sh
invader-build -g ringworld -t ringworld-tags/tags -t halopc-restored/tags levels/ui/ui
```

## Directory Layout
### `/tags`
Tags that replace or extend the ones in `halopc-restored/tags`, using the same paths.
### `/data`
UTF-16 text sources for the `unicode_string_list` tags. Rebuild a list with:

```sh
invader-string -d data -t tags -T unicode_string_list <tag path>
```

## Notice
The tags here are derived from the Halo Custom Edition and Restored tags, and are assumed to
remain under the Halo Custom Edition EULA.
