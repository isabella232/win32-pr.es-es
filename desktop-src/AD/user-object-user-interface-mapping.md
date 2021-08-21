---
title: Asignación de la interfaz de usuario de objetos de usuario
description: En las tablas siguientes se identifican las páginas de propiedades proporcionadas por Usuarios y equipos de Active Directory complemento.
ms.assetid: f309c139-c957-40c4-b369-f527aa87157c
ms.tgt_platform: multiple
keywords:
- User Object Interfaz de usuario Mapping AD
- Interfaz de usuario asignación de AD , objeto de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 656e8071b558b730ecb1fc0463834f6fbadb7eb9bf4c56b11640e2b95209735f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024512"
---
# <a name="user-object-user-interface-mapping"></a>Asignación de la interfaz de usuario de objetos de usuario

En las tablas siguientes se identifican las páginas de propiedades proporcionadas por Usuarios y equipos de Active Directory complemento. Cada tabla identifica los elementos de la interfaz de usuario de la página de propiedades y el atributo asociado a ese elemento de interfaz de usuario. Dado que las páginas de propiedades mostradas por el complemento Usuarios y equipos de Active Directory se pueden ampliar, no es posible proporcionar estos datos para todas las páginas mostradas en una hoja de propiedades.

## <a name="general-property-page"></a>Página de propiedades General

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de la **página de** propiedades General.



| Etiqueta de interfaz de usuario         | Atributo en Active Directory Domain Services                           |
|------------------|-------------------------------------------------------------------------|
| Nombre       | [**givenName**](/windows/desktop/ADSchema/a-givenname)                                   |
| Apellido        | [**Sn**](/windows/desktop/ADSchema/a-sn)                                                 |
| Iniciales         | [**Iniciales**](/windows/desktop/ADSchema/a-initials)                                     |
| Display Name (Nombre para mostrar)     | [**Displayname**](/windows/desktop/ADSchema/a-displayname)                               |
| Descripción      | [**Descripción**](/windows/desktop/ADSchema/a-description)                               |
| Office           | [**physicalDeliveryOfficeName**](/windows/desktop/ADSchema/a-physicaldeliveryofficename) |
| Número de teléfono | [**telephoneNumber**](/windows/desktop/ADSchema/a-telephonenumber)                       |
| Teléfono: otros | [**otherTelephone**](/windows/desktop/ADSchema/a-othertelephone)                         |
| Correo electrónico           | [**Direcciones de correo electrónico**](/windows/desktop/ADSchema/a-mail)                                 |
| Página web         | [**wWWHomePage**](/windows/desktop/ADSchema/a-wwwhomepage)                               |
| Página web: Otros  | [**Url**](/windows/desktop/ADSchema/a-url)                                               |



 

## <a name="account-property-page"></a>Página de propiedades de la cuenta

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de **la página de** propiedades Cuenta.



