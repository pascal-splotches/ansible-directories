# ansible-directories

![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)

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

We use [SemVer](https://semver.org/) for versioning. For the versions available, see the [tags on this repository]().

## Authors

- Pascal Scheepers <[pascal@splotch.es](mailto:pascal@splotch.es)>

## License

This project is licensed under the GPLv3 License - see the [LICENSE](./LICENSE) file for details.
