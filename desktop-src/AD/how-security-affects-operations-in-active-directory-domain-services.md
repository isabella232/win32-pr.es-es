---
title: Cómo afecta la seguridad a las operaciones en Active Directory Domain Services
description: Active Directory Domain Services usar el control de acceso para conceder o denegar el acceso a objetos, propiedades y operaciones en función de la identidad del usuario que realiza el intento de acceso.
ms.assetid: d5d53354-fa97-4e46-9632-20ac49f7db5a
ms.tgt_platform: multiple
keywords:
- Efectos de seguridad en Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be628acd1709985aeaa9539bfa527de674732ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903113"
---
# <a name="how-security-affects-operations-in-active-directory-domain-services"></a>Cómo afecta la seguridad a las operaciones en Active Directory Domain Services

Active Directory Domain Services usar el control de acceso para conceder o denegar el acceso a objetos, propiedades y operaciones en función de la identidad del usuario que realiza el intento de acceso. Cuando la aplicación se enlaza al directorio, se enlaza con las credenciales de usuario específicas. Cuando se autentica, estas credenciales determinan el contexto de seguridad de la aplicación. Independientemente de si las credenciales son las del usuario que ha iniciado sesión, un usuario especificado, una cuenta de servicio, una cuenta de equipo o un usuario no autenticado (invitado/todos), el servidor de Active Directory comprueba el derecho del usuario para tener acceso a un objeto antes de que se realice cualquier operación en ese objeto. El usuario puede o no tener acceso a un objeto determinado, a sus elementos secundarios, a sus propiedades u operaciones en ese objeto, lo que significa que la aplicación debe controlar los posibles errores causados por el acceso denegado.

Para obtener más información sobre los contextos de seguridad y los efectos del control de acceso en varias operaciones, vea:

-   [Operaciones de Access Control y de lectura](access-control-and-read-operations.md)
-   [Operaciones de Access Control y escritura](access-control-and-write-operations.md)
-   [Access Control y creación de objetos](access-control-and-object-creation.md)
-   [Access Control y eliminación de objetos](access-control-and-object-deletion.md)

 

 




