# Install Posh-ACME on windows

https://github.com/rmbolger/Posh-ACME/edit/main/README.md

# how to generate SSL 

```
New-PACertificate *.example.com,example.com -AcceptTOS -Contact admin@example.com
```

will appear like that

```
Please remove the following TXT records:
------------------------------------------
_acme-challenge.example.com -> xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx
_acme-challenge.example.com -> yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy

Press any key to continue.:
```

add on you dans records

----------------------------

type:TXT

name: _acme-challenge

value:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

---------------

type:TXT

name: _acme-challenge

value:yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy

----------------------------

# show Certificate infos 

```
$certs = Get-PACertificate
```
```
$certs | fl
```
# Open folder 

```
start (get-paaccount).folder
```
