---
description: Para sincronizar el acceso a un recurso, use uno de los objetos de sincronización en una de las funciones de espera.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Acerca de la sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ad53dc8c309d8ec55f37cef5f78839348071477
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667988"
---
# <a name="about-synchronization"></a>Acerca de la sincronización

Para sincronizar el acceso a un recurso, use uno de los [objetos de sincronización](synchronization-objects.md) en una de las [funciones de espera](wait-functions.md). El estado de un objeto de sincronización es *señalado* o no *señalado*. Las funciones de espera permiten que un subproceso bloquee su propia ejecución hasta que un objeto no señalado especificado se establezca en el estado señalado. Para obtener más información, consulte [sincronización entre procesos](interprocess-synchronization.md).

A continuación se muestran otros mecanismos de sincronización:

-   [entrada y salida superpuestas](synchronization-and-overlapped-input-and-output.md)
-   [llamadas a procedimientos asincrónicos](asynchronous-procedure-calls.md)
-   [objetos de sección crítica](critical-section-objects.md)
-   [variables de condición](condition-variables.md)
-   [bloqueos finos de lector/escritor](slim-reader-writer--srw--locks.md)
-   [inicialización única](one-time-initialization.md)
-   [acceso a variables entrelazadas](interlocked-variable-access.md)
-   [listas vinculadas de un solo vínculo](interlocked-singly-linked-lists.md)
-   [colas de temporizador](timer-queues.md)
-   la macro [**MemoryBarrier**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Para obtener información adicional sobre la sincronización, vea [problemas de sincronización y multiprocesador](synchronization-and-multiprocessor-issues.md).

 

 
