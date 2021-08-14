---
title: Cómo se usan los grupos de seguridad en Access Control
description: El identificador de seguridad (SID) es el identificador de objeto del usuario o grupo de seguridad cuando el usuario o grupo se usa con fines de seguridad.
ms.assetid: 3236c51f-21c1-4c07-9b76-2668ae72a42f
ms.tgt_platform: multiple
keywords:
- Cómo se usan los grupos de seguridad en Access Control
- control de acceso, grupos de seguridad usados en
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e8e14d4d8c371d07619d93f4a6d06318f91e7ec011a4c4fe6d436074ac8ff94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188136"
---
# <a name="how-security-groups-are-used-in-access-control"></a>Cómo se usan los grupos de seguridad en Access Control

El identificador de seguridad (SID) es el identificador de objeto del usuario o grupo de seguridad cuando el usuario o grupo se usa con fines de seguridad. El nombre del usuario o grupo no se usa como identificador único dentro del sistema. El SID se almacena en el atributo **objectSid** de objetos de usuario y objetos de grupo de seguridad. El Active Directory genera el **objectSid** cuando se crea el usuario o grupo. El sistema garantiza que los SID son únicos en un bosque. Tenga en cuenta que **objectGuid** es el identificador único de un usuario, grupo o cualquier otro objeto de directorio. El SID cambia si un usuario o grupo se mueve a otro dominio; **objectGuid** sigue siendo el mismo.

Cuando se concede permiso a un usuario o grupo para acceder a un recurso, como una impresora o un recurso compartido de archivos, el SID del usuario o grupo se agrega a la entrada de control de acceso (ACE) que define el permiso concedido en la lista de control de acceso discrecional (DACL) del recurso. En Active Directory Domain Services, cada objeto tiene un atributo **nTSecurityDescriptor** que almacena una DACL que define el acceso a ese objeto o atributos concretos en ese objeto. Para obtener más información sobre cómo establecer el control de acceso en objetos de Active Directory Domain Services, vea Controlar el acceso a [objetos en Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).

Cuando un usuario inicia sesión en un dominio Windows 2000, el sistema operativo genera un token de acceso. Este token de acceso se usa para determinar a qué recursos puede acceder el usuario. El token de acceso de usuario incluye los datos siguientes:

-   SID de usuario.
-   SID de todos los grupos de seguridad globales y universales de los que el usuario es miembro.
-   SID de todos los grupos de seguridad globales y universales anidados.

Cada proceso ejecutado en nombre de este usuario tiene una copia de este token de acceso.

Cuando el usuario intenta acceder a los recursos de un equipo, el servicio a través del cual el usuario accede al recurso suplanta al usuario mediante la creación de un nuevo token de acceso basado en el token de acceso creado en el momento del inicio de sesión del usuario. Este nuevo token de acceso también contendrá los siguientes SID:

-   SID para todos los grupos locales de dominio del dominio de destino del que el usuario es miembro.
-   SID para todos los grupos locales de la máquina en el equipo de destino del que el usuario es miembro.

El servicio usa este nuevo token de acceso para evaluar el acceso al recurso. Si aparece un SID en el token de acceso en cualquier ACE de la DACL, el servicio concede al usuario los permisos especificados en esas ACE.

 

 




