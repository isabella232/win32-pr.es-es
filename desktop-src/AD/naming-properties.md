---
title: Atributos de nomenclatura de usuario
description: Los atributos de nomenclatura de usuario identifican objetos de usuario, como nombres de inicio de sesión e id. usados con fines de seguridad.
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Atributos de nomenclatura de usuario AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8548178bba8012231a803d476699e8ebb386b6fa9a29015f3721e7b32d94158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118185935"
---
# <a name="user-naming-attributes"></a>Atributos de nomenclatura de usuario

Los atributos de nomenclatura de usuario identifican objetos de usuario, como nombres de inicio de sesión e id. usados con fines de seguridad. Los **atributos cn**, **name** y **distinguishedName** son ejemplos de atributos de nomenclatura de usuario. Un objeto de usuario es un objeto de entidad de seguridad, por lo que también incluye los siguientes atributos de nomenclatura de usuario:

-   [userPrincipalName:](#userprincipalname) el nombre de inicio de sesión del usuario
-   [objectGUID:](#objectguid) identificador único de un usuario
-   [sAMAccountName:](#samaccountname) un nombre de inicio de sesión que admite la versión anterior de Windows
-   [objectSid:](#objectsid) identificador de seguridad (SID) del usuario
-   [sIDHistory:](#sidhistory) los SID anteriores del objeto de usuario

> [!Note]  
> Puede ver y administrar estos atributos mediante el complemento MMC Active Directory Usuarios y equipos, que está disponible en el Herramientas de administración remota del servidor [(RSAT).](https://www.microsoft.com/download/details.aspx?id=45520)

 

## <a name="userprincipalname"></a>userPrincipalName

El **atributo userPrincipalName** es el nombre de inicio de sesión del usuario. El atributo consta de un nombre principal de usuario (UPN), que es el nombre de inicio de sesión más común para Windows usuarios. Normalmente, los usuarios usan su UPN para iniciar sesión en un dominio. Este atributo es una cadena indizada con un solo valor.

Un UPN es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet RFC 822. El UPN es más corto que un nombre distintivo y es más fácil de recordar. Por convención, se debe asignar al nombre de correo electrónico del usuario. El punto del UPN es consolidar los espacios de nombres de correo electrónico y de inicio de sesión para que el usuario solo necesite recordar un nombre único.

### <a name="upn-format"></a>Formato UPN

Un UPN consta de un prefijo de UPN (el nombre de la cuenta de usuario) y un sufijo de UPN (un nombre de dominio DNS). El prefijo se une con el sufijo mediante el símbolo \"\@\". Por ejemplo, "someone@ example.com". Un UPN debe ser único entre todos los objetos de entidad de seguridad dentro de un bosque de directorio. Esto significa que el prefijo de un UPN se puede reutilizar, pero no con el mismo sufijo.

Un sufijo UPN tiene las restricciones siguientes:

-   Debe ser el nombre DNS de un dominio, pero no es necesario que sea el nombre del dominio que contiene el usuario.
-   Debe ser el nombre de un dominio en el bosque de dominio actual o un nombre alternativo enumerado en el atributo **upnSuffixes** del contenedor Partitions dentro del contenedor Configuration.

### <a name="upn-management"></a>Administración de UPN

Se puede asignar un UPN, pero no es necesario, cuando se crea una cuenta de usuario. Cuando se crea un UPN, no se ven afectados por los cambios en otros atributos del objeto de usuario, como el usuario al que se va a cambiar el nombre o al que se va a mover. Esto permite al usuario mantener el mismo nombre de inicio de sesión si se reestructura un directorio. Sin embargo, un administrador puede cambiar un UPN. Al crear un nuevo objeto de usuario, debe comprobar el dominio local y el catálogo global para el nombre propuesto para asegurarse de que aún no existe.

Cuando un usuario usa un UPN para iniciar sesión en un dominio, el UPN se valida buscando en el dominio local y, a continuación, en el catálogo global. Si el UPN no se encuentra en el catálogo global, se produce un error en el intento de inicio de sesión.

## <a name="objectguid"></a>objectGUID

El **atributo objectGUID** es el identificador único de un usuario. El atributo es un identificador único global (GUID) de 128 bits con un solo valor y se almacena como una estructura [**\_ ADS OCTET \_ STRING.**](/windows/win32/api/iads/ns-iads-ads_octet_string) El GUID lo crea el Active Directory cuando se crea un objeto de usuario.

Dado que el nombre distintivo de un objeto cambia si se cambia el nombre del objeto o se mueve, el nombre distintivo no es un identificador confiable de un objeto. En Active Directory Domain Services, el atributo **objectGUID** de un objeto nunca cambia, incluso si se cambia el nombre del objeto o se mueve. Puede recuperar el formato de cadena de **objectGUID** mediante el método de propiedad **GUID** en [Métodos de propiedad IADs](/windows/desktop/ADSI/iads-property-methods).

## <a name="samaccountname"></a>sAMAccountName

El atributo **sAMAccountName** es un nombre de inicio de sesión que se usa para admitir clientes y servidores de la versión anterior de Windows, como Windows NT 4.0, Windows 95, Windows 98 y LAN Manager. El nombre de inicio de sesión debe tener 20 caracteres o menos y ser único entre todos los objetos de entidad de seguridad del dominio.

## <a name="objectsid"></a>objectSid

El **atributo objectSid** es el identificador de seguridad (SID) del usuario. El sistema usa el SID para identificar un usuario y sus pertenencias a grupos durante las interacciones con Windows seguridad. El atributo es de un solo valor. El SID es un valor binario único que se usa para identificar al usuario como una entidad de seguridad.

El sistema establece el SID cuando se crea el usuario. Cada usuario tiene un SID único emitido por un Windows y almacenado en el **atributo objectSid** del objeto de usuario en el directorio. Cada vez que un usuario inicia sesión, el sistema recupera el SID del usuario del directorio y lo coloca en el token de acceso del usuario. El SID del usuario también se usa para recuperar los SID de los grupos de los que el usuario es miembro y los coloca en el token de acceso del usuario. Cuando se ha usado un SID como identificador único de un usuario o grupo, no se puede usar de nuevo para identificar a otro usuario o grupo.

## <a name="sidhistory"></a>Sidhistory

El **atributo sIDHistory** contiene los SID anteriores para el objeto de usuario. Se trata de un atributo de varios valores. Un objeto de usuario tiene SID anteriores si el usuario se movió a otro dominio. Cada vez que se mueve un objeto de usuario a un nuevo dominio, se crea un nuevo SID y se le asigna el atributo **objectSid,** y el SID anterior se agrega al atributo **sIDHistory.**

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de objeto de usuario](user-object-attributes.md)
</dt> </dl>

 

 