---
description: El sensor de Windows y la plataforma de ubicación define las constantes para los eventos de controlador. Sensor manfuactureres también puede definir sus propias constantes.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Constantes de evento (Sensors. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668005"
---
# <a name="event-constants-sensorsh"></a>Constantes de evento (Sensors. h)

El sensor de Windows y la plataforma de ubicación define las constantes para los eventos de controlador. Sensor manfuactureres también puede definir sus propias constantes.

**Tipos de eventos de sensor**

La plataforma define los siguientes identificadores de tipo de evento de sensor.



| Tipo de evento de sensor                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**Sensor \_ de EVENT \_ Accelerometer \_ agite**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Indica que el dispositivo se ha agitado.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**Sensor \_ de Datos de eventos \_ \_ actualizados**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Indica que los nuevos datos están disponibles.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**Sensor \_ de Propiedad de evento \_ \_ cambiada**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Indica que ha cambiado un valor de propiedad. Compruebe la interfaz [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , que pasa a través del parámetro *pEventData* a [**onEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), para determinar qué propiedad ha cambiado y su nuevo valor.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**Sensor \_ de Estado de evento \_ \_ cambiado**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Indica un cambio de estado operativo, por ejemplo, de la \_ inicialización del estado del sensor \_ al estado del sensor \_ \_ .<br/>                                                                                                                                                                                            |



**PROPERTYKEYs de evento de sensor**

Las claves de propiedad definidas por la plataforma para los eventos se basan en el siguiente GUID:

{64346E30-8728-4B34-BDF6-4F52442C5C28}

La plataforma de sensor define los siguientes **PROPERTYKEY** s que identifican los parámetros de eventos del sensor.



| Evento de sensor PROPERTYKEY y PID                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**Sensor \_ de \_ \_ \_ ID. de evento de parámetro de evento**</dt> <dt>(PID = 2)</dt> </dl> | Indica que el valor **GUID** de [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) es un identificador de tipo de evento, como los datos de eventos de sensor \_ \_ \_ actualizados.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**Sensor \_ de \_ \_ Estado del parámetro de evento**</dt> <dt>(PID = 3)</dt> </dl>           | Indica que el valor entero sin signo de **IPortableDeviceValues** es un estado de sensor, como \_ preparado para estado del sensor \_ .<br/>                                                  |



**PROPERTYKEYs de error de sensor**

Las claves de propiedad definidas por la plataforma para errores se basarán en el siguiente GUID:

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

La plataforma del sensor reserva este GUID para su uso futuro.

<dl></dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors. h</dt> </dl> |



 

