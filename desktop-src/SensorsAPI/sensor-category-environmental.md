---
description: La categoría de entorno de categoría de SENSOR \_ \_ contiene sensores que proporcionan información sobre el entorno circundante o el tiempo.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b5c41d4c117dc27a3303210a485b2233cf24cde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907798"
---
# <a name="sensor_category_environmental"></a>\_entorno de categoría de sensor \_

La categoría de entorno de categoría de SENSOR \_ \_ contiene sensores que proporcionan información sobre el entorno circundante o el tiempo.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                                                                                     | Descripción               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**Sensor \_ de TIPO \_ de \_ \_ presión atmosférica del entorno**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barómetros.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**Sensor \_ de TIPO \_ de \_ humedad ambiental**</dt> <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Hygrometers.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**Sensor \_ de \_ \_ Temperatura ambiental de tipo**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Termómetros<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**Sensor \_ de \_Dirección del \_ viento \_ del entorno de tipo**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Meteorología Vanes.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**Sensor \_ de \_Velocidad del \_ viento \_ del entorno de tipo**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemometers.<br/>   |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ GUID del \_ entorno \_ :

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**Sensor \_ de \_Barra de \_ \_ presión atmosférica \_ de tipo de datos**</dt> <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Presión atmosférica en atmósferas (barras).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**Sensor \_ de \_Tipo de \_ datos \_ Celsius**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Temperatura en grados Celsius.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**Sensor \_ de \_Porcentaje de \_ \_ humedad relativa \_ del tipo de datos**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Humedad relativa como porcentaje.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**Sensor \_ de \_Grado de \_ dirección del viento del tipo de datos en \_ sentido contrario a las \_ \_ agujas del reloj**</dt> <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Dirección del viento en relación con el norte magnético, en grados. North se representa como 0,0 (parte superior del eje X), con valores que aumentan en sentido contrario a las agujas del reloj. El eje Z apunta hacia arriba. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**Sensor \_ de \_Medidores de velocidad de viento de tipo de datos \_ \_ \_ \_ por \_ segundo**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Velocidad de viento en metros por segundo.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




