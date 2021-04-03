---
title: Procesamiento de solicitudes
description: El procesamiento de solicitudes incluye cuatro pasos.
ms.assetid: fb170d73-c26d-4bec-abed-b614b7dad322
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e820d425e44daab9d687d1d43b756b833582a092
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2021
ms.locfileid: "103913965"
---
# <a name="processing-requests"></a>Procesamiento de solicitudes

El procesamiento de solicitudes incluye cuatro pasos:

-   Recibir una solicitud
-   Control de la solicitud
-   Enviar la respuesta
-   Cancelar solicitudes que no se pueden procesar

![Diagrama que muestra el bucle de solicitud de proceso.](images/processloop.png)

## <a name="receiving-a-request"></a>Recibir una solicitud

La API del servidor HTTP proporciona una estructura de solicitud para almacenar la solicitud de entrada analizada. La aplicación asigna esta estructura y se inicializa cuando se recibe una solicitud entrante. La aplicación llama a la función [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para recibir la solicitud. Si el búfer de solicitud es demasiado pequeño para recibir la solicitud, la aplicación puede aumentar el tamaño del búfer y volver a llamar a **HttpReceiveHttpRequest** para recibir la solicitud completa.

Si la solicitud incluye los datos del cuerpo de la entidad que se van a recibir, las aplicaciones llaman a [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con el identificador de solicitud devuelto en el parámetro *pRequestBuffer* durante la llamada a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).

## <a name="handling-the-request"></a>Control de la solicitud

La aplicación realiza el procesamiento específico de la aplicación de la solicitud y formula una respuesta. La API del servidor HTTP no impone ningún tiempo de espera en este proceso.

## <a name="sending-the-response"></a>Enviar la respuesta

Cuando la aplicación termina de administrar la solicitud y formula la respuesta, llama a la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar la respuesta. Si la respuesta incluye los datos del cuerpo de la entidad que se van a enviar, la aplicación también llama a [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).

## <a name="canceling-requests"></a>Cancelar solicitudes

Una vez que la aplicación ha recibido un identificador de solicitud de su llamada a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), puede cancelar la solicitud en cualquier momento llamando a [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).

 

 




