---
title: Configuración de la cola de solicitudes
description: Configuración de la cola de solicitudes
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42ed397ffbcb42d887d519bc4492bd167dd98c57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903466"
---
# <a name="configuring-the-request-queue"></a><span data-ttu-id="ef14b-103">Configuración de la cola de solicitudes</span><span class="sxs-lookup"><span data-stu-id="ef14b-103">Configuring the Request Queue</span></span>

<span data-ttu-id="ef14b-104">Cuando se abre o se crea la cola de solicitudes, la aplicación que realiza la llamada recibe un identificador que se puede usar para enviar solicitudes o configurar la cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="ef14b-104">When the request queue is opened or created, the calling application receives a handle to it that can be used to send requests or configure the request queue.</span></span> <span data-ttu-id="ef14b-105">La llamada a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** y la especificación del identificador de la cola de solicitudes en la estructura de  [**\_ \_ información de enlace http**](/windows/desktop/api/Http/ns-http-http_binding_info) , especificada en el parámetro pPropertyInformation, asocia el grupo de direcciones URL a la cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="ef14b-105">Calling [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) with **HttpServerBindingProperty** and supplying the request queue handle in the [**HTTP\_BINDING\_INFO**](/windows/desktop/api/Http/ns-http-http_binding_info) structure, specified in the *pPropertyInformation* parameter, associates the URL group with the request queue.</span></span> <span data-ttu-id="ef14b-106">Las propiedades de la cola de solicitudes solo se establecen en la aplicación que crea la cola de solicitudes.</span><span class="sxs-lookup"><span data-stu-id="ef14b-106">Request queue properties are set only by the application that creates the request queue.</span></span> <span data-ttu-id="ef14b-107">Por ejemplo, para establecer la propiedad longitud de la cola del servidor, la aplicación creador llama a [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) especificando **HttpServerQueueLengthProperty** en el parámetro *Property* .</span><span class="sxs-lookup"><span data-stu-id="ef14b-107">For example, to set the server queue length property, the creator application calls [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) specifying **HttpServerQueueLengthProperty** in the *Property* parameter.</span></span>

 

 




