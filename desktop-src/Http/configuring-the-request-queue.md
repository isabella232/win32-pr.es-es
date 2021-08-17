---
title: Configuración de la cola de solicitudes
description: Configuración de la cola de solicitudes
ms.assetid: ab03089c-2ef1-457d-a5f5-a4d400f3a7f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e08a8f931d8875fda43b485bada93d2bf5291d0d2b90e85c8b31bd631e8c7fbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014933"
---
# <a name="configuring-the-request-queue"></a>Configuración de la cola de solicitudes

Cuando se abre o crea la cola de solicitudes, la aplicación que realiza la llamada recibe un identificador que se puede usar para enviar solicitudes o configurar la cola de solicitudes. Al llamar [**a HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** y proporcionar el identificador de cola de solicitudes en la estructura [**HTTP BINDING \_ \_ INFO,**](/windows/desktop/api/Http/ns-http-http_binding_info) especificada en el *parámetro pPropertyInformation,* se asocia el grupo de direcciones URL a la cola de solicitudes. Las propiedades de la cola de solicitudes solo las establece la aplicación que crea la cola de solicitudes. Por ejemplo, para establecer la propiedad de longitud de cola del servidor, la aplicación creator llama a [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) **especificando HttpServerQueueLengthProperty** en el *parámetro Property.*

 

 




