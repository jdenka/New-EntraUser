# New-EntraUser
This function is primarly created to be run interactivly, it requires you to connect to Microsoft Graph using 
Connect-MgGraph -Scopes "User.ReadWrite.All"
It also requires the module BinaryPasswordGenerator (https://www.powershellgallery.com/packages/BinaryPasswordGenerator/1.0.3)

If you are going to use this you will need to edit the Parameter validateset with your own custom domains. Without changeing it you wont be able to use the script, the minimal you have to do is to add your primary domain.

## Exapmles 
```
New-EntraUser -GivenName Dennis -SurName Johansson
```
This command will create the user Dennis Johansson with the tenants default domain as the UserPrincipalName

```
New-EntraUser -GivenName Dennis -SurName Johansson -Domain cloudidentity.se
```
This command will create the user Dennis Johansson with the domain cloudidentity.se as the UserPrincipalName
