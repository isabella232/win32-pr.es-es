---
title: Control de errores (RPC)
description: En RPC sincrónica, un cliente realiza una llamada remota que devuelve con un código correcto o de error.
ms.assetid: 7dfc9f84-ce3c-49f3-8f72-b212095133fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6daf29091602c36a23c0ed7e08eb0459985e13ca26ec128f401754f64c2329ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021665"
---
# <a name="error-handling-rpc"></a>Control de errores (RPC)

En RPC sincrónica, un cliente realiza una llamada remota que devuelve con un código correcto o de error. RPC asincrónica proporciona más oportunidades para que se produzca un error en una llamada y estos errores se controlan de forma diferente, en función de dónde y cuándo se produzcan. En la tabla siguiente se describen las formas en que se puede producir un error en una llamada y cómo se controla.

## <a name="client-side-cleanup"></a>Limpieza del lado cliente



| Síntoma de error                                                                                                                                  | Limpieza                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| El cliente detecta una excepción cuando llama al procedimiento remoto.                                                                                  | No se necesita ninguna llamada API RPC. Se ha limpiado todo el estado RPC.                                                              |
| El cliente recibe una notificación completa de llamada, pero cuando llama a [**RpcAsyncCompleteCall,**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)recibe un código de error. | No se necesita ninguna llamada API RPC. Se ha limpiado todo el estado RPC.                                                              |
| El cliente emite una cancelación no abortiva o anulativa.                                                                                                   | El cliente debe esperar la notificación y llamar [**a RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) cuando llegue la notificación. |



 

En la limpieza del lado servidor, un concepto clave es el punto de entrega. Durante el procesamiento del lado servidor de una llamada asincrónica, se suele realizar algún procesamiento en el subproceso que recibió la llamada (también conocido como subproceso de *distribuidor)* y, opcionalmente, el subproceso de distribuidor coloca el estado suficiente en un bloque de memoria y señala a otro subproceso (también conocido como subproceso de *trabajo)* para continuar el procesamiento de la llamada. Momento en el que el subproceso de distribuidor indica correctamente que el subproceso de trabajo se denomina punto *de entrega*.

## <a name="server-side-cleanup"></a>Limpieza del lado servidor



| Error detectado      | Limpieza                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Antes del punto de entrega. | Iniciar excepción. No es necesaria [**ninguna llamada a RpcAsyncCompleteCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Después del punto de entrega.  | Llame [**a RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall) o, si el error no es grave y los resultados todavía se pueden devolver al cliente, [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall). Si se produce un error en la llamada a la función **RpcAsyncCompleteCall,** el tiempo de ejecución de RPC libera los parámetros. El usuario no debe tener acceso a esos parámetros. El subproceso del distribuidor no debe realizar ningún procesamiento sustancial que pueda producir un error después del punto de entrega, ya que ya no puede anular la llamada de forma segura. En concreto, no debe producir una excepción después del punto de entrega o el servidor puede bloquearse. |



 

## <a name="special-error-handling-cases-for-pipes"></a>Casos especiales de control de errores para canalizaciones

Hay casos especiales para el control de errores al usar canalizaciones. En la lista siguiente se explica el origen del error y cómo controlar el error.



| Origen del error                                                                                                 | Cómo se controla                                                                                                |
|-------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| El cliente llama a push y se produce un error en la llamada.                                                                             | No se necesita ninguna llamada API RPC. Se ha limpiado todo el estado RPC.                                         |
| El cliente llama [**a RpcAsyncCompleteCall antes**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) de [**purgar**](/windows/desktop/Midl/in) las canalizaciones de entrada. | Se produce un error en la llamada con el código de error de relleno de canalización adecuado.                                                   |
| El cliente llama a pull y se produce un error en la llamada.                                                                             | No se necesita ninguna llamada API RPC. Se ha limpiado todo el estado RPC.                                         |
| El cliente o el servidor llaman a inserción o extracción en el orden incorrecto.                                                    | El tiempo de ejecución devuelve el estado de error de relleno de canalización.                                                                |
| El servidor llama a push o pull y se produce un error en la llamada.                                                                     | La inserción devuelve un código de error. No es necesaria [**ninguna llamada a RpcAsyncCompleteCall.**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) |
| El servidor llama **a RpcAsyncCompleteCall antes** de que se hayan purgado las canalizaciones.                                         | La llamada de canalización devuelve un estado de error de relleno de canalización.                                                         |
| Después de la distribución, se produce un error en una operación de recepción.                                                                    | La próxima vez que el servidor llame a pull para recibir datos de canalización, se devuelve un error.                            |



 

 

 
