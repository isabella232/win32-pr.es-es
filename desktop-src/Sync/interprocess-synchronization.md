---
description: Varios procesos pueden tener identificadores para el mismo evento, exclusión mutua, semáforo o objeto de temporizador, por lo que estos objetos se pueden usar para realizar la sincronización entre procesos.
ms.assetid: 1738e586-580f-4b74-95dc-ede300b6ac9a
title: Sincronización entre procesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0caf4818a05d526a70a1e3257ec6f86d0279f39ce3cf05a4411e49991db6ba15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886356"
---
# <a name="interprocess-synchronization"></a>Sincronización entre procesos

Varios procesos pueden tener identificadores para el mismo evento, exclusión mutua, semáforo o objeto de temporizador, por lo que estos objetos se pueden usar para realizar la sincronización entre procesos. El proceso que crea un objeto puede usar el identificador devuelto por la función de creación ([**CreateEvent**](/windows/win32/api/synchapi/nf-synchapi-createeventa), [**CreateMutex,**](/windows/win32/api/synchapi/nf-synchapi-createmutexa) [**CreateSemaphore**](/windows/desktop/api/WinBase/nf-winbase-createsemaphorea)o [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw)). Otros procesos pueden abrir un identificador para el objeto mediante su nombre o mediante herencia o duplicación. Para obtener más información, vea los temas siguientes:

-   [Nombres de objeto](object-names.md)
-   [Herencia de objetos](object-inheritance.md)
-   [Duplicación de objetos](object-duplication.md)

 

 
