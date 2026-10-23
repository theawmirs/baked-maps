# baked-assets

The runtime assets the Vesper loader requires: every baked map package, the
model pack, the radar images, the hit sounds, and the agent portrait. This tree
mirrors the loader's `assets/` directory, path for path, so the signed release's
`installPath` is the same relative path seen here.

The loader fetches nothing from this repository. `infra/scripts/ops.sh`
(`release-asset`) downloads this branch as a tarball, refuses any file whose
digest disagrees with the table below, and publishes the whole set as one signed
`asset` release; the loader installs only what that signed catalogue names.

A re-bake means a new commit here, new digests in that task, and a new asset
release version.

| Path | Bytes | SHA-256 |
|---|---:|---|
| `agent.png` | 233744 | `918f00c294a5c22550b7f38d49e6d23f66e4a69f254f3fe5f4e5708eebcc14af` |
| `maps/ar_baggage.occ` | 10715472 | `807a32c1258416f28850cb87f1434bb7e8d859fc08bbb5285d28157b5a213856` |
| `maps/ar_pool_day.occ` | 9247068 | `b43ea28959f1bb41d105c7c8bb4a42aeb41a6c236892f9b3b50382fa7db28a75` |
| `maps/ar_shoots.occ` | 28906380 | `21f9d68005ed09eaec0258f2752a12c8b483e6285e69b286a0a307026bd55ea5` |
| `maps/cs_italy.occ` | 47155860 | `45579c432209c475526c11731322e3b14eacf3a3048d94501fe0ee2c8227c60b` |
| `maps/cs_office.occ` | 3820356 | `e9dd424b471db15e28909c5c9c7e76461ce9826b4f4c343d45354400608651fb` |
| `maps/de_ancient.occ` | 34588584 | `32ee636c3646cfdb198b6767374d5ad1140bfc4cae4eb37702059c94181583cd` |
| `maps/de_anubis.occ` | 24356556 | `333da4c56128cdbf9c77e32748b08a47715c596559bb5ccc922a52eb379653dd` |
| `maps/de_dust2.occ` | 15229620 | `e19bf9790fcda9f9c1d4a7e42e3e23d8b75262e0bda4b99517404b8cddbaf00e` |
| `maps/de_inferno.occ` | 97329996 | `6da89464ce6830e09a95e6bdc64d4736b94ee9c44638da4af65abee83f24f444` |
| `maps/de_mirage.occ` | 4482432 | `0dc13e213eff21e1eaca3665f0f2ccb25f11728e7dcc7b8705dda20115ebc274` |
| `maps/de_nuke.occ` | 6407532 | `3f70444ef8979801802fa5f63c39ef4708387935993cc2bb1801f777ae85bfe4` |
| `maps/de_overpass.occ` | 49521888 | `16ca78151b636ced9fcf3c92dc043fb3144685756c15aab0318b8b2380c892bf` |
| `maps/de_vertigo.occ` | 7193448 | `5e23f80c4b99aec42f4f12f3f5036a318622f27511059035afd2e50bd718a738` |
| `models/models.vmp` | 2806186 | `8cf81315976edbafeb8add5fd44a2c1729f999b9604c4c3c73a64b5344e926da` |
| `radar/LICENSE` | 32495 | `def9bfa7ce94b0b39990fd6fc2493bd0eef9308e019caac51367cc5f8bde76d1` |
| `radar/SOURCE.txt` | 167 | `02073d807a02c35bbbeed12a4b67ec94af337f999aaba4191b48e7f5411ef25d` |
| `radar/de_ancient/LICENSE` | 1087 | `f882b7dd6095b3c2be4cadcfecb7fd6ef60e29a42e7b437e692f190999a70b02` |
| `radar/de_ancient/meta.json5` | 1001 | `6676bbf90cd9fad49905f28317deab82072f7f9ba25f07162623f6ec34c32134` |
| `radar/de_ancient/radar.png` | 200140 | `34381b0349a145a75cf779ed8313425cd5602693a015b600d3d9b9bd2f0e6fe9` |
| `radar/de_anubis/LICENSE` | 1087 | `f882b7dd6095b3c2be4cadcfecb7fd6ef60e29a42e7b437e692f190999a70b02` |
| `radar/de_anubis/meta.json5` | 692 | `396bb19a2aa5524a7dacf6c90d1aa9a4483e04f90c554bf69df5438291477a7f` |
| `radar/de_anubis/radar.png` | 361480 | `a117c55fcd6690c74210125c2f409a32b9348c931213b388cf3ab5ed0c3d47ae` |
| `radar/de_cache/meta.json5` | 579 | `aa9ffa791234bbe9996b54666f78539fc6148d4b6879f76aa7a6cf274fbdece4` |
| `radar/de_cache/radar.png` | 132550 | `2f2e26043469a962a141e2f23b649c8750a71d02d3f4a7ab6a703e4046b27d2d` |
| `radar/de_dust2/meta.json5` | 1004 | `a164093559947d0892427c7e10ff7f20f16cc6ead0dcef91f0176fc4529fa25b` |
| `radar/de_dust2/radar.png` | 183510 | `058db75547a934f35da928c20048edaa51152fd1028eba42a310bb4d6144f977` |
| `radar/de_inferno/meta.json5` | 1001 | `e2e09d66dfcfed245bcdf275df79907c79c72c862875eb2c96552bcd8645187e` |
| `radar/de_inferno/radar.png` | 173365 | `ebbb73cf9a73b80e699d7765476c7bb490ba2524189ead14db6ed2a1a0bacc99` |
| `radar/de_mirage/meta.json5` | 1004 | `0ec66216e5e836b3f81cb966116b881ac0398cd8cc28753c6c9bf65f54b609f2` |
| `radar/de_mirage/radar.png` | 119422 | `13daee22f5807f0e3672bc42b606bfd273ef913dc01f5720b2215e6a2239063e` |
| `radar/de_nuke/meta.json5` | 1609 | `098bea6d78946fdaf60cc3d6a529c11db0c1c66e77fa637de44151a0664cffcd` |
| `radar/de_nuke/radar.png` | 116890 | `8e9651be759665480a91b35de036e57e7feeb6e8537f6c4fb95c3f953925f4b8` |
| `radar/de_overpass/meta.json5` | 1001 | `992cb48fdf516ec87f34bd8c43cbce61fea08d50efc971f05295d5b63fa925e8` |
| `radar/de_overpass/radar.png` | 308854 | `b5d0f31e8d2258e342952a3412a225654a2be4ef9d261adca8dd78a657509177` |
| `radar/de_train/meta.json5` | 1002 | `964dcbc3f28c5cf4d633d3107a4b9ae16cba54e0692f8036ecf663992fc1bf67` |
| `radar/de_train/radar.png` | 256114 | `bbfd1d10931df7cc2f76ab676c6b0a7de4bd5f63f60efbc16c93ffba2eb3473d` |
| `radar/de_vertigo/meta.json5` | 1081 | `4110cefbe74fa9afb3169c319aa165d002f5ef7e5692f6e69f72ba2f36ce882a` |
| `radar/de_vertigo/radar.png` | 88838 | `1e713246692d74b22d8720cf2c0dfb99fac2e559d73d8a3b59a380d77362ce51` |
| `sounds/cod.wav` | 11786 | `c33bf37e7bd2418c20ec5ec98c6b02c6d2f297556018a97fa46a089501106f84` |
| `sounds/skeet.wav` | 41606 | `73d76055b4d0d52f601f9eba929b4ddcd5f60edb41384acaa1e0afb4963b1698` |

41 files, 344,034,487 bytes.
