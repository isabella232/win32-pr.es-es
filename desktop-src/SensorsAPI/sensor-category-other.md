---
description: La categoría de SENSOR \_ \_ otra categoría contiene sensores que admiten la clase personalizada en el controlador de clase HID.
ms.assetid: 866F7BF4-15CC-4F69-9510-B5858D47C4D0
title: SENSOR_CATEGORY_OTHER (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e26ece66ae74e873c48cd973cc447beec2dd8f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104082056"
---
# <a name="sensor_category_other"></a>Categoría de SENSOR \_ \_ diferente

La categoría de SENSOR \_ \_ otra categoría contiene sensores que admiten la clase personalizada en el controlador de clase HID.

<dl> <dt>

<span id="SENSOR_TYPE_CUSTOM"></span><span id="sensor_type_custom"></span>**tipo de SENSOR \_ \_ personalizado**
</dt> <dd> <dl> <dt>

{E83AF229-8640-4D18-A213-E22675EBB2C3}
</dt> <dt>



Sensor personalizado que admite la clase personalizada en el controlador de clase de HID.


</dt> </dl> </dd> </dl>

**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ \_ \_ GUID personalizado:

{B14C764F-07CF-41E8-9D82-EBE3D0776A6F}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                    | Descripción                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_CUSTOM_USAGE"></span><span id="sensor_data_type_custom_usage"></span><dl> <dt>**Sensor \_ de \_ \_ \_ Uso personalizado de tipo de datos**</dt> <dt> (PID = 5)</dt> </dl>                          | **VT \_ UI4**<br/> Un uso de HID que se puede usar para distinguir varios sensores personalizados.<br/> |
| <span id="SENSOR_DATA_TYPE_CUSTOM_BOOLEAN_ARRAY"></span><span id="sensor_data_type_custom_boolean_array"></span><dl> <dt>**Sensor \_ de \_ \_ \_ \_ Matriz booleana personalizada de tipo de datos**</dt> <dt> (PID = 6)</dt> </dl> | **VT \_ UI4**<br/> Matriz de valores booleanos para un sensor personalizado determinado.<br/>                  |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE1"></span><span id="sensor_data_type_custom_value1"></span><dl> <dt>**Sensor \_ de Tipo de datos \_ \_ Custom \_ VALUE1**</dt> <dt> (PID = 7)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Uno de los seis valores disponibles para un sensor personalizado determinado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE2"></span><span id="sensor_data_type_custom_value2"></span><dl> <dt>**Sensor \_ de Tipo de datos \_ \_ personalizado \_ VALUE2**</dt> <dt> (PID = 8)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Uno de los seis valores disponibles para un sensor personalizado determinado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE3"></span><span id="sensor_data_type_custom_value3"></span><dl> <dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE3 personalizado**</dt> <dt> (PID = 9)</dt> </dl>                       | **VT \_ UI4 \| \| VT \_ R4**<br/> Uno de los seis valores disponibles para un sensor personalizado determinado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE4"></span><span id="sensor_data_type_custom_value4"></span><dl> <dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE4 personalizado**</dt> <dt> (PID = 10)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Uno de los seis valores disponibles para un sensor personalizado determinado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE5"></span><span id="sensor_data_type_custom_value5"></span><dl> <dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE5 personalizado**</dt> <dt> (PID = 11)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Uno de los seis valores disponibles para un sensor personalizado determinado.<br/>       |
| <span id="SENSOR_DATA_TYPE_CUSTOM_VALUE6"></span><span id="sensor_data_type_custom_value6"></span><dl> <dt>**Sensor \_ de \_Tipo de \_ datos \_ VALUE6 personalizado**</dt> <dt> (PID = 12)</dt> </dl>                      | **VT \_ UI4 \| \| VT \_ R4**<br/> Uno de los seis valores disponibles para un sensor personalizado determinado.<br/>       |



## <a name="remarks"></a>Observaciones

Un sensor que admita la clase genérica en el controlador de clase HID se asignará a una de las otras categorías definidas (biométrico, eléctrico, entorno, etc.).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




