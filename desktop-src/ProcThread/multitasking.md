---
description: Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitarea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127375026"
---
# <a name="multitasking"></a>Multitarea

Un sistema operativo multitarea divide el tiempo de procesador disponible entre los procesos o subprocesos que lo necesitan. El sistema está diseñado para la multitarea preferente; asigna un segmento de *tiempo de procesador* a cada subproceso que ejecuta. El subproceso que se está ejecutando actualmente se suspende cuando transcurre su intervalo de tiempo, lo que permite que se ejecute otro subproceso. Cuando el sistema cambia de un subproceso a otro, guarda el contexto del subproceso preferente y restaura el contexto guardado del siguiente subproceso en la cola.

La duración del período de tiempo depende del sistema operativo y del procesador. Dado que cada segmento de tiempo es pequeño (aproximadamente 20 milisegundos), varios subprocesos parecen estar ejecutándose al mismo tiempo. Este es realmente el caso en sistemas multiprocesador, donde los subprocesos ejecutables se distribuyen entre los procesadores disponibles. Sin embargo, debe tener cuidado al usar varios subprocesos en una aplicación, ya que el rendimiento del sistema puede disminuir si hay demasiados subprocesos.

Para obtener más información, vea los temas siguientes:

-   [Ventajas de la multitarea](advantages-of-multitasking.md)
-   [Cuándo usar multitarea](when-to-use-multitasking.md)
-   [Consideraciones de multitarea](multitasking-considerations.md)

 

 



