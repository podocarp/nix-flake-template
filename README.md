# Nix flake template repository

This is a minimal config to get you started with modern nix shell.
The shell is defined by a flake and entered with direnv.

## How to use

This is dead simple if you have `direnv` installed.
Simply clone this repo and cd into the directory.
You might need to run `direnv allow`, after which everytime you enter the directory you will enter your nix shell.

If you don't have `direnv`, you can alternatively run `nix develop` to enter the shell.

To change the packages available in your shell, simply add them to the `buildInputs` section in `flake.nix`.
Seach for packages [here](https://search.nixos.org/packages).
You can also expose environment variables by adding entries to `mkShell` (this is behaviour inherited from `mkDerivation`).

For more info take a look at the nix docs.
- https://nix.dev/manual/nix/2.17/command-ref/new-cli/nix3-develop
- https://ryantm.github.io/nixpkgs/stdenv/stdenv/
- https://nixos.wiki/wiki/Flakes
