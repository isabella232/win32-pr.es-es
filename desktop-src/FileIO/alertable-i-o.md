---
description: La e/s de alertas es el método por el que los subprocesos de la aplicación procesan las solicitudes de e/s asincrónicas solo cuando se encuentran en un estado de alerta.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/s de alertas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687141"
---
# <a name="alertable-io"></a>E/s de alertas

La e/s de alertas es el método por el que los subprocesos de la aplicación procesan las solicitudes de e/s asincrónicas solo cuando se encuentran en un estado de alerta.

Para saber si un subproceso está en un estado de alerta, considere el siguiente escenario:

1.  Un subproceso inicia una solicitud de lectura asincrónica mediante una llamada a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) con un puntero a una función de devolución de llamada.
2.  El subproceso inicia una solicitud de escritura asincrónica mediante una llamada a [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) con un puntero a una función de devolución de llamada.
3.  El subproceso llama a una función que captura una fila de datos de un servidor de base de datos remoto.

En este escenario, lo más probable es que las llamadas a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) devuelvan antes de la llamada de función en el paso 3. Cuando lo hacen, el kernel coloca los punteros a las funciones de devolución de llamada en la cola de llamadas a procedimiento asincrónico (APC) del subproceso. El kernel mantiene esta cola específicamente para almacenar los datos de solicitud de e/s devueltos hasta que el subproceso correspondiente pueda procesarlas.

Cuando se completa la recopilación de filas y el subproceso vuelve de la función, su prioridad más alta es procesar las solicitudes de e/s devueltas en la cola llamando a las funciones de devolución de llamada. Para ello, debe especificar un estado de alerta. Un subproceso solo puede hacerlo mediante una llamada a una de las siguientes funciones con las marcas apropiadas:

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

Cuando el subproceso entra en un estado de alerta, se producen los siguientes eventos:

1.  El kernel comprueba la cola APC del subproceso. Si la cola contiene punteros de función de devolución de llamada, el kernel quita el puntero de la cola y lo envía al subproceso.
2.  El subproceso ejecuta la función de devolución de llamada.
3.  Los pasos 1 y 2 se repiten para cada puntero que quede en la cola.
4.  Cuando la cola está vacía, el subproceso vuelve de la función que la colocó en un estado de alerta.

En este escenario, una vez que el subproceso entra en un estado de alerta, llamará a las funciones de devolución de llamada enviadas a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)y, a continuación, devolverá desde la función que la colocó en un estado de alerta.

Si un subproceso entra en un estado de alerta mientras su cola APC está vacía, el kernel suspenderá la ejecución del subproceso hasta que se produzca uno de los siguientes casos:

-   El objeto de kernel en el que se espera se señala.
-   Se coloca un puntero de función de devolución de llamada en la cola APC.

Un subproceso que usa e/s de alerta procesa las solicitudes de e/s asincrónicas de forma más eficaz que cuando simplemente esperan la marca de evento en la estructura [**superpuesta**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que se va a establecer, y el mecanismo de e/s de alertas es menos complicado que los [puertos de finalización de e/s](i-o-completion-ports.md) que se van a usar. Sin embargo, la e/s de alertas devuelve el resultado de la solicitud de e/s solo al subproceso que la inició. Los puertos de finalización de e/s no tienen esta limitación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamadas a procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
