---
description: El objeto de sensor representa un sensor determinado.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: El objeto sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127265148"
---
# <a name="the-sensor-object"></a>El objeto sensor

El objeto de sensor representa un sensor determinado.

Sensor API representa cada sensor como un objeto de sensor. Puede trabajar con un objeto de sensor determinado a través de su [**interfaz ISensor.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) Esta interfaz le permite:

-   Recupere metadatos sobre el sensor, como su identificador, tipo o nombre descriptivo.
-   Recupere información sobre los datos específicos que el sensor puede proporcionar.
-   Recupere los datos de forma sincrónica.
-   Recupere información de estado, como si el sensor está listo.
-   Especifique qué eventos recibirá el programa.
-   Especifique la interfaz de devolución de llamada que la API del sensor puede usar para proporcionar al programa notificaciones de eventos.

 

 



