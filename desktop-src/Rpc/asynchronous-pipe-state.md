---
title: Estado de canalización asincrónica
description: En esta página se describe el estado de canalización asincrónica para las llamadas RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35e54d9f86228cb4c957f53411c105e20e2109
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122468172"
---
# <a name="asynchronous-pipe-state"></a>Estado de canalización asincrónica

En esta página se describe el estado de canalización asincrónica para las llamadas RPC.

## <a name="in-pipe"></a>Canalización IN

Comportamiento del cliente


| State | Nombre de estado | Acción | 
|-------|------------|--------|
| C | Realización de la llamada | Realización de la RPC<ul><li>Si se ejecuta correctamente, vaya al estado WS</li><li>En la excepción, vaya a Fin.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| P | Insertar | Realizar una inserción<ul><li>En caso de error, vaya a End (Fin).</li><li>Si se ejecuta correctamente, vaya a WS.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| WS | Wait for Send | Esperar notificación<ul><li>En caso de error al obtener una notificación, vaya a Can (Puede)</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y es necesario enviar más datos, vaya a P.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete</strong></a> correctamente y no es necesario enviar más datos, vaya a NP.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un error RpcCallComplete,</strong></a> vaya a Comp.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| NP | Inserción nula | Inserción de 0 bytes (inserción nula)<ul><li>En caso de error, vaya a End (Fin).</li><li>Si se ejecuta correctamente, vaya a WComp.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| Enlatar | Cancelar la llamada | Llamada <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>a RpcAsyncCancelCall</strong></a>Ir a WComp<br /> | 
| WComp | Esperar a la finalización | Espere a que se reciba la notificaciónCall-complete notification.<br /> Ir a Comp<br /> | 
| Comp | Completion | Emisión <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>de RpcAsyncCompleteCall</strong></a>Ir al final<br /> | 
| End | 




 

Comportamiento del servidor


| State | Nombre de estado | Acción | 
|-------|------------|--------|
| D | Dispatch | El tiempo de ejecución de RPC envía la llamada a P.<br /> Para producir un error grave (mientras se ejecuta en el subproceso RPC): generar una excepción; vaya a End (Fin).<br /> Para producir un error correctamente: vaya a A.<br /> | 
| P | Extracción | Realizar una extracción<ul><li>En caso de error, vaya a End (Fin).</li><li>Si la finalización es correcta y sincrónica con bytes distintos de cero, vaya a P.</li><li>Si la finalización es correcta y sincrónica con cero bytes leídos (extracción nula), vaya a Comp.</li><li>Si la finalización es correcta y asincrónica (ERROR_IO_PENDING se devuelve), vaya a WP.</li></ul>Para producir un error: vaya a A.<br /> | 
| WP | Esperar a la extracción | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a A.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un error RpcReceiveComplete,</strong></a> vaya a A.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> bytes distintos de cero, vaya a P.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> cero bytes leídos (extracción nula), vaya a Comp.</li><li>Si se recibe un error, vaya a A.</li></ul>Para producir un error: vaya a A.<br /> | 
| A | Anular la llamada | Llamada <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>a RpcAsyncAbortCall</strong></a>Ir al final<br /> | 
| Comp | Completion | Llamada <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>a RpcAsyncCompleteCall</strong></a>Ir al final<br /> | 
| End | 




 

## <a name="out-pipe"></a>Canalización OUT

Comportamiento del cliente


| State | Nombre de estado | Acción | 
|-------|------------|--------|
| C | Realización de la llamada | Realización de la RPC<ul><li>Si se ejecuta correctamente, vaya a P.</li><li>En caso de error, vaya a Comp</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| P | Extracción | Realizar una extracción<ul><li>En caso de error, vaya a End (Fin).</li><li>Si la finalización es correcta y sincrónica con bytes distintos de cero, vaya a P.</li><li>Si la finalización es correcta y sincrónica con cero bytes leídos (extracción nula), vaya a WComp.</li><li>Si la finalización es correcta y asincrónica (ERROR_IO_PENDING se devuelve), vaya a WP.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| WP | Esperar a la extracción | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a Puede.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un error RpcReceiveComplete,</strong></a> vaya a Puede.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> bytes distintos de cero, vaya a P.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> cero bytes leídos (extracción nula), vaya a Comp.</li><li>Si se recibe un error, vaya a Puede.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| Enlatar | Cancelar la llamada | Llamada <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>a RpcAsyncCancelCall</strong></a>Ir a WComp<br /> | 
| WComp | Esperar a la finalización | Espere la notificación. Se debe recibir una notificación de llamada completa.<br /> Vaya a Comp<br /> | 
| Comp | Completion | Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Ir al final<br /> | 
| End | 




 

Comportamiento del servidor


