---
description: La categoría de eléctrico de categoría de SENSOR \_ \_ contiene sensores que proporcionan información acerca de los sistemas eléctricos.
ms.assetid: c4efa821-fb9f-4606-898a-5be103581f39
title: SENSOR_CATEGORY_ELECTRICAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b3487b779cfefc78a541fcc72d1f2c5c5e7c0db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666361"
---
# <a name="sensor_category_electrical"></a>Categoría de SENSOR \_ \_ eléctrica

La categoría de eléctrico de categoría de SENSOR \_ \_ contiene sensores que proporcionan información acerca de los sistemas eléctricos.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                              | Descripción                             |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------|
| <span id="SENSOR_TYPE_CAPACITANCE"></span><span id="sensor_type_capacitance"></span><dl> <dt>**Sensor \_ de Escriba \_**</dt> la <dt>CA2FFB1C-2317-49C0-A0B4-B63CE63461A0}</dt> </dl>                 | Sensores de la<br/>         |
| <span id="SENSOR_TYPE_CURRENT"></span><span id="sensor_type_current"></span><dl> <dt>**Sensor \_ de TIPO \_ actual**</dt> <dt>{5ADC9FCE-15A0-4BBE-A1AD-2D38A9AE831C}</dt> </dl>                             | Sensores eléctricos actuales.<br/>  |
| <span id="SENSOR_TYPE_ELECTRICAL_POWER"></span><span id="sensor_type_electrical_power"></span><dl> <dt>**Sensor \_ de Escriba \_ la \_ energía eléctrica**</dt> <dt>{212F10F5-14AB-4376-9A43-A7794098C2FE}</dt> </dl> | Sensores eléctricos de energía.<br/>    |
| <span id="SENSOR_TYPE_FREQUENCY"></span><span id="sensor_type_frequency"></span><dl> <dt>**Sensor \_ de \_Frecuencia de tipos**</dt> <dt>{8CD2CBB6-73E6-4640-A709-72AE8FB60D7F}</dt> </dl>                       | Sensor de frecuencia eléctrica.<br/> |
| <span id="SENSOR_TYPE_INDUCTANCE"></span><span id="sensor_type_inductance"></span><dl> <dt>**Sensor \_ de Escriba \_ inductancia**</dt> <dt>{DC1D933F-C435-4C7D-A2FE-607192A524D3}</dt> </dl>                    | Sensores de inductancia.<br/>          |
| <span id="SENSOR_TYPE_POTENTIOMETER"></span><span id="sensor_type_potentiometer"></span><dl> <dt>**Sensor \_ de TIPO de \_ potenciómetro**</dt> <dt>{2B3681A9-CADC-45AA-A6FF-54957C8BB440}</dt> </dl>           | Potenciómetros.<br/>              |
| <span id="SENSOR_TYPE_RESISTANCE"></span><span id="sensor_type_resistance"></span><dl> <dt>**Sensor \_ de \_Resistencia de tipos**</dt> <dt>{9993D2C8-C157-4A52-A7B5-195C76037231}</dt> </dl>                    | Sensores de resistencia.<br/>          |
| <span id="SENSOR_TYPE_VOLTAGE"></span><span id="sensor_type_voltage"></span><dl> <dt>**Sensor \_ de \_Voltaje de tipo**</dt> <dt>{C5484637-4FB7-4953-98B8-A56D8AA1FB1E}</dt> </dl>                             | Sensores de voltaje.<br/>             |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el \_ GUID eléctrico del tipo de datos del sensor \_ \_ \_ :

{BBB246D1-E242-4780-A2D3-CDED84F35842}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                         | Descripción                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CAPACITANCE_FARAD"></span><span id="sensor_data_type_capacitance_farad"></span><dl> <dt>**Sensor \_ de \_Tipo de \_ datos \_ Farad (**</dt> <dt> (PID = 4)</dt> </dl>                                | **VT \_ R8**<br/> La farads.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_CURRENT_AMPS"></span><span id="sensor_data_type_current_amps"></span><dl> <dt>**Sensor \_ de Los \_ \_ \_ amperios actuales de tipo de datos**</dt> <dt>(PID = 3)</dt> </dl>                                                | **VT \_ R8**<br/> Actual en amperes.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_FREQUENCY_HERTZ"></span><span id="sensor_data_type_electrical_frequency_hertz"></span><dl> <dt>**Sensor \_ de \_Frecuencia eléctrica de tipo de datos \_ \_ \_ hercios**</dt> <dt>(PID = 9)</dt> </dl>     | **VT \_ R8**<br/> Frecuencia eléctrica en hercios.<br/>                               |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_PERCENT_OF_RANGE"></span><span id="sensor_data_type_electrical_percent_of_range"></span><dl> <dt>**Sensor \_ de \_ \_ \_ Porcentaje eléctrico del tipo \_ de datos del \_ intervalo**</dt> <dt>(PID = 8)</dt> </dl> | **VT \_ R8**<br/> La lectura de potenciómetro como un porcentaje de su posible intervalo.<br/> |
| <span id="SENSOR_DATA_TYPE_ELECTRICAL_POWER_WATTS"></span><span id="sensor_data_type_electrical_power_watts"></span><dl> <dt>**Sensor \_ de \_Alimentación eléctrica de tipo de datos \_ \_ \_ vatios**</dt> <dt> (PID = 7)</dt> </dl>                | **VT \_ R8**<br/> Alimentación eléctrica en vatios.<br/>                                   |
| <span id="SENSOR_DATA_TYPE_INDUCTANCE_HENRY"></span><span id="sensor_data_type_inductance_henry"></span><dl> <dt>**Sensor \_ de Tipo de datos \_ \_ inductancia \_ Henry**</dt> <dt>(PID = 6)</dt> </dl>                                    | **VT \_ R8**<br/> Inductancia en henries.<br/>                                       |
| <span id="SENSOR_DATA_TYPE_RESISTANCE_OHMS"></span><span id="sensor_data_type_resistance_ohms"></span><dl> <dt>**Sensor \_ de La \_ \_ resistencia de \_ tipos de datos**</dt> <dt>(PID = 5)</dt> </dl>                                       | **VT \_ R8**<br/> Resistencia en ohmios.<br/>                                          |
| <span id="SENSOR_DATA_TYPE_VOLTAGE_VOLTS"></span><span id="sensor_data_type_voltage_volts"></span><dl> <dt>**Sensor \_ de Voltaje de tipo de datos \_ \_ \_ voltios**</dt> <dt>(PID = 2)</dt> </dl>                                             | **VT \_ R8**<br/> Potencial eléctrico en voltios.<br/>                               |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




