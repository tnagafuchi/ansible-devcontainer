# Devcontainer for Ansible

> THIS PROJECT IS ARCHIVED
>
> See [hspaans/ansible-playbook-template](https://github.com/hspaans/ansible-playbook-template) as an alternative.

## Using within you project

Add `.devcontainer/devcontainer.json` to your repository.

```json
{
  "image": "ghcr.io/hspaans/ansible-devcontainer:latest",
  "name": "Ansible",
  "settings": {
    "terminal.integrated.shell.linux": "/bin/bash"
  },
  "appPort": [],
  "postCreateCommand": "ansible-galaxy install -r roles/requirements.yml",
  "remoteUser": "vscode",
  "extensions": [
    "github.vscode-pull-request-github",
    "ms-python.python",
    "redhat.vscode-yaml"
  ]
}
```

## Versions

The container is based on [LTS](https://en.wikipedia.org/wiki/Long-term_support) distribution versions with official support and fall within N and N-2. The *latest*-tag is an experimental tag to test future releases. See [Ansible: Release and Maintenance](ansible-releases) for the upstream maintenance and release matrix.

| Platform     | Version | Image                                                             |
|:------------:|:-------:|:-----------------------------------------------------------------:|
| Ansible      | 2.8     | [hspaans/ansible-devcontainer:2.8][ansible-devcontainer:2.8]       |
| Ansible      | 2.9     | [hspaans/ansible-devcontainer:2.9][ansible-devcontainer:2.9]       |
| Ansible Base | 2.10    | [hspaans/ansible-devcontainer:2.10][ansible-devcontainer:2.10]     |
| Ansible Core | 2.11    | [hspaans/ansible-devcontainer:latest][ansible-devcontainer:latest] |

[ansible]: https://github.com/ansible/ansible
[ansible-releases]: https://docs.ansible.com/ansible/devel/reference_appendices/release_and_maintenance.html
[molecule]: https://github.com/ansible-community/molecule
[ansible-devcontainer:latest]: ghcr.io/hspaans/ansible-devcontainer:latest
[ansible-devcontainer:2.8]: ghcr.io/hspaans/ansible-devcontainer:2.8
[ansible-devcontainer:2.9]: ghcr.io/hspaans/ansible-devcontainer:2.9
[ansible-devcontainer:2.10]: ghcr.io/hspaans/ansible-devcontainer:2.10
