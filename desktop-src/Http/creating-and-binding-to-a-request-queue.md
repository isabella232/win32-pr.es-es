---
title: Crear y enlazar a una cola de solicitudes
description: Una cola de solicitudes es una cola de servicio que contiene solicitudes pendientes para una aplicación específica.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 945b8451f9128357b7da0ddc64600b74deffd0d7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418945"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Crear y enlazar a una cola de solicitudes

Una cola de solicitudes es una cola de servicio que contiene solicitudes pendientes para una aplicación específica. Una aplicación crea la cola de solicitudes independientemente del grupo de direcciones URL o la sesión del servidor mediante una llamada a la función [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) y establece las propiedades de la cola de solicitudes llamando a la función [**HttpSetRequestQueueProperty**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) . Estas propiedades son el nivel de detalle de las respuestas 503, la longitud máxima de la cola y el estado de la actividad.

Para hacer que las solicitudes se enruten a su cola de solicitudes, la aplicación enlaza el grupo de direcciones URL que creó como parte de la [configuración de tiempo de ejecución](run-time-configuration.md) a la cola mediante una llamada a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty** especificado en el parámetro *Property* . Las solicitudes entrantes de las direcciones URL del grupo se enrutan a la cola de solicitudes especificada.

 

 




