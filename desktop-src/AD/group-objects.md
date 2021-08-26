---
title: Objetos de grupo
description: Un grupo se representa como un objeto de grupo en Active Directory Domain Services.
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15de5c1577e6c4b0ca738c0f17ea5453020987d9
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469942"
---
# <a name="group-objects"></a>Objetos de grupo

Un grupo se representa como un [**objeto de**](/windows/desktop/ADSchema/c-group) grupo en Active Directory Domain Services. En la tabla siguiente se enumeran los atributos importantes del **objeto de** grupo.




| Atributo | Descripción | 
|-----------|-------------|
| <strong>Cn</strong> | Cn <strong></strong> (o Common-Name) es un atributo de un solo valor que es el nombre distintivo relativo del objeto. Cn <strong>es</strong> el nombre del grupo en Active Directory Domain Services. Al igual que con todos los demás objetos, el <strong>cn</strong> de un grupo debe ser único entre los objetos relacionados del contenedor que contiene el grupo.<br /> | 
| <strong>miembro</strong> | El <strong>atributo</strong> miembro es un atributo de varios valores que contiene la lista de nombres distintivos para los objetos de usuario, grupo y contacto que son miembros del grupo. Cada elemento de la lista es una referencia vinculada al objeto que representa el miembro; por lo tanto, Active Directory servidor actualiza automáticamente los nombres distintivos de la propiedad miembro cuando se mueve o se cambia el nombre de un objeto miembro.<br /> | 
| <strong>groupType</strong> | El <strong>atributo groupType</strong> es un atributo de un solo valor que es un entero que especifica el tipo de grupo y el ámbito mediante las siguientes marcas de bits:<ul><li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li><li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li></ul><br /> Las tres primeras marcas especifican el ámbito del grupo. La <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong> indica el tipo de grupo. Si se establece esta marca, el grupo es un grupo de seguridad. Si no se establece esta marca, el grupo es un grupo de distribución. Para obtener más información, vea <a href="#group-types">Tipos de grupo.</a><br /> | 
| <strong>Miembro</strong> | El <strong>atributo memberOf</strong> es un atributo de varios valores que contiene la lista de nombres distintivos para los grupos que contienen el grupo como miembro. Este atributo enumera los grupos bajo los que el grupo está anidado directamente no contiene la lista recursiva de predecesores anidados. Por ejemplo, si el grupo D estuviera anidado en el grupo C y el grupo B y el grupo B estuvieran anidados en el grupo A, el atributo <strong>memberOf</strong> del grupo D enumeraría el grupo C y el grupo B, pero no el grupo A.<br /> | 
| <strong>objectGUID</strong> | El <strong>atributo objectGUID</strong> es un atributo de un solo valor que es el identificador único del objeto. Este atributo es un identificador único global (GUID). Cuando se crea un objeto en el directorio , el servidor Active Directory genera un GUID y lo asigna al atributo <strong>objectGUID del</strong> objeto. El GUID es único en toda la empresa y en cualquier otro lugar.<br /> <strong>ObjectGUID es</strong> una estructura GUID de 128 bits almacenada como OctetString.<br /> | 
| <strong>objectSid</strong> | El <strong>atributo objectSid</strong> es un atributo de un solo valor que especifica el identificador de seguridad (SID) del grupo. El SID es un valor único que se usa para identificar el grupo como una entidad de seguridad. Es un valor binario que el sistema establece cuando se crea el grupo.<br /> Cada grupo tiene un SID único que el dominio de Windows NT/Windows 2000 Server se almacena en el atributo <strong>objectSid</strong> del objeto de grupo en el directorio. Cada vez que un usuario inicia sesión, el sistema recupera el SID de los grupos de los que el usuario es miembro y lo coloca en el token de acceso del usuario. El sistema usa los SID del token de acceso del usuario para identificar al usuario y sus pertenencias a grupos en todas las interacciones posteriores con la seguridad de Windows NT/Windows 2000.<br /> Cuando se ha usado un SID como identificador único de un usuario o grupo, no se puede volver a usar para identificar a otro usuario o grupo.<br /> | 
| <strong>sAMAccountName</strong> | El atributo <strong>sAMAccountName</strong> es un atributo de un solo valor que es el nombre de inicio de sesión que se usa para admitir clientes y servidores de una versión anterior (Windows 95, Windows 98 y LAN Manager). <strong>SAMAccountName</strong> debe tener menos de 20 caracteres para admitir clientes y servidores de una versión anterior.<br /> <strong>sAMAccountName</strong> debe ser único entre todos los objetos de entidad de seguridad dentro de un dominio.<br /> | 




 

