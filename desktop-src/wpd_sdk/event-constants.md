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
# <a name="event-constants-portabledeviceh"></a>Constantes de evento (PortableDevice. h)

Dispositivos portátiles de Windows define los siguientes valores de evento.



| Constante                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**\_capacidades del dispositivo de eventos WPD \_ \_ \_ actualizadas**</dt> </dl> | Este evento indica que las funcionalidades del dispositivo han cambiado. Los clientes deben reconsultar el dispositivo si han tomado decisiones en función de las capacidades del dispositivo.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**\_dispositivo de eventos WPD \_ \_ quitado**</dt> </dl>                                         | Este evento se envía cuando se descarga un controlador para un dispositivo. Normalmente, se debe a que el dispositivo se está desenchufando.<br/> Los clientes deben liberar la interfaz **IPortableDevice** y las interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) especificadas en el parámetro de evento de **WPD ID. de \_ \_ \_ \_ dispositivo \_ PNP**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**\_restablecimiento del \_ dispositivo de eventos de WPD \_**</dt> </dl>                                               | Este evento indica que el dispositivo está a punto de restablecerse y que todos los clientes conectados deben cerrar sus conexiones con el dispositivo.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**\_objeto de evento WPD \_ \_ agregado**</dt> </dl>                                               | Este evento indica que un nuevo objeto está disponible en el dispositivo.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**\_objeto de evento WPD \_ \_ quitado**</dt> </dl>                                         | Este evento se envía una vez que se ha quitado un objeto existente previamente del dispositivo.<br/> El objeto puede ser un objeto de contenido; por ejemplo, se ha eliminado un archivo de imagen; o bien, podría tratarse de un objeto funcional, por ejemplo, un nuevo dispositivo de almacenamiento se desconectó del dispositivo.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**\_transferencia de objeto de evento WPD \_ \_ \_ solicitada**</dt> </dl>       | Este evento se envía para solicitar a una aplicación que transfiera un objeto determinado desde el dispositivo.<br/> Normalmente, el objeto es un objeto de contenido, por ejemplo, un archivo de imagen.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**\_objeto de evento WPD \_ \_ actualizado**</dt> </dl>                                         | Este evento se envía una vez que se ha actualizado un objeto y cualquier cliente conectado debe actualizar su vista de ese objeto.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**\_método de servicio de eventos WPD \_ \_ \_ completado**</dt> </dl>             | Este evento se envía cuando un controlador ha finalizado la invocación de un método de servicio. Este evento se debe enviar incluso cuando se produce un error en el método. Este es un evento interno de DDI de WPD y no estará disponible para las aplicaciones a través de [**IPortableDevice:: Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) o [**IPortableDeviceService:: Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**\_formato de \_ almacenamiento de eventos de WPD \_**</dt> </dl>                                         | Este evento indica el progreso de una operación de formato en un objeto de almacenamiento.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
</dt> </dl>

 

 




