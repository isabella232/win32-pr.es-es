---
description: El objeto de sensor representa un sensor determinado.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: El objeto sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01ad666153be31958bb758ca4b504e10591ccbe29c9d37355499c9d22c5aae2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666415"
---
# <a name="the-sensor-object"></a>El objeto sensor

El objeto de sensor representa un sensor determinado.

Sensor API representa cada sensor como un objeto de sensor. Puede trabajar con un objeto de sensor determinado a través de su [**interfaz ISensor.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) Esta interfaz le permite:

-   Recupere metadatos sobre el sensor, como su identificador, tipo o nombre descriptivo.
-   Recupere información sobre los datos específicos que puede proporcionar el sensor.
-   Recupere los datos de forma sincrónica.
-   Recupere información de estado, como si el sensor está listo.
-   Especifique qué eventos recibirá el programa.
-   Especifique la interfaz de devolución de llamada que la API de sensor puede usar para proporcionar notificaciones de eventos al programa.

 

 



