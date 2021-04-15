---
title: Asignación entre propiedades de IADsUser y atributos de Active Directory
description: Cuando sea aplicable, se asigna una propiedad del objeto de usuario ADSI a un atributo de Active Directory adecuado. Las propiedades del objeto de usuario ADSI están asociadas a los métodos de la propiedad IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Asignación entre las propiedades de IADsUser y los atributos de Active Directory ADSI
- ADSI Provider de LDAP, objeto de usuario, asignación entre propiedades de IADsUser y atributos de Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17b817a8c56e2c74c846e1343e0ed7803427f4a2
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104421411"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Asignación entre propiedades de IADsUser y atributos de Active Directory

Cuando sea aplicable, se asigna una propiedad del objeto de usuario ADSI a un atributo de Active Directory adecuado. Las propiedades del objeto de usuario ADSI están asociadas a los métodos de la propiedad [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) .

En la tabla siguiente se muestra la asignación entre las propiedades de [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) para el proveedor LDAP y el atributo de Active Directory correspondiente.



| Propiedad IADsUser                                           | Atributo de Active Directory                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **Anuncios \_ de Marca fi \_ ACCOUNTDISABLE** en el atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) .  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | No compatible.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Departamento**](iadsuser-property-methods.md)             | [**department**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Descripción**](iadsuser-property-methods.md)            | [**denominación**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**División**](iadsuser-property-methods.md)               | [**ella**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**EmployeeID**](iadsuser-property-methods.md)             | [**employeeID**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**FaxNumber**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**FirstName**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**Mostrar**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | No compatible.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | No compatible.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Página principal**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Lenguajes**](iadsuser-property-methods.md)              | No compatible.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**LastName**](iadsuser-property-methods.md)               | [**NS**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**Manager**](iadsuser-property-methods.md)                | [**Manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | No compatible.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**NameSuffix**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Establecer con el editor de directiva de grupo                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Establecer con el editor de directiva de grupo                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **Anuncios \_ de Marca de fi \_ passwd \_ NOTREQD** en el atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) . |
| [**Imagen**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**PostalCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Perfil**](iadsuser-property-methods.md)                | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Establecer con el editor de directiva de grupo                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**Movilidad**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**buscapersonas**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Title**](iadsuser-property-methods.md)                  | [**Titulo**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 