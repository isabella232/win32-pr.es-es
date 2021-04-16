---
description: Dispositivos portátiles de Windows define los siguientes valores de evento.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Constantes de evento (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_EVENT_DEVICE_CAPABILITIES_UPDATED
- WPD_EVENT_DEVICE_REMOVED
- WPD_EVENT_DEVICE_RESET
- WPD_EVENT_OBJECT_ADDED
- WPD_EVENT_OBJECT_REMOVED
- WPD_EVENT_OBJECT_TRANSFER_REQUESTED
- WPD_EVENT_OBJECT_UPDATED
- WPD_EVENT_SERVICE_METHOD_COMPLETE
- WPD_EVENT_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e60c44cda2585655a86ca1cdb4653ad002a0225d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699756"
---
# <a name="event-constants-portabledeviceh"></a><span data-ttu-id="a3971-103">Constantes de evento (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="a3971-103">Event Constants (PortableDevice.h)</span></span>

<span data-ttu-id="a3971-104">Dispositivos portátiles de Windows define los siguientes valores de evento.</span><span class="sxs-lookup"><span data-stu-id="a3971-104">Windows Portable Devices defines the following event values.</span></span>



| <span data-ttu-id="a3971-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a3971-105">Constant</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="a3971-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="a3971-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <span data-ttu-id="a3971-107"><dt>**\_capacidades del dispositivo de eventos WPD \_ \_ \_ actualizadas**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-107"><dt>**WPD\_EVENT\_DEVICE\_CAPABILITIES\_UPDATED**</dt></span></span> </dl> | <span data-ttu-id="a3971-108">Este evento indica que las funcionalidades del dispositivo han cambiado.</span><span class="sxs-lookup"><span data-stu-id="a3971-108">This event indicates that the device capabilities have changed.</span></span> <span data-ttu-id="a3971-109">Los clientes deben reconsultar el dispositivo si han tomado decisiones en función de las capacidades del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-109">Clients should requery the device if they have made any decisions based on device capabilities.</span></span><br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <span data-ttu-id="a3971-110"><dt>**\_dispositivo de eventos WPD \_ \_ quitado**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-110"><dt>**WPD\_EVENT\_DEVICE\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="a3971-111">Este evento se envía cuando se descarga un controlador para un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-111">This event is sent when a driver for a device is being unloaded.</span></span> <span data-ttu-id="a3971-112">Normalmente, se debe a que el dispositivo se está desenchufando.</span><span class="sxs-lookup"><span data-stu-id="a3971-112">Typically this is a result of the device being unplugged.</span></span><br/> <span data-ttu-id="a3971-113">Los clientes deben liberar la interfaz **IPortableDevice** y las interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) especificadas en el parámetro de evento de **WPD ID. de \_ \_ \_ \_ dispositivo \_ PNP**.</span><span class="sxs-lookup"><span data-stu-id="a3971-113">Clients should release the **IPortableDevice** interface and any [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) interfaces specified in **WPD\_EVENT\_PARAMETER\_PNP\_DEVICE\_ID**.</span></span><br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <span data-ttu-id="a3971-114"><dt>**\_restablecimiento del \_ dispositivo de eventos de WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-114"><dt>**WPD\_EVENT\_DEVICE\_RESET**</dt></span></span> </dl>                                               | <span data-ttu-id="a3971-115">Este evento indica que el dispositivo está a punto de restablecerse y que todos los clientes conectados deben cerrar sus conexiones con el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-115">This event indicates that the device is about to be reset, and all connected clients should close their connections to the device.</span></span><br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <span data-ttu-id="a3971-116"><dt>**\_objeto de evento WPD \_ \_ agregado**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-116"><dt>**WPD\_EVENT\_OBJECT\_ADDED**</dt></span></span> </dl>                                               | <span data-ttu-id="a3971-117">Este evento indica que un nuevo objeto está disponible en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-117">This event indicates that a new object is available on the device.</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <span data-ttu-id="a3971-118"><dt>**\_objeto de evento WPD \_ \_ quitado**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-118"><dt>**WPD\_EVENT\_OBJECT\_REMOVED**</dt></span></span> </dl>                                         | <span data-ttu-id="a3971-119">Este evento se envía una vez que se ha quitado un objeto existente previamente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-119">This event is sent after a previously existing object has been removed from the device.</span></span><br/> <span data-ttu-id="a3971-120">El objeto puede ser un objeto de contenido; por ejemplo, se ha eliminado un archivo de imagen; o bien, podría tratarse de un objeto funcional, por ejemplo, un nuevo dispositivo de almacenamiento se desconectó del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-120">The object might be a content object, for example, an image file was deleted; or it might be a functional object, for example, a new storage device was unplugged from the device.</span></span><br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <span data-ttu-id="a3971-121"><dt>**\_transferencia de objeto de evento WPD \_ \_ \_ solicitada**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-121"><dt>**WPD\_EVENT\_OBJECT\_TRANSFER\_REQUESTED**</dt></span></span> </dl>       | <span data-ttu-id="a3971-122">Este evento se envía para solicitar a una aplicación que transfiera un objeto determinado desde el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3971-122">This event is sent to request an application to transfer a particular object from the device.</span></span><br/> <span data-ttu-id="a3971-123">Normalmente, el objeto es un objeto de contenido, por ejemplo, un archivo de imagen.</span><span class="sxs-lookup"><span data-stu-id="a3971-123">The object is usually a content object, for example, an image file.</span></span><br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <span data-ttu-id="a3971-124"><dt>**\_objeto de evento WPD \_ \_ actualizado**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-124"><dt>**WPD\_EVENT\_OBJECT\_UPDATED**</dt></span></span> </dl>                                         | <span data-ttu-id="a3971-125">Este evento se envía una vez que se ha actualizado un objeto y cualquier cliente conectado debe actualizar su vista de ese objeto.</span><span class="sxs-lookup"><span data-stu-id="a3971-125">This event is sent after an object has been updated, and any connected client should refresh its view of that object.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <span data-ttu-id="a3971-126"><dt>**\_método de servicio de eventos WPD \_ \_ \_ completado**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-126"><dt>**WPD\_EVENT\_SERVICE\_METHOD\_COMPLETE**</dt></span></span> </dl>             | <span data-ttu-id="a3971-127">Este evento se envía cuando un controlador ha finalizado la invocación de un método de servicio.</span><span class="sxs-lookup"><span data-stu-id="a3971-127">This event is sent when a driver has completed invoking a service method.</span></span> <span data-ttu-id="a3971-128">Este evento se debe enviar incluso cuando se produce un error en el método.</span><span class="sxs-lookup"><span data-stu-id="a3971-128">This event must be sent even when the method fails.</span></span> <span data-ttu-id="a3971-129">Este es un evento interno de DDI de WPD y no estará disponible para las aplicaciones a través de [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) o [**IPortableDeviceService:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span><span class="sxs-lookup"><span data-stu-id="a3971-129">This is an internal WPD DDI event, and will not be available to any applications through [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) or [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).</span></span><br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <span data-ttu-id="a3971-130"><dt>**\_formato de \_ almacenamiento de eventos de WPD \_**</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-130"><dt>**WPD\_EVENT\_STORAGE\_FORMAT**</dt></span></span> </dl>                                         | <span data-ttu-id="a3971-131">Este evento indica el progreso de una operación de formato en un objeto de almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="a3971-131">This event indicates the progress of a format operation on a storage object.</span></span><br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a><span data-ttu-id="a3971-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3971-132">Requirements</span></span>



| <span data-ttu-id="a3971-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="a3971-133">Requirement</span></span> | <span data-ttu-id="a3971-134">Value</span><span class="sxs-lookup"><span data-stu-id="a3971-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3971-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a3971-135">Header</span></span><br/> | <dl> <span data-ttu-id="a3971-136"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="a3971-136"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a3971-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="a3971-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a3971-138">Constantes</span><span class="sxs-lookup"><span data-stu-id="a3971-138">Constants</span></span>](constants.md)
</dt> </dl>

 

 




