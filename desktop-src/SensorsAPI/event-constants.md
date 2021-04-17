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
# <a name="event-constants-sensorsh"></a><span data-ttu-id="aee3b-104">Constantes de evento (Sensors. h)</span><span class="sxs-lookup"><span data-stu-id="aee3b-104">Event Constants (Sensors.h)</span></span>

<span data-ttu-id="aee3b-105">El sensor de Windows y la plataforma de ubicación define las constantes para los eventos de controlador.</span><span class="sxs-lookup"><span data-stu-id="aee3b-105">The Windows Sensor and Location platform defines constants for driver events.</span></span> <span data-ttu-id="aee3b-106">Sensor manfuactureres también puede definir sus propias constantes.</span><span class="sxs-lookup"><span data-stu-id="aee3b-106">Sensor manfuactureres can also define their own constants.</span></span>

<span data-ttu-id="aee3b-107">**Tipos de eventos de sensor**</span><span class="sxs-lookup"><span data-stu-id="aee3b-107">**Sensor Event Types**</span></span>

<span data-ttu-id="aee3b-108">La plataforma define los siguientes identificadores de tipo de evento de sensor.</span><span class="sxs-lookup"><span data-stu-id="aee3b-108">The platform defines the following sensor event type identifiers.</span></span>



| <span data-ttu-id="aee3b-109">Tipo de evento de sensor</span><span class="sxs-lookup"><span data-stu-id="aee3b-109">Sensor event type</span></span>                                                                                                                                                                                                                                                                                                    | <span data-ttu-id="aee3b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="aee3b-110">Description</span></span>                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_ACCELEROMETER_SHAKE"></span><span id="sensor_event_accelerometer_shake"></span><dl> <span data-ttu-id="aee3b-111"><dt>**Sensor \_ de EVENT \_ Accelerometer \_ agite**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-111"><dt>**SENSOR\_EVENT\_ACCELEROMETER\_SHAKE**</dt> <dt>{825F5A94-0F48-4396-9CA0-6ECB5C99D915}</dt></span></span> </dl> | <span data-ttu-id="aee3b-112">Indica que el dispositivo se ha agitado.</span><span class="sxs-lookup"><span data-stu-id="aee3b-112">Indicates that the device was shaken.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_DATA_UPDATED"></span><span id="sensor_event_data_updated"></span><dl> <span data-ttu-id="aee3b-113"><dt>**Sensor \_ de Datos de eventos \_ \_ actualizados**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-113"><dt>**SENSOR\_EVENT\_DATA\_UPDATED**</dt> <dt>{2ED0F2A4-0087-41D3-87DB-6773370B3C88}</dt></span></span> </dl>                      | <span data-ttu-id="aee3b-114">Indica que los nuevos datos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="aee3b-114">Indicates that new data is available.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <span id="SENSOR_EVENT_PROPERTY_CHANGED"></span><span id="sensor_event_property_changed"></span><dl> <span data-ttu-id="aee3b-115"><dt>**Sensor \_ de Propiedad de evento \_ \_ cambiada**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-115"><dt>**SENSOR\_EVENT\_PROPERTY\_CHANGED**</dt> <dt>{2358F099-84C9-4D3D-90DF-C2421E2B2045}</dt></span></span> </dl>          | <span data-ttu-id="aee3b-116">Indica que ha cambiado un valor de propiedad.</span><span class="sxs-lookup"><span data-stu-id="aee3b-116">Indicates that a property value changed.</span></span> <span data-ttu-id="aee3b-117">Compruebe la interfaz [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) , que pasa a través del parámetro *pEventData* a [**onEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), para determinar qué propiedad ha cambiado y su nuevo valor.</span><span class="sxs-lookup"><span data-stu-id="aee3b-117">Check the [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) interface, passed through the *pEventData* parameter to [**OnEvent**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onevent), to determine which property changed and its new value.</span></span><br/> |
| <span id="SENSOR_EVENT_STATE_CHANGED"></span><span id="sensor_event_state_changed"></span><dl> <span data-ttu-id="aee3b-118"><dt>**Sensor \_ de Estado de evento \_ \_ cambiado**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-118"><dt>**SENSOR\_EVENT\_STATE\_CHANGED**</dt> <dt>{BFD96016-6BD7-4560-AD34-F2F6607E8F81}</dt></span></span> </dl>                   | <span data-ttu-id="aee3b-119">Indica un cambio de estado operativo, por ejemplo, de la \_ inicialización del estado del sensor \_ al estado del sensor \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="aee3b-119">Indicates a change of operational state, for example, from SENSOR\_STATE\_INITIALIZING to SENSOR\_STATE\_READY.</span></span><br/>                                                                                                                                                                                            |



