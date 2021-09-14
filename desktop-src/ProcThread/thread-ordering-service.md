---
description: El servicio de ordenación de subprocesos controla la ejecución de uno o varios subprocesos de cliente. Garantiza que cada subproceso de cliente se ejecute una vez durante el período especificado y en orden relativo.
ms.assetid: 5c37873a-ced4-447e-a6e1-55cfa8ab24b4
title: Servicio de ordenación de subprocesos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72b3cd12b26124b47d506585425388a4542a70df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062788"
---
# <a name="thread-ordering-service"></a>Servicio de ordenación de subprocesos

El *servicio de ordenación de* subprocesos controla la ejecución de uno o varios subprocesos de cliente. Garantiza que cada subproceso de cliente se ejecute una vez durante el período especificado y en orden relativo.

**Windows Server 2003 y Windows XP:** El servicio de ordenación de subprocesos está disponible a partir de Windows Vista y Windows Server 2008.

El servicio de ordenación de subprocesos está desactivado de forma predeterminada y el usuario debe iniciarlo. Mientras se ejecuta el servicio de ordenación de subprocesos, se activa cada 5 segundos para comprobar si hay una nueva solicitud, incluso si el sistema está inactivo. Esto evita que el sistema se alome durante más de 5 segundos, lo que hace que el sistema consuma más energía. Si la eficiencia energética es fundamental para la aplicación, es mejor no usar el servicio de ordenación de subprocesos y, en su lugar, permitir que el programador del sistema administre la ejecución de subprocesos.

Cada subproceso de cliente pertenece a un *grupo de ordenación de subprocesos*. El *subproceso primario crea* uno o varios grupos de ordenación de subprocesos mediante una llamada a la función [**AvRtCreateThreadOrderingGroup.**](/windows/desktop/api/Avrt/nf-avrt-avrtcreatethreadorderinggroup) El subproceso primario usa esta función para especificar el período para el grupo de ordenación de subprocesos y un intervalo de tiempo de espera.

Los subprocesos de cliente adicionales llaman a la función [**AvRtJoinThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtjointhreadorderinggroup) para unirse a un grupo de ordenación de subprocesos existente. Estos subprocesos indican si van a ser predecesores o sucesores del subproceso primario en el orden de ejecución. Se espera que cada subproceso de cliente complete una determinada cantidad de procesamiento cada período. Todos los subprocesos del grupo deben completar su ejecución dentro del período más el intervalo de tiempo de espera.

Los subprocesos de un grupo de ordenación de subprocesos incluyen su código de procesamiento dentro de un bucle controlado por la función [**AvRtWaitOnThreadOrderingGroup.**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) En primer lugar, los subprocesos predecesores se ejecutan de uno en uno en el orden en que se unieron al grupo, mientras que los subprocesos primarios y sucesores se bloquean en sus llamadas a **AvRtWaitOnThreadOrderingGroup**. Cuando cada subproceso predecesor termina con su procesamiento, el control de ejecución vuelve a la parte superior de su bucle de procesamiento y el subproceso llama a **AvRtWaitOnThreadOrderingGroup** de nuevo para bloquear hasta su siguiente turno. Una vez que todos los subprocesos predecesores han llamado a esta función, el servicio de ordenación de subprocesos puede programar el subproceso primario. Por último, cuando el subproceso primario finaliza su procesamiento y llama de nuevo a **AvRtWaitOnThreadOrderingGroup,** el servicio de ordenación de subprocesos puede programar los subprocesos sucesores de uno en uno en el orden en que se unieron al grupo. Si todos los subprocesos completan su ejecución antes de que finalice un período, todos los subprocesos esperan hasta que transcurra el resto del período antes de que se vuelvan a ejecutar.

Cuando el cliente ya no necesita ejecutarse como parte del grupo de ordenación de subprocesos, llama a la función [**AvRtLeaveThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtleavethreadorderinggroup) para quitarse del grupo. Tenga en cuenta que el subproceso primario no debe quitarse de un grupo de ordenación de subprocesos. Si un subproceso no completa su ejecución antes de que transcurra el período más el intervalo de tiempo de espera, se elimina del grupo.

El subproceso primario llama a la [**función AvRtDeleteThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtdeletethreadorderinggroup) para eliminar el grupo de ordenación de subprocesos. El grupo de ordenación de subprocesos también se destruye si el subproceso primario no completa su ejecución antes de que transcurra el período más el intervalo de tiempo de espera. Cuando se destruye el grupo de ordenación de subprocesos, cualquier llamada a [**AvRtWaitOnThreadOrderingGroup**](/windows/desktop/api/Avrt/nf-avrt-avrtwaitonthreadorderinggroup) desde subprocesos de ese grupo producirá un error o se producirá un tiempo de espera.

 

 



