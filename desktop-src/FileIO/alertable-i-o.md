---
description: E/S que se puede alertar es el método por el que los subprocesos de aplicación procesan solicitudes de E/S asincrónicas solo cuando se encuentran en un estado de alerta.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/S que se puede alertar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b76df0a59726d6fb0eea0bd99ff960e9b18ba80f7c17bf0ae7e4338953895e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119766245"
---
# <a name="alertable-io"></a>E/S que se puede alertar

E/S que se puede alertar es el método por el que los subprocesos de aplicación procesan solicitudes de E/S asincrónicas solo cuando se encuentran en un estado de alerta.

Para comprender cuándo un subproceso está en un estado que se puede alertar, considere el siguiente escenario:

1.  Un subproceso inicia una solicitud de lectura asincrónica llamando a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) con un puntero a una función de devolución de llamada.
2.  El subproceso inicia una solicitud de escritura asincrónica llamando a [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) con un puntero a una función de devolución de llamada.
3.  El subproceso llama a una función que captura una fila de datos de un servidor de bases de datos remoto.

En este escenario, las llamadas a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) probablemente devolverán antes de la llamada de función en el paso 3. Cuando lo hacen, el kernel coloca los punteros a las funciones de devolución de llamada en la cola llamada a procedimiento asincrónico (APC) del subproceso. El kernel mantiene esta cola específicamente para contener los datos de solicitud de E/S devueltos hasta que el subproceso correspondiente pueda procesarlo.

Cuando se completa la captura de filas y el subproceso vuelve de la función, su prioridad más alta es procesar las solicitudes de E/S devueltas en la cola mediante una llamada a las funciones de devolución de llamada. Para ello, debe entrar en un estado de alerta. Un subproceso solo puede hacerlo llamando a una de las siguientes funciones con las marcas adecuadas:

-   [**SleepEx**](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [**WaitForMultipleObjectsEx**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [**SignalObjectAndWait**](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [**MsgWaitForMultipleObjectsEx**](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

Cuando el subproceso entra en un estado de alerta, se producen los siguientes eventos:

1.  El kernel comprueba la cola de APC del subproceso. Si la cola contiene punteros de función de devolución de llamada, el kernel quita el puntero de la cola y lo envía al subproceso.
2.  El subproceso ejecuta la función de devolución de llamada.
3.  Los pasos 1 y 2 se repiten para cada puntero que queda en la cola.
4.  Cuando la cola está vacía, el subproceso vuelve de la función que la colocó en un estado de alerta.

En este escenario, una vez que el subproceso entra en un estado de alerta, llamará a las funciones de devolución de llamada enviadas a [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) y [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex)y, a continuación, devolverá de la función que lo colocó en un estado de alerta.

Si un subproceso entra en un estado de alerta mientras su cola de APC está vacía, el kernel suspenderá la ejecución del subproceso hasta que se produzca una de las siguientes acciones:

-   El objeto de kernel en el que se está esperando se señala.
-   Un puntero de función de devolución de llamada se coloca en la cola de APC.

Un subproceso que usa las solicitudes de E/S asincrónicas que se pueden alertar procesa de forma más eficaz que cuando simplemente esperan en la marca de evento de la estructura [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) que se va a establecer y el mecanismo de E/S que se puede alertar es menos complicado que usar los puertos de finalización de [E/S.](i-o-completion-ports.md) Sin embargo, la E/S que admite alertas devuelve el resultado de la solicitud de E/S solo al subproceso que la inició. Los puertos de finalización de E/S no tienen esta limitación.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Llamadas a procedimiento asincrónico](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
