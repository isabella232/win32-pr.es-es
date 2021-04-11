---
description: Una barrera de sincronización permite que varios subprocesos esperen hasta que todos los subprocesos hayan alcanzado un punto de ejecución determinado antes de que continúe cualquier subproceso.
ms.assetid: 3A76E6F7-C38B-4843-9496-36F3C78B700C
title: Barreras de sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4276f0bbc5a10eef391c12cc51ebd475e563bd44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278790"
---
# <a name="synchronization-barriers"></a>Barreras de sincronización

Una barrera de sincronización permite que varios subprocesos esperen hasta que todos los subprocesos hayan alcanzado un punto de ejecución determinado antes de que continúe cualquier subproceso. No se pueden compartir barreras de sincronización entre procesos.

Las barreras de sincronización son útiles para los cálculos por fases, en los que los subprocesos que ejecutan el mismo código en paralelo deben completar una fase antes de pasar a la siguiente.

Para crear una barrera de sincronización, llame a la función [**InitializeSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-initializesynchronizationbarrier) y especifique un número máximo de subprocesos y el número de veces que un subproceso debe girar antes de que se bloquee. A continuación, inicie los subprocesos que usarán la barrera. Una vez que cada subproceso finaliza su trabajo, llama a [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) para esperar a la barrera. La función **EnterSynchronizationBarrier** bloquea cada subproceso hasta que el número de subprocesos bloqueados en la barrera alcanza el número máximo de subprocesos para la barrera, momento en el cual **EnterSynchronizationBarrier** Desbloquea todos los subprocesos. La función **EnterSynchronizationBarrier** devuelve **true** para exactamente uno de los subprocesos que entró en la barrera y devuelve **false** para todos los demás subprocesos.

Para liberar una barrera de sincronización cuando ya no sea necesaria, llame a [**DeleteSynchronizationBarrier**](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier). Es seguro llamar a esta función inmediatamente después de llamar a [**EnterSynchronizationBarrier**](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier) , ya que la función garantiza que todos los subprocesos han terminado de usar la barrera antes de que se libere.

Si nunca se va a eliminar una barrera de sincronización, los subprocesos pueden especificar las **marcas de barrera de sincronización sin marca de \_ \_ \_ \_ eliminación** cuando entran en la barrera. Todos los subprocesos que usan la barrera deben especificar esta marca; Si no hay ningún subproceso, se omite la marca. Esta marca hace que la función omita el trabajo adicional necesario para la seguridad de la eliminación, lo que puede mejorar el rendimiento. Tenga en cuenta que la eliminación de una barrera mientras esta marca está en vigor puede dar lugar a un acceso de identificador no válido y a uno o más subprocesos bloqueados de forma permanente.

 

 



