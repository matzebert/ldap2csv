# LDAP to CSV converter

## Purpose

Tool that reads data via LDAP and writes the query result to a CSV file.

The example configurations in the `./etc` directory are suitable for a typical linuxmuster.net setup.


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
