---
title: Realización de la llamada asincrónica
description: Antes de que pueda realizar una llamada remota asincrónica, el cliente debe inicializar el identificador asincrónico. Los programas de cliente y servidor usan punteros a \_ la \_ estructura de estado de RPC Async para los identificadores asincrónicos.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- RPC llamada a procedimiento remoto, tareas, realizar llamadas asincrónicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105676439"
---
# <a name="making-the-asynchronous-call"></a>Realización de la llamada asincrónica

Antes de que pueda realizar una llamada remota asincrónica, el cliente debe inicializar el identificador asincrónico. Los programas de cliente y servidor usan punteros a la estructura de [**\_ \_ Estado de RPC Async**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) para los identificadores asincrónicos.

Cada llamada pendiente debe tener su propio identificador asincrónico único. El cliente crea el identificador y lo pasa a la función [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) . Para que la llamada se complete correctamente, el cliente debe asegurarse de que la memoria para el identificador no se libere hasta que reciba la respuesta asincrónica del servidor. Además, antes de realizar otra llamada en un identificador asincrónico existente, el cliente debe reinicializar el identificador. Si no lo hace, el código auxiliar del cliente puede provocar una excepción durante la llamada. El cliente también debe asegurarse de que los búferes que proporciona para los \[ parámetros [**out**](/windows/desktop/Midl/out-idl) \] y \[ [**en**](/windows/desktop/Midl/in), los parámetros **out** de \] un procedimiento remoto asincrónico permanecen asignados hasta que se ha recibido la respuesta del servidor.

Cuando invoca un procedimiento remoto asincrónico, el cliente debe seleccionar el método que la biblioteca en tiempo de ejecución de RPC utilizará para notificar la finalización de la llamada. El cliente puede recibir esta notificación de cualquiera de las siguientes maneras:

-   Ceso. El cliente puede especificar un evento que se va a desencadenar cuando se complete la llamada. Para obtener más información, consulte [objetos de evento](/windows/desktop/Sync/event-objects).
-   Sondeo. El cliente puede llamar repetidamente a [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Si el valor devuelto es distinto de RPC \_ S \_ Async \_ Call \_ Pending, se completa la llamada. Este método usa más tiempo de CPU que los otros métodos descritos aquí.
-   APC. El cliente puede especificar una [llamada a procedimiento asincrónico (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) que recibe una llamada cuando se completa la llamada. Para el prototipo de la función de APC, vea [**RPCNOTIFICATION ( \_ rutina**](/previous-versions/aa375808(v=vs.80))). Se llama al APC con su parámetro de evento establecido en RpcCallComplete. Para que APC se envíe, el subproceso del cliente debe estar en un estado de espera de alerta.

    Si el campo **hThread** del identificador asincrónico se establece en 0, el APC se pone en cola en el subproceso que realizó la llamada asincrónica. Si es distinto de cero, los APC se ponen en cola en el subproceso especificado por m.

-   IOC. El puerto de finalización de e/s recibe una notificación con los parámetros especificados en el identificador asincrónico. Para obtener más información, vea [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   Identificador de Windows. Se envía un mensaje al identificador de ventana especificado (HWND).

En el fragmento de código siguiente se muestran los pasos esenciales necesarios para inicializar un identificador asincrónico y usarlo para realizar una llamada asincrónica a un procedimiento remoto.


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



Como se muestra en este ejemplo, el programa cliente puede ejecutar llamadas a procedimiento remoto sincrónicas mientras una llamada a un procedimiento asincrónico todavía está pendiente. Este cliente crea un objeto de evento para que la biblioteca en tiempo de ejecución de RPC lo use para recibir una notificación cuando se complete la llamada asincrónica.

> [!Note]  
> La notificación de finalización no se devolverá desde una rutina RPC asincrónica si se genera una excepción RPC durante una llamada asincrónica.

 

 

 