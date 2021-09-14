---
description: Windows Dispositivos portátiles admite las siguientes propiedades de evento.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Propiedades de eventos (PortableDevice.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251409"
---
# <a name="event-properties"></a>Propiedades de evento

Windows Dispositivos portátiles admite las siguientes propiedades de evento.



<table>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>VarType</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Reservado para uso futuro.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valor booleano que especifica si el evento se difunde a todos los clientes. Los clientes pueden recibir este evento registrando su devolución de llamada <strong>con IPortableDevice::Advise</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valor booleano que especifica si la jerarquía secundaria del objeto ha cambiado. Este parámetro se usa para notificar al autor de la llamada que se han agregado o quitado algunos secundarios del objeto especificado. Normalmente, el cambio de jerarquía se inicia en el lado del dispositivo. Es posible que los clientes tengan que volver a enumerar los elementos secundarios de esta carpeta para mantener actualizadas sus vistas.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Valor que identifica un evento.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>La cookie se devuelve a un cliente cuando solicita la creación de un objeto mediante una llamada al <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>método IPortableDeviceContent::CreateObjectWithPropertiesAndData.</strong></a> Este parámetro se agrega por comodidad para ayudar al autor de la llamada a vincular un evento agregado a un objeto a la solicitud que envió para crear el objeto. El controlador devuelve esta cookie como WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT <strong>valor</strong> devuelto al procesar <strong>el WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> comando.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valor que identifica de forma única el objeto primario. Esta propiedad es similar a <strong>WPD_OBJECT_PARENT_ID</strong>, pero este identificador no cambia entre sesiones.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valor que especifica el progreso de una operación que se está ejecutando actualmente. El valor de esta propiedad puede oscilar entre 0 y 100, y 100 indica que la operación se ha completado.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valor que indica el estado actual de la operación, por ejemplo, iniciado, en ejecución, detenido, y así sucesivamente. Los valores posibles de este parámetro son de la <strong>WPD_OPERATION_STATES</strong> enumeración definida en PortableDevice.h. Los valores posibles son:<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valor que especifica el dispositivo que originó el evento. Se trata del identificador de dispositivo o servicio que proporciona el sistema Plug-and-Play (PnP) y es la misma cadena que se usa en los métodos <strong>IPortableDevice::Open</strong>o <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService::Open.</strong></a><br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Cadena que usa un controlador WPD para identificar el funcionamiento de un método device-service. Las aplicaciones no deben usar este parámetro directamente.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades y atributos de WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




