---
title: Control de errores (RPC)
description: En RPC sincrónico, un cliente realiza una llamada remota que devuelve con un código de error o correcto.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 017892b94438cc73f88cbfe60c03c088bf3ebcc9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078776"
---
# <a name="error-handling-rpc"></a>Control de errores (RPC)

En RPC sincrónico, un cliente realiza una llamada remota que devuelve con un código de error o correcto. RPC asincrónico proporciona más oportunidades para que se produzca un error en una llamada y estos errores se controlan de manera diferente, en función de dónde y cuándo se producen. En la tabla siguiente se describen las formas en que se puede producir un error en una llamada y cómo se administra.

## <a name="client-side-cleanup"></a>Limpieza del lado cliente



| Síntoma de error                                                                                                                                  | Limpieza                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| El cliente detecta una excepción cuando llama al procedimiento remoto.                                                                                  | No es necesaria ninguna llamada API de RPC. Se ha limpiado todo el estado de RPC.                                                              |
| El cliente recibe una notificación de llamada completa, pero cuando llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall), recibe un código de error. | No es necesaria ninguna llamada API de RPC. Se ha limpiado todo el estado de RPC.                                                              |
| El cliente emite una cancelación no anulada o anulada.                                                                                                   | El cliente debe esperar la notificación y llamar a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) cuando llega la notificación. |



 

En la limpieza del lado servidor, un concepto clave es el punto de la mano. Durante el procesamiento del lado servidor de una llamada asincrónica, normalmente se realiza algún procesamiento en el subproceso que recibió la llamada (también conocido como *subproceso de distribuidor*) y, a continuación, opcionalmente, el subproceso de distribuidor coloca el estado suficiente en un bloque de memoria y señala otro subproceso (también conocido como *subproceso de trabajo*) para continuar el procesamiento de la llamada. El momento en el que el subproceso de distribuidor indica correctamente que el subproceso de trabajo se denomina *punto de entrega*.

## <a name="server-side-cleanup"></a>Limpieza del lado servidor



| Error detectado      | Limpieza                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Antes del punto de entrega. | Excepción de inicio. No es necesario realizar ninguna llamada a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Después del punto de entrega.  | Llame a [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) o, si el error no es grave, y los resultados todavía se pueden devolver al cliente, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Si se produce un error en la llamada a la función **RpcAsyncCompleteCall** , el tiempo de ejecución de RPC libera los parámetros. El usuario no debe tener acceso a estos parámetros. El subproceso del distribuidor no debe realizar ningún procesamiento sustancial que pueda producir un error después del punto de la mano, porque ya no puede anular la llamada de forma segura. En concreto, no debe producir una excepción después del punto de la mano o el servidor puede bloquearse. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Casos especiales de control de errores para canalizaciones

Hay casos especiales para el control de errores al usar canalizaciones. En la lista siguiente se explica el origen del error y cómo controlar el error.



| Origen de error                                                                                                 | Cómo se controla                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| El cliente llama a la extracción y se produce un error en la llamada.                                                                             | No es necesaria ninguna llamada API de RPC. Se ha limpiado todo el estado de RPC.                                         |
| El cliente llama a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) antes de que se vacíen las canalizaciones [**de**](/windows/desktop/Midl/in) . | Se produce un error en la llamada con el código de error de relleno de canalización adecuado.                                                   |
| El cliente llama a Pull y se produce un error en la llamada.                                                                             | No es necesaria ninguna llamada API de RPC. Se ha limpiado todo el estado de RPC.                                         |
| El cliente o el servidor llama a la inserción o extracción en el orden equivocado.                                                    | Tiempo de ejecución devuelve el estado de error de rellenado de canalización.                                                                |
| El servidor llama a la inserción o extracción y se produce un error en la llamada.                                                                     | La extracción devuelve un código de error. No es necesario realizar ninguna llamada a [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) . |
| El servidor llama a **RpcAsyncCompleteCall** antes de que se hayan purgado las canalizaciones.                                         | La llamada de canalización devuelve un estado de error de llenado de canalización.                                                         |
| Después del envío, se produce un error en una operación de recepción.                                                                    | La próxima vez que el servidor llame a pull para recibir los datos de canalización, se devuelve un error.                            |



 

 

 
