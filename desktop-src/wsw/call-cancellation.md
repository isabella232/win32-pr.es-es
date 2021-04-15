---
title: Cancelación de llamada
description: La notificación de cancelación de llamada cancela el funcionamiento de las operaciones de servicio del lado servidor y las devoluciones de llamada del modelo de servicio.
ms.assetid: dc371921-869f-4775-98d3-80a1006358ba
keywords:
- Llamar a servicios Web de cancelación para Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5107f9ece421a3130f99c78b3b33788ee6c7e9f0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "105695808"
---
# <a name="call-cancellation"></a>Cancelación de llamada

La notificación de cancelación de llamada cancela el funcionamiento de [las operaciones de servicio del lado servidor y las](server-side-service-operations.md) devoluciones de llamada del modelo de servicio. Dicha cancelación puede ser por uno de estos dos motivos:

-   El host de servicio ha detenido las operaciones debido a una llamada a la función [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost) .
-   El canal subyacente ha generado un error.


Para recibir una notificación de cancelación, la operación de servicio o la devolución de llamada del modelo de servicio deben registrar una devolución de [](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) llamada de [**devolución de llamada de \_ cancelación de operación \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) llamando a la función WsRegisterOperationForCancel.

Opcionalmente, como parte del registro de la notificación de cancelación, la operación de servicio o la devolución de llamada del modelo de servicio también puede registrar datos de estado específicos de la aplicación y la devolución de llamada de [**\_ devolución de \_ \_ \_ llamada de estado de la operación WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) .

Los datos de estado se ponen a disposición de la devolución de llamada de cancelación de la [**\_ operación \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback) . Al finalizar la llamada, se llama a la devolución de llamada de devolución de llamada de estado de la [**\_ operación \_ \_ \_ WS**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) para ofrecer a la aplicación la oportunidad de liberar los datos de estado.

Para obtener un ejemplo de código, vea [BlockingServiceExample](blockingserviceexample.md).

Solo se llama una vez a la devolución de llamada de cancelación para la duración de las [operaciones del servicio del servidor](server-side-service-operations.md) o de la función de devolución de llamada.

La cancelación de llamadas está disponible en para todas las devoluciones de llamada de host de servicio que toman el [ \_ \_ contexto de operación WS](ws-operation-context.md) como parámetro.

Los siguientes elementos de la API se relacionan con la cancelación de llamadas.

| Devolución de llamada                                                                         | Descripción                                                                                                                                |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_devolución de \_ llamada de cancelación de operación WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)          | Invocado por el modelo de servicio para notificar la cancelación de una operación de servicio asincrónica como resultado de un cierre del host de servicio anulado. |
| [**\_devolución de \_ \_ llamada de estado libre de operación WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback) | Invocado por el modelo de servicio para permitir que una aplicación Limpie los datos de estado que se registraron con la devolución de llamada de cancelación.                |



 



| Función                                                             | Descripción                                                                                       |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**WsRegisterOperationForCancel**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) | Permite a una operación de servicio o a una devolución de llamada del modelo de servicio registrarse para una notificación de cancelación. |



 

 

 




