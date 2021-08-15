---
title: Cómo afecta la seguridad a las operaciones Active Directory Domain Services
description: Active Directory Domain Services control de acceso para conceder o denegar el acceso a objetos, propiedades y operaciones en función de la identidad del usuario que realiza el intento de acceso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Efectos de seguridad en Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d8f5599afbc8552f9708fcfa953a069f429a152c4f0fff37546ffb7d9f6b809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118188210"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Cómo afecta la seguridad a las operaciones Active Directory Domain Services

Active Directory Domain Services control de acceso para conceder o denegar el acceso a objetos, propiedades y operaciones en función de la identidad del usuario que realiza el intento de acceso. Cuando la aplicación se enlaza al directorio, se enlaza con credenciales de usuario específicas. Cuando se autentican, estas credenciales determinan el contexto de seguridad de la aplicación. Independientemente de si las credenciales son las del usuario que ha iniciado sesión, un usuario especificado, una cuenta de servicio, una cuenta de equipo o un usuario no autenticado (invitado o todos), el servidor Active Directory comprueba el derecho del usuario a acceder a un objeto antes de realizar cualquier operación en ese objeto. El usuario puede, o no, tener acceso a un objeto determinado, sus secundarios, sus propiedades u operaciones en ese objeto, lo que significa que la aplicación debe controlar los posibles errores causados por el acceso denegado.

Para obtener más información sobre los contextos de seguridad y los efectos del control de acceso en varias operaciones, consulte:

-   [Access Control y operaciones de lectura](access-control-and-read-operations.md)
-   [Access Control y operaciones de escritura](access-control-and-write-operations.md)
-   [Access Control y creación de objetos](access-control-and-object-creation.md)
-   [Access Control y eliminación de objetos](access-control-and-object-deletion.md)

 

 




