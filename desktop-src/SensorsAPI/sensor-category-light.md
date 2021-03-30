---
description: La \_ categoría de la categoría de la luz del sensor \_ contiene sensores que proporcionan información sobre las características de la luz.
ms.assetid: 0327bda5-f1d7-476d-9f0f-f4d60a6a106f
title: SENSOR_CATEGORY_LIGHT (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca14bba297a8f445312873fc810e7d0b5ba13a4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907797"
---
# <a name="sensor_category_light"></a>\_luz de categoría de sensor \_

La \_ categoría de la categoría de la luz del sensor \_ contiene sensores que proporcionan información sobre las características de la luz.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                     | Descripción                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------|
| <span id="SENSOR_TYPE_AMBIENT_LIGHT"></span><span id="sensor_type_ambient_light"></span><dl> <dt>**Sensor \_ de Escriba \_ \_ luz ambiente**</dt> <dt>{97F115C8-599A-4153-8894-D2D12899918A}</dt> </dl> | Sensores de luz ambiente.<br/> |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ \_ \_ GUID Light:

{E4C77CE2-DCB7-46E9-8439-4FEC548833A6}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                                | Descripción                                                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_LIGHT_CHROMACITY__"></span><span id="sensor_data_type_light_chromacity__"></span><dl> <dt> **Tipo de datos de sensor \_ \_ \_ Light \_ CHROMACITY**</dt> <dt>(PID = 4)</dt> </dl>                     | **VT \_ Vector \| VT \_ UI1**<br/> Cromaticidad como una matriz contada de valores float.<br/> Los datos de los tipos de vector siempre se serializan como **VT \_ UI1** (una matriz de caracteres sin signo de 1 byte). Este campo de datos contiene realmente cada valor como un valor real de 4 bytes de IEEE (**VT \_ R4**).<br/> Para obtener información sobre cómo trabajar con matrices, vea [recuperar tipos de vectores](retrieving-vector-types.md).<br/> |
| <span id="SENSOR_DATA_TYPE_LIGHT_LEVEL_LUX"></span><span id="sensor_data_type_light_level_lux"></span><dl> <dt>**Sensor \_ de \_Nivel ligero de tipo de datos \_ \_ \_ Lux**</dt> <dt> (PID = 2)</dt> </dl>                            | **VT \_ R4**<br/> Nivel de luminancia, en Lux.<br/>                                                                                                                                                                                                                                                                                                                                                              |
| <span id="SENSOR_DATA_TYPE_LIGHT_TEMPERATURE_KELVIN"></span><span id="sensor_data_type_light_temperature_kelvin"></span><dl> <dt>**Sensor \_ de \_Temperatura ligera de tipo de datos \_ \_ \_ Kelvin**</dt> <dt> (PID = 3)</dt> </dl> | **VT \_ R4**<br/> Temperatura de color, en grados Kelvin.<br/>                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




