---
title: Lo que los desarrolladores de aplicaciones y servicios necesitan saber sobre los grupos
description: Al desarrollar una aplicación o un servicio, puede usar grupos para delegar la administración o controlar el acceso a la aplicación o servicio en su totalidad o en parte.
ms.assetid: 19e189a5-2880-4b45-84c8-e7b542c4fbb6
ms.tgt_platform: multiple
keywords:
- Lo que los desarrolladores de aplicaciones y servicios necesitan saber sobre los grupos
- grupos AD, información para desarrolladores de aplicaciones y servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd23f598925c959502e1013ff43ad18bbb42ed7b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103789436"
---
# <a name="what-application-and-service-developers-need-to-know-about-groups"></a>Lo que los desarrolladores de aplicaciones y servicios necesitan saber sobre los grupos

Al desarrollar una aplicación o un servicio, puede usar grupos para delegar la administración o controlar el acceso a la aplicación o servicio en su totalidad o en parte. Por ejemplo, una aplicación puede controlar quién puede realizar diversas operaciones administrativas. Para ello, cree ACE que concedan los derechos de acceso especificados a los grupos adecuados. Una buena práctica de programación es tener una ACE que conceda acceso a un grupo que tenga varias ACE que concedan acceso a usuarios individuales o equipos.

Se recomienda que las aplicaciones usen las siguientes directrices al usar grupos:

-   No cree dependencias en grupos codificados de forma rígida, lo que puede crear complicaciones si se elimina o se mueve el grupo.
-   Evite el uso de grupos integrados a menos que la función del grupo proporcione las necesidades específicas de la aplicación. Por ejemplo, no es necesario que un usuario sea miembro del grupo administradores solo para proporcionar al usuario permiso para crear una cuenta de equipo. Al hacerlo, se proporciona al usuario permisos y privilegios que es posible que no necesiten, lo que puede provocar vulnerabilidades de seguridad. En su lugar, debe crear un nuevo grupo de seguridad que tenga los permisos específicos necesarios y agregar el usuario a este grupo nuevo.
-   Al crear nuevos grupos, tenga en cuenta las siguientes recomendaciones:
    -   Proteja el grupo estableciendo las ACE que controlan quién puede Agregar o quitar miembros.
    -   Use los grupos globales si se usan para el control de acceso en los objetos de Active Directory Domain Services.
    -   Use grupos universales solo si es necesario (los datos de miembro son necesarios globalmente mediante el catálogo global; el grupo puede contener cualquier usuario o grupo). Si usa grupos universales, coloque los grupos globales en el grupo universal y agregue o quite usuarios del grupo global. Evite el exceso de cambios en los grupos universales para mejorar la eficacia de la replicación.
-   No use la pertenencia a grupos para el control de acceso. En su lugar, use una ACE y controle el acceso haciendo que el sistema realice una comprobación de acceso.

Para controlar el acceso a las operaciones que no se ajustan a los derechos de acceso predefinidos para los objetos de Dominio de Active Directory Services, utilice la característica controlar derechos de acceso de control de acceso en Windows 2000. Para obtener más información, vea [**ADS \_ Rights \_ enum**](/windows/win32/api/iads/ne-iads-ads_rights_enum).

**Para usar un derecho de control de acceso para controlar el derecho a realizar una operación**

1.  Cree un derecho de acceso de control que defina el tipo de acceso a la aplicación o servicio. Para obtener más información, vea [controlar derechos de acceso](control-access-rights.md).
2.  Cree un objeto en Active Directory Domain Services que represente la aplicación, el servicio o el recurso.
3.  Agregue ACE de objeto a la DACL en el descriptor de seguridad de objeto para conceder o denegar a los usuarios o grupos el derecho de acceso de control en ese objeto. Para obtener más información, consulte [configuración de derechos de acceso en un objeto](setting-access-rights-on-an-object.md).
4.  Cuando un usuario intenta realizar la operación protegida, su aplicación o servicio utiliza la función [**AccessCheckByTypeResultList**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) para determinar si se concede al usuario el derecho de acceso de control. Para obtener más información, vea [comprobar un derecho de acceso a un control en la ACL de un objeto](checking-a-control-access-right-in-an-objectampaposs-acl.md).
5.  En función del resultado de la comprobación de acceso en el objeto, la aplicación o el servicio pueden conceder o denegar el acceso del usuario a la aplicación o servicio.

Una aplicación de servicio también podría crear un grupo cuyos miembros serían las distintas instancias de servicio. Por ejemplo, un servicio con instancias instaladas en varios equipos de una empresa puede tener un archivo de registro común en el que se escriben todas las instancias de servicio. El programa de instalación del servicio crea el archivo de registro y utiliza una DACL para conceder acceso solo a los miembros de un grupo. Los miembros del grupo serían las cuentas de usuario en las que se ejecutan las distintas instancias de servicio, o si los servicios se ejecutan con la cuenta LocalSystem, los miembros serían las cuentas de equipo de los servidores host.

 

 