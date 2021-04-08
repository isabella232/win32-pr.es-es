---
title: Objetos de grupo
description: Un grupo se representa como un objeto de grupo en Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a935d2a44d3350d8c24ca3bdb388f0a4bd8f16ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103995081"
---
# <a name="group-objects"></a>Objetos de grupo

Un grupo se representa como un objeto de [**Grupo**](/windows/desktop/ADSchema/c-group) en Active Directory Domain Services. En la tabla siguiente se enumeran los atributos importantes del objeto **Group** .



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>CN</strong></td>
<td>El <strong>CN</strong> (o nombre común) es un atributo de un solo valor que es el nombre distintivo relativo del objeto. El <strong>CN</strong> es el nombre del grupo en Active Directory Domain Services. Como con todos los demás objetos, el <strong>CN</strong> de un grupo debe ser único entre los objetos relacionados en el contenedor que contiene el grupo.<br/></td>
</tr>
<tr class="even">
<td><strong>miembro</strong></td>
<td>El atributo <strong>member</strong> es un atributo de varios valores que contiene la lista de nombres distintivos de los objetos user, Group y Contact que son miembros del grupo. Cada elemento de la lista es una referencia vinculada al objeto que representa el miembro; por lo tanto, el servidor de Active Directory actualiza automáticamente los nombres distintivos de la propiedad de miembro cuando se mueve o se cambia el nombre de un objeto de miembro.<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td>El atributo <strong>GroupType</strong> es un atributo de un solo valor que es un entero que especifica el tipo y el ámbito de grupo mediante las siguientes marcas de bits:
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> Las tres primeras marcas especifican el ámbito de grupo. La marca <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> indica el tipo de grupo. Si se establece esta marca, el grupo es un grupo de seguridad. Si no se establece esta marca, el grupo es un grupo de distribución. Para obtener más información, vea <a href="#group-types">tipos de grupo</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td>El atributo <strong>memberOf</strong> es un atributo de varios valores que contiene la lista de nombres distintivos de los grupos que contienen el grupo como miembro. Este atributo muestra los grupos bajo los que el grupo está anidado directamente y no contiene la lista recursiva de predecesoras anidadas. Por ejemplo, si el grupo D estuviese anidado en el grupo C y el grupo b y el grupo B estuviesen anidados en el grupo A, el atributo <strong>memberOf</strong> del grupo D mostraría el grupo C y el grupo b, pero no el grupo a.<br/></td>
</tr>
<tr class="odd">
<td><strong>GUID</strong></td>
<td>El atributo <strong>objectGUID</strong> es un atributo de un solo valor que es el identificador único para el objeto. Este atributo es un identificador único global (GUID). Cuando se crea un objeto en el directorio, el servidor de Active Directory genera un GUID y lo asigna al atributo <strong>objectGUID</strong> del objeto. El GUID es único en toda la empresa y en cualquier otra parte.<br/> <strong>ObjectGUID</strong> es una estructura de GUID de 128 bits almacenada como OctetString.<br/></td>
</tr>
<tr class="even">
<td><strong>objectSid</strong></td>
<td>El atributo <strong>objectSid</strong> es un atributo de un solo valor que especifica el identificador de seguridad (SID) del grupo. El SID es un valor único que se usa para identificar el grupo como entidad de seguridad. Es un valor binario que el sistema establece cuando se crea el grupo.<br/> Cada grupo tiene un SID único que emite el dominio del servidor de Windows NT/Windows 2000 y que se almacena en el atributo <strong>objectSid</strong> del objeto de grupo en el directorio. Cada vez que un usuario inicia sesión, el sistema recupera el SID de los grupos de los que el usuario es miembro y lo coloca en el token de acceso del usuario. El sistema utiliza los SID en el token de acceso del usuario para identificar al usuario y a su pertenencia a grupos en todas las interacciones posteriores con la seguridad de Windows NT/Windows 2000.<br/> Cuando se ha usado un SID como identificador único para un usuario o grupo, no se puede usar de nuevo para identificar a otro usuario o grupo.<br/></td>
</tr>
<tr class="odd">
<td><strong>Atributo</strong></td>
<td>El atributo <strong>samAccountName</strong> es un atributo de un solo valor que es el nombre de inicio de sesión que se usa para admitir clientes y servidores de una versión anterior (Windows 95, Windows 98 y LAN Manager). <strong>SamAccountName</strong> debe tener menos de 20 caracteres para admitir clientes y servidores de una versión anterior.<br/> <strong>SamAccountName</strong> debe ser único entre todos los objetos de entidad de seguridad dentro de un dominio.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>Tipos de grupo

