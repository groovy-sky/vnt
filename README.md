# VirtualNetworkTweak (VNT)

The VirtualNetworkTweak (VNT) is a command-line tool designed to manage and modify Azure Virtual Networks (VNets). It allows users to split the address space of a given VNet into smaller subnets.

## Features

- Split the address space of a VNet into smaller subnets.
- (More features to come as the project grows)

## Prerequisites

- Python 3.6+
- An Azure account and subscription
- Azure CLI authenticated, or service principal set up

## Installation

1. Clone the repository:

```bash
git clone https://github.com/groovy-sky/vnt.git
```

2. Change into the `vnt` directory:

```bash
cd vnt
```

3. Install the required Python packages:

```bash
pip install -r requirements.txt
```

## Usage

To split the address space of a VNet, use the `split` command. Provide the resource ID of the VNet and the new prefix length as arguments:

```bash
python vnt/azure.py split /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName} {newPrefix}
```

To see existing subnets of a VNet, use the `print` command. Provide the resource ID of the VNet as an argument:

```bash
python vnt/azure.py print /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName}
```

To store results in a file, use the `--output` option:

```bash
python vnt/azure.py print /subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Network/virtualNetworks/{vnetName} --output {outputFile}
```

## Contributing

Contributions are welcome! Please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
