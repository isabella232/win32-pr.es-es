---
title: Qué necesitan saber los desarrolladores de aplicaciones y servicios sobre los grupos
description: Al desarrollar una aplicación o un servicio, puede usar grupos para delegar la administración o controlar el acceso a la aplicación o servicio en su totalidad o parte.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Qué necesitan saber los desarrolladores de aplicaciones y servicios sobre los grupos
- groups AD , información para desarrolladores de aplicaciones y servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b59a8a1ce369d9b5fa1093297f219bf6a206178a950b9d0762fde3069846551
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024402"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Qué necesitan saber los desarrolladores de aplicaciones y servicios sobre los grupos

Al desarrollar una aplicación o un servicio, puede usar grupos para delegar la administración o controlar el acceso a la aplicación o servicio en su totalidad o parte. Por ejemplo, una aplicación puede controlar quién puede realizar varias operaciones administrativas. Para ello, cree AEE que concedan derechos de acceso especificados a los grupos adecuados. Es una buena práctica de programación tener una ACE que conceda acceso a un grupo que tener varias ACE que concedan acceso a usuarios o equipos individuales.

Se recomienda que las aplicaciones usen las siguientes directrices al usar grupos:

-   No cree dependencias en grupos codificados de forma permanente, lo que puede crear complicaciones si el grupo se elimina o se mueve.
-   Evite el uso de grupos integrados a menos que la función del grupo proporciona las necesidades específicas de la aplicación. Por ejemplo, no es necesario que un usuario sea miembro del grupo Administradores solo para proporcionar al usuario permiso para crear una cuenta de equipo. Esto proporciona al usuario permisos y privilegios que puede que no necesite, lo que puede provocar una vulnerabilidad de seguridad. En su lugar, debe crear un nuevo grupo de seguridad que tenga los permisos específicos necesarios y agregar el usuario a este nuevo grupo.
-   Al crear nuevos grupos, tenga en cuenta las siguientes recomendaciones:
    -   Proteja el grupo estableciendo AEE que controlan quién puede agregar o quitar miembros.
    -   Use grupos globales si se usan para el control de acceso en objetos de Active Directory Domain Services.
    -   Use grupos universales solo si es necesario (los datos de miembro se requieren globalmente mediante el catálogo global; el grupo puede contener cualquier usuario o grupo). Si usa grupos universales, coloque los grupos globales en el grupo universal y agregue o quite usuarios del grupo global. Evite el cambio excesivo en los grupos universales para mejorar la eficacia de la replicación.
-   No use la pertenencia a grupos para el control de acceso. En su lugar, use una ACE y controle el acceso haciendo que el sistema realice una comprobación de acceso.

Para controlar el acceso a las operaciones que no se ajustan a los derechos de acceso predefinidos para los objetos de los servicios de Dominio de Active Directory, use la característica de derechos de acceso de control del control de acceso en Windows 2000. Para obtener más información, vea [**ADS \_ RIGHTS \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**Para usar un derecho de acceso de control para controlar el derecho a realizar una operación**

1.  Cree un derecho de acceso de control que defina el tipo de acceso a la aplicación o servicio. Para obtener más información, vea [Controlar los derechos de acceso.](control-access-rights.md)
2.  Cree un objeto en Active Directory Domain Services que represente la aplicación, el servicio o el recurso.
3.  Agregue A ACE de objeto a la DACL en el descriptor de seguridad de objetos para conceder o denegar a los usuarios o grupos el derecho de acceso de control en ese objeto. Para obtener más información, vea [Establecer los derechos de acceso en un objeto](setting-access-rights-on-an-object.md).
4.  Cuando un usuario intenta realizar la operación protegida, la aplicación o el servicio usa la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar si se concede al usuario el derecho de acceso de control. Para obtener más información, vea [Comprobar un derecho de acceso de control en la ACL de un objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  En función del resultado de la comprobación de acceso en el objeto, la aplicación o el servicio pueden conceder o denegar al usuario acceso a la aplicación o servicio.

Una aplicación de servicio también podría crear un grupo cuyos miembros serían las distintas instancias de servicio. Por ejemplo, un servicio con instancias instaladas en varios equipos de una empresa podría tener un archivo de registro común en el que todas las instancias de servicio escriben. El programa de instalación del servicio crea el archivo de registro y usa una DACL para conceder acceso solo a los miembros de un grupo. Los miembros del grupo serían las cuentas de usuario con las que se ejecutan las distintas instancias de servicio, o si los servicios se ejecutan en la cuenta LocalSystem, los miembros serían las cuentas de equipo de los servidores host.

 

 