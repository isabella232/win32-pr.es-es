---
description: Windows Dispositivos portátiles define los siguientes valores de evento.
ms.assetid: d73788a1-d0fe-4a69-b472-edf438a28f90
title: Constantes de evento (PortableDevice.h)
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
ms.openlocfilehash: 5ae8a0a519af32a68bd65241f847cadcaa3d623be932a747e21a3b86338d680d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119704795"
---
# <a name="event-constants-portabledeviceh"></a>Constantes de evento (PortableDevice.h)

Windows Dispositivos portátiles define los siguientes valores de evento.



| Constante                                                                                                                                                                                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WPD_EVENT_DEVICE_CAPABILITIES_UPDATED"></span><span id="wpd_event_device_capabilities_updated"></span><dl> <dt>**FUNCIONALIDADES DEL DISPOSITIVO DE EVENTOS WPD \_ \_ \_ \_ ACTUALIZADAS**</dt> </dl> | Este evento indica que las funcionalidades del dispositivo han cambiado. Los clientes deben volver a consultar el dispositivo si han tomado alguna decisión en función de las funcionalidades del dispositivo.<br/>                                                                                                                                                                                              |
| <span id="WPD_EVENT_DEVICE_REMOVED"></span><span id="wpd_event_device_removed"></span><dl> <dt>**DISPOSITIVO DE \_ EVENTOS WPD \_ \_ QUITADO**</dt> </dl>                                         | Este evento se envía cuando se descarga un controlador para un dispositivo. Normalmente, esto se debe a que el dispositivo está desconectado.<br/> Los clientes deben liberar **la interfaz IPortableDevice** y todas las interfaces [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice) especificadas en **WPD EVENT PARAMETER \_ \_ \_ PNP DEVICE \_ \_ ID**.<br/>                          |
| <span id="WPD_EVENT_DEVICE_RESET"></span><span id="wpd_event_device_reset"></span><dl> <dt>**RESTABLECIMIENTO DEL \_ DISPOSITIVO DE EVENTOS \_ WPD \_**</dt> </dl>                                               | Este evento indica que el dispositivo está a punto de restablecerse y todos los clientes conectados deben cerrar sus conexiones al dispositivo.<br/>                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_ADDED"></span><span id="wpd_event_object_added"></span><dl> <dt>**OBJETO DE \_ EVENTO \_ \_ WPD AGREGADO**</dt> </dl>                                               | Este evento indica que hay un nuevo objeto disponible en el dispositivo.<br/>                                                                                                                                                                                                                                                                                           |
| <span id="WPD_EVENT_OBJECT_REMOVED"></span><span id="wpd_event_object_removed"></span><dl> <dt>**SE HA QUITADO \_ EL OBJETO DE EVENTO \_ \_ WPD**</dt> </dl>                                         | Este evento se envía después de quitar un objeto existente previamente del dispositivo.<br/> El objeto podría ser un objeto de contenido, por ejemplo, se eliminó un archivo de imagen; o podría ser un objeto funcional; por ejemplo, se deseconseje un nuevo dispositivo de almacenamiento del dispositivo.<br/>                                                                        |
| <span id="WPD_EVENT_OBJECT_TRANSFER_REQUESTED"></span><span id="wpd_event_object_transfer_requested"></span><dl> <dt>**SE SOLICITÓ \_ LA TRANSFERENCIA DE OBJETOS DE EVENTO \_ \_ \_ WPD**</dt> </dl>       | Este evento se envía para solicitar a una aplicación que transfiera un objeto determinado desde el dispositivo.<br/> El objeto suele ser un objeto de contenido, por ejemplo, un archivo de imagen.<br/>                                                                                                                                                                                 |
| <span id="WPD_EVENT_OBJECT_UPDATED"></span><span id="wpd_event_object_updated"></span><dl> <dt>**OBJETO DE \_ EVENTO WPD \_ \_ ACTUALIZADO**</dt> </dl>                                         | Este evento se envía después de actualizar un objeto y cualquier cliente conectado debe actualizar su vista de ese objeto.<br/>                                                                                                                                                                                                                                        |
| <span id="WPD_EVENT_SERVICE_METHOD_COMPLETE"></span><span id="wpd_event_service_method_complete"></span><dl> <dt>**MÉTODO DE \_ SERVICIO DE EVENTOS WPD \_ \_ \_ COMPLETADO**</dt> </dl>             | Este evento se envía cuando un controlador ha completado la invocación de un método de servicio. Este evento debe enviarse incluso cuando se produce un error en el método . Se trata de un evento interno de WPD DDI y no estará disponible para ninguna aplicación a través de [**IPortableDevice::Advise**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-advise) o [**IPortableDeviceService::Advise**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-advise).<br/> |
| <span id="WPD_EVENT_STORAGE_FORMAT"></span><span id="wpd_event_storage_format"></span><dl> <dt>**FORMATO DE \_ ALMACENAMIENTO DE \_ EVENTOS \_ WPD**</dt> </dl>                                         | Este evento indica el progreso de una operación de formato en un objeto de almacenamiento.<br/>                                                                                                                                                                                                                                                                                 |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes](constants.md)
</dt> </dl>

 

 




