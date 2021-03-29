---
title: Asignación de la interfaz de usuario de objetos de usuario
description: En las tablas siguientes se identifican las páginas de propiedades proporcionadas por el complemento usuarios y equipos de Active Directory.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- Asignación de interfaz de usuario de objeto de usuario AD
- Asignación de interfaz de usuario AD, objeto de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc797be7c53ba7759051016ddd0548c8c7124cd2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104487406"
---
# <a name="user-object-user-interface-mapping"></a>Asignación de la interfaz de usuario de objetos de usuario

En las tablas siguientes se identifican las páginas de propiedades proporcionadas por el complemento usuarios y equipos de Active Directory. Cada tabla identifica los elementos de la interfaz de usuario de la página de propiedades y el atributo asociado a ese elemento de la interfaz de usuario. Dado que las páginas de propiedades que se muestran en el complemento usuarios y equipos de Active Directory se pueden extender, no es posible proporcionar estos datos para todas las páginas que se muestran en una hoja de propiedades.

## <a name="general-property-page"></a>Página de propiedades general

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la página de propiedades **General** .



| Etiqueta de la interfaz de usuario         | Atributo en Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Nombre       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Apellido        | [**NS**](/windows/desktop/ADSchema/a-sn)                                                 |
| Iniciales         | [**iniciales**](/windows/desktop/ADSchema/a-initials)                                     |
| Display Name (Nombre para mostrar)     | [**Mostrar**](/windows/desktop/ADSchema/a-displayname)                               |
| Descripción      | [**denominación**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Número de teléfono | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Teléfono: otros | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Correo electrónico           | [**Direcciones de correo electrónico**](/windows/desktop/ADSchema/a-mail)                                 |
| Página web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Página Web: otra  | [**Dirección**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Página de propiedades de cuenta

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la página de propiedades de la **cuenta** .



| Etiqueta de la interfaz de usuario                                | Atributo en Active Directory Domain Services                                                   | Comentario                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de UserLogon                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Este campo se toma de todo en el atributo [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) que precede al último carácter ' @ '. El último carácter ' @ ' y todo lo que aparece después se coloca en el cuadro combinado de sufijo.                                                                                                                                                      |
| Nombre de inicio de sesión de usuario (anterior a Windows 2000)      | [**Atributo**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| Horas de inicio de sesión                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| Iniciar sesión en                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| La cuenta está bloqueada                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) y [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Si el atributo [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) no es cero, el atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) se agrega a **lockoutTime** y se compara con la fecha y hora actuales para determinar si la cuenta está bloqueada.                                                                                                                                |
| El usuario debe cambiar la contraseña en el siguiente inicio de sesión | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| El usuario no puede cambiar la contraseña             | N/D                                                                                             | Este es el control cambiar contraseña en la ACL.                                                                                                                                                                                                                                                                                                                                         |
| Otras opciones de cuenta                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Los elementos restantes de las opciones de cuenta alternan bits en la máscara de bits del atributo [**UserAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (marcas en un valor DWORD).                                                                                                                                                                                                                                 |
| La cuenta expira                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | El control **cuenta Expires** muestra la fecha de expiración de la cuenta al final de. El atributo [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires) se almacena como la fecha de expiración de la cuenta. Por este motivo, la fecha mostrada en el control **Expires** de la cuenta se mostrará como un día anterior a la fecha incluida en el atributo **accountExpires** . |



 

## <a name="address-property-page"></a>Página de propiedades Dirección

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la página de propiedades **Dirección** .



| Etiqueta de la interfaz de usuario        | Atributo en Active Directory Domain Services                                                 | Comentario                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Calle          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Sin comentarios.                                               |
| P. O. Box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Sin comentarios.                                               |
| City (Ciudad)            | [**l**](/windows/desktop/ADSchema/a-l)                                                                         | El nombre del atributo **l** es una "l" minúscula como en la configuración regional. |
| Estado o provincia  | [**primer**](/windows/desktop/ADSchema/a-st)                                                                       | Sin comentarios.                                               |
| Código postal | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Sin comentarios.                                               |
| País/región  | [**c**](/windows/desktop/ADSchema/a-c), [**Co**](/windows/desktop/ADSchema/a-co)y [**CountryCode**](/windows/desktop/ADSchema/a-countrycode) | Sin comentarios.                                               |



 

## <a name="member-of-property-page"></a>Miembro de la página de propiedades

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario del **miembro de** la página de propiedades.



| Etiqueta de la interfaz de usuario          | Atributo en Active Directory Domain Services   | Comentario                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Miembro de         | [**memberOf**](/windows/desktop/ADSchema/a-memberof)             | Incluye todos los grupos de la lista de interfaz de usuario, excepto el grupo principal, que se representa en el AD mediante el atributo [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) . |
| Establecer grupo principal | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: vinculado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo principal.                                                                                  |



 

## <a name="organization-property-page"></a>Página de propiedades de la organización

En la tabla siguiente se muestran las etiquetas de la interfaz de usuario de la página de propiedades de la **organización** .



| Etiqueta de la interfaz de usuario       | Atributo en Active Directory Domain Services | Comentario     |
|----------------|-----------------------------------------------|-------------|
| Title          | [**título**](/windows/desktop/ADSchema/a-title)                 | Sin comentarios. |
| department     | [**department**](/windows/desktop/ADSchema/a-department)       | Sin comentarios. |
| Compañía        | [**recíproca**](/windows/desktop/ADSchema/a-company)             | Sin comentarios. |
| Administrador: nombre   | [**Manager**](/windows/desktop/ADSchema/a-manager)             | Sin comentarios. |
| Subordinados directos | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Sin comentarios. |



 

## <a name="profile-property-page"></a>Página de propiedades perfil

En la tabla siguiente se enumeran las etiquetas de la interfaz de usuario de la página de propiedades **perfil** .



| Etiqueta de la interfaz de usuario                | Atributo en Active Directory Domain Services | Comentario                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Ruta de acceso al perfil            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | Sin comentarios.                                                                                                             |
| Script de inicio de sesión            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Sin comentarios.                                                                                                             |
| Carpeta principal: ruta de acceso local | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Si está seleccionada la opción **ruta de acceso local** , la ruta de acceso local se almacena en el atributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) . |
| Carpeta principal: conectar    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Si se selecciona **conectar** , la unidad asignada se almacena en el atributo [**HOMEDRIVE**](/windows/desktop/ADSchema/a-homedrive) .          |
| Carpeta principal: para         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Si se selecciona **conectar** , la ruta de acceso se almacena en el atributo [**HomeDirectory**](/windows/desktop/ADSchema/a-homedirectory) .          |



 

## <a name="telephones-property-page"></a>Página de propiedades de teléfonos

En la tabla siguiente se enumeran los elementos de la interfaz de usuario de la página de propiedades **telephones** y sus correspondientes atributos de Active Directory.



| Etiqueta de la interfaz de usuario        | Atributo en Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Página principal            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Inicio: otros     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Buscapersonas           | [**buscapersonas**](/windows/desktop/ADSchema/a-pager)                                                 |
| Buscapersonas: otros    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Móvil          | [**Movilidad**](/windows/desktop/ADSchema/a-mobile)                                               |
| Móvil: otros   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: otros      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Teléfono IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Teléfono IP: otro | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Notas           | [**superclase**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Páginas de propiedades de Perfil de entorno, sesiones, control remoto y Terminal Services

Las páginas de Perfil de **entorno**, **sesiones**, **control remoto** y **Terminal Services** se proporcionan para que un objeto de usuario admita Terminal Services. Los elementos de la interfaz de usuario de estas páginas no se corresponden con los atributos individuales. En su lugar, los valores se almacenan en datos privados dentro de Active Directory Domain Services. Se puede tener acceso a la configuración de Terminal Services con la interfaz [**IADsTsUserEx**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex) .

 

 