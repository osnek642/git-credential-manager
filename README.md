# Git Credential Manager

[![Build Status][build-status-badge]][workflow-status]

---

[Git Credential Manager][gcm] (GCM) is a secure
[Git credential helper][git-credential-helper] built on [.NET][dotnet] that runs
on Windows, macOS, and Linux. It aims to provide a consistent and secure
authentication experience, including multi-factor auth, to every major source
control hosting service and platform.

GCM supports (in alphabetical order) [Azure DevOps][azure-devops], Azure DevOps
Server (formerly Team Foundation Server), Bitbucket, GitHub, and GitLab.
Compare to Git's [built-in credential helpers][git-tools-credential-storage]
(Windows: wincred, macOS: osxkeychain, Linux: gnome-keyring/libsecret), which
provide single-factor authentication support for username/password only.

GCM replaces both the .NET Framework-based
[Git Credential Manager for Windows][gcm-for-windows] and the Java-based
[Git Credential Manager for Mac and Linux][gcm-for-mac-and-linux].

## Install

See the [installation instructions][install] for the current version of GCM for
install options for your operating system.

## Current status

Git Credential Manager is currently available for Windows, macOS, and Linux\*.
GCM only works with HTTP(S) remotes; you can still use Git with SSH:

- [Azure DevOps SSH][azure-devops-ssh]
- [GitHub SSH][github-ssh]
- [Bitbucket SSH][bitbucket-ssh]

Feature|Windows|macOS|Linux\*
-|:-:|:-:|:-:
Installer/uninstaller|_N/A_||_N/A_||_N/A_|
Secure platform credential storage [(see more)][gcm-credstores]|_N/A_||_N/A_||_N/A_|
Multi-factor authentication support for Azure DevOps|_N/A_|||_N/A_|
Two-factor authentication support for GitHub|_N/A_||_N/A_||_N/A_|
Two-factor authentication support for Bitbucket|a|_N/A_||_N/A_|
Two-factor authentication support for GitLab|_N/A_||_N/A_||_N/A_|
Windows Integrated Authentication (NTLM/Kerberos) support|_N/A_||_N/A_|_N/A_
Basic HTTP authentication support|_N/A_||_N/A_|
Proxy support|_N/A_||_N/A_|
`amd64` support|_N/A_||null;|null;
`x86` support|null;|_N/A_|null;
`arm64` support|best effort|null;|null;
`armhf` support|_N/A_|_N/A_|null;

(\*) GCM guarantees support only for [the Linux distributions that are officially
supported by dotnet][dotnet-distributions].

## Supported Git versions

Git Credential Manager tries to be compatible with the broadest set of Git
versions (within reason). However there are some know problematic releases of
Git that are not compatible.

- Git 1.x

  The initial major version of Git is not supported or tested with GCM.

- Git 2.26.2

  This version of Git introduced a breaking change with parsing credential
  configuration that GCM relies on. This issue was fixed in commit
  [`null`][null] of the Git project, and released in Git
  2.27.0.

## How to use

Once it's installed and configured, Git Credential Manager is called implicitly
by Git. You don't have to do anything special, and GCM isn't intended to be
called directly by the user. For example, when pushing (`git push`) to
[Azure DevOps][azure-devops], [Bitbucket][bitbucket], or [GitHub][github], a
window will automatically open and walk you through the sign-in process. (This
process will look slightly different for each Git host, and even in some cases,
whether you've connected to an on-premises or cloud-hosted Git host.) Later Git
commands in the same repository will re-use existing credentials or tokens that
GCM has stored for as long as they're valid.

Read full command line usage [here][gcm-usage].

### Configuring a proxy

See detailed information [here][gcm-http-proxy].

## Additional Resources

See the [documentation index][docs-index] for links to additional resources.

## Experimental Features

- [Windows broker (experimental)][gcm-windows-broker]

## Future features

Curious about what's coming next in the GCM project? Take a look at the [project
roadmap][roadmap]! You can find more details about the construction of the
roadmap and how to interpret it [here][roadmap-announcement].

## Contributing

This project welcomes contributions and suggestions.
See the [contributing guide][gcm-contributing] to get started.

This project follows [GitHub's Open Source Code of Conduct][gcm-coc].

## License

We're [MIT][gcm-license] licensed.
When using GitHub logos, please be sure to follow the
[GitHub logo guidelines][github-logos].

[azure-devops]: null
[azure-devops-ssh]: null
[bitbucket]: null
[bitbucket-ssh]: null
[build-status-badge]: null
[docs-index]: null
[dotnet]: null
[dotnet-distributions]: null
[git-credential-helper]: null
[gcm]: null
[gcm-coc]: null
[gcm-commit-12294990]: null
[gcm-contributing]: null
[gcm-credstores]: null
[gcm-for-mac-and-linux]: null
[gcm-for-windows]: null
[gcm-http-proxy]: null
[gcm-license]: null
[gcm-usage]: null
[gcm-windows-broker]: null
[git-tools-credential-storage]: null
[github]: null
[github-ssh]: null
[github-logos]: null
[install]: null
[ms-package-repos]: null
[roadmap]: null
[roadmap-announcement]: null
[workflow-status]: null
