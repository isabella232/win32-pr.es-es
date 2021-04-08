---
title: Atributos de asignación de nombres de usuario
description: Los atributos de asignación de nombres de usuario identifican los objetos de usuario, como los nombres de inicio de sesión y los identificadores usados por motivos de seguridad
ms.assetid: 2192743c-cedd-4b03-a402-3992d64a4801
ms.tgt_platform: multiple
keywords:
- Atributos de asignación de nombres de usuario AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a504070cf2e78cf5647072ff740d137b4a6e6056
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995069"
---
# <a name="user-naming-attributes"></a>Atributos de asignación de nombres de usuario

Los atributos de asignación de nombres de usuario identifican los objetos de usuario, como los nombres de inicio de sesión y los identificadores usados por motivos de seguridad Los atributos **CN**, **Name** y **distinguishedName** son ejemplos de atributos de asignación de nombres de usuario. Un objeto de usuario es un objeto de entidad de seguridad, por lo que también incluye los siguientes atributos de asignación de nombres de usuario:

-   [userPrincipalName](#userprincipalname) : el nombre de inicio de sesión del usuario
-   [objectGUID](#objectguid) : el identificador único de un usuario
-   [samAccountName](#samaccountname) : un nombre de inicio de sesión que admite la versión anterior de Windows
-   [objectSid](#objectsid) : identificador de seguridad (SID) del usuario
-   [SIDHistory](#sidhistory) : los SID anteriores para el objeto de usuario

> [!Note]  
> Puede ver y administrar estos atributos con el complemento MMC Active Directory usuarios y equipos, que está disponible en el [herramientas de administración remota del servidor (RSAT)](https://www.microsoft.com/download/details.aspx?id=45520).

 

## <a name="userprincipalname"></a>userPrincipalName

El atributo **userPrincipalName** es el nombre de inicio de sesión del usuario. El atributo se compone de un nombre principal de usuario (UPN), que es el nombre de inicio de sesión más común para los usuarios de Windows. Los usuarios suelen usar su UPN para iniciar sesión en un dominio. Este atributo es una cadena indizada que tiene un solo valor.

Un UPN es un nombre de inicio de sesión de estilo Internet para un usuario basado en el estándar de Internet RFC 822. El UPN es más corto que un nombre distintivo y más fácil de recordar. Por convención, se debe asignar al nombre de correo electrónico del usuario. El punto del UPN es consolidar el correo electrónico y los espacios de nombres de inicio de sesión para que el usuario solo tenga que recordar un nombre único.

### <a name="upn-format"></a>Formato UPN

Un UPN consta de un prefijo de UPN (el nombre de la cuenta de usuario) y un sufijo de UPN (un nombre de dominio DNS). El prefijo se une con el sufijo mediante el símbolo \"\@\". Por ejemplo, "someone@ example.com". Un UPN debe ser único entre todos los objetos de entidad de seguridad dentro de un bosque de directorio. Esto significa que se puede volver a usar el prefijo de un UPN, no solo con el mismo sufijo.

Un sufijo UPN tiene las siguientes restricciones:

-   Debe ser el nombre DNS de un dominio, pero no es necesario que sea el nombre del dominio que contiene el usuario.
-   Debe ser el nombre de un dominio en el bosque de dominio actual o un nombre alternativo que aparezca en el atributo **upnSuffixes** del contenedor de particiones en el contenedor de configuración.

### <a name="upn-management"></a>Administración de UPN

Se puede asignar un UPN, pero no es necesario cuando se crea una cuenta de usuario. Cuando se crea un UPN, no se ve afectado por los cambios realizados en otros atributos del objeto de usuario como, por ejemplo, el cambio de nombre o la ubicación del usuario. Esto permite al usuario mantener el mismo nombre de inicio de sesión si se reestructura un directorio. Sin embargo, un administrador puede cambiar un UPN. Al crear un nuevo objeto de usuario, debe comprobar el dominio local y el catálogo global del nombre propuesto para asegurarse de que aún no existe.

Cuando un usuario usa un UPN para iniciar sesión en un dominio, el UPN se valida buscando en el dominio local y, a continuación, en el catálogo global. Si no se encuentra el UPN en el catálogo global, se produce un error en el intento de inicio de sesión.

## <a name="objectguid"></a>objectGUID

El atributo **objectGUID** es el identificador único de un usuario. El atributo es un identificador único global (GUID) de 128 bits de valor único y se almacena como una estructura de [**\_ \_ cadenas de octetos de anuncios**](/windows/win32/api/iads/ns-iads-ads_octet_string) . El servidor de Active Directory crea el GUID cuando se crea un objeto de usuario.

Dado que el nombre distintivo de un objeto cambia si se cambia el nombre del objeto o se mueve, el nombre distintivo no es un identificador confiable de un objeto. En Active Directory Domain Services, el atributo **objectGUID** de un objeto nunca cambia, aunque se cambie el nombre del objeto o se mueva. Puede recuperar el formato de cadena de **objectGUID** mediante el método de propiedad **GUID** en [los métodos de propiedad de iAds](/windows/desktop/ADSI/iads-property-methods).

## <a name="samaccountname"></a>sAMAccountName

El atributo **samAccountName** es un nombre de inicio de sesión que se usa para admitir clientes y servidores de la versión anterior de Windows, como windows NT 4,0, Windows 95, Windows 98 y LAN Manager. El nombre de inicio de sesión debe tener 20 caracteres o menos y ser único entre todos los objetos de entidad de seguridad del dominio.

## <a name="objectsid"></a>objectSid

El atributo **objectSid** es el identificador de seguridad (SID) del usuario. El sistema utiliza el SID para identificar a un usuario y su pertenencia a grupos durante las interacciones con la seguridad de Windows. El atributo tiene un solo valor. El SID es un valor binario único que se usa para identificar al usuario como una entidad de seguridad.

El sistema establece el SID cuando se crea el usuario. Cada usuario tiene un SID único emitido por un dominio de Windows y se almacena en el atributo **objectSid** del objeto de usuario en el directorio. Cada vez que un usuario inicia sesión, el sistema recupera el SID del usuario del directorio y lo coloca en el token de acceso del usuario. El SID del usuario también se usa para recuperar los SID de los grupos de los que el usuario es miembro y los coloca en el token de acceso del usuario. Cuando se ha usado un SID como identificador único para un usuario o grupo, no se puede volver a usar para identificar a otro usuario o grupo.

## <a name="sidhistory"></a>Correspondientes

El atributo **SIDHistory** contiene los SID anteriores del objeto de usuario. Se trata de un atributo con varios valores. Un objeto de usuario tiene SID anteriores si el usuario se ha migrado a otro dominio. Cada vez que se mueve un objeto de usuario a un nuevo dominio, se crea un nuevo SID y se le asigna el atributo **objectSid** y se agrega el SID anterior al atributo **SIDHistory** .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Atributos de objeto de usuario](user-object-attributes.md)
</dt> </dl>

 

 