Hay dos tipos de grupos definidos por Active Directory Domain Services, *grupos de seguridad* y *grupos de distribución*.

Un grupo de seguridad proporciona una agrupación lógica de objetos y el propio grupo se puede usar como entidad de seguridad en una lista de Access Control (ACL). Cuando a un grupo de seguridad se le concede acceso a un objeto, todos los miembros del grupo de seguridad reciben automáticamente el mismo acceso al objeto. Los grupos de seguridad con ámbito universal también se pueden usar como una entidad de correo electrónico. El envío de un mensaje de correo electrónico a un grupo de seguridad universal envía el mensaje a todos los miembros del grupo.

Un grupo de distribución también proporciona una agrupación lógica de objetos, pero no puede proporcionar ningún privilegio de acceso. Los grupos de distribución no tienen seguridad habilitada y no se pueden usar como entidad de seguridad en una ACL. Los grupos de distribución solo se usan con fines de agrupación. Por ejemplo, las listas de distribución se pueden usar con aplicaciones de correo electrónico, como Exchange, para enviar correo electrónico a una recopilación de usuarios.

Para obtener más información acerca de los tipos de grupo en Active Directory Domain Services, consulte el tema [tipos de grupos](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) en [Microsoft TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Ámbito de grupo

Hay tres ámbitos de grupo definidos por Active Directory Domain Services, *universal*, *global* y *dominio local*. El ámbito del grupo define los tipos de objeto que puede pertenecer al grupo, los tipos de grupos de los que puede ser miembro el grupo y el ámbito de los objetos a los que se puede conceder acceso a los grupos de seguridad. Cuando el nivel funcional del dominio se establece en modo mixto de Windows 2000, no se pueden crear grupos de seguridad con ámbito universal.

En la tabla siguiente se enumeran los tres ámbitos de grupo y más información sobre cada ámbito de un grupo de seguridad.

| Ámbito                   | Miembros posibles                                                                                                                                                                                                                                      | Conversión de ámbito                                                                                                                                                 | Puede conceder permisos                                                       | Miembro posible de                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universal<br/>    | Cuentas de cualquier dominio del mismo bosque.<br/> Grupos globales de cualquier dominio del mismo bosque.<br/> Otros grupos universales de cualquier dominio del mismo bosque.<br/>                                                            | Se puede convertir al ámbito local de dominio.<br/> Se puede convertir en un ámbito global siempre que el grupo no contenga ningún otro grupo universal.<br/> | En cualquier dominio del mismo bosque o con bosques de confianza.<br/>            | Otros grupos universales en el mismo bosque.<br/> Grupos locales de dominio en el mismo bosque o en bosques de confianza.<br/> Grupos locales en equipos en el mismo bosque o en bosques de confianza.<br/>            |
| Global<br/>       | Cuentas del mismo dominio.<br/> Otros grupos globales del mismo dominio.<br/>                                                                                                                                                        | Se puede convertir en el ámbito universal siempre y cuando el grupo no sea miembro de ningún otro grupo global.<br/>                                                   | En cualquier dominio del mismo bosque o dominios de confianza o bosques.<br/> | Grupos universales de cualquier dominio del mismo bosque.<br/> Otros grupos globales del mismo dominio.<br/> Los grupos locales de dominio de cualquier dominio del mismo bosque o de cualquier dominio de confianza.<br/> |
| Dominio local<br/> | Cuentas de cualquier dominio o dominio de confianza.<br/> Grupos globales de cualquier dominio o cualquier dominio de confianza.<br/> Grupos universales de cualquier dominio del mismo bosque.<br/> Otros grupos locales de dominio del mismo dominio.<br/> | Se puede convertir en el ámbito universal siempre y cuando el grupo no contenga otros grupos locales de dominio.<br/>                                              | Dentro del mismo dominio.<br/>                                          | Otros grupos locales de dominio del mismo dominio.<br/> Grupos locales en equipos del mismo dominio, excepto los grupos integrados que tienen SID conocidos.<br/>                                             |



 

 