| Etiqueta de interfaz de usuario                                | Atributo en Active Directory Domain Services                                                   | Comentario                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Nombre de UserLogon                          | [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname)                                           | Este campo se toma de todo el atributo [**userPrincipalName**](/windows/desktop/ADSchema/a-userprincipalname) que precede al último carácter "@". El último carácter "@" y todo lo que hay después de colocarlo en el cuadro combinado de sufijos.                                                                                                                                                      |
| Nombre de inicio de sesión de usuario (Windows 2000)      | [**Samaccountname**](/windows/desktop/ADSchema/a-samaccountname)                                                 | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| Horas de inicio de sesión                             | [**logonHours**](/windows/desktop/ADSchema/a-logonhours)                                                         | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| Iniciar sesión en                               | [**logonWorkstation**](/windows/desktop/ADSchema/a-logonworkstation)                                             | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| La cuenta está bloqueada                   | [**lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) y [ **lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) | Si el [**atributo lockoutTime**](/windows/desktop/ADSchema/a-lockouttime) no es cero, el atributo [**lockoutDuration**](/windows/desktop/ADSchema/a-lockoutduration) se agrega a **lockoutTime** y se compara con la fecha y hora actuales para determinar si la cuenta está bloqueada.                                                                                                                                |
| El usuario debe cambiar la contraseña en el siguiente inicio de sesión | [**pwdLastSet**](/windows/desktop/ADSchema/a-pwdlastset)                                                         | Sin comentarios.                                                                                                                                                                                                                                                                                                                                                                             |
| El usuario no puede cambiar la contraseña             | N/D                                                                                             | Este es el control Cambiar contraseña de la ACL.                                                                                                                                                                                                                                                                                                                                         |
| Otras opciones de cuenta                   | [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)                                         | Los elementos restantes de Opciones de cuenta alternan bits en la máscara de bits del atributo [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) (marcas en una DWORD).                                                                                                                                                                                                                                 |
| La cuenta expira                         | [**accountExpires**](/windows/desktop/ADSchema/a-accountexpires)                                                 | El **control Expiración de** la cuenta muestra la fecha en que la cuenta expirará al final. El [**atributo accountExpires**](/windows/desktop/ADSchema/a-accountexpires) se almacena como la fecha en que expira la cuenta. Por este problema, la fecha que se muestra en el control **Account Expires** se mostrará como un día anterior a la fecha contenida en el atributo **accountExpires.** |



 

## <a name="address-property-page"></a>Página de propiedades Address

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de la **página de** propiedades Dirección.



| Etiqueta de interfaz de usuario        | Atributo en Active Directory Domain Services                                                 | Comentario                                                   |
|-----------------|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| Calle          | [**streetAddress**](/windows/desktop/ADSchema/a-streetaddress)                                                 | Sin comentarios.                                               |
| P.o.box         | [**postOfficeBox**](/windows/desktop/ADSchema/a-postofficebox)                                                 | Sin comentarios.                                               |
| City (Ciudad)            | [**L**](/windows/desktop/ADSchema/a-l)                                                                         | El nombre del atributo **l** es una "L" minúscula como en Configuración regional. |
| Estado o provincia  | [**St**](/windows/desktop/ADSchema/a-st)                                                                       | Sin comentarios.                                               |
| Código postal | [**postalCode**](/windows/desktop/ADSchema/a-postalcode)                                                       | Sin comentarios.                                               |
| País/región  | [**c,**](/windows/desktop/ADSchema/a-c) [**co**](/windows/desktop/ADSchema/a-co)y [**countryCode**](/windows/desktop/ADSchema/a-countrycode) | Sin comentarios.                                               |



 

## <a name="member-of-property-page"></a>Miembro de la página de propiedades

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario **de la página de** propiedades Miembro de .



| Etiqueta de interfaz de usuario          | Atributo en Active Directory Domain Services   | Comentario                                                                                                                                                                    |
|-------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Miembro de         | [**Miembro**](/windows/desktop/ADSchema/a-memberof)             | Incluye todos los grupos de la lista de interfaz de usuario, excepto el grupo principal, que se representa en AD a través del [**atributo primaryGroupId.**](/windows/desktop/ADSchema/a-primarygroupid) |
| Establecer grupo principal | [**primaryGroupId**](/windows/desktop/ADSchema/a-primarygroupid) | LDAP: asociado a [**primaryGroupToken**](/windows/desktop/ADSchema/a-primarygrouptoken) del grupo principal.                                                                                  |



 

## <a name="organization-property-page"></a>Página de propiedades de la organización

En la tabla siguiente se muestran las etiquetas de interfaz de usuario de **la página de** propiedades Organización.



| Etiqueta de interfaz de usuario       | Atributo en Active Directory Domain Services | Comentario     |
|----------------|-----------------------------------------------|-------------|
| Título          | [**Título**](/windows/desktop/ADSchema/a-title)                 | Sin comentarios. |
| Departamento     | [**Departamento**](/windows/desktop/ADSchema/a-department)       | Sin comentarios. |
| Compañía        | [**Empresa**](/windows/desktop/ADSchema/a-company)             | Sin comentarios. |
| Manager:Name   | [**manager**](/windows/desktop/ADSchema/a-manager)             | Sin comentarios. |
| Informes directos | [**directReports**](/windows/desktop/ADSchema/a-directreports) | Sin comentarios. |



 

