---
title: ¿Cuáles son las acciones básicas de la API de punto de control?
description: Todos los puntos de control realizan las siguientes tareas.
ms.assetid: f681468f-90ab-4533-8ee7-6e4f93e08cf2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a102c389a41b32fd7a79bf749ce38f1267912c3993e2461adac9b6730ea92325
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513645"
---
# <a name="what-are-the-basic-actions-of-the-control-point-api"></a>¿Cuáles son las acciones básicas de la API de punto de control?

Todos los puntos de control realizan las siguientes tareas:

-   Busque los dispositivos basados en UPnP disponibles en la red.
-   Determine cuál de estos dispositivos es de interés.
-   Emita solicitudes de control a los dispositivos de interés y reciba eventos generados por los dispositivos.

Una aplicación debe buscar primero los dispositivos basados en UPnP disponibles en la red mediante una búsqueda. Dado que los criterios de búsqueda definidos por la arquitectura de UPnP son bastante amplios, la aplicación podría encontrar más dispositivos de los necesarios. Por lo tanto, la aplicación debe examinar las características de los dispositivos que se encontraron para determinar cuáles coinciden mejor con los criterios de búsqueda. A continuación, la aplicación puede emitir solicitudes de control a esos dispositivos.

En las secciones siguientes se describe cómo llevar a cabo estas operaciones mediante la API de punto de control con tecnología UPnP:

-   [Búsqueda de dispositivos](finding-devices.md)
-   [Descripción de dispositivos](describing-devices.md)
-   [Controlar dispositivos](controlling-devices.md)

Para obtener documentación detallada sobre cada interfaz de la API de punto de control, consulte [Referencia de la API de punto de control.](control-point-api-with-upnp-technology-reference.md)

 

 




