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
# <a name="processing-requests"></a><span data-ttu-id="37c2b-103">Procesamiento de solicitudes</span><span class="sxs-lookup"><span data-stu-id="37c2b-103">Processing Requests</span></span>

<span data-ttu-id="37c2b-104">El procesamiento de solicitudes incluye cuatro pasos:</span><span class="sxs-lookup"><span data-stu-id="37c2b-104">Processing requests includes four steps:</span></span>

-   <span data-ttu-id="37c2b-105">Recibir una solicitud</span><span class="sxs-lookup"><span data-stu-id="37c2b-105">Receiving a request</span></span>
-   <span data-ttu-id="37c2b-106">Control de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37c2b-106">Handling the request</span></span>
-   <span data-ttu-id="37c2b-107">Enviar la respuesta</span><span class="sxs-lookup"><span data-stu-id="37c2b-107">Sending the response</span></span>
-   <span data-ttu-id="37c2b-108">Cancelar solicitudes que no se pueden procesar</span><span class="sxs-lookup"><span data-stu-id="37c2b-108">Canceling requests that cannot be processed</span></span>

![Diagrama que muestra el bucle de solicitud de proceso.](images/processloop.png)

## <a name="receiving-a-request"></a><span data-ttu-id="37c2b-110">Recibir una solicitud</span><span class="sxs-lookup"><span data-stu-id="37c2b-110">Receiving a Request</span></span>

<span data-ttu-id="37c2b-111">La API del servidor HTTP proporciona una estructura de solicitud para almacenar la solicitud de entrada analizada.</span><span class="sxs-lookup"><span data-stu-id="37c2b-111">The HTTP Server API supplies a request structure to store the parsed incoming request.</span></span> <span data-ttu-id="37c2b-112">La aplicación asigna esta estructura y se inicializa cuando se recibe una solicitud entrante.</span><span class="sxs-lookup"><span data-stu-id="37c2b-112">This structure is allocated by the application, and initialized when an incoming request is received.</span></span> <span data-ttu-id="37c2b-113">La aplicación llama a la función [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) para recibir la solicitud.</span><span class="sxs-lookup"><span data-stu-id="37c2b-113">The application calls the [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest) function to receive the request.</span></span> <span data-ttu-id="37c2b-114">Si el búfer de solicitud es demasiado pequeño para recibir la solicitud, la aplicación puede aumentar el tamaño del búfer y volver a llamar a **HttpReceiveHttpRequest** para recibir la solicitud completa.</span><span class="sxs-lookup"><span data-stu-id="37c2b-114">If the request buffer is too small to receive the request, the application can increase the buffer size and call **HttpReceiveHttpRequest** again to receive the entire request.</span></span>

<span data-ttu-id="37c2b-115">Si la solicitud incluye los datos del cuerpo de la entidad que se van a recibir, las aplicaciones llaman a [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) con el identificador de solicitud devuelto en el parámetro *pRequestBuffer* durante la llamada a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span><span class="sxs-lookup"><span data-stu-id="37c2b-115">If the request includes entity body data to be received, the applications calls [**HttpReceiveRequestEntityBody**](/windows/desktop/api/Http/nf-http-httpreceiverequestentitybody) with the request ID returned in the *pRequestBuffer* parameter during the call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest).</span></span>

## <a name="handling-the-request"></a><span data-ttu-id="37c2b-116">Control de la solicitud</span><span class="sxs-lookup"><span data-stu-id="37c2b-116">Handling the Request</span></span>

<span data-ttu-id="37c2b-117">La aplicación realiza el procesamiento específico de la aplicación de la solicitud y formula una respuesta.</span><span class="sxs-lookup"><span data-stu-id="37c2b-117">The application performs application-specific processing of the request and formulates a response.</span></span> <span data-ttu-id="37c2b-118">La API del servidor HTTP no impone ningún tiempo de espera en este proceso.</span><span class="sxs-lookup"><span data-stu-id="37c2b-118">The HTTP Server API imposes no timeout on this process.</span></span>

## <a name="sending-the-response"></a><span data-ttu-id="37c2b-119">Enviar la respuesta</span><span class="sxs-lookup"><span data-stu-id="37c2b-119">Sending the Response</span></span>

<span data-ttu-id="37c2b-120">Cuando la aplicación termina de administrar la solicitud y formula la respuesta, llama a la función [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) para enviar la respuesta.</span><span class="sxs-lookup"><span data-stu-id="37c2b-120">When the application is finished handling the request and formulating the response, it calls the [**HttpSendHttpResponse**](/windows/desktop/api/Http/nf-http-httpsendhttpresponse) function to send the response.</span></span> <span data-ttu-id="37c2b-121">Si la respuesta incluye los datos del cuerpo de la entidad que se van a enviar, la aplicación también llama a [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span><span class="sxs-lookup"><span data-stu-id="37c2b-121">If the response includes entity body data to send, the application also calls [HttpSendResponseEntityBody](/windows/desktop/api/Http/nf-http-httpsendresponseentitybody).</span></span>

## <a name="canceling-requests"></a><span data-ttu-id="37c2b-122">Cancelar solicitudes</span><span class="sxs-lookup"><span data-stu-id="37c2b-122">Canceling Requests</span></span>

<span data-ttu-id="37c2b-123">Una vez que la aplicación ha recibido un identificador de solicitud de su llamada a [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), puede cancelar la solicitud en cualquier momento llamando a [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span><span class="sxs-lookup"><span data-stu-id="37c2b-123">After the application has received a request ID from its call to [**HttpReceiveHttpRequest**](/windows/desktop/api/Http/nf-http-httpreceivehttprequest), it can at any time cancel the request by calling [HttpCancelHttpRequest](/windows/desktop/api/Http/nf-http-httpcancelhttprequest).</span></span>

 

 




