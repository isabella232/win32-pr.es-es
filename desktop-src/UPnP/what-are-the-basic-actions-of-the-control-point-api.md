---
title: ¿Cuáles son las acciones básicas de la API de punto de control?
description: Todos los puntos de control realizan las siguientes tareas.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5252e2db09aa8283034da20dc1bd2dc877bf0e5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779063"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>¿Cuáles son las acciones básicas de la API de punto de control?

Todos los puntos de control realizan las siguientes tareas:

-   Busque los dispositivos basados en UPnP disponibles en la red.
-   Determine cuáles de estos dispositivos son de interés.
-   Emitir solicitudes de control a los dispositivos de interés y recibir eventos generados por los dispositivos.

Una aplicación debe buscar en primer lugar los dispositivos basados en UPnP disponibles en la red mediante la realización de una búsqueda. Dado que los criterios de búsqueda definidos por la arquitectura de UPnP son bastante amplios, es posible que la aplicación encuentre más dispositivos de los necesarios. Por lo tanto, la aplicación debe examinar las características de los dispositivos que se han encontrado para determinar cuáles coinciden con más exactitud con los criterios de búsqueda. A continuación, la aplicación puede emitir solicitudes de control a esos dispositivos.

En las secciones siguientes se describe cómo llevar a cabo estas operaciones mediante la API de punto de control con tecnología UPnP:

-   [Búsqueda de dispositivos](finding-devices.md)
-   [Describir dispositivos](describing-devices.md)
-   [Control de dispositivos](controlling-devices.md)

Para obtener documentación detallada sobre cada interfaz de la API de punto de control, consulte [referencia de API de punto de control](control-point-api-with-upnp-technology-reference.md).

 

 




