---
description: El objeto de sensor representa un sensor determinado.
ms.assetid: b969a153-d957-4323-bafe-6f8d62b0a627
title: El objeto de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6034c008edf75b16a8156ab53ff66a418261d965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667889"
---
# <a name="the-sensor-object"></a>El objeto de sensor

El objeto de sensor representa un sensor determinado.

La API del sensor representa cada sensor como un objeto de sensor. Puede trabajar con un objeto de sensor determinado a través de su interfaz [**ISensor**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensor) . Esta interfaz le permite:

-   Recupere los metadatos sobre el sensor, como su identificador, tipo o nombre descriptivo.
-   Recupera información sobre los datos específicos que el sensor puede proporcionar.
-   Recupere los datos de forma sincrónica.
-   Recupera la información de estado, por ejemplo, si el sensor está listo.
-   Especifique los eventos que recibirá el programa.
-   Especifique la interfaz de devolución de llamada que la API de sensor puede usar para proporcionar el programa con notificaciones de eventos.

 

 