| State | Nombre de estado | Acción | 
|-------|------------|--------|
| D | Dispatch | El tiempo de ejecución de RPC envía la llamada a P.<br /> Para producir un error grave (mientras se ejecuta en el subproceso RPC): generar una excepción; vaya a End (Fin).<br /> Para producir un error correctamente: vaya a A.<br /> | 
| P | Insertar | Realizar una inserción<ul><li>En caso de éxito, vaya a WP.</li><li>En caso de error, vaya a End (Fin).</li></ul>Para producir un error: vaya a A.<br /> | 
| WP | Espera de inserción | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a A.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y es necesario enviar más datos, vaya a P.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y no es necesario enviar más datos, vaya a NP.</li><li>Si se recibe un error, vaya a Comp.</li></ul>Para producir un error: vaya a A.<br /> | 
| NP | Inserción nula | Inserción de 0 bytes<ul><li>en caso de éxito, vaya a WNP.</li><li>en caso de error, vaya a Comp</li></ul>Para producir un error: vaya a A.<br /> | 
| WNP | Espera de inserción nula | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a A.</li><li>Si se recibe un error, vaya a Comp.</li><li>Si se recibe correctamente, vaya a Comp.</li></ul> | 
| A | Anular la llamada | Llame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>a RpcAsyncAbortCall</strong></a>; vaya a End (Fin). | 
| Comp | Completion | Emita <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; vaya a End (Fin). | 
| End | 




 

## <a name="in-out-pipe"></a>Canalización IN-OUT

Comportamiento del cliente


| State | Nombre de estado | Acción | 
|-------|------------|--------|
| C | Realización de la llamada | Realización de rpc<ul><li>En caso de éxito, vaya a WS</li><li>En la excepción, vaya a End (Fin).</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| PS | Insertar | Realizar una inserción<ul><li>En caso de error, vaya a End (Fin).</li><li>En caso de éxito, vaya a WS</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| WS | Wait for Send | Esperar notificación<ul><li>En caso de error al obtener una notificación, vaya a Puede.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y es necesario enviar más datos, vaya a PS.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y no es necesario enviar más datos, vaya a NP.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un error RpcCallComplete,</strong></a> vaya a Comp.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| NP | Inserción nula | Inserción de 0 bytes (inserción nula)<ul><li>En caso de error, vaya a End (Fin).</li><li>Si se ejecuta correctamente, vaya a PL.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| PL | Extracción | Realizar una extracción<ul><li>En caso de error, vaya a End (Fin).</li><li>En caso de finalización correcta y sincrónica con bytes distintos de cero, vaya a PL.</li><li>Si la finalización es correcta y sincrónica con cero bytes leídos (extracción nula), vaya a WComp.</li><li>Si la finalización es correcta y asincrónica (ERROR_IO_PENDING se devuelve), vaya a WPL.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| WPL | Esperar a la extracción | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a Puede.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un error RpcReceiveComplete,</strong></a> vaya a Puede.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> bytes distintos de cero, vaya a PL.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> cero bytes leídos, vaya a Comp.</li><li>Si se recibe un error, vaya a Puede.</li></ul>Para producir un error: vaya a Can (Puede)<br /> | 
| Enlatar | Cancelar la llamada | Llamada <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>a RpcAsyncCancelCall</strong></a>Ir a WComp<br /> | 
| WComp | Esperar a la finalización | Espere la notificación. Se debe recibir la notificación CallComplete.<br /> Vaya a Comp<br /> | 
| Comp | Completion | Emitir <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Ir al final<br /> | 
| End | 




 

Comportamiento del servidor


| State | Nombre de estado | Acción | 
|-------|------------|--------|
| D | Dispatch | El runtime de RPC envía la llamada a PL.<br /> Para producir un error grave (mientras se ejecuta en el subproceso RPC): generar una excepción; vaya a End (Fin).<br /> Para producir un error correctamente: vaya a A.<br /> | 
| PL | Extracción | Realizar una extracción<ul><li>En caso de error, vaya a End (Fin).</li><li>En caso de finalización correcta y sincrónica con bytes distintos de cero, vaya a PL.</li><li>Si la finalización es correcta y sincrónica con cero bytes leídos (extracción nula), vaya a PS.</li><li>Si la finalización es correcta y asincrónica (ERROR_IO_PENDING se devuelve), vaya a WPL.</li></ul>Para producir un error: vaya a A<br /> | 
| WPL | Esperar a la extracción | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a A.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>un error RpcReceiveComplete,</strong></a> vaya a A.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> bytes distintos de cero, vaya a PL.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcReceiveComplete correctamente con</strong></a> cero bytes leídos, vaya a PS.</li><li>Si se recibe un error, vaya A.</li></ul>Para producir un error: vaya a A<br /> | 
| PS | Insertar | Realizar una inserción<ul><li>En caso de éxito, vaya a WPS.</li><li>En caso de error, vaya a End (Fin).</li></ul>Para producir un error: vaya a A<br /> | 
| WPS | Esperar inserción | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a A.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y es necesario enviar más datos, vaya a PS.</li><li>Si se recibe <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>rpcSendComplete correctamente</strong></a> y no es necesario enviar más datos, vaya a NP.</li><li>Si se recibe un error, vaya a Comp.</li></ul>Para producir un error: vaya a A<br /> | 
| NP | Inserción nula | Inserción de 0 bytes<ul><li>en caso de éxito, vaya a WNP.</li><li>en caso de error, vaya a Comp</li></ul>Para producir un error: vaya a A<br /> | 
| WNP | Espera de inserción nula | Esperar notificación<ul><li>Si no se puede obtener una finalización, vaya a A.</li><li>Si se recibe un error, vaya a Comp.</li><li>Si se recibe correctamente, vaya a Comp.</li></ul><br /> | 
| A | Anular la llamada | Llame <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>a RpcAsyncAbortCall</strong></a>; vaya a End (Fin). | 
| Comp | Completion | Emita <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; vaya a End (Fin). | 
| End | 




 

 

 





