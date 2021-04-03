---
title: Estado de llamada asincrónica
description: En esta página se describe el estado de la llamada asincrónica para las llamadas RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903887"
---
# <a name="asynchronous-call-state"></a>Estado de llamada asincrónica

En esta página se describe el estado de la llamada asincrónica para las llamadas RPC.

## <a name="client-behavior"></a>Comportamiento del cliente



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre del estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Hacer la llamada</td>
<td>Hacer que la RPC
<ul>
<li>En caso de éxito, vaya al estado WComp</li>
<li>Al final de la excepción</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>Poder</td>
<td>Cancelar la llamada</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp<br/></td>
</tr>
<tr class="odd">
<td>WComp</td>
<td>Esperar a que finalice</td>
<td>Espere a que se reciba la notificación de notificationCall complete<br/> Ir a comp<br/></td>
</tr>
<tr class="even">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final<br/></td>
</tr>
<tr class="odd">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a>Comportamiento del servidor



| Estado | Nombre del estado     | Acción                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D     | Dispatch       | La llamada se envía mediante el runtimeProcess de RPC<br/> Ir a comp<br/> Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final<br/> Para que se produzca un error: vaya a<br/> |
| A     | Anular la llamada | Llamar a [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ir al final<br/>                                                                                                                                             |
| Comp  | Completion     | Problema [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)ir al final<br/>                                                                                                                                      |
| End   |                |                                                                                                                                                                                                                     |



 

 

 