## <a name="group-types"></a>Tipos de grupo

Hay dos tipos de grupos definidos por Active Directory Domain Services, *Grupos de seguridad* y Grupos de *distribución*.

Un grupo de seguridad proporciona una agrupación lógica de objetos y el propio grupo se puede usar como entidad de seguridad en una lista de Access Control (ACL). Cuando un grupo de seguridad tiene acceso a un objeto, todos los miembros del grupo de seguridad reciben automáticamente el mismo acceso al objeto. Los grupos de seguridad con ámbito universal también se pueden usar como una entidad de correo electrónico. El envío de un mensaje de correo electrónico a un grupo de seguridad universal envía el mensaje a todos los miembros del grupo.

Un grupo de distribución también proporciona una agrupación lógica de objetos, pero no puede proporcionar privilegios de acceso. Los grupos de distribución no están habilitados para la seguridad y no se pueden usar como entidad de seguridad en una ACL. Los grupos de distribución solo se usan con fines de agrupación. Por ejemplo, las listas de distribución se pueden usar con aplicaciones de correo electrónico, como Exchange, para enviar correo electrónico a una colección de usuarios.

Para obtener más información sobre los tipos de grupo Active Directory Domain Services, vea el [tema Tipos de](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10)) grupo en Microsoft [TechNet](https://technet.microsoft.com/default.aspx).

## <a name="group-scope"></a>Ámbito de grupo

Hay tres ámbitos de grupo definidos por Active Directory Domain Services, *Universal*, *Global* *y Domain Local*. El ámbito del grupo define los tipos de objeto que pueden pertenecer al grupo, los tipos de grupos de los que el grupo puede ser miembro y el ámbito de los objetos a los que se puede dar acceso a los grupos de seguridad. Cuando el nivel funcional del dominio se establece Windows modo mixto 2000, no se pueden crear grupos de seguridad con ámbito universal.

En la tabla siguiente se enumeran los tres ámbitos de grupo y más información sobre cada ámbito de un grupo de seguridad.

| Ámbito                   | Posibles miembros                                                                                                                                                                                                                                      | Conversión de ámbito                                                                                                                                                 | Puede conceder permisos                                                       | Posible miembro de                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Universal<br/>    | Cuentas de cualquier dominio del mismo bosque.<br/> Grupos globales de cualquier dominio del mismo bosque.<br/> Otros grupos universales de cualquier dominio del mismo bosque.<br/>                                                            | Se puede convertir al ámbito local del dominio.<br/> Se puede convertir al ámbito global siempre y cuando el grupo no contenga ningún otro grupo universal.<br/> | En cualquier dominio del mismo bosque o bosques de confianza.<br/>            | Otros grupos universales del mismo bosque.<br/> Grupos locales de dominio en el mismo bosque o bosques de confianza.<br/> Grupos locales en máquinas del mismo bosque o bosques de confianza.<br/>            |
| Global<br/>       | Cuentas del mismo dominio.<br/> Otros grupos globales del mismo dominio.<br/>                                                                                                                                                        | Se puede convertir al ámbito universal siempre que el grupo no sea miembro de ningún otro grupo global.<br/>                                                   | En cualquier dominio del mismo bosque o dominios o bosques de confianza.<br/> | Grupos universales de cualquier dominio del mismo bosque.<br/> Otros grupos globales del mismo dominio.<br/> Grupos locales de dominio de cualquier dominio del mismo bosque o de cualquier dominio de confianza.<br/> |
| Dominio local<br/> | Cuentas de cualquier dominio o de cualquier dominio de confianza.<br/> Grupos globales de cualquier dominio o de cualquier dominio de confianza.<br/> Grupos universales de cualquier dominio del mismo bosque.<br/> Otros grupos locales de dominio del mismo dominio.<br/> | Se puede convertir al ámbito universal siempre y cuando el grupo no contenga ningún otro grupo local de dominio.<br/>                                              | Dentro del mismo dominio.<br/>                                          | Otros grupos locales de dominio del mismo dominio.<br/> Grupos locales en máquinas del mismo dominio, excepto los grupos integrados que tienen SID conocidos.<br/>                                             |



 

 

