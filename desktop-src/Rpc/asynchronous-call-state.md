---
title: Estado de llamada asincrónica
description: En esta página se describe el estado de llamada asincrónica para las llamadas RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db7ab00104b305ac87fa87883031d2425f229ce5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478631"
---
# <a name="asynchronous-call-state"></a>Estado de llamada asincrónica

En esta página se describe el estado de llamada asincrónica para las llamadas RPC.

## <a name="client-behavior"></a>Comportamiento del cliente




| State | Nombre del estado | Acción | 
|-------|------------|--------|
| C | Realización de la llamada | Realización de la RPC<ul><li>Si se ejecuta correctamente, vaya al estado WComp.</li><li>En la excepción, vaya a Fin.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| Enlatar | Cancelación de la llamada | Llamada <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>a RpcAsyncCancelCall</strong></a>Ir a WComp<br /> | 
| WComp | Esperar a la finalización | Espere a que se reciba la notificaciónCall-complete notification<br /> Ir a Comp<br /> | 
| Comp | Completion | Emisión <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>de RpcAsyncCompleteCall</strong></a>Ir al final<br /> | 
| End | 




 

## <a name="server-behavior"></a>Comportamiento del servidor



| State | Nombre del estado     | Acción                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | El runtimeProcess de RPC envía la llamada.<br/> Ir a Comp<br/> Para producir un error grave (mientras se ejecuta en el subproceso RPC): generar una excepción; vaya a End (Fin).<br/> Para producir un error correctamente: vaya a A.<br/> |
| A     | Anulación de la llamada | Llamada [**a RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Ir al final<br/>                                                                                                                                             |
| Comp  | Completion     | Emisión [**de RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Ir al final<br/>                                                                                                                                      |
| End   |                |                                                                                                                                                                                                                     |



 

 

 





