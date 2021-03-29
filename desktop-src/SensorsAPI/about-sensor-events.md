---
description: La API de sensor puede proporcionar notificaciones de eventos.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Acerca de los eventos de la API de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912238"
---
# <a name="about-sensor-api-events"></a>Acerca de los eventos de la API de sensor

La API de sensor puede proporcionar notificaciones de eventos.

Al registrarse para recibir eventos, a través de [**ISensor:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager:: SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), debe proporcionar un puntero a una interfaz de devolución de llamada. Debe implementar los métodos de la interfaz de devolución de llamada en el código. La API de sensor define las siguientes interfaces de devolución de llamada:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implemente esta interfaz para recibir eventos de los sensores. Los sensores pueden notificar a la aplicación los nuevos datos, los cambios en el estado del sensor, la desconexión del sensor y los eventos personalizados definidos por el fabricante del sensor.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implemente esta interfaz para recibir eventos del administrador del sensor. El administrador del sensor puede notificar a la aplicación cuando se conecta un sensor y, por tanto, puede estar disponible para su uso.

Puede cancelar las notificaciones de eventos llamando a [**SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) de nuevo, esta vez pasando un valor **null** a través del parámetro.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de eventos de la API de sensor](using-sensor-api-events.md)
</dt> </dl>

 

 
