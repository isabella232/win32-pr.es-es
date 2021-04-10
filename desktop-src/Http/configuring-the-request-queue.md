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
# <a name="configuring-the-request-queue"></a>Configuración de la cola de solicitudes

Cuando se abre o se crea la cola de solicitudes, la aplicación que realiza la llamada recibe un identificador que se puede usar para enviar solicitudes o configurar la cola de solicitudes. La llamada a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** y la especificación del identificador de la cola de solicitudes en la estructura de  [**\_ \_ información de enlace http**](/windows/desktop/api/Http/ns-http-http_binding_info) , especificada en el parámetro pPropertyInformation, asocia el grupo de direcciones URL a la cola de solicitudes. Las propiedades de la cola de solicitudes solo se establecen en la aplicación que crea la cola de solicitudes. Por ejemplo, para establecer la propiedad longitud de la cola del servidor, la aplicación creador llama a [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) especificando **HttpServerQueueLengthProperty** en el parámetro *Property* .

 

 




