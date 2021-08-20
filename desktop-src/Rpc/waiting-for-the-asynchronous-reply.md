---
title: Esperando la respuesta asincrónica
description: Lo que hace el cliente mientras espera recibir una notificación de una respuesta del servidor depende del mecanismo de notificación que seleccione.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Llamada a procedimiento remoto RPC, tareas, esperando respuestas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff50357402d96c32444f077d07558c01ed93d0367514e947643a28bf3041f204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010483"
---
# <a name="waiting-for-the-asynchronous-reply"></a>Esperando la respuesta asincrónica

Lo que hace el cliente mientras espera recibir una notificación de una respuesta del servidor depende del mecanismo de notificación que seleccione.

Si el cliente usa un evento para la notificación, normalmente llamará a la [**función WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o a la [**función WaitForSingleObjectEx.**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) El cliente entra en un estado bloqueado cuando llama a cualquiera de estas funciones. Esto es eficaz porque el cliente no consume ciclos de ejecución de CPU mientras está bloqueado.

Cuando usa el sondeo para esperar sus resultados, el programa cliente entra en un bucle que llama repetidamente a la [**función RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Se trata de un método eficaz de espera si el programa cliente realiza otro procesamiento en el bucle de sondeo. Por ejemplo, puede preparar los datos en fragmentos pequeños para una llamada a procedimiento remoto asincrónico posterior. Una vez finalizado cada fragmento, el cliente puede sondear la llamada a procedimiento remoto asincrónico pendiente para ver si se ha completado.

El programa cliente puede proporcionar una llamada a procedimiento asincrónico (APC), que es un tipo de función de devolución de llamada que la biblioteca en tiempo de ejecución de RPC invocará cuando se complete la llamada a procedimiento remoto asincrónico. El programa cliente debe estar en un estado de espera que se pueda alertar. Esto suele significar que el cliente llama a una función Windows API para ponerse en un estado bloqueado. Para obtener más información, vea [Llamadas a procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls).

> [!Note]  
> La notificación de finalización no se devolverá desde una rutina RPC asincrónica si se produce una excepción RPC durante una llamada asincrónica.

 

Si el programa cliente usa un puerto de finalización de E/S para recibir la notificación de finalización, debe llamar a la [**función GetQueuedCompletionStatus.**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) Cuando lo hace, puede esperar indefinidamente una respuesta o seguir haciendo otro procesamiento. Si realiza otro procesamiento mientras espera una respuesta, debe sondear el puerto de finalización con la **función GetQueuedCompletionStatus.** En este caso, normalmente debe establecer *dwMilliseconds* en cero. Esto hace **que GetQueuedCompletionStatus** devuelva inmediatamente, incluso si la llamada asincrónica no se ha completado.

Los programas cliente también pueden recibir notificaciones de finalización a través de sus colas de mensajes de ventana. En esta situación, simplemente procesan el mensaje de finalización como lo harían Windows mensaje.

En una aplicación multiproceso, el cliente puede cancelar una llamada asincrónica solo después de que el subproceso que originó la llamada se haya devuelto correctamente de la llamada. Esto garantiza que otro subproceso no cancele la llamada de forma asincrónica después de que no se realizara una llamada sincrónica. Como práctica estándar, una llamada asincrónica que produce un error de forma sincrónica no debe cancelarse de forma asincrónica. La aplicación cliente debe observar este comportamiento si se pueden emitir y cancelar llamadas en subprocesos diferentes. Además, después de cancelar la llamada, el código de cliente debe esperar a la notificación de finalización y completar la llamada. La [**función RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) simplemente genera la notificación de finalización. no es un sustituto de completar la llamada.

En el fragmento de código siguiente se muestra cómo un programa cliente puede usar un evento para esperar una respuesta asincrónica.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



Los programas cliente que usan un APC para recibir la notificación de una respuesta asincrónica normalmente se ponen en estado bloqueado. El siguiente fragmento de código muestra esto.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



En este caso, el programa cliente entra en suspensión, sin consumir ciclos de CPU, hasta que la biblioteca rpc en tiempo de ejecución llama a APC (no se muestra).

En el ejemplo siguiente se muestra un cliente que usa un puerto de finalización de E/S para esperar una respuesta asincrónica.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



En el ejemplo anterior, la llamada a [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) espera indefinidamente hasta que se complete la llamada a procedimiento remoto asincrónico.

Un posible problema se produce al escribir aplicaciones multiproceso. Si un subproceso invoca una llamada a procedimiento remoto y, a continuación, finaliza antes de recibir la notificación de que el envío se ha completado, la llamada al procedimiento remoto puede producir un error y el código auxiliar del cliente puede cerrar la conexión al servidor. Por lo tanto, los subprocesos que llaman a un procedimiento remoto no deben finalizar antes de que la llamada se complete o cancele cuando no se desea el comportamiento.

 

 