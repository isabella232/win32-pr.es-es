---
description: En una comprobación de acceso, el sistema compara la información de seguridad del token de acceso de subprocesos con la información de seguridad del descriptor de seguridad de objetos.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interacción entre subprocesos y objetos protegibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ab85aa461892d0e6fdf6bdbd9adc8aa7b78a3d9bf1b3896d53ad8e2e236de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670825"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interacción entre subprocesos y objetos protegibles

Cuando un subproceso intenta usar un [objeto protegible](securable-objects.md), el sistema realiza una comprobación de acceso antes de permitir que el subproceso continúe. En una comprobación de acceso, el sistema compara la información de seguridad del [*token*](/windows/desktop/SecGloss/a-gly) de acceso del subproceso con la información de seguridad del descriptor de [*seguridad del objeto*](/windows/desktop/SecGloss/s-gly).

-   El token de acceso [*contiene identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que identifican al usuario asociado al subproceso.
-   El descriptor de seguridad identifica el propietario del objeto y contiene una lista de control de [*acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL). La DACL contiene [*entradas de control de*](/windows/desktop/SecGloss/a-gly) acceso (ACE), cada una de las cuales especifica los derechos de acceso permitidos o denegados a un usuario o grupo específico.

El sistema comprueba la DACL del objeto y busca las ACE que se aplican a los SID de usuario y grupo desde el token de acceso del subproceso. El sistema comprueba cada ACE hasta que se concede o deniega el acceso o hasta que no haya más ACE que comprobar. Posiblemente, una lista [*de control*](/windows/desktop/SecGloss/a-gly) de acceso (ACL) podría tener varias ACE que se aplican a los SID del token. Y, si esto ocurre, se acumulan los derechos de acceso concedidos por cada ACE. Por ejemplo, si una ACE concede acceso de lectura a un grupo y otra ACE concede acceso de escritura a un usuario que es miembro del grupo, el usuario puede tener acceso de lectura y escritura al objeto.

En la ilustración siguiente se muestra la relación entre estos bloques de información de seguridad:

![relaciones entre procesos, aces y dacls](images/cssec-02.png)

 

 
