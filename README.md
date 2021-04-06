# Create an Azure Public IP with PowerShell

Run the following commands in PowerShell to create an Azure Public IP

```PowerShell
# Replace the following required variables
$PublicIpVars = @{
    Name = "your-public-ip-700"
    Location = 'EastUS2'
    AllocationMethod = "Static"
    Sku = "Standard"
    Zone = "1", "2", "3"
    ResourceGroupName = 'your-rg-name'
}

# Deploy a zone-redundant public IP
$PublicIp = New-AzPublicIpAddress @PublicIpVars
```

## Notes

Display available Azure locations

```PowerShell
Get-AzLocation | Format-Table -Property Location, DisplayName
```

## Troubleshooting

## Alternatives

## Additional Resources

- [MS | Docs | New-AzPublicIpAddress][1]
- [MS | Docs | Get-AzLocations][2]

<!-- Reference Links -->

[1]: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azpublicipaddress?view=azps-5.7.0
[2]: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azlocation?view=azps-5.7.0
