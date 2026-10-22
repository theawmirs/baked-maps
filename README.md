# baked-maps

The baked map collision packages the Vesper loader requires, one `.occ` per
competitive map. The loader fetches nothing from here: these files are staged on
the release host and published as the signed `asset` release, and the loader
installs only what that signed catalogue names.

| File | Bytes | SHA-256 |
|---|---:|---|
| `de_dust2.occ` | 15229620 | `e19bf9790fcda9f9c1d4a7e42e3e23d8b75262e0bda4b99517404b8cddbaf00e` |
| `de_mirage.occ` | 4482432 | `0dc13e213eff21e1eaca3665f0f2ccb25f11728e7dcc7b8705dda20115ebc274` |
| `de_inferno.occ` | 97329996 | `6da89464ce6830e09a95e6bdc64d4736b94ee9c44638da4af65abee83f24f444` |
| `de_nuke.occ` | 6407532 | `3f70444ef8979801802fa5f63c39ef4708387935993cc2bb1801f777ae85bfe4` |
| `de_ancient.occ` | 34588584 | `32ee636c3646cfdb198b6767374d5ad1140bfc4cae4eb37702059c94181583cd` |
| `de_anubis.occ` | 24356556 | `333da4c56128cdbf9c77e32748b08a47715c596559bb5ccc922a52eb379653dd` |
| `de_vertigo.occ` | 7193448 | `5e23f80c4b99aec42f4f12f3f5036a318622f27511059035afd2e50bd718a738` |

`infra/scripts/ops.sh` (`release-asset`) downloads these files, refuses any that
does not match the digest above, and publishes the set as one signed release.
A re-bake means a new commit here, new digests in that task, and a new asset
release version.
