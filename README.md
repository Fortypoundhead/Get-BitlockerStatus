# Get-BitlockerStatus

A PowerShell script to retrieve the BitLocker protection status for all computers in an Active Directory domain.

## Description

This script queries Active Directory for all computer objects, then remotely checks the BitLocker status of the C: drive on each computer. It outputs the computer name and protection status for each machine.

## Prerequisites

- PowerShell with Active Directory module installed
- Domain administrator credentials or equivalent permissions to query AD and run remote commands
- Network access to all domain computers
- BitLocker must be enabled on the target systems (if applicable)

## Usage

1. Ensure you have the necessary permissions and network access.
2. Run the script in a PowerShell environment with domain access:
   ```
   .\Get-BitlockerStatus.ps1
   ```
3. When prompted, enter valid domain credentials.

The script will iterate through all computers in Active Directory and display the BitLocker status for each.

## Output

The script outputs a list in the format:
- ComputerName: [Computer Name]
- ProtectionStatus: [On/Off]

## Notes

- This script requires remote PowerShell execution to be enabled on target computers.
- Large domains may take time to process all computers.
- Ensure firewall settings allow remote management.

## License

GNU GENERAL PUBLIC LICENSE v3
