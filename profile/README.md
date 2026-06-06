# Stratza Labs

Stratza Labs builds infrastructure tooling for real production environments:
small public APIs, explicit behavior, modern security defaults, and measurable
runtime behavior.

Our current public focus is **SpindleX**, a typed Python SSHv2 and SFTP library
for async automation, secure file transfer, port forwarding, and controlled
SSH/SFTP server workflows.

## Active Project

### [SpindleX](https://github.com/stratza/spindlex)

Modern SSH and SFTP for Python.

- Package: [`spindlex` on PyPI](https://pypi.org/project/spindlex/)
- Docs: [spindlex.readthedocs.io](https://spindlex.readthedocs.io/)
- Source: [github.com/stratza/spindlex](https://github.com/stratza/spindlex)
- Changelog: [docs/changelog.md](https://github.com/stratza/spindlex/blob/main/docs/changelog.md)
- Security policy: [GitHub Security Policy](https://github.com/stratza/spindlex/security/policy)

```bash
pip install spindlex
```

```python
from spindlex import SSHClient

with SSHClient() as client:
    client.get_host_keys().load()
    client.connect("example.com", username="admin")
    stdin, stdout, stderr = client.exec_command("uptime")
    print(stdout.read().decode().strip())
```

## What We Care About

- Explicit APIs over hidden behavior.
- Secure defaults that do not require users to remember dangerous footnotes.
- Typed Python interfaces for infrastructure automation.
- Compatibility claims backed by tests, reports, and documented boundaries.
- Release and security practices that can be audited by users.

## Maintainers

- [Adi Roth](https://github.com/adirothbuilds)
- [David Azani](https://github.com/Di3Z1E)

## Community

- Ask usage questions in [SpindleX Discussions](https://github.com/stratza/spindlex/discussions).
- Report bugs or compatibility findings in [SpindleX Issues](https://github.com/stratza/spindlex/issues).
- Report security issues privately through the [SpindleX security policy](https://github.com/stratza/spindlex/security/policy).

