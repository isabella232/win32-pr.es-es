---
description: Una barrera de sincronización permite que varios subprocesos esperen hasta que todos los subprocesos han alcanzado un punto de ejecución determinado antes de que continúe cualquier subproceso.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Barreras de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1247d7ab3b20d4fe89763aea0429d742e8ce1c4d11030088316d4e9f3272556b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118885987"
---
# <a name="synchronization-barriers"></a>Barreras de sincronización

Una barrera de sincronización permite que varios subprocesos esperen hasta que todos los subprocesos han alcanzado un punto de ejecución determinado antes de que continúe cualquier subproceso. Las barreras de sincronización no se pueden compartir entre procesos.

Las barreras de sincronización son útiles para los cálculos por fases, en los que los subprocesos que ejecutan el mismo código en paralelo deben completar una fase antes de pasar a la siguiente.

Para crear una barrera de sincronización, llame a la función [**InitializeSynchronizationBarrona**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) y especifique un número máximo de subprocesos y cuántas veces debe girar un subproceso antes de que se bloquee. A continuación, inicie los subprocesos que usarán la barrera. Una vez que cada subproceso finaliza su trabajo, llama a [**EnterSynchronizationBar monet**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) para esperar a la barrera. La **función EnterSynchronizationBarprocesamiento** bloquea cada subproceso hasta que el número de subprocesos bloqueados en la barrera alcanza el número máximo de subprocesos para la barrera, momento en el que **EnterSynchronizationBarbloquea** todos los subprocesos. La **función EnterSynchronizationBarrona** devuelve **TRUE** exactamente para uno de los subprocesos que entraron en la barrera y devuelve **FALSE** para todos los demás subprocesos.

Para liberar una barrera de sincronización cuando ya no sea necesaria, llame a [**DeleteSynchronizationBarrona**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier). Es seguro llamar a esta función inmediatamente después de llamar a [**EnterSynchronizationBarrona,**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) ya que esa función garantiza que todos los subprocesos han terminado de usar la barrera antes de liberarla.

Si nunca se eliminará una barrera de sincronización, los subprocesos pueden especificar la marca **SYNCHRONIZATION \_ BARRIER \_ FLAGS NO \_ \_ DELETE** cuando entran en la barrera. Todos los subprocesos que usan la barrera deben especificar esta marca; Si algún subproceso no lo hace, se omite la marca. Esta marca hace que la función omita el trabajo adicional necesario para la seguridad de eliminación, lo que puede mejorar el rendimiento. Tenga en cuenta que la eliminación de una barrera mientras esta marca está en vigor puede dar lugar a un acceso de identificador no válido y a uno o varios subprocesos bloqueados permanentemente.

 

 



