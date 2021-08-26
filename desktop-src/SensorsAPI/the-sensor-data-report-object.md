---
description: El objeto de informe de datos del sensor contiene datos del sensor.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: El objeto de informe de datos del sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ca1a8e5f61b23753437bd8b1cf4c2a176515b7042b21e84c4d2f431debc8fe6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119992605"
---
# <a name="the-sensor-data-report-object"></a>El objeto de informe de datos del sensor

El objeto de informe de datos del sensor contiene datos del sensor.

Para que un sensor sea útil, debe proporcionar datos significativos. La cantidad y frecuencia de generación de datos varía de un sensor a otro. Por ejemplo, un sensor que detecta si una puerta está abierta generaría una pequeña cantidad de datos **booleanos,** mientras que un sensor de movimiento podría generar continuamente varios elementos de datos. Para estandarizar la forma en que el programa recibe datos, sensor API usa el objeto de informe de datos del sensor.

Puede acceder a la información de un informe de datos del sensor a través de la [**interfaz ISensorDataReport.**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) Esta interfaz le permite recuperar la marca de tiempo del informe de datos para que pueda determinar si la información del informe es útil. Puede recuperar los propios datos de dos maneras: como un valor de campo de datos individual o como un conjunto de valores. Para recuperar datos como un valor individual, llame al [**método GetSensorValue.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) Para recuperar varios valores, llame al [**método GetSensorValues.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues)

Especifique el tipo de datos, o campos de datos, que desea recuperar del informe mediante una **constante PROPERTYKEY.** Las claves de propiedad de los campos de datos de tipos de sensor comunes se definen en Sensors.h.

 

 
