---
description: La categoría SENSOR \_ CATEGORY \_ BIOMETRIC contiene sensores que proporcionan información sobre los seres humanos.
ms.assetid: dfc7ad46-c13b-46d1-8854-0d93ecaac55a
title: SENSOR_CATEGORY_BIOMETRIC (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1551a82e359d2277c8b46f227d7a72660b1419b3ba3ddfcf58bdd4ac1de5425b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889582"
---
# <a name="sensor_category_biometric"></a>CATEGORÍA DEL SENSOR \_ \_ BIOMÉTRICA

La categoría SENSOR \_ CATEGORY \_ BIOMETRIC contiene sensores que proporcionan información sobre los seres humanos.

**Tipos de sensor definidos por la plataforma**

Esta categoría incluye los siguientes tipos de sensor definidos por la plataforma.



| Tipo de sensor                                                                                                                                                                                                                                                                                           | Descripción                                     |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------|
| <span id="SENSOR_TYPE_HUMAN_PRESENCE"></span><span id="sensor_type_human_presence"></span><dl> <dt>**SENSOR \_ TYPE \_ HUMAN \_ PRESENCE**</dt> <dt>{C138C12B-AD52-451C-9375-87F518FF10C6}</dt> </dl>    | Sensores que detectan la presencia humana.<br/>  |
| <span id="SENSOR_TYPE_HUMAN_PROXIMITY"></span><span id="sensor_type_human_proximity"></span><dl> <dt>**SENSOR \_ ESCRIBA \_ HUMAN \_ PROXIMITY**</dt> <dt>{5220DAE9-3179-4430-9F90-06266D2A34DE}</dt> </dl> | Sensores que detectan proximidad humana.<br/> |
| <span id="SENSOR_TYPE_TOUCH"></span><span id="sensor_type_touch"></span><dl> <dt>**SENSOR \_ TYPE \_ TOUCH**</dt> <dt>{17DB3018-06C4-4F7D-81AF-9274B7599C27}</dt> </dl>                                | Sensores táctiles.<br/>                       |



**Campos de datos definidos por la plataforma**

Las claves de propiedad definidas por la plataforma para esta categoría se basan en EL GUID BIOMÉTRICO DEL TIPO DE \_ \_ DATOS \_ \_ SENSOR:

{2299288A-6D9E-4B0B-B7EC-3528F89E40AF}

Esta categoría incluye los siguientes campos de datos definidos por la plataforma.



| Nombre del campo de datos y PID                                                                                                                                                                                                                                                                                         | Descripción                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_DATA_TYPE_HUMAN_PRESENCE"></span><span id="sensor_data_type_human_presence"></span><dl> <dt>**SENSOR \_ PRESENCIA \_ HUMANA DE TIPO \_ \_ DE**</dt> <dt>DATOS (PID = 2)</dt> </dl>                          | **VT \_ BOOL**<br/> **TRUE** cuando una persona usa el equipo.<br/>                           |
| <span id="SENSOR_DATA_TYPE_HUMAN_PROXIMITY_METERS"></span><span id="sensor_data_type_human_proximity_meters"></span><dl> <dt>**SENSOR \_ DATA \_ TYPE \_ HUMAN \_ PROXIMITY \_ METERS**</dt> <dt>(PID = 3)</dt> </dl> | **VT \_ R4**<br/> Distancia entre una persona y el equipo, en metros.<br/>                    |
| <span id="SENSOR_DATA_TYPE_TOUCH_STATE"></span><span id="sensor_data_type_touch_state"></span><dl> <dt>**SENSOR \_ ESTADO \_ TÁCTIL DEL TIPO \_ \_ DE**</dt> <dt>DATOS (PID = 4)</dt> </dl>                                   | **VT \_ BOOL**<br/> **TRUE** cuando se está tocndo el sensor táctil; de lo contrario, **FALSE**.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows solo 7 \[ aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Header<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

 




