---
description: Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360692"
---
# <a name="multitasking"></a>Multitarea

Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan. El sistema está diseñado para la multitarea preferente; asigna un *intervalo de tiempo* de procesador a cada subproceso que se ejecuta. El subproceso que se está ejecutando actualmente se suspende cuando transcurre el intervalo de tiempo, lo que permite la ejecución de otro subproceso. Cuando el sistema cambia de un subproceso a otro, guarda el contexto del subproceso que se ha cambiado y restaura el contexto guardado del subproceso siguiente en la cola.

La duración del período de tiempo depende del sistema operativo y del procesador. Dado que cada intervalo de tiempo es pequeño (aproximadamente 20 milisegundos), parece que varios subprocesos se ejecutan al mismo tiempo. Este es realmente el caso en sistemas multiprocesador, donde los subprocesos ejecutables se distribuyen entre los procesadores disponibles. Sin embargo, debe tener cuidado al usar varios subprocesos en una aplicación, ya que el rendimiento del sistema puede disminuir si hay demasiados subprocesos.

Para obtener más información, vea los temas siguientes:

-   [Ventajas de la multitarea](advantages-of-multitasking.md)
-   [Cuándo usar la multitarea](when-to-use-multitasking.md)
-   [Consideraciones sobre la multitarea](multitasking-considerations.md)

 

 



