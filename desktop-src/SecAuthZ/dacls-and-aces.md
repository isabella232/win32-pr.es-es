---
description: Si un Windows no tiene una lista de control de acceso discrecional (DACL), el sistema permite a todos los usuarios acceder a él.
ms.assetid: be9633fb-14ef-42d2-9269-84287b35b653
title: DACL y ACE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c28bf351fd59f634a7c7bf960aedac1c76659ad3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160824"
---
# <a name="dacls-and-aces"></a>DACL y ACE

Si un Windows no tiene una lista [*de control*](/windows/desktop/SecGloss/d-gly) de acceso discrecional (DACL), el sistema permite a todos los usuarios acceder a él. Si un objeto tiene una DACL, el sistema solo permite el acceso que permiten explícitamente las entradas de [*control*](/windows/desktop/SecGloss/a-gly) de acceso (ACE) de la DACL. Si no hay ninguna ACE en la DACL, el sistema no permite el acceso a nadie. Del mismo modo, si una DACL tiene ACE que permiten el acceso a un conjunto limitado de usuarios o grupos, el sistema deniega implícitamente el acceso a todos los administradores de confianza que no están incluidos en las ACE.

En la mayoría de los casos, puede controlar el acceso a un objeto mediante AEA con acceso permitido; no es necesario denegar explícitamente el acceso a un objeto. La excepción es cuando una ACE permite el acceso a un grupo y desea denegar el acceso a un miembro del grupo. Para ello, coloque una ACE de acceso denegado para el usuario en la DACL antes de la ACE con acceso permitido para el grupo. Tenga en cuenta [que el orden de las ACE](order-of-aces-in-a-dacl.md) es importante porque el sistema lee las ACE en secuencia hasta que se concede o se deniega el acceso. La ACE de acceso denegado del usuario debe aparecer primero; De lo contrario, cuando el sistema lea la ACE de acceso permitido del grupo, concederá acceso al usuario restringido.

En la ilustración siguiente se muestra una DACL que deniega el acceso a un usuario y concede acceso a dos grupos. Los miembros del grupo A obtienen derechos de acceso de lectura, escritura y ejecución acumulando los derechos permitidos para el grupo A y los derechos permitidos a Todos. La excepción es Andrew, a quien la ACE con acceso denegado deniega el acceso a pesar de ser miembro del grupo Todos.

![dacl que concede distintos derechos de acceso en función de la pertenencia a grupos](images/accctrl1.png)

 

 
