# Install Posh-ACME on windows

https://github.com/rmbolger/Posh-ACME/edit/main/README.md

## Installation (Stable)

The latest release can found in the [PowerShell Gallery](https://www.powershellgallery.com/packages/Posh-ACME/) or the [GitHub releases page](https://github.com/rmbolger/Posh-ACME/releases). Installing is easiest from the gallery using `Install-Module`. *See [Installing PowerShellGet](https://docs.microsoft.com/en-us/powershell/scripting/gallery/installing-psget) if you run into problems with it.*

```powershell
# install for all users (requires elevated privs)
Install-Module -Name Posh-ACME -Scope AllUsers

# install for current user
Install-Module -Name Posh-ACME -Scope CurrentUser
```


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

add on you dans records on you dns before press Enter

----------------------------

type:TXT

name: _acme-challenge

value:xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx

---------------

type:TXT

name: _acme-challenge

value:yyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyyy

----------------------------

then press enter 

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
