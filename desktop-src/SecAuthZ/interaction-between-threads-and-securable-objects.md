---
description: En una comprobación de acceso, el sistema compara la información de seguridad del token de acceso de subprocesos con la información de seguridad del descriptor de seguridad de objetos.
ms.assetid: 40871179-d383-43d0-810d-0805c88dbbd6
title: Interacción entre subprocesos y objetos protegibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3e2b18f707ece4d651eeca1c6897bb67aad334
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912426"
---
# <a name="interaction-between-threads-and-securable-objects"></a>Interacción entre subprocesos y objetos protegibles

Cuando un subproceso intenta utilizar un [objeto protegible](securable-objects.md), el sistema realiza una comprobación de acceso antes de permitir que el subproceso continúe. En una comprobación de acceso, el sistema compara la información de seguridad en el [*token de acceso*](/windows/desktop/SecGloss/a-gly) del subproceso con la información de seguridad del [*descriptor de seguridad*](/windows/desktop/SecGloss/s-gly)del objeto.

-   El token de acceso contiene los [*identificadores de seguridad*](/windows/desktop/SecGloss/s-gly) (SID) que identifican al usuario asociado al subproceso.
-   El descriptor de seguridad identifica el propietario del objeto y contiene una [*lista de control de acceso discrecional*](/windows/desktop/SecGloss/d-gly) (DACL). La DACL contiene [*entradas de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACE), cada una de las cuales especifica los derechos de acceso permitidos o denegados a un usuario o grupo específico.

El sistema comprueba la DACL del objeto, buscando las ACE que se aplican a los SID de usuario y de grupo del token de acceso del subproceso. El sistema comprueba cada ACE hasta que se haya concedido o denegado el acceso o hasta que no haya más ACE para comprobar. Es posible que una [*lista de control de acceso*](/windows/desktop/SecGloss/a-gly) (ACL) tenga varias ACE que se aplican a los SID del token. Y, si esto ocurre, se acumulan los derechos de acceso concedidos por cada ACE. Por ejemplo, si una ACE concede acceso de lectura a un grupo y otra ACE concede acceso de escritura a un usuario que sea miembro del grupo, el usuario puede tener acceso de lectura y escritura al objeto.

En la ilustración siguiente se muestra la relación entre estos bloques de información de seguridad:

![relaciones entre procesos, ACE y DACL](images/cssec-02.png)

 

 
