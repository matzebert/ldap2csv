# LDAP to CSV converter

## Purpose

Tool that reads data via LDAP and writes the query result to a CSV file.

The example configurations in the `./etc` directory are suitable for a typical linuxmuster.net setup.


## Configuration

Configurations are stored in YAML files. The `-c` option is required and takes at least one configuration file name. When using more than one file, later values overwrite previous ones.

The following table shows the keys available.

| Key             | Description                                    | Example                                                                          |
| --------------- | ---------------------------------------------- | -------------------------------------------------------------------------------- |
| `host`          | URL of the LDAP host                           | `ldaps://ldap.schule.de`                                                         |
| `bind-user`     | full DN of the bind user                       | `CN=bind-user,OU=Management,OU=default-school,OU=SCHOOLS,DC=lmn,DC=schule,DC=de` |
| `bind-passwd`   | password for the bind user                     | `TopSecret!`                                                                     |
| `search-base`   | search base in the LDAP tree                   | `OU=students,OU=default-school,OU=SCHOOLS,DC=lmn,DC=schule,DC=de`                |
| `search-filter` | search filter for the LDAP query               | `(&(objectClass=person)(!(sophomorixAdminClass=attic)))`                         |
| `attributes`    | LDAP attributes to be included in the CSV file | `[sAMAccountName, sn, givenName]`                                                |


## Examples

``` bash
ldap2csv --help
ldap2csv --version
ldap2csv -c ldap.yaml webuntis.yaml
ldap2csv -c ldap.yaml webuntis.yaml -o students.csv
```


---

Copyright (C) 2024 Matthias Ebert
 
This program is free software: you can redistribute it and/or modify it under
the terms of the GNU General Public License as published by the Free Software
Foundation, version 3.
 
This program is distributed in the hope that it will be useful, but WITHOUT
ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS
FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.
 
You should have received a copy of the GNU General Public License along with
this program. If not, see <https://www.gnu.org/licenses/>.
