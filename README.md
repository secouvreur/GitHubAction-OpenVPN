# GitHubAction-OpenVPN

This project provides a GitHub Action workflow for managing and deploying OpenVPN configurations. It is designed to automate the setup and maintenance of OpenVPN clients.

## Features

- Automates OpenVPN server setup.
- Generates client configuration files.
- Supports secure certificate management.
- Easily integrates into CI/CD pipelines.

## Prerequisites

- A GitHub repository.
- Basic knowledge of OpenVPN.
- Access to a server for hosting OpenVPN.

## Usage
### YAML

```yaml
    steps:
- name: Connect to OpenVPN
    uses: secouvreur/GitHubAction-OpenVPN@v0.0.1
    with:
    vpn_config: ${{ secrets.VPN_CONFIG }}
    vpn_username: ${{ secrets.VPN_USERNAME }}
    vpn_password: ${{ secrets.VPN_PASSWORD }}
```

### Arguments
```markdown
| Argument       | Description                          | Required | Default Value |
|----------------|--------------------------------------|----------|---------------|
| `vpn_config`   | OpenVPN configuration file content. | Yes      | None          |
| `vpn_username` | Username for OpenVPN authentication.| NO      | None          |
| `vpn_password` | Password for OpenVPN authentication.| NO      | None          |
| `timeout`.     | VPN connection timeout             .| NO      | 15(sec)       |
```

## License

This project is licensed under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Support

For any issues or questions, please open an issue in this repository.