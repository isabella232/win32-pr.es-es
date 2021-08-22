---
description: Sensor API puede proporcionar notificaciones de eventos.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Acerca de los eventos de sensor API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4af21bfed2a36c0c79fa46811221afbf2fcf87a4a5f15cf21adfbeaac8601f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003903"
---
# <a name="about-sensor-api-events"></a>Acerca de los eventos de sensor API

Sensor API puede proporcionar notificaciones de eventos.

Al registrarse para recibir eventos, a través de [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink), debe proporcionar un puntero a una interfaz de devolución de llamada. Debe implementar los métodos de la interfaz de devolución de llamada en el código. Sensor API define las siguientes interfaces de devolución de llamada:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implemente esta interfaz para recibir eventos de sensores. Los sensores pueden notificar a la aplicación sobre nuevos datos, cambios en el estado del sensor, desconexión del sensor y eventos personalizados definidos por el fabricante del sensor.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implemente esta interfaz para recibir eventos del administrador de sensores. El administrador de sensores puede notificar a la aplicación cuando se conecta un sensor y, por tanto, puede estar disponible para su uso.

Puede cancelar las notificaciones de eventos llamando de nuevo a [**SetEventSink,**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) esta vez pasando un **valor NULL** a través del parámetro .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de eventos de sensor API](using-sensor-api-events.md)
</dt> </dl>

 

 
