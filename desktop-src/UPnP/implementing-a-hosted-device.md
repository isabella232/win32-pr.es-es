---
title: Implementación de un dispositivo hospedado
description: El host de dispositivo con tecnología UPnP implementa la detección, descripción, control y eventos de los protocolos UPnP principales.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 172e9935dcbca73dbb285ba73270375fb5bfb6cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779111"
---
# <a name="implementing-a-hosted-device"></a>Implementación de un dispositivo hospedado

El host de dispositivo con tecnología UPnP implementa los principales protocolos UPnP: detección, descripción, control y eventos. El desarrollador que implementa un dispositivo hospedado solo debe proporcionar:

-   Descripción del dispositivo y sus servicios.
-   Implementación de la funcionalidad del dispositivo.

Por ejemplo, el desarrollador de un dispositivo de reloj debe proporcionar descripciones de dispositivos y servicios basados en UPnP, y una implementación de las funciones de reloj (por ejemplo, mantener el tiempo, establecer el tiempo y responder a las consultas de la hora actual). El host del dispositivo:

-   Anuncia el dispositivo según el protocolo de detección de UPnP.
-   Responde a las consultas de la descripción del dispositivo.
-   Enruta las solicitudes de control a la parte del código del dispositivo que implementa las funciones de reloj.
-   Mantiene las suscripciones de eventos a los servicios.
-   Envía notificaciones de eventos a los suscriptores cuando cambia el estado del servicio.

 

 




