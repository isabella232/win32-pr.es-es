---
description: El servicio de ordenación de subprocesos controla la ejecución de uno o más subprocesos de cliente. Garantiza que cada subproceso de cliente se ejecuta una vez durante el período especificado y en el orden relativo.
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: Servicio de ordenación de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b3cd12b26124b47d506585425388a4542a70df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677825"
---
# <a name="thread-ordering-service"></a>Servicio de ordenación de subprocesos

El *servicio de ordenación de subprocesos* controla la ejecución de uno o más subprocesos de cliente. Garantiza que cada subproceso de cliente se ejecuta una vez durante el período especificado y en el orden relativo.

**Windows Server 2003 y Windows XP:** El servicio de ordenación de subprocesos está disponible a partir de Windows Vista y Windows Server 2008.

El servicio de ordenación de subprocesos está desactivado de forma predeterminada y el usuario debe iniciarlo. Mientras se ejecuta el servicio de ordenación de subprocesos, se activa cada 5 segundos para comprobar si hay una nueva solicitud, incluso si el sistema está inactivo. Esto evita que el sistema se suspenda durante más de 5 segundos, lo que hace que el sistema consuma más energía. Si la eficacia energética es fundamental para la aplicación, es mejor no usar el servicio de ordenación de subprocesos y, en su lugar, permitir que el programador del sistema administre la ejecución de subprocesos.

Cada subproceso de cliente pertenece a un *grupo de pedidos de subprocesos*. El *subproceso primario* crea uno o más grupos de ordenación de subprocesos mediante una llamada a la función [**AvRtCreateThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup) . El subproceso primario usa esta función para especificar el período del grupo de pedidos de subprocesos y un intervalo de tiempo de espera.

Los subprocesos de cliente adicionales llaman a la función [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) para unirse a un grupo de pedidos de subprocesos existente. Estos subprocesos indican si se trata de un predecesor o sucesor del subproceso primario en el orden de ejecución. Se espera que cada subproceso de cliente complete una determinada cantidad de procesamiento cada período. Todos los subprocesos del grupo deben completar su ejecución dentro del período más el intervalo de tiempo de espera.

Los subprocesos de un grupo de ordenación de subprocesos encierran su código de procesamiento dentro de un bucle controlado por la función [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) . En primer lugar, los subprocesos predecesores se ejecutan de uno en uno en el orden en que se unen al grupo, mientras que los subprocesos primario y sucesor se bloquean en sus llamadas a **AvRtWaitOnThreadOrderingGroup**. Cuando cada subproceso de la predecesora finaliza con su procesamiento, el control de la ejecución vuelve a la parte superior de su bucle de procesamiento y el subproceso llama a **AvRtWaitOnThreadOrderingGroup** de nuevo para bloquear hasta su siguiente activación. Después de que todos los subprocesos predecesores hayan llamado a esta función, el servicio de ordenación de subprocesos puede programar el subproceso primario. Por último, cuando el subproceso primario finaliza su procesamiento y llama de nuevo a **AvRtWaitOnThreadOrderingGroup** , el servicio de ordenación de subprocesos puede programar los subprocesos sucesoros de uno en uno en el orden en que se unen al grupo. Si todos los subprocesos completan su ejecución antes de que finalice un período, todos los subprocesos esperan hasta que el resto del período transcurre antes de que se ejecute de nuevo.

Cuando el cliente ya no necesita ejecutarse como parte del grupo de pedidos de subprocesos, llama a la función [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) para quitarse del grupo. Tenga en cuenta que el subproceso primario no debe quitarse a sí mismo de un grupo de orden de subprocesos. Si un subproceso no completa su ejecución antes de que transcurra el período más el intervalo de tiempo de espera, se elimina del grupo.

El subproceso primario llama a la función [**AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) para eliminar el grupo de orden de subprocesos. El grupo de orden de subprocesos también se destruye si el subproceso primario no completa su ejecución antes de que transcurra el período más tiempo de espera. Cuando se destruye el grupo de orden de subprocesos, se produce un error o el tiempo de espera de las llamadas a [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) desde los subprocesos de ese grupo.

 

 



