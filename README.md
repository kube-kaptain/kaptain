# Kaptain

A Kubernetes deployment system unlike anything you've seen before.


# Branchout repo management

The set of related repos in the `kube-kaptain` GitHub org are managed here
using [Branchout/branchout](https://github.com/Branchout/branchout), a tool for
documenting and working with a set of repos in a consistent way. This project is
for those looking to tinker with the small Keelson ecosystem. To use it start by
installing branchout with brew or by cloning it and adding it to your path, then
running one of the following commands on your machine:

```bash
branchout init git@github.com:kube-kaptain/kaptain.git
# or
branchout init https://github.com/kube-kaptain/kaptain.git
```

Then the following two commands, in order:

```bash
cd ~/projects/kaptain
branchout pull
```

After which you can explore the repositories inside ` ~/projects/kaptain/*/`


# More info

See [CLAUDE.md](CLAUDE.md) for more information until this README.md is enriched.
