---
description: La Windows sensor y la ubicación definen constantes para los eventos de controlador. Los manfuactureres de sensor también pueden definir sus propias constantes.
ms.assetid: ca61c912-bce5-4e41-ab48-40615d5b93ba
title: Constantes de evento (Sensors.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc9fb3ced92c1fe263538f2ce27c3fc65fdd7676
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374859"
---
# <a name="event-constants-sensorsh"></a>Constantes de evento (Sensors.h)

La Windows sensor y la ubicación definen constantes para los eventos de controlador. Los manfuactureres de sensor también pueden definir sus propias constantes.

**Tipos de eventos de sensor**

La plataforma define los siguientes identificadores de tipo de evento de sensor.



| Tipo de evento sensor                                                                                                                                                                                                                                                                                                    | Descripción                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <dt>**SENSOR \_ EVENT \_ ACCELEROMETER \_ SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt> </dl> | Indica que el dispositivo se agite.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <dt>**SENSOR \_ DATOS \_ DE \_ EVENTOS ACTUALIZADOS**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt> </dl>                      | Indica que hay nuevos datos disponibles.<br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <dt>**SENSOR \_ PROPIEDAD \_ DE \_ EVENTO MODIFICADA**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt> </dl>          | Indica que ha cambiado un valor de propiedad. Compruebe la [interfaz IPortableDeviceValues,](/previous-versions//ms740012(v=vs.85)) que se pasa a través del parámetro *pEventData* a [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), para determinar qué propiedad ha cambiado y su nuevo valor.<br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <dt>**SENSOR \_ ESTADO \_ DEL \_ EVENTO CAMBIADO**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt> </dl>                   | Indica un cambio del estado operativo, por ejemplo, de SENSOR \_ STATE \_ INITIALIZING a SENSOR \_ STATE \_ READY.<br/>                                                                                                                                                                                            |



**Sensor Event PROPERTYKEYs**

Las claves de propiedad definidas por la plataforma para los eventos se basan en el GUID siguiente:

{64346E30-8728-4B34-BDF6-4F52442C5C28}

La plataforma del sensor define los siguientes **PROPERTYKEY** que identifican los parámetros de evento del sensor.



| Evento de sensor PROPERTYKEY y PID                                                                                                                                                                                                                                                      | Descripción                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <dt>**SENSOR \_ ID. \_ \_ DE EVENTO \_ DE PARÁMETRO**</dt> DE EVENTO <dt>(PID = 2)</dt> </dl> | Indica que el valor **GUID** de [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) es un identificador de tipo de evento, como SENSOR \_ EVENT DATA \_ \_ UPDATED.<br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <dt>**SENSOR \_ ESTADO \_ DEL PARÁMETRO \_ DE**</dt> <dt>EVENTO (PID = 3)</dt> </dl>           | Indica que el valor entero sin signo de **IPortableDeviceValues** es un estado de sensor, como SENSOR \_ STATE \_ READY.<br/>                                                  |



**Sensor Error PROPERTYKEYs**

Las claves de propiedad definidas por la plataforma para errores se basarán en el GUID siguiente:

{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}

La plataforma del sensor reserva este GUID para su uso futuro.

<dl></dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                            |
| Encabezado<br/>                   | <dl> <dt>Sensors.h</dt> </dl> |



 

