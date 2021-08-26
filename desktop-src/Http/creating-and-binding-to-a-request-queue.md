---
title: Creación y enlace a una cola de solicitudes
description: Una cola de solicitudes es una cola de servicio que contiene solicitudes pendientes para una aplicación específica.
ms.assetid: 93f8b230-af0a-4582-b35b-d65f6841e525
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24c3a36fbbb9a8bcaa1c4e708240e99c276b09448ca56615df7da3d2cdf26836
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914285"
---
# <a name="creating-and-binding-to-a-request-queue"></a>Creación y enlace a una cola de solicitudes

Una cola de solicitudes es una cola de servicio que contiene solicitudes pendientes para una aplicación específica. Una aplicación crea la cola de solicitudes independientemente del grupo de direcciones URL o la sesión del servidor mediante una llamada a la función [**HttpCreateRequestQueue**](/windows/desktop/api/Http/nf-http-httpcreaterequestqueue) y establece las propiedades de la cola de solicitudes mediante una llamada a la [**función HttpSetRequestQueueProperty.**](/windows/desktop/api/Http/nf-http-httpsetrequestqueueproperty) Estas propiedades son el nivel de detalle de 503 respuestas, la longitud máxima de la cola y el estado de la actividad.

Para hacer que las solicitudes se enruten a su cola de solicitudes, la aplicación enlaza el grupo de direcciones URL que creó como parte de la configuración en tiempo de ejecución a la cola mediante una llamada a [**HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty) con **HttpServerBindingProperty especificado** en el *parámetro Property.* [](run-time-configuration.md) A continuación, las solicitudes entrantes de las direcciones URL del grupo se enruta a la cola de solicitudes especificada.

 

 