## <a name="profile-property-page"></a>Página de propiedades perfil

En la tabla siguiente se enumeran las etiquetas de interfaz de usuario de la **página de** propiedades Perfil.



| Etiqueta de interfaz de usuario                | Atributo en Active Directory Domain Services | Comentario                                                                                                                 |
|-------------------------|-----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Ruta de acceso al perfil            | [**profilePath**](/windows/desktop/ADSchema/a-profilepath)     | Sin comentarios.                                                                                                             |
| Script de inicio de sesión            | [**scriptPath**](/windows/desktop/ADSchema/a-scriptpath)       | Sin comentarios.                                                                                                             |
| Carpeta principal: ruta de acceso local | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Si **se selecciona Ruta de** acceso local, la ruta de acceso local se almacena en el atributo [**homeDirectory.**](/windows/desktop/ADSchema/a-homedirectory) |
| Carpeta principal: Conectar    | [**homeDrive**](/windows/desktop/ADSchema/a-homedrive)         | Si **Conectar** está seleccionada, la unidad asignada se almacena en el [**atributo homeDrive.**](/windows/desktop/ADSchema/a-homedrive)          |
| Carpeta principal: a         | [**homeDirectory**](/windows/desktop/ADSchema/a-homedirectory) | Si **Conectar** está seleccionada, la ruta de acceso se almacena en el [**atributo homeDirectory.**](/windows/desktop/ADSchema/a-homedirectory)          |



 

## <a name="telephones-property-page"></a>Página de propiedades Teléfonos

En la tabla siguiente se enumeran los elementos de la interfaz de usuario de **la página de propiedades Telephones** y sus atributos Active Directory correspondientes.



| Etiqueta de interfaz de usuario        | Atributo en Active Directory Domain Services                                 |
|-----------------|-------------------------------------------------------------------------------|
| Página principal            | [**homePhone**](/windows/desktop/ADSchema/a-homephone)                                         |
| Inicio: Otros     | [**otherHomePhone**](/windows/desktop/ADSchema/a-otherhomephone)                               |
| Buscapersonas           | [**Buscapersonas**](/windows/desktop/ADSchema/a-pager)                                                 |
| Paginador: Otros    | [**otherPager**](/windows/desktop/ADSchema/a-otherpager)                                       |
| Móvil          | [**Móvil**](/windows/desktop/ADSchema/a-mobile)                                               |
| Móvil: otros   | [**otherMobile**](/windows/desktop/ADSchema/a-othermobile)                                     |
| Fax             | [**facsimileTelephoneNumber**](/windows/desktop/ADSchema/a-facsimiletelephonenumber)           |
| Fax: Otros      | [**otherFacsimileTelephoneNumber**](/windows/desktop/ADSchema/a-otherfacsimiletelephonenumber) |
| Teléfono IP        | [**ipPhone**](/windows/desktop/ADSchema/a-ipphone)                                             |
| Teléfono IP: Otros | [**otherIpPhone**](/windows/desktop/ADSchema/a-otheripphone)                                   |
| Notas           | [**Información**](/windows/desktop/ADSchema/a-info)                                                   |



 

## <a name="environment-sessions-remote-control-and-terminal-services-profile-property-pages"></a>Páginas de propiedades de entorno, sesiones, control remoto y perfil de Terminal Services

Las **páginas Entorno**, **Sesiones,** **Control remoto** y Perfil de Terminal **Services** se proporcionan para que un objeto de usuario admita terminal services. Los elementos de la interfaz de usuario de estas páginas no se corresponden con atributos individuales. En su lugar, la configuración se almacena en datos privados dentro de Active Directory Domain Services. Se puede acceder a la configuración de terminal Services con la [**interfaz IADsTsUserEx.**](/windows/desktop/api/tsuserex/nn-tsuserex-iadstsuserex)

 

 