---
title: Cancelación de llamadas
description: La notificación de cancelación de llamadas cancela el funcionamiento de las operaciones de servicio del lado servidor y las devoluciones de llamada del modelo de servicio.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Llamar a servicios web de cancelación para Windows
- WWSAPI
- Wws
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dda4ec4227403bed5239b68cfa05d2064976517a7473fa7926c8de5f56227645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026703"
---
# <a name="call-cancellation"></a>Cancelación de llamadas

La notificación de cancelación de llamadas cancela el funcionamiento de las operaciones de servicio [del lado servidor](server-side-service-operations.md) y las devoluciones de llamada del modelo de servicio. Esta cancelación puede deberse a uno de estos dos motivos:

-   El host de servicio ha detenido las operaciones debido a una llamada a la [**función WsAbortServiceHost.**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)
-   El canal subyacente ha producido un error.


Para recibir una notificación de cancelación, la operación de servicio o la devolución de llamada del modelo de servicio deben registrar una devolución de llamada [**WS \_ OPERATION CANCEL \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) llamando a la [**función WsRegisterOperationForCancel.**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel)

Opcionalmente, como parte del registro para la notificación de cancelación, la operación de servicio o la devolución de llamada del modelo de servicio también pueden registrar datos de estado específicos de la aplicación y la devolución de llamada [**WS \_ OPERATION FREE \_ STATE \_ \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)

Los datos de estado están disponibles para la devolución de llamada [**\_ WS OPERATION \_ CANCEL \_ CALLBACK.**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) Al finalizar la llamada, se llama a la devolución de llamada [**WS \_ OPERATION FREE \_ STATE \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) para dar a la aplicación la oportunidad de liberar los datos de estado.

Para obtener un ejemplo de código, [vea BlockingServiceExample](blockingserviceexample.md).

La devolución de llamada de cancelación solo se llama una vez durante la vigencia de las operaciones de [servicio del lado](server-side-service-operations.md) servidor o la función de devolución de llamada.

La cancelación de llamadas está disponible en para todas las devoluciones de llamada de host de servicio que toman [WS \_ OPERATION \_ CONTEXT](ws-operation-context.md) como parámetro.

Los siguientes elementos de API se relacionan con la cancelación de llamadas.

| Devolución de llamada                                                                         | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**WS \_ OPERATION \_ CANCEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Invocado por el modelo de servicio para notificar una cancelación de una operación de servicio asincrónica como resultado de un apagado anulado del host de servicio. |
| [**WS \_ OPERATION \_ FREE \_ STATE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Invocado por el modelo de servicio para permitir que una aplicación limpie los datos de estado registrados con la devolución de llamada de cancelación.                |



 



| Función                                                             | Descripción                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Permite que una operación de servicio o una devolución de llamada de modelo de servicio se registren para una notificación de cancelación. |



 

 

 




