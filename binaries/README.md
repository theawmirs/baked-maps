# binaries

The two executables a `loader` release publishes, at the tag named after the
release (`loader-1.6.0`). The ops task verifies each file against the digest
table in `infra/scripts/ops.sh` before signing, so a changed byte here fails the
publish instead of shipping.

`vesper_helper.exe` is not here: the helper replaces the loader process and
cannot replace itself, so it ships in the installer package only.
