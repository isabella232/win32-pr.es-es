---
title: Procesamiento de solicitudes
description: El procesamiento de solicitudes incluye cuatro pasos.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ea69ca4e431a4ff1841f08913b33bcb7dd57128f327aaeeac158fb62ea7a7b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117996259"
---
# <a name="processing-requests"></a>Procesamiento de solicitudes

El procesamiento de solicitudes incluye cuatro pasos:

-   Recepción de una solicitud
-   Control de la solicitud
-   Envío de la respuesta
-   Cancelación de solicitudes que no se pueden procesar

![Diagrama que muestra el bucle de solicitud de proceso.](images/processloop.png)

## <a name="receiving-a-request"></a>Recepción de una solicitud

La API del servidor HTTP proporciona una estructura de solicitudes para almacenar la solicitud entrante analizada. La aplicación asigna esta estructura y se inicializa cuando se recibe una solicitud entrante. La aplicación llama a [**la función HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para recibir la solicitud. Si el búfer de solicitudes es demasiado pequeño para recibir la solicitud, la aplicación puede aumentar el tamaño del búfer y volver a llamar a **HttpReceiveHttpRequest** para recibir toda la solicitud.

Si la solicitud incluye los datos del cuerpo de la entidad que se va a recibir, las aplicaciones llaman a [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con el identificador de solicitud devuelto en el *parámetro pRequestBuffer* durante la llamada a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).

## <a name="handling-the-request"></a>Control de la solicitud

La aplicación realiza el procesamiento específico de la aplicación de la solicitud y formula una respuesta. La API del servidor HTTP no impone ningún tiempo de espera en este proceso.

## <a name="sending-the-response"></a>Envío de la respuesta

Cuando la aplicación termina de controlar la solicitud y formular la respuesta, llama a la [**función HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar la respuesta. Si la respuesta incluye datos del cuerpo de la entidad que se enviarán, la aplicación también llama a [HttpSendResponseEntityBody.](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody)

## <a name="canceling-requests"></a>Cancelación de solicitudes

Una vez que la aplicación ha recibido un identificador de solicitud de su llamada a [**HttpReceiveHttpRequest,**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest)puede cancelar la solicitud en cualquier momento llamando a [HttpCancelHttpRequest.](/windows/desktop/api/Http/nf-http-httpcancelhttprequest)

 

 




