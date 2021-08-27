---
description: Para sincronizar el acceso a un recurso, use uno de los objetos de sincronización en una de las funciones de espera.
ms.assetid: 0930bf12-6d5f-4f2c-914d-53e6e862d3bd
title: Acerca de la sincronización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb8bca156eec523b30d8f28df8b18a24d9691a33598f5dfe985e4b6b9756ffe3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886409"
---
# <a name="about-synchronization"></a>Acerca de la sincronización

Para sincronizar el acceso a un recurso, use uno de los objetos [de sincronización](synchronization-objects.md) en una de las funciones [de espera](wait-functions.md). El estado de un objeto de sincronización es *señalado* *o no con signo.* Las funciones de espera permiten que un subproceso bloquee su propia ejecución hasta que un objeto no con signo especificado se establezca en el estado señalado. Para obtener más información, vea [Sincronización entre procesos.](interprocess-synchronization.md)

Estos son otros mecanismos de sincronización:

-   [entrada y salida superpuestas](synchronization-and-overlapped-input-and-output.md)
-   [llamadas a procedimiento asincrónico](asynchronous-procedure-calls.md)
-   [objetos de sección críticos](critical-section-objects.md)
-   [variables de condición](condition-variables.md)
-   [bloqueos de lector/escritor de qr](slim-reader-writer--srw--locks.md)
-   [inicialización única](one-time-initialization.md)
-   [acceso a variables entrelazado](interlocked-variable-access.md)
-   [listas vinculadas por sí solos entrelazados](interlocked-singly-linked-lists.md)
-   [colas de temporizador](timer-queues.md)
-   la [**macro MemoryBarproceso**](/windows/win32/api/winnt/nf-winnt-memorybarrier)

Para obtener información adicional sobre la sincronización, vea [Synchronization and Multiprocessor Issues](synchronization-and-multiprocessor-issues.md).

 

 
