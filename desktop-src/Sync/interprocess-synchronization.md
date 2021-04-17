---
description: Varios procesos pueden tener identificadores para el mismo objeto de evento, exclusión mutua, semáforo o temporizador, por lo que estos objetos se pueden usar para realizar la sincronización entre procesos.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronización entre procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7c18fb26d6a64fdc2d785d16c7bccb8b007c3f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667976"
---
# <a name="interprocess-synchronization"></a>Sincronización entre procesos

Varios procesos pueden tener identificadores para el mismo objeto de evento, exclusión mutua, semáforo o temporizador, por lo que estos objetos se pueden usar para realizar la sincronización entre procesos. El proceso que crea un objeto puede usar el identificador devuelto por la función de creación ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex**](/windows/win32/api/synchapi/nf-synchapi-createmutexa), [**createsemaphore (**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Otros procesos pueden abrir un identificador para el objeto utilizando su nombre o a través de la herencia o la duplicación. Para obtener más información, vea los temas siguientes:

-   [Nombres de objeto](object-names.md)
-   [Herencia de objetos](object-inheritance.md)
-   [Duplicación de objetos](object-duplication.md)

 

 
