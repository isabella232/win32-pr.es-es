---
description: La categoría SENSOR \_ CATEGORY \_ MECHANICAL contiene sensores que proporcionan información relacionada con dispositivos mecánicos y medidas.
ms.assetid: d1243303-d26c-45ce-b97b-d554daeeb462
title: SENSOR_CATEGORY_MECHANICAL (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbac9a00895b08bd99106af7f0b6986118b4645dac690fd190f734e1499940dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119666715"
---
# <a name="sensor_category_mechanical"></a>MECÁNICA \_ DE CATEGORÍA DEL \_ SENSOR

La categoría SENSOR \_ CATEGORY \_ MECHANICAL contiene sensores que proporcionan información relacionada con dispositivos mecánicos y medidas.

**Tipos de sensor definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                                           | Descripción                                         |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------|
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH"></span><span id="sensor_type_boolean_switch"></span><dl> <dt>**SENSOR \_ TYPE \_ BOOLEAN \_ SWITCH**</dt> <dt>{9C7E371F-1041-460B-8D5C-71E4752E350C}</dt> </dl>                    | Modificadores de dos estados (desactivados o on).<br/>          |
| <span id="SENSOR_TYPE_BOOLEAN_SWITCH_ARRAY"></span><span id="sensor_type_boolean_switch_array"></span><dl> <dt>**SENSOR \_ TYPE \_ BOOLEAN \_ SWITCH \_ ARRAY**</dt> <dt>{545C8BA5-B143-4545-868F-CA7FD986B4F6}</dt> </dl> | Matriz de modificadores de dos estados (desactivado o on).<br/> |
| <span id="SENSOR_TYPE_FORCE"></span><span id="sensor_type_force"></span><dl> <dt>**SENSOR \_ TYPE \_ FORCE**</dt> <dt>{C2AB2B02-1A1C-4778-A81B-954A1788CC75}</dt> </dl>                                                | Forzar sensores.<br/>                           |
| <span id="SENSOR_TYPE_MULTIVALUE_SWITCH"></span><span id="sensor_type_multivalue_switch"></span><dl> <dt>**SENSOR \_ TYPE \_ MULTIVALUE \_ SWITCH**</dt> <dt>{B3EE4D76-37A4-4402-B25E-99C60A775FA1}</dt> </dl>           | Modificadores de varias posiciones.<br/>              |
| <span id="SENSOR_TYPE_PRESSURE"></span><span id="sensor_type_pressure"></span><dl> <dt>**SENSOR \_ TYPE \_ PRESSURE**</dt> <dt>{26D31F34-6352-41CF-B793-EA0713D53D77}</dt> </dl>                                       | Sensores de presión.<br/>                        |
| <span id="SENSOR_TYPE_SCALE"></span><span id="sensor_type_scale"></span><dl> <dt>**SENSOR \_ ESCALA \_ DE**</dt> <dt>TIPOS {C06DD92C-7FEB-438E-9BF6-82207FFF5BB8}</dt> </dl>                                                | Sensores de peso.<br/>                          |
| <span id="SENSOR_TYPE_STRAIN"></span><span id="sensor_type_strain"></span><dl> <dt>**SENSOR \_ TYPE \_ STRAIN**</dt> <dt>{C6D1EC0E-6803-4361-AD3D-85BCC58C6D29}</dt> </dl>                                             | Sensores de tensión.<br/>                          |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el GUID DE GUID DE GUID DEL \_ \_ TIPO DE DATOS \_ \_ \_ SENSOR:

{38564A7C-F2F2-49BB-9B2B-BA60F66A58DF}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                         | Descripción                                                                        |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_ABSOLUTE_PRESSURE_PASCAL"></span><span id="sensor_data_type_absolute_pressure_pascal"></span><dl> <dt>**SENSOR \_ PASCAL \_ \_ DE PRESIÓN ABSOLUTA DE \_ TIPO \_ DE**</dt> <dt> DATOS (PID = 5)</dt> </dl>          | **VT \_ R8**<br/> Presión absoluta, en pascales.<br/>                    |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_ARRAY_STATES"></span><span id="sensor_data_type_boolean_switch_array_states"></span><dl> <dt>**SENSOR \_ ESTADOS \_ DE \_ MATRIZ DE MODIFICADOR \_ \_ BOOLEANO DE TIPO \_ DE**</dt> <dt>DATOS (PID = 10)</dt> </dl> | **VT \_ UI4**<br/> Campos de estado para una matriz de modificadores booleanos.<br/>   |
| <span id="SENSOR_DATA_TYPE_BOOLEAN_SWITCH_STATE"></span><span id="sensor_data_type_boolean_switch_state"></span><dl> <dt>**SENSOR \_ ESTADO \_ DEL \_ CONMUTADOR \_ BOOLEANO DE TIPO \_ DE**</dt> <dt>DATOS (PID = 2)</dt> </dl>                       | **VT \_ BOOL**<br/> Campo de estado para SENSOR \_ TYPE \_ BOOLEAN \_ SWITCH.<br/>  |
| <span id="SENSOR_DATA_TYPE_FORCE_NEWTONS"></span><span id="sensor_data_type_force_newtons"></span><dl> <dt>**SENSOR \_ TIPO \_ DE DATOS FORCE \_ \_ NEWTONS**</dt> <dt> (PID = 4)</dt> </dl>                                            | **VT \_ R8**<br/> Force, en newtons.<br/>                                |
| <span id="SENSOR_DATA_TYPE_GAUGE_PRESSURE_PASCAL"></span><span id="sensor_data_type_gauge_pressure_pascal"></span><dl> <dt>**SENSOR \_ PASCAL DE PRESIÓN DEL MEDIDOR DE TIPO \_ \_ \_ \_ DE**</dt> <dt> DATOS (PID = 6)</dt> </dl>                   | **VT \_ R8**<br/> Presión relativa del medidor, en pascales.<br/>              |
| <span id="SENSOR_DATA_TYPE_MULTIVALUE_SWITCH_STATE"></span><span id="sensor_data_type_multivalue_switch_state"></span><dl> <dt>**SENSOR \_ ESTADO \_ DE \_ CONMUTADOR \_ MULTIVALOR DE \_**</dt> TIPO <dt> DE DATOS (PID = 3)</dt> </dl>             | **VT \_ R8**<br/> Campo de estado para SENSOR \_ TYPE \_ MULTIVALUE \_ SWITCH.<br/> |
| <span id="SENSOR_DATA_TYPE_STRAIN"></span><span id="sensor_data_type_strain"></span><dl> <dt>**SENSOR \_ TENSIÓN \_ DE \_ TIPO DE**</dt> DATOS <dt> (PID = 7)</dt> </dl>                                                                  | **VT \_ R8**<br/> Cepa.<br/>                                           |
| <span id="SENSOR_DATA_TYPE_WEIGHT_KILOGRAMS"></span><span id="sensor_data_type_weight_kilograms"></span><dl> <dt>**SENSOR \_ PONDERACIONES \_ \_ DE TIPO DE \_ DATOS**</dt> <dt> (PID = 8)</dt> </dl>                                   | **VT \_ R8**<br/> Peso, en pesos.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




