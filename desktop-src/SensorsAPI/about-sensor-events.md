---
description: Sensor API puede proporcionar notificaciones de eventos.
ms.assetid: 2400619c-ee9c-4662-ae57-6d4bc317e730
title: Acerca de los eventos de SENSOR API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e941dca86d5b7ec3aa9922220c1232b10429f60a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073561"
---
# <a name="about-sensor-api-events"></a>Acerca de los eventos de SENSOR API

Sensor API puede proporcionar notificaciones de eventos.

Al registrarse para recibir eventos, a través de [**ISensor::SetEventSink**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) o [**ISensorManager::SetEventSink,**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-seteventsink)debe proporcionar un puntero a una interfaz de devolución de llamada. Debe implementar los métodos de la interfaz de devolución de llamada en el código. Sensor API define las siguientes interfaces de devolución de llamada:

-   [**ISensorEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensorevents). Implemente esta interfaz para recibir eventos de sensores. Los sensores pueden notificar a la aplicación nuevos datos, cambios en el estado del sensor, desconexión del sensor y eventos personalizados definidos por el fabricante del sensor.
-   [**ISensorManagerEvents**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanagerevents). Implemente esta interfaz para recibir eventos del administrador de sensores. El administrador de sensores puede notificar a la aplicación cuándo se conecta un sensor y, por tanto, puede estar disponible para su uso.

Puede cancelar las notificaciones de eventos llamando de nuevo a [**SetEventSink,**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensor-seteventsink) esta vez pasando un **valor NULL** a través del parámetro .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de eventos de SENSOR API](using-sensor-api-events.md)
</dt> </dl>

 

 
