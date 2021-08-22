---
title: Implementación de un dispositivo hospedado
description: El host de dispositivo con tecnología UPnP implementa la detección, descripción, control y eventos de los protocolos UPnP principales.
ms.assetid: ab113d76-5fc9-4be2-a814-8772dd1e9600
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9fd12788c40d21dc84e896f1aba83085b440b86fbb54b68b4fbcfddbbe910c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008055"
---
# <a name="implementing-a-hosted-device"></a>Implementación de un dispositivo hospedado

El host de dispositivo con tecnología UPnP implementa los principales protocolos UPnP: detección, descripción, control y eventos. El desarrollador que implementa un dispositivo hospedado solo debe proporcionar:

-   Descripción del dispositivo y sus servicios.
-   Una implementación de la funcionalidad del dispositivo.

Por ejemplo, el desarrollador de un dispositivo de reloj debe proporcionar descripciones del dispositivo y del servicio basados en UPnP, así como una implementación de las funciones de reloj (por ejemplo, mantener la hora, establecer la hora y responder a las consultas de la hora actual). El host del dispositivo:

-   Anuncia el dispositivo según el protocolo de detección de UPnP.
-   Responde a las consultas de la descripción del dispositivo.
-   Enruta las solicitudes de control a la parte del código del dispositivo que implementa las funciones de reloj.
-   Mantiene las suscripciones de eventos a los servicios.
-   Envía notificaciones de eventos a los suscriptores cuando cambia el estado del servicio.

 

 




