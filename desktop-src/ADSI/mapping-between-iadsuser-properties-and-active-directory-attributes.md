---
title: Asignación entre propiedades IADsUser y Active Directory atributos
description: Si procede, una propiedad del objeto de usuario ADSI se asigna a un atributo Active Directory adecuado. Las propiedades del objeto de usuario ADSI están asociadas a los métodos de propiedad IADsUser.
ms.assetid: 9b568084-5a6b-4a73-be88-9d9cd8007824
ms.tgt_platform: multiple
keywords:
- Asignación entre propiedades IADsUser y ADSI Active Directory atributos de usuario
- ADSI del proveedor LDAP, objeto de usuario, asignación entre IADs Propiedades de usuario y atributos Active Directory usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e659c6325457b2654ad5cfeef964975949150232c4ae3376fac640c51c41aa8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839485"
---
# <a name="mapping-between-iadsuser-properties-and-active-directory-attributes"></a>Asignación entre propiedades IADsUser y Active Directory atributos

Si procede, una propiedad del objeto de usuario ADSI se asigna a un atributo Active Directory adecuado. Las propiedades del objeto de usuario ADSI están asociadas a [**los métodos de propiedad IADsUser.**](/windows/desktop/api/Iads/nn-iads-iadsuser)

En la tabla siguiente se muestra la asignación [**entre las propiedades IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) del proveedor LDAP y el atributo Active Directory correspondiente.



| Propiedad IADsUser                                           | Atributo de Active Directory                                                                                  |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | **ADS \_ Marca \_ ACCOUNTDISABLE de UF** en el [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol)  |
| [**AccountExpirationDate**](iadsuser-property-methods.md)  | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                             |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | No compatible.                                                                                              |
| [**BadLoginCount**](iadsuser-property-methods.md)          | [**badPwdCount**](/windows/desktop/ADSchema/a-badpwdcount)                                                                   |
| [**Departamento**](iadsuser-property-methods.md)             | [**Departamento**](/windows/desktop/ADSchema/a-department)                                                                     |
| [**Descripción**](iadsuser-property-methods.md)            | [**Descripción**](/windows/desktop/ADSchema/a-description)                                                                   |
| [**División**](iadsuser-property-methods.md)               | [**División**](/windows/desktop/ADSchema/a-division)                                                                         |
| [**EmailAddress**](iadsuser-property-methods.md)           | [**mail**](/windows/desktop/ADSchema/a-mail)                                                                                 |
| [**Employeeid**](iadsuser-property-methods.md)             | [**Employeeid**](/windows/desktop/ADSchema/a-employeeid)                                                                     |
| [**FaxNumber**](iadsuser-property-methods.md)              | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)                                         |
| [**Nombre**](iadsuser-property-methods.md)              | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                                                       |
| [**FullName**](iadsuser-property-methods.md)               | [**Displayname**](/windows/desktop/ADSchema/a-displayname)                                                                   |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | No compatible.                                                                                              |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | No compatible.                                                                                              |
| [**HomeDirectory**](iadsuser-property-methods.md)          | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory)                                                               |
| [**Página principal**](iadsuser-property-methods.md)               | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                                                                   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime)                                                                   |
| [**Idiomas**](iadsuser-property-methods.md)              | No compatible.                                                                                              |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | [**badPasswordTime**](/windows/desktop/ADSchema/a-badpasswordtime)                                                           |
| [**LastLogin**](iadsuser-property-methods.md)              | [**lastLogon**](/windows/desktop/ADSchema/a-lastlogon)                                                                       |
| [**LastLogoff**](iadsuser-property-methods.md)             | [**lastLogoff**](/windows/desktop/ADSchema/a-lastlogoff)                                                                     |
| [**Apellidos**](iadsuser-property-methods.md)               | [**Sn**](/windows/desktop/ADSchema/a-sn)                                                                                     |
| [**LoginHours**](iadsuser-property-methods.md)             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                                     |
| [**LoginScript**](iadsuser-property-methods.md)            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)                                                                     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | [**userWorkstations**](/windows/desktop/ADSchema/a-userworkstations)                                                         |
| [**director**](iadsuser-property-methods.md)                | [**manager**](/windows/desktop/ADSchema/a-manager)                                                                           |
| [**MaxLogins**](iadsuser-property-methods.md)              | No compatible.                                                                                              |
| [**MaxStorage**](iadsuser-property-methods.md)             | [**maxStorage**](/windows/desktop/ADSchema/a-maxstorage)                                                                     |
| [**NamePrefix**](iadsuser-property-methods.md)             | [**personalTitle**](/windows/desktop/ADSchema/a-personaltitle)                                                               |
| [**Sufijonombre**](iadsuser-property-methods.md)             | [**generationQualifier**](/windows/desktop/ADSchema/a-generationqualifier)                                                   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename)                                     |
| [**OtherName**](iadsuser-property-methods.md)              | [**middleName**](/windows/desktop/ADSchema/a-middlename)                                                                     |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | Establecer mediante directiva de grupo Editor                                                                               |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                                     |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | Establecer mediante directiva de grupo Editor                                                                               |
| [**PasswordRequired**](iadsuser-property-methods.md)       | **ADS \_ Marca UF \_ PASSWD \_ NOTREQD** en el [**atributo userAccountControl.**](/windows/desktop/ADSchema/a-useraccountcontrol) |
| [**Imagen**](iadsuser-property-methods.md)                | [**thumbnailPhoto**](/windows/desktop/ADSchema/a-thumbnailphoto)                                                             |
| [**PostalAddresses**](iadsuser-property-methods.md)        | [**postalAddress**](/windows/desktop/ADSchema/a-postaladdress)                                                               |
| [**PostalCodes**](iadsuser-property-methods.md)            | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                                     |
| [**Perfil**](iadsuser-property-methods.md)                | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)                                                                   |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | Establecer mediante directiva de grupo Editor                                                                               |
| [**SeeAlso**](iadsuser-property-methods.md)                | [**seeAlso**](/windows/desktop/ADSchema/a-seealso)                                                                           |
| [**TelephoneHome**](iadsuser-property-methods.md)          | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                                                       |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | [**Móvil**](/windows/desktop/ADSchema/a-mobile)                                                                             |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                                                           |
| [**TelephonePager**](iadsuser-property-methods.md)         | [**Buscapersonas**](/windows/desktop/ADSchema/a-pager)                                                                               |
| [**Título**](iadsuser-property-methods.md)                  | [**Título**](/windows/desktop/ADSchema/a-title)                                                                               |



 

 

 