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
<table>
  <thead>
    <tr>
      <th>Argument</th>
      <th>Description</th>
      <th>Required</th>
      <th>Default Value</th>
    </tr>
  </thead>
  <tbody>
    <tr>
        <td>vpn_config</td>
        <td>OpenVPN configuration file content</td>
        <td>Yes</td>
        <td>None</td>
    </tr>
    <tr>
        <td>vpn_username</td>
        <td>Username for OpenVPN authentication</td>
        <td>No</td>
        <td>None</td>
    </tr>
    <tr>
        <td>vpn_password</td>
        <td>Password for OpenVPN authentication</td>
        <td>No</td>
        <td>None</td>
    </tr>
    <tr>
        <td>timeout</td>
        <td>VPN connection timeout in seconds</td>
        <td>No</td>
        <td>15</td>
    </tr>
  </tbody>
</table>

## License

This project is licensed under the [MIT License](LICENSE).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.

## Support

For any issues or questions, please open an issue in this repository.