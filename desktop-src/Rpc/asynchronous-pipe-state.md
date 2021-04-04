---
title: Estado de canalización asincrónica
description: En esta página se describe el estado de la canalización asincrónica para las llamadas RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077325"
---
# <a name="asynchronous-pipe-state"></a>Estado de canalización asincrónica

En esta página se describe el estado de la canalización asincrónica para las llamadas RPC.

## <a name="in-pipe"></a>EN canalización

Comportamiento del cliente

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre de estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Hacer la llamada</td>
<td>Hacer que la RPC
<ul>
<li>En caso de éxito, vaya a estado WS</li>
<li>Al final de la excepción</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Inserción</td>
<td>Hacer una inserciones
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito, vaya a WS</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Esperar envío</td>
<td>Esperar notificación
<ul>
<li>Si se produce un error al recibir una notificación, puede</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a P</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</li>
<li>Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a></li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Inserciones nulas</td>
<td>Inserte 0 bytes (inserciones nulas)
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito, vaya a WComp</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="odd">
<td>Poder</td>
<td>Cancelar la llamada</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Esperar a que finalice</td>
<td>Espere a que se reciba la notificación de notificationCall complete.<br/> Ir a comp<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

Comportamiento del servidor

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre de estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>La llamada se envía mediante el tiempo de ejecución de RPC Go a P<br/> Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final<br/> Para que se produzca un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Extracción</td>
<td>Crear una extracción
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to P</li>
<li>En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula) vaya a comp</li>
<li>En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WP</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Esperar a la extracción</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un error de <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , vaya a un</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con una lectura de bytes distinta de cero, vaya a P</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos (extracción nula) vaya a comp</li>
<li>Si se recibe un error, vaya a</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>Anular la llamada</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>ir al final<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a>Canalización de salida

Comportamiento del cliente

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre de estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Hacer la llamada</td>
<td>Hacer que la RPC
<ul>
<li>En caso de éxito, vaya a P</li>
<li>En caso de error, vaya a comp</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Extracción</td>
<td>Crear una extracción
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to P</li>
<li>En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula), vaya a WComp</li>
<li>En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WP</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Esperar a la extracción</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , ir a puede</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con una lectura de bytes distinta de cero, vaya a P</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos (extracción nula) vaya a comp</li>
<li>Si se recibe un error, puede</li>
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
<td>Esperar notificación. Se debe recibir la notificación de llamada completa.<br/> Ir a comp<br/></td>
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



 

Comportamiento del servidor

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre de estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>La llamada se envía mediante el tiempo de ejecución de RPC Go a P<br/> Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final<br/> Para que se produzca un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>P</td>
<td>Inserción</td>
<td>Hacer una inserciones
<ul>
<li>En caso de éxito, vaya a WP</li>
<li>En caso de error, ir al final</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="odd">
<td>WP</td>
<td>Esperar a la inserciones</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a P</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</li>
<li>Si se recibe un error de la comp.</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Inserciones nulas</td>
<td>Inserte 0 bytes
<ul>
<li>en caso de éxito, vaya a WNP</li>
<li>en caso de error, vaya a comp</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="odd">
<td>PERSISTENTE</td>
<td>Esperar una inserciones nulas</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un error de la comp.</li>
<li>Si se ha recibido un éxito</li>
</ul></td>
</tr>
<tr class="even">
<td>A</td>
<td>Anular la llamada</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir al final</td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir al final</td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a>Canalización de salida

Comportamiento del cliente

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre de estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>C</td>
<td>Hacer la llamada</td>
<td>Hacer que la RPC
<ul>
<li>En caso de éxito, vaya a WS</li>
<li>Al final de la excepción</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Inserción</td>
<td>Hacer una inserciones
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito, vaya a WS</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="odd">
<td>WS</td>
<td>Esperar envío</td>
<td>Esperar notificación
<ul>
<li>Si se produce un error al recibir una notificación, puede</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a PS</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</li>
<li>Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a></li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Inserciones nulas</td>
<td>Inserte 0 bytes (inserciones nulas)
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito, vaya a PL</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="odd">
<td>PL</td>
<td>Extracción</td>
<td>Crear una extracción
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to PL</li>
<li>En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula), vaya a WComp</li>
<li>En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WPL</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="even">
<td>WPL</td>
<td>Esperar a la extracción</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un error <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , ir a puede</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con bytes de lectura distintos de cero, vaya a PL</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos, vaya a comp</li>
<li>Si se recibe un error, puede</li>
</ul>
En error: ir a<br/></td>
</tr>
<tr class="odd">
<td>Poder</td>
<td>Cancelar la llamada</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>ir a WComp<br/></td>
</tr>
<tr class="even">
<td>WComp</td>
<td>Esperar a que finalice</td>
<td>Esperar notificación. Se debe recibir la notificación de CallComplete.<br/> Ir a comp<br/></td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>ir al final<br/></td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

Comportamiento del servidor

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Estado</th>
<th>Nombre de estado</th>
<th>Acción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D</td>
<td>Dispatch</td>
<td>La llamada se envía mediante el runtimeGo de RPC a PL<br/> Para producir un error irrecuperable (mientras se ejecuta en el subproceso RPC): generar excepción; ir al final<br/> Para que se produzca un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>PL</td>
<td>Extracción</td>
<td>Crear una extracción
<ul>
<li>En caso de error, ir al final</li>
<li>En caso de éxito y finalización sincrónica con bytes distintos de cero, lea Go to PL</li>
<li>En caso de éxito y finalización sincrónica con cero bytes leídos (extracción nula), vaya a PS</li>
<li>En caso de éxito y finalización asincrónica (se devuelve ERROR_IO_PENDING) vaya a WPL</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="odd">
<td>WPL</td>
<td>Esperar a la extracción</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un error de <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> , vaya a un</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con bytes de lectura distintos de cero, vaya a PL</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> correcto con cero bytes leídos, vaya a PS</li>
<li>Si se recibe un error, vaya A</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>PS</td>
<td>Inserción</td>
<td>Hacer una inserciones
<ul>
<li>En caso de éxito, vaya a WPS</li>
<li>En caso de error, ir al final</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="odd">
<td>WPS</td>
<td>Esperar a la inserciones</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y es necesario enviar más datos, vaya a PS</li>
<li>Si se recibe un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> correcto y no es necesario enviar más datos, vaya a NP</li>
<li>Si se recibe un error de la comp.</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="even">
<td>NP</td>
<td>Inserciones nulas</td>
<td>Inserte 0 bytes
<ul>
<li>en caso de éxito, vaya a WNP</li>
<li>en caso de error, vaya a comp</li>
</ul>
Para generar un error: vaya a<br/></td>
</tr>
<tr class="odd">
<td>PERSISTENTE</td>
<td>Esperar una inserciones nulas</td>
<td>Esperar notificación
<ul>
<li>En caso de error al obtener una finalización, vaya a</li>
<li>Si se recibe un error de la comp.</li>
<li>Si se ha recibido un éxito</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td>A</td>
<td>Anular la llamada</td>
<td>Llamar a <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; ir al final</td>
</tr>
<tr class="odd">
<td>Comp</td>
<td>Completion</td>
<td>Problema <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; ir al final</td>
</tr>
<tr class="even">
<td>End</td>


</tr>
</tbody>
</table>



 

 

 