<span data-ttu-id="aee3b-120">**PROPERTYKEYs de evento de sensor**</span><span class="sxs-lookup"><span data-stu-id="aee3b-120">**Sensor Event PROPERTYKEYs**</span></span>

<span data-ttu-id="aee3b-121">Las claves de propiedad definidas por la plataforma para los eventos se basan en el siguiente GUID:</span><span class="sxs-lookup"><span data-stu-id="aee3b-121">Platform-defined property keys for events are based on the following GUID:</span></span>

<span data-ttu-id="aee3b-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span><span class="sxs-lookup"><span data-stu-id="aee3b-122">{64346E30-8728-4B34-BDF6-4F52442C5C28}</span></span>

<span data-ttu-id="aee3b-123">La plataforma de sensor define los siguientes **PROPERTYKEY** s que identifican los parámetros de eventos del sensor.</span><span class="sxs-lookup"><span data-stu-id="aee3b-123">The sensor platform defines the following **PROPERTYKEY** s that identify sensor event parameters.</span></span>



| <span data-ttu-id="aee3b-124">Evento de sensor PROPERTYKEY y PID</span><span class="sxs-lookup"><span data-stu-id="aee3b-124">Sensor event PROPERTYKEY and PID</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="aee3b-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="aee3b-125">Description</span></span>                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SENSOR_EVENT_PARAMETER_EVENT_ID"></span><span id="sensor_event_parameter_event_id"></span><dl> <span data-ttu-id="aee3b-126"><dt>**Sensor \_ de \_ \_ \_ ID. de evento de parámetro de evento**</dt> <dt>(PID = 2)</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-126"><dt>**SENSOR\_EVENT\_PARAMETER\_EVENT\_ID**</dt> <dt>(PID = 2)</dt></span></span> </dl> | <span data-ttu-id="aee3b-127">Indica que el valor **GUID** de [IPORTABLEDEVICEVALUES](/previous-versions//ms740012(v=vs.85)) es un identificador de tipo de evento, como los datos de eventos de sensor \_ \_ \_ actualizados.</span><span class="sxs-lookup"><span data-stu-id="aee3b-127">Indicates that the **GUID** value in [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85)) is an event type ID, such as SENSOR\_EVENT\_DATA\_UPDATED.</span></span><br/> |
| <span id="SENSOR_EVENT_PARAMETER_STATE"></span><span id="sensor_event_parameter_state"></span><dl> <span data-ttu-id="aee3b-128"><dt>**Sensor \_ de \_ \_ Estado del parámetro de evento**</dt> <dt>(PID = 3)</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-128"><dt>**SENSOR\_EVENT\_PARAMETER\_STATE**</dt> <dt>(PID = 3)</dt></span></span> </dl>           | <span data-ttu-id="aee3b-129">Indica que el valor entero sin signo de **IPortableDeviceValues** es un estado de sensor, como \_ preparado para estado del sensor \_ .</span><span class="sxs-lookup"><span data-stu-id="aee3b-129">Indicates that the unsigned integer value in **IPortableDeviceValues** is a sensor state, such as SENSOR\_STATE\_READY.</span></span><br/>                                                  |



<span data-ttu-id="aee3b-130">**PROPERTYKEYs de error de sensor**</span><span class="sxs-lookup"><span data-stu-id="aee3b-130">**Sensor Error PROPERTYKEYs**</span></span>

<span data-ttu-id="aee3b-131">Las claves de propiedad definidas por la plataforma para errores se basarán en el siguiente GUID:</span><span class="sxs-lookup"><span data-stu-id="aee3b-131">Platform-defined property keys for errors will be based on the following GUID:</span></span>

<span data-ttu-id="aee3b-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span><span class="sxs-lookup"><span data-stu-id="aee3b-132">{77112BCD-FCE1-4f43-B8B8-A88256ADB4B3}</span></span>

<span data-ttu-id="aee3b-133">La plataforma del sensor reserva este GUID para su uso futuro.</span><span class="sxs-lookup"><span data-stu-id="aee3b-133">The sensor platform reserves this GUID for future use.</span></span>

<dl></dl>

## <a name="requirements"></a><span data-ttu-id="aee3b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aee3b-134">Requirements</span></span>



| <span data-ttu-id="aee3b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="aee3b-135">Requirement</span></span> | <span data-ttu-id="aee3b-136">Value</span><span class="sxs-lookup"><span data-stu-id="aee3b-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aee3b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aee3b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="aee3b-138">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="aee3b-138">Windows 7 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aee3b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="aee3b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="aee3b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="aee3b-140">None supported</span></span><br/>                                                            |
| <span data-ttu-id="aee3b-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="aee3b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="aee3b-142"><dt>Sensors. h</dt></span><span class="sxs-lookup"><span data-stu-id="aee3b-142"><dt>Sensors.h</dt></span></span> </dl> |



 

