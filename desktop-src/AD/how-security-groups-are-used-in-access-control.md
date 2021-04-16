---
title: Cómo se usan los grupos de seguridad en Access Control
description: El identificador de seguridad (SID) es el identificador de objeto del usuario o grupo de seguridad cuando el usuario o el grupo se utiliza por motivos de seguridad.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Cómo se usan los grupos de seguridad en Access Control
- control de acceso, grupos de seguridad usados en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf7096e32c64fe420ca6625378725ce8e4864beb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105656230"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Cómo se usan los grupos de seguridad en Access Control

El identificador de seguridad (SID) es el identificador de objeto del usuario o grupo de seguridad cuando el usuario o el grupo se utiliza por motivos de seguridad. El nombre del usuario o grupo no se utiliza como identificador único en el sistema. El SID se almacena en el atributo **objectSid** de objetos de usuario y objetos de grupo de seguridad. El servidor de Active Directory genera el **objectSid** cuando se crea el usuario o grupo. El sistema garantiza que los SID son únicos en todo el bosque. Tenga en cuenta que **objectGuid** es el identificador único de un usuario, grupo o cualquier otro objeto de directorio. El SID cambia si un usuario o grupo se mueve a otro dominio; **objectGuid** sigue siendo el mismo.

Cuando a un usuario o grupo se le concede permiso para tener acceso a un recurso, como una impresora o un recurso compartido de archivos, se agrega el SID del usuario o grupo a la entrada de control de acceso (ACE) que define el permiso concedido en la lista de control de acceso discrecional (DACL) del recurso. En Active Directory Domain Services, cada objeto tiene un atributo **nTSecurityDescriptor** que almacena una DACL que define el acceso a ese objeto o atributos concretos en ese objeto. Para obtener más información sobre cómo establecer el control de acceso en los objetos de Active Directory Domain Services, vea [controlar el acceso a objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Cuando un usuario inicia sesión en un dominio de Windows 2000, el sistema operativo genera un token de acceso. Este token de acceso se usa para determinar a qué recursos puede tener acceso el usuario. El token de acceso de usuario incluye los datos siguientes:

-   SID de usuario.
-   SID de todos los grupos de seguridad globales y universales de los que es miembro el usuario.
-   SID de todos los grupos de seguridad globales y universales anidados.

Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

Cuando el usuario intenta obtener acceso a los recursos de un equipo, el servicio a través del cual el usuario tiene acceso al recurso suplantará al usuario mediante la creación de un nuevo token de acceso basado en el token de acceso creado en el momento de inicio de sesión del usuario. Este nuevo token de acceso también contendrá los siguientes SID:

-   SID para todos los grupos locales de dominio del dominio de destino de los que el usuario es miembro.
-   SID para todos los grupos locales de la máquina del equipo de destino de los que el usuario es miembro.

El servicio usa este nuevo token de acceso para evaluar el acceso al recurso. Si aparece un SID en el token de acceso en cualquier ACE de la DACL, el servicio concede al usuario los permisos especificados en esas ACE.

 

 




