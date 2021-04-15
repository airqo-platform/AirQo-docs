# Security

(ToDo: add detail, make private if this doc becomes sufficiently platform specific.)

When developing for the AirQo platform and configuring infrastructure, please take these general priniciples into account:

## Firewall

Only microservices that need to be publicly accessible e.g. for mobile app, web site or public API access should have open ports, the rest should be restricted.

## Control of access

“Least Privilege Access” should be employed e.g. if a microservice only needs to read a subset of data, it should do so with a read only account that can only access the subset.

## Encryption

Data should be encrypted in-flight, encryption at-rest should be considered for personally identifiable or otherwise private data in line with local and international law.

## Anti-virus

The plaform largely runs on Linux, so anti virus is a mainly concern for clients. It must be ensured that the plaform does not pass malicious code to clients.

## Dependency versions

Microservices should be automatically checked for vulnerabilities, patched and redeployed.