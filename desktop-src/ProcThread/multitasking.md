---
description: Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee7826ca79d6095715c722b4b5c3da479e276444825343ac096cd9822d9e365a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032185"
---
# <a name="multitasking"></a>Multitarea

Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan. El sistema está diseñado para la multitarea preferente. asigna un segmento de *tiempo de procesador* a cada subproceso que ejecuta. El subproceso que se está ejecutando actualmente se suspende cuando transcurre su intervalo de tiempo, lo que permite que se ejecute otro subproceso. Cuando el sistema cambia de un subproceso a otro, guarda el contexto del subproceso adelantado y restaura el contexto guardado del siguiente subproceso en la cola.

La duración del período de tiempo depende del sistema operativo y del procesador. Dado que cada segmento de tiempo es pequeño (aproximadamente 20 milisegundos), parece que varios subprocesos se están ejecutando al mismo tiempo. Este es realmente el caso en sistemas multiprocesador, donde los subprocesos ejecutables se distribuyen entre los procesadores disponibles. Sin embargo, debe tener cuidado al usar varios subprocesos en una aplicación, ya que el rendimiento del sistema puede disminuir si hay demasiados subprocesos.

Para obtener más información, vea los temas siguientes:

-   [Ventajas de la multitarea](advantages-of-multitasking.md)
-   [Cuándo usar multitarea](when-to-use-multitasking.md)
-   [Consideraciones sobre multitarea](multitasking-considerations.md)

 

 



