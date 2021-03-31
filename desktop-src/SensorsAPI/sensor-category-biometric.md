---
description: La categoría de \_ BIOmétrica de categoría de sensor \_ contiene sensores que proporcionan información sobre los seres vivo.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71660c7bc94037c21502c91e017a8eba369766a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154060"
---
# <a name="sensor_category_biometric"></a>biométrica de categoría de SENSOR \_ \_

La categoría de \_ BIOmétrica de categoría de sensor \_ contiene sensores que proporcionan información sobre los seres vivo.

**Tipos de sensores definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                           | Descripción                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**Sensor \_ de ESCRIBIR \_ \_ presencia humana**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensores que detectan la presencia humana.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**Sensor \_ de Escriba \_ \_ proximidad humana**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensores que detectan proximidad humana.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**Sensor \_ de Escriba \_ Touch**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Sensores táctiles.<br/>                       |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en el tipo de datos del SENSOR \_ \_ \_ GUID biométrico \_ :

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                         | Descripción                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**Sensor \_ de \_ \_ \_ Presencia humana de tipo de datos**</dt> <dt>(PID = 2)</dt> </dl>                          | **VT \_ bool**<br/> **True** cuando un usuario usa el equipo.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**Sensor \_ de \_Medidor de \_ \_ proximidad humana \_ de tipo de datos**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Distancia entre un usuario y el equipo, en metros.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**Sensor \_ de \_ \_ \_ Estado de tipo de datos táctil**</dt> <dt>(PID = 4)</dt> </dl>                                   | **VT \_ bool**<br/> **True** cuando se toca el sensor táctil; en caso contrario, **false**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

 




