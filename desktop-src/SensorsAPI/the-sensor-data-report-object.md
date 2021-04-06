---
description: El objeto de informe de datos de sensor contiene datos de sensor.
ms.assetid: 8a812860-338b-4ada-8f5f-ea693e038941
title: Objeto de informe de datos de sensor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d43753aa28be5cd20c85b7e65bf4c7516d4c90
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002333"
---
# <a name="the-sensor-data-report-object"></a>Objeto de informe de datos de sensor

El objeto de informe de datos de sensor contiene datos de sensor.

Para que un sensor sea útil, debe proporcionar datos significativos. La cantidad y la frecuencia de generación de datos varían de un sensor a un sensor. Por ejemplo, un sensor que detecta si una puerta está abierta generará una pequeña cantidad de datos **booleanos** , mientras que un sensor de movimiento podría generar continuamente varios elementos de datos. Para estandarizar la forma en que el programa recibe los datos, la API de sensor usa el objeto de informe de datos de sensor.

Puede tener acceso a la información de un informe de datos de sensor a través de la interfaz [**ISensorDataReport**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensordatareport) . Esta interfaz le permite recuperar la marca de tiempo del informe de datos para que pueda determinar si la información del informe es útil. Puede recuperar los datos en sí de dos maneras: como un valor de campo de datos individual o como un conjunto de valores. Para recuperar los datos como un valor individual, llame al método [**GetSensorValue**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalue) . Para recuperar varios valores, llame al método [**GetSensorValues**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensordatareport-getsensorvalues) .

Especifique el tipo de datos o campos de datos que desea recuperar del informe mediante una constante **PROPERTYKEY** . Las claves de propiedad de los campos de datos de los tipos de sensor comunes se definen en Sensors. h.

 

 
