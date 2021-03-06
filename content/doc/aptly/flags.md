---
date: "2014-08-08T11:17:38Z"
title: "Global Flags"
menu:
    doc:
        parent: Commands
        weight: 5
---

Global Flags
------------

There are several flags that could be specfied almost with any aptly command.
Flags could be specified before or after command name:

    $ aptly -option1 command ...

Global flags are:

-   `-architectures=""`: list of architectures to consider during
    (comma-separated), default to all available
-   `-config=""`: location of configuration file (default locations are
    `/etc/aptly.conf`, `~/.aptly.conf`)
-   `-db-open-attempts=10`: number of attempts to open DB if it's locked by
    other instance of aptly  {{< version "1.1.0" >}}
-   `-dep-follow-all-variants=false`: when processing dependencies,
    follow a & b if depdency is 'a|b'
-   `-dep-follow-recommends=false`: when processing dependencies, follow
    Recommends
-   `-dep-follow-source=false`: when processing dependencies, follow
    from binary package to source package
-   `-dep-follow-suggests=false`: when processing dependencies, follow
    Suggests
-   `-dep-verbose-resolve=false`: when processing dependencies, print detailed
    logs {{< version "1.1.0" >}}
-   `-gpg-provider=gpg`: PGP provider implementation
    (`gpg` for external gpg or `internal` for [Go internal implementation](/doc/feature/pgp-providers))    

Global flags override [configuration](/doc/configuration) parameters with similar names.

For more information on `-dep-*` flags, please see [dependency resolving](/doc/feature/dependencies).
 
