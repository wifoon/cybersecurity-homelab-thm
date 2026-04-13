**DNS (Domain Name System)** is a hierarchical, distributed database system that translates human-readable Fully Qualified Domain Names (FQDNs), such as `example.com`, into machine-usable IP addresses (IPv4/IPv6).

#### DNS queries
nslookup `--type=` website.com

#### Record types

**A Record**
Resolve to IPv4 addresses, for example 104.26.10.229

**AAAA Record**
Resolve to IPv6 addresses, for example 2606:4700:20::681a:be5

**CNAME Record**
These records resolve to another domain name.

**MX Record**
These records resolve to the address of the servers that handle the email for the domain you are querying.

