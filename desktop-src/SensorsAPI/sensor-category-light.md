---
description: La categoría SENSOR \_ CATEGORY \_ LIGHT contiene sensores que proporcionan información sobre las características de la luz.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d42243cc5efeae54a06dd25ca92d5fa99f2d954e9115a10f77ac1278ced93125
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119406505"
---
# <a name="sensor_category_light"></a>SENSOR \_ CATEGORY \_ LIGHT

La categoría SENSOR \_ CATEGORY \_ LIGHT contiene sensores que proporcionan información sobre las características de la luz.

**Tipos de sensor definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                     | Descripción                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <dt>**SENSOR \_ TYPE \_ AMBIENT \_ LIGHT**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt> </dl> | Sensores de luz ambiental.<br/> |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en SENSOR \_ DATA \_ TYPE LIGHT \_ \_ GUID:

{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <dt> **SENSOR \_ DATA TYPE \_ \_ \_ LIGHTCITY**</dt> <dt>(PID = 4)</dt> </dl>                     | **VT \_ VECTOR \| VT \_ UI1**<br/> Ticidad como matriz con recuento de valores float.<br/> Los datos de los tipos de vector siempre se serializan **como \_ VT UI1** (una matriz de caracteres sin signo de 1 byte). Este campo de datos contiene realmente cada valor como un valor real ieee de 4 bytes **(VT \_ R4).**<br/> Para obtener información sobre cómo trabajar con matrices, vea [Recuperar tipos de vector.](retrieving-vector-types.md)<br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE LIGHT LEVEL \_ \_ \_ LX**</dt> <dt> (PID = 2)</dt> </dl>                            | **VT \_ R4**<br/> Nivel de iluminance, enum.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE LIGHT TEMPERATURE \_ \_ \_ KELVIN**</dt> <dt> (PID = 3)</dt> </dl> | **VT \_ R4**<br/> Temperatura del color, en grados Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




