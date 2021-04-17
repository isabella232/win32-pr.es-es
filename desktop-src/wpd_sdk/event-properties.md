---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de evento.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Propiedades de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700363"
---
# <a name="event-properties"></a><span data-ttu-id="e7fd1-103">Propiedades de evento</span><span class="sxs-lookup"><span data-stu-id="e7fd1-103">Event Properties</span></span>

<span data-ttu-id="e7fd1-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de evento.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-104">Windows Portable Devices supports the following event properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e7fd1-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e7fd1-105">Property</span></span></th>
<th><span data-ttu-id="e7fd1-106">VarType</span><span class="sxs-lookup"><span data-stu-id="e7fd1-106">VarType</span></span></th>
<th><span data-ttu-id="e7fd1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e7fd1-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7fd1-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-108"><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></span></span></td>
<td><span data-ttu-id="e7fd1-109"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-109"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="e7fd1-110">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-110">Reserved for future use.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fd1-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-111"><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></span></span></td>
<td><span data-ttu-id="e7fd1-112"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-112"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="e7fd1-113">Valor booleano que especifica si el evento se difunde a todos los clientes. Los clientes pueden recibir este evento registrando su devolución de llamada con <strong>IPortableDevice:: Advise</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-113">A Boolean value that specifies whether the event is broadcast to all clients.Clients can receive this event by registering their callback with <strong>IPortableDevice::Advise</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fd1-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-114"><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></span></span></td>
<td><span data-ttu-id="e7fd1-115"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-115"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="e7fd1-116">Valor booleano que especifica si la jerarquía secundaria del objeto ha cambiado. Este parámetro se utiliza para notificar al autor de la llamada que algunos elementos secundarios del objeto especificado se han agregado o quitado.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-116">A Boolean value that specifies whether the child hierarchy for the object has changed.This parameter is used to notify the caller that some children for the specified object have been added or removed.</span></span> <span data-ttu-id="e7fd1-117">Normalmente, el cambio de jerarquía se inicia en el lado del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-117">Typically the hierarchy change is initiated on the device side.</span></span> <span data-ttu-id="e7fd1-118">Es posible que los clientes tengan que volver a enumerar los elementos secundarios de esta carpeta para mantener sus vistas actualizadas.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-118">Clients may have to re-enumerate this folder's children to keep their views up to date.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fd1-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-119"><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></span></span></td>
<td><span data-ttu-id="e7fd1-120"><strong>VT_CLSID</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-120"><strong>VT_CLSID</strong></span></span></td>
<td><span data-ttu-id="e7fd1-121">Valor que identifica un evento.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-121">A value that identifies an event.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fd1-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-122"><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></span></span></td>
<td><span data-ttu-id="e7fd1-123"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-123"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="e7fd1-124">La cookie se entrega a un cliente cuando solicita la creación de un objeto llamando al método <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent:: CreateObjectWithPropertiesAndData</strong></a> . Este parámetro se agrega como una comodidad para ayudar al autor de la llamada a asociar un evento de adición de objeto a la solicitud enviada para crear el objeto.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-124">The cookie handed back to a client when it requests an object creation by calling the <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent::CreateObjectWithPropertiesAndData</strong></a> method.This parameter is added as a convenience to help the caller tie an object-added event to the request it sent to create the object.</span></span> <span data-ttu-id="e7fd1-125">El controlador vuelve a esta cookie como el <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> valor devuelto al procesar el comando <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .</span><span class="sxs-lookup"><span data-stu-id="e7fd1-125">The driver hands this cookie back as the <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> return value when processing the <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> command.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fd1-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-126"><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="e7fd1-127"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-127"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="e7fd1-128">Valor que identifica de forma única el objeto primario.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-128">A value that uniquely identifies the parent object.</span></span> <span data-ttu-id="e7fd1-129">Esta propiedad es similar a <strong>WPD_OBJECT_PARENT_ID</strong>, pero este identificador no cambia entre sesiones.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-129">This property is similar to <strong>WPD_OBJECT_PARENT_ID</strong>, but this ID does not change between sessions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fd1-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-130"><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></span></span></td>
<td><span data-ttu-id="e7fd1-131"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-131"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="e7fd1-132">Valor que especifica el progreso de una operación que se está ejecutando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-132">A value that specifies the progress of a currently executing operation.</span></span> <span data-ttu-id="e7fd1-133">El valor de esta propiedad puede oscilar entre 0 y 100, con 100, lo que indica que la operación ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-133">The value of this property can range from 0 to 100, with 100 indicating that the operation is complete.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fd1-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-134"><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></span></span></td>
<td><span data-ttu-id="e7fd1-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="e7fd1-136">Valor que indica el estado actual de la operación, por ejemplo, iniciado, en ejecución, detenido, etc. Los valores posibles de este parámetro proceden de la enumeración <strong>WPD_OPERATION_STATES</strong> definida en PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-136">A value that indicates the current state of the operation, for example, started, running, stopped, and so on.This parameter's possible values are from the <strong>WPD_OPERATION_STATES</strong> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="e7fd1-137">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="e7fd1-137">Possible values are:</span></span><br/> <dl> <span data-ttu-id="e7fd1-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-138"><strong>WPD_OPERATION_STATE_UNSPECIFIED</strong></span></span><br /><span data-ttu-id="e7fd1-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-139">
<strong>WPD_OPERATION_STATE_STARTED</strong></span></span><br /><span data-ttu-id="e7fd1-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-140">
<strong>WPD_OPERATION_STATE_RUNNING</strong></span></span><br /><span data-ttu-id="e7fd1-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-141">
<strong>WPD_OPERATION_STATE_PAUSED</strong></span></span><br /><span data-ttu-id="e7fd1-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-142">
<strong>WPD_OPERATION_STATE_CANCELLED</strong></span></span><br /><span data-ttu-id="e7fd1-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-143">
<strong>WPD_OPERATION_STATE_FINISHED</strong></span></span><br /><span data-ttu-id="e7fd1-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-144">
<strong>WPD_OPERATION_STATE_ABORTED</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7fd1-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-145"><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></span></span></td>
<td><span data-ttu-id="e7fd1-146"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-146"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="e7fd1-147">Valor que especifica el dispositivo que originó el evento. Este es el identificador de dispositivo o servicio proporcionado por el sistema Plug-and-Play (PnP) y es la misma cadena que se usa en los métodos <strong>IPortableDevice:: Open</strong>o <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService:: Open</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="e7fd1-147">A value that specifies the device that originated the event.This is the device or service identifier given by the Plug-and-Play (PnP) system, and is the same string used in the <strong>IPortableDevice::Open</strong>or <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open</strong></a> methods.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7fd1-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-148"><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></span></span></td>
<td><span data-ttu-id="e7fd1-149"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="e7fd1-149"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="e7fd1-150">Una cadena utilizada por un controlador de WPD para identificar la operación de un método de servicio de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-150">A string that is used by a WPD driver to identify the operation of a device-service method.</span></span> <span data-ttu-id="e7fd1-151">Las aplicaciones no deben usar este parámetro directamente.</span><span class="sxs-lookup"><span data-stu-id="e7fd1-151">Applications should not use this parameter directly.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="e7fd1-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7fd1-152">Requirements</span></span>



| <span data-ttu-id="e7fd1-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7fd1-153">Requirement</span></span> | <span data-ttu-id="e7fd1-154">Value</span><span class="sxs-lookup"><span data-stu-id="e7fd1-154">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7fd1-155">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7fd1-155">Header</span></span><br/> | <dl> <span data-ttu-id="e7fd1-156"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7fd1-156"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7fd1-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7fd1-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7fd1-158">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="e7fd1-158">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




