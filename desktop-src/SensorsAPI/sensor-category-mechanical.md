---
description: La categoría de SENSOR \_ \_ mecánico contiene sensores que proporcionan información relacionada con los dispositivos mecánicos y las medidas.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2446559820141b65a70bc75d25680da79563388c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666358"
---
# <a name="sensor_category_mechanical"></a>Categoría de SENSOR \_ \_ mecánica

La categoría de SENSOR \_ \_ mecánico contiene sensores que proporcionan información relacionada con los dispositivos mecánicos y las medidas.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                                           | Descripción                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**Sensor \_ de TIPO \_ booleano \_ Switch**</dt> <dt>{9C7E371F-1041-460b-8D5C-71E4752E350C}</dt> </dl>                    | Modificadores de dos Estados (desactivado o activado).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**Sensor \_ de Escriba \_ una \_ \_ matriz de modificadores de tipo booleano**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | Matriz de modificadores de dos Estados (desactivado o activado).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**Sensor \_ de TIPO \_ Force**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | Fuerce sensores.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**Sensor \_ de Cambiar el tipo de \_ multivalor \_**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Modificadores de varias posiciones.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**Sensor \_ de \_Presión de tipos**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Sensores de presión.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**Sensor \_ de \_Escala de tipos**</dt> <dt>{C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Sensores de peso.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**Sensor \_ de \_Restricción de tipos**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Sensores de cepas.<br/>                          |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el \_ \_ GUID mecánico del tipo de datos del sensor \_ \_ \_ :

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                         | Descripción                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**Sensor \_ de La \_ presión absoluta de tipo de datos \_ \_ \_ Pascal**</dt> <dt> (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Presión absoluta, en pascales.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**Sensor \_ de \_Estados de \_ \_ matriz de \_ \_ conmutador booleanos de tipo de datos**</dt> <dt>(PID = 10)</dt> </dl> | **VT \_ UI4**<br/> Campos de estado para una matriz de modificadores booleanos.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**Sensor \_ de Tipo de datos de \_ \_ \_ \_ Estado de modificador booleano**</dt> <dt>(PID = 2)</dt> </dl>                       | **VT \_ bool**<br/> Campo de estado para \_ el \_ modificador booleano de tipo de sensor \_ .<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**Sensor \_ de DATA \_ Type \_ Force \_ Newtons**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Force, en Newtons.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**Sensor \_ de Medidor de tipos de datos \_ \_ \_ \_ Pascal de presión**</dt> <dt> (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Presión del medidor relativo, en pascales.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**Sensor \_ de \_ \_ \_ \_ Estado del conmutador multivalor de tipo de datos**</dt> <dt> (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Campo de estado del \_ conmutador multivalor de tipo de sensor \_ \_ .<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**Sensor \_ de \_ \_ Restricción de tipo de datos**</dt> <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Limitar.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**Sensor \_ de Peso del tipo de datos \_ \_ \_ kilogramos**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Peso, en kilogramos.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




