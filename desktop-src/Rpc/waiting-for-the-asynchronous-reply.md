---
title: Esperando la respuesta asincrónica
description: Lo que hace el cliente mientras espera recibir una respuesta del servidor depende del mecanismo de notificación que seleccione.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- RPC llamada a procedimiento remoto, tareas, esperar respuestas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104359224"
---
# <a name="waiting-for-the-asynchronous-reply"></a>Esperando la respuesta asincrónica

Lo que hace el cliente mientras espera recibir una respuesta del servidor depende del mecanismo de notificación que seleccione.

Si el cliente usa un evento para la notificación, normalmente llamará a la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) o a la función [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) . El cliente entra en un estado bloqueado cuando llama a cualquiera de estas funciones. Esto es eficaz porque el cliente no consume ciclos de ejecución de la CPU mientras está bloqueado.

Cuando usa el sondeo para esperar los resultados, el programa cliente entra en un bucle que llama repetidamente a la función [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Se trata de un método eficaz de espera si el programa cliente realiza otro procesamiento en el bucle de sondeo. Por ejemplo, puede preparar los datos en fragmentos pequeños para una llamada a procedimiento remoto asincrónica subsiguiente. Una vez finalizado cada fragmento, el cliente puede sondear la llamada a procedimiento remoto asincrónica pendiente para ver si se ha completado.

El programa cliente puede proporcionar una llamada a procedimiento asincrónico (APC), que es un tipo de función de devolución de llamada que la biblioteca en tiempo de ejecución de RPC invocará cuando se complete la llamada a procedimiento remoto asincrónica. El programa cliente debe estar en un estado de espera de alerta. Normalmente, esto significa que el cliente llama a una función de la API de Windows para que se ponga en estado bloqueado. Para obtener más información, vea [llamadas a procedimientos asincrónicos](/windows/desktop/Sync/asynchronous-procedure-calls).

> [!Note]  
> La notificación de finalización no se devolverá desde una rutina RPC asincrónica si se genera una excepción RPC durante una llamada asincrónica.

 

Si el programa cliente usa un puerto de finalización de e/s para recibir la notificación de finalización, debe llamar a la función [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Cuando lo hace, puede esperar indefinidamente una respuesta o seguir realizando otro procesamiento. Si realiza otro procesamiento mientras espera una respuesta, debe sondear el puerto de finalización con la función **GetQueuedCompletionStatus** . En este caso, normalmente es necesario establecer *dwMilliseconds* en cero. Esto hace que **GetQueuedCompletionStatus** se devuelva inmediatamente, aunque no se haya completado la llamada asincrónica.

Los programas cliente también pueden recibir notificaciones de finalización a través de sus colas de mensajes de ventana. En esta situación, simplemente procesan el mensaje de finalización como cualquier mensaje de Windows.

En una aplicación multiproceso, el cliente solo puede cancelar una llamada asincrónica una vez que el subproceso que originó la llamada se ha devuelto correctamente desde la llamada. Esto garantiza que otro subproceso no cancele la llamada de forma asincrónica después de que se haya producido un error en una llamada sincrónica. Como práctica estándar, una llamada asincrónica que genera un error sincrónicamente no se debe cancelar de forma asincrónica. La aplicación cliente debe observar este comportamiento si se pueden emitir y cancelar llamadas en subprocesos diferentes. Además, después de que se cancele la llamada, el código de cliente debe esperar la notificación de finalización y completar la llamada. La función [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) simplemente realiza una prisa en la notificación de finalización. no es un sustituto de la finalización de la llamada.

En el fragmento de código siguiente se muestra cómo un programa cliente puede usar un evento para esperar una respuesta asincrónica.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



Los programas cliente que usan una APC para recibir la notificación de una respuesta asincrónica normalmente se ponen en estado bloqueado. En el fragmento de código siguiente se muestra esto.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



En este caso, el programa cliente entra en suspensión y no está consumiendo ningún ciclo de CPU, hasta que la biblioteca en tiempo de ejecución de RPC llama a APC (no se muestra).

En el ejemplo siguiente se muestra un cliente que utiliza un puerto de finalización de e/s para esperar una respuesta asincrónica.


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



En el ejemplo anterior, la llamada a [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) espera indefinidamente hasta que se completa la llamada a procedimiento remoto asincrónica.

Al escribir aplicaciones multiproceso, se produce una posible dificultad. Si un subproceso invoca una llamada a procedimiento remoto y, a continuación, finaliza antes de recibir la notificación de que se ha completado el envío, la llamada a procedimiento remoto puede producir un error y el código auxiliar del cliente puede cerrar la conexión al servidor. Por lo tanto, los subprocesos que llaman a un procedimiento remoto no deben finalizar antes de que la llamada se complete o se cancele cuando no se desea el comportamiento.

 

 