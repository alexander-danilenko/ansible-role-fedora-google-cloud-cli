<p align="center">
  <img src="https://cdn.svgporn.com/logos/google-cloud.svg" width="33%" />
</p>

<h1 align="center"><img src="https://cdn.svgporn.com/logos/fedora.svg" height="22" /> Fedora/RHEL Google Cloud CLI Ansible Role</h1>

This repo contains an Ansible role Ansible role for installing Google Cloud CLI and tools using [official Fedora/RHEL repositories](https://cloud.google.com/sdk/docs/install#rpm).

## Requirements

Fedora or RHEL system against the ansible role is running for.

## Example Ansible Playbooks

### Simple

```yaml
- hosts: 127.0.0.1
  roles:
    - role: ansible-role-fedora-google-cloud-cli
```

### Advanced

It's possible to override global settings for Docksal: just pass docksal_global_config variable with configuration object.

```yaml
- hosts: 127.0.0.1
  roles:
    - role: ansible-role-fedora-google-cloud-cli
      vars:
        # Repository URL.
        google_cloud_repo_url: 'https://packages.cloud.google.com/yum/repos/cloud-sdk-el9-x86_64'
        # Repository GPG key URL.
        google_cloud_repo_gpgkey: 'https://packages.cloud.google.com/yum/doc/rpm-package-key.gpg'
        # Repository file.
        google_cloud_repo_file: '/etc/yum.repos.d/google-cloud-sdk.repo'
        # Packages to install after repo is added.
        google_cloud_packages:
          - 'google-cloud-cli'
          - 'google-cloud-cli-minikube'
```

See [Google Cloud CLI documentation](https://cloud.google.com/sdk/docs/install#rpm) for all available packages.

## Show your support

Give a ⭐️ if this project helped you!

## 🤝 Contributing

Contributions, issues and feature requests are welcome!<br />Feel free to check [issues page](https://github.com/alexander-danilenko/ansible-role-fedora-google-cloud-cli/issues). 

Experiencing any problems with your distribution? [Raise and issue](https://github.com/alexander-danilenko/ansible-role-fedora-google-cloud-cli/issues/new)!


## 📝 License

Copyright © 2024 [Alexander Danilenko](https://github.com/alexander-danilenko).<br />

<p>
  <a href="./LICENSE" target="_blank">
    <img alt="License: MIT" src="https://img.shields.io/badge/License-MIT-green.svg" />
  </a>
</p>
