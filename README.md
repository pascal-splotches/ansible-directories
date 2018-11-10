# ansible-directories

[![Travis CI](https://img.shields.io/travis/com/pascal-splotches/ansible-directories.svg?style=flat-square)](https://travis-ci.com/pascal-splotches/ansible-directories)
[![GitHub tag (latest SemVer)](https://img.shields.io/github/tag/pascal-splotches/ansible-directories.svg?style=flat-square)](https://github.com/pascal-splotches/ansible-directories/releases)
[![Ansible Role](https://img.shields.io/ansible/role/32495.svg?style=flat-square)](https://galaxy.ansible.com/pascal_splotches/directories)
![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-brightgreen.svg?style=flat-square)
[![GitHub License](https://img.shields.io/github/license/pascal-splotches/ansible-directories.svg?style=flat-square)](https://github.com/pascal-splotches/ansible-directories/blob/master/LICENSE)

Create pre-defined directory structures.

## Getting Started
### Role Variables

| Name          | Description                                              | Default                          |
|---------------|----------------------------------------------------------|----------------------------------|
| `users`       | The users for whom we provision the relative directories | `[ '{{ ansible_user_id }}' ]`    |
| `directories` | The directories to be created                            | `{ relative: [], absolute: [] }` |

### Example

```YAML
directories:
  relative:
  - path: directory/path # required
    mode: 0700           # optional
  absolute:
  - path:  /directory/path # required
    owner: root            # optional
    mode:  0700            # optional
```

## Dependencies

- _none_

## Built With

- [Ansible](https://www.ansible.com/)

## Versioning

We use [SemVer](https://semver.org/) for versioning. For the versions available, see the [releases on this repository](https://github.com/pascal-splotches/ansible-directories/releases).

## Authors

- Pascal Scheepers <[pascal@splotch.es](mailto:pascal@splotch.es)>

## License

This project is licensed under the GPLv3 License - see the [LICENSE](./LICENSE) file for details.
