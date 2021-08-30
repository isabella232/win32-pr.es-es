---
description: La categoría SENSOR \_ CATEGORY \_ ELECTRICAL contiene sensores que proporcionan información sobre los sistemas eléctricos.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155859dd82dbc9f43368d149c6d644bd42d4875661c87526b9fa66d7f20f0686
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126635"
---
# <a name="sensor_category_electrical"></a>CATEGORÍA DE SENSOR \_ \_ ELÉCTRICA

La categoría SENSOR \_ CATEGORY \_ ELECTRICAL contiene sensores que proporcionan información sobre los sistemas eléctricos.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensores definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                              | Descripción                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**SENSOR \_ TYPE \_ CAPACITANCE**</dt> <dt>{CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Sensores de capacidad.<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**SENSOR \_ TIPO \_ CURRENT**</dt> <dt>{5ADC9FCE-15A0-4 A1AD-2D38A9AE831C}</dt> </dl>                             | Sensores de corriente eléctrica.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**SENSOR \_ TYPE \_ ELECTRICAL \_ POWER**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | Sensores de energía eléctrica.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**SENSOR \_ FRECUENCIA \_ DE**</dt> <dt>TIPO {8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | Sensor de frecuencia eléctrica.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**SENSOR \_ TYPE \_ INDUCTANCE**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | Sensores de inducción.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**SENSOR \_ TYPE \_ MAGNETIOMETER**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | Potenciómetros.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**SENSOR \_ RESISTENCIA \_ DE**</dt> <dt>TIPOS {9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | Sensores de resistencia.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**SENSOR \_ TYPE \_ VOLTAGE**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Sensores de voltaje.<br/>             |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en EL \_ GUID DE SENSOR DATA TYPE \_ \_ \_ ELECTRICAL:

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                         | Descripción                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**SENSOR \_ FARAD \_ \_ DE CAPACITANCIA DE TIPO \_ DE**</dt> <dt> DATOS (PID = 4)</dt> </dl>                                | **VT \_ R8**<br/> Capacitancia en farads.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**SENSOR \_ AMPS \_ \_ ACTUALES \_ DEL TIPO DE**</dt> DATOS <dt>(PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> Actual en amperes.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**SENSOR \_ HERTZ \_ DE FRECUENCIA ELÉCTRICA DEL TIPO \_ \_ \_ DE**</dt> <dt>DATOS (PID = 9)</dt> </dl>     | **VT \_ R8**<br/> Frecuencia eléctrica en hercios.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**SENSOR \_ PORCENTAJE \_ ELÉCTRICO DEL INTERVALO DEL TIPO \_ \_ \_ \_ DE**</dt> <dt>DATOS (PID = 8)</dt> </dl> | **VT \_ R8**<br/> Lectura del iómetro como porcentaje de su intervalo posible.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE ELECTRICAL POWER \_ \_ \_ VATS**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> Energía eléctrica en vatios.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**SENSOR \_ TIPO \_ DE \_ DATOS INDUCTANCE \_ HRS (PID**</dt> <dt>= 6)</dt> </dl>                                    | **VT \_ R8**<br/> Inducción en los condados.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**SENSOR \_ OMM \_ DE RESISTENCIA DE TIPOS \_ \_ DE**</dt> <dt>DATOS (PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Resistencia en ohms.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**SENSOR \_ VOLTES \_ DE VOLTAJE DE TIPO \_ \_ DE**</dt> <dt>DATOS (PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> Potencial eléctrico en volts.<br/>                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




