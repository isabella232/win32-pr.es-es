---
description: La categoría \_ SENSOR CATEGORY ENVIRONMENTAL contiene \_ sensores que proporcionan información sobre el entorno circundante o el tiempo.
ms.assetid: 4a29d44b-8949-474d-a2bf-0c6e1d30b198
title: SENSOR_CATEGORY_ENVIRONMENTAL (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7cc2a6ca1d2832045a77f0a2ffa1902732e484700afaacd757719e99d667c55
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126615"
---
# <a name="sensor_category_environmental"></a>SENSOR \_ CATEGORY \_ ENVIRONMENTAL

La categoría \_ SENSOR CATEGORY ENVIRONMENTAL contiene \_ sensores que proporcionan información sobre el entorno circundante o el tiempo.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensores definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                                                                                     | Descripción               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------|
| <span id="SENSOR_TYPE_ENVIRONMENTAL_ATMOSPHERIC_PRESSURE"></span><span id="sensor_type_environmental_atmospheric_pressure"></span><dl> <dt>**SENSOR \_ PRESIÓN \_ \_ AMBIENTAL DE \_ TIPO**</dt> <dt>{0E903829-FF8A-4A93-97DF-3DCBDE402288}</dt> </dl> | Barómetros.<br/>    |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_HUMIDITY"></span><span id="sensor_type_environmental_humidity"></span><dl> <dt>**SENSOR \_ ESCRIBA \_ ENVIRONMENTAL \_ HUMIDITY**</dt> <dt>{5C72BF67-BD7E-4257-990B-98A3BA3B400A}</dt> </dl>                                      | Higrómetros.<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_TEMPERATURE"></span><span id="sensor_type_environmental_temperature"></span><dl> <dt>**SENSOR \_ TYPE \_ ENVIRONMENTAL \_ TEMPERATURE**</dt> <dt>{04FD0EC4-D5DA-45FA-95A9-5DB38EE19306}</dt> </dl>                             | Termómetros<br/>   |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_DIRECTION"></span><span id="sensor_type_environmental_wind_direction"></span><dl> <dt>**SENSOR \_ ESCRIBA \_ ENVIRONMENTAL \_ WIND \_ DIRECTION**</dt> <dt>{9EF57A35-9306-434D-AF09-37FA5A9C00BD}</dt> </dl>                   | Vanes meteorológicos.<br/> |
| <span id="SENSOR_TYPE_ENVIRONMENTAL_WIND_SPEED"></span><span id="sensor_type_environmental_wind_speed"></span><dl> <dt>**SENSOR \_ TYPE \_ ENVIRONMENTAL \_ WIND \_ SPEED**</dt> <dt>{DD50607B-A45F-42CD-8EFD-EC61761C4226}</dt> </dl>                               | Anemómetros.<br/>   |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en SENSOR \_ DATA \_ TYPE ENVIRONMENTAL \_ \_ GUID:

{8B0AA2F1-2D57-42EE-8CC0-4D27622B46C4}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ATMOSPHERIC_PRESSURE_BAR"></span><span id="sensor_data_type_atmospheric_pressure_bar"></span><dl> <dt>**SENSOR \_ BARRA \_ DE PRESIÓN AMBIENTAL DEL TIPO DE \_ \_ \_ DATOS**</dt> <dt>(PID = 4)</dt> </dl>                                      | **VT \_ R4**<br/> Presión ambiental en ambientes (barras).<br/>                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_TEMPERATURE_CELSIUS"></span><span id="sensor_data_type_temperature_celsius"></span><dl> <dt>**SENSOR \_ TEMPERATURA \_ \_ DEL TIPO DE DATOS \_ CELSIUS**</dt> <dt>(PID = 2)</dt> </dl>                                                      | **VT \_ R4**<br/> Temperatura en grados Centígrados.<br/>                                                                                                                                                          |
| <span id="SENSOR_DATA_TYPE_RELATIVE_HUMIDITY_PERCENT"></span><span id="sensor_data_type_relative_humidity_percent"></span><dl> <dt>**SENSOR \_ PORCENTAJE \_ DE HUMEDAD RELATIVA DEL TIPO DE \_ \_ \_ DATOS**</dt> <dt> (PID = 3)</dt> </dl>                                  | **VT \_ R4**<br/> Humedad relativa como porcentaje.<br/>                                                                                                                                                       |
| <span id="SENSOR_DATA_TYPE_WIND_DIRECTION_DEGREES_ANTICLOCKWISE"></span><span id="sensor_data_type_wind_direction_degrees_anticlockwise"></span><dl> <dt>**SENSOR \_ TIPO \_ DE DATOS WIND DIRECTION \_ \_ \_ DEGREES \_ ANTICLOCKWISE**</dt> <dt>(PID = 5)</dt> </dl> | **VT \_ R4**<br/> Dirección del viento con respecto al norte magnético, en grados. El norte se representa como 0,0 (parte superior del eje X), con valores que aumentan en una rotación a la izquierda de las agujas del reloj. El eje Z apunta hacia arriba. <br/> |
| <span id="SENSOR_DATA_TYPE_WIND_SPEED_METERS_PER_SECOND"></span><span id="sensor_data_type_wind_speed_meters_per_second"></span><dl> <dt>**SENSOR \_ MEDIDORES DE VELOCIDAD DEL VIENTO DEL TIPO DE DATOS \_ \_ POR \_ \_ \_ \_ SEGUNDO**</dt> <dt>(PID = 6)</dt> </dl>                        | **VT \_ R4**<br/> Velocidad del viento en metros por segundo.<br/>                                                                                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




