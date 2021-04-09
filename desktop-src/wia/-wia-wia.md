---
description: El objeto WIA es el punto de entrada para todas las funciones de scripting de adquisición de imágenes de Windows (WIA).
ms.assetid: 1905e344-32cc-41ec-885f-bfabd8edd419
title: WIA (objeto)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Wia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 3ab1a9d150eebe77537e18aebc8ab1a3e342099e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154377"
---
# <a name="wia-object"></a>WIA (objeto)

El objeto **WIA** es el punto de entrada para todas las funciones de scripting de adquisición de imágenes de Windows (WIA). Cualquier aplicación que use el modelo de scripting de WIA debe crear un objeto [**SafeWia**](-wia-safewia.md) o **WIA** . Use ese objeto para enumerar y crear dispositivos y recibir notificaciones de eventos de hardware.

> [!Note]  
> Este objeto no es seguro para el scripting. Para obtener una versión de este objeto segura para el scripting, vea [**SafeWia**](-wia-safewia.md).

 

## <a name="members"></a>Miembros

El objeto **WIA** tiene estos tipos de miembros:

-   [Eventos](#events)
-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="events"></a>Events

El objeto **WIA** tiene estos eventos.



| Evento                                                                 | Descripción                                                                  |
|:----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [**OnDeviceConnected**](-wia--iwiaevents-ondeviceconnected.md)       | Evento que tiene lugar cuando se conecta un nuevo dispositivo de hardware WIA.<br/>    |
| [**OnDeviceDisconnected**](-wia--iwiaevents-ondevicedisconnected.md) | Evento que tiene lugar cuando se desconecta un dispositivo de hardware WIA nuevo.<br/> |
| [**OnTransferComplete**](-wia--iwiaevents-ontransfercomplete.md)     | Evento que tiene lugar cuando se completa una transferencia de datos correctamente.<br/> |



 

### <a name="methods"></a>Métodos

El objeto **WIA** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                |
|:-----------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**A**](-wia-iwia-create.md) | El método [**Create**](-wia-iwia-create.md) del objeto **WIA** establece una conexión con el dispositivo WIA especificado y devuelve un objeto de [**elemento**](-wia-item.md) que representa el dispositivo.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **WIA** tiene estas propiedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propiedad</th>
<th style="text-align: left;">Tipo de acceso</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Dispositivos</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Colección de objetos <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> que representa todos los dispositivos instalados en el equipo. Solo lectura. <br/>
<blockquote>
[!Note]<br />
Esta colección está basada en 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Wiascr.dll (versión 4,90 o posterior)</dt> </dl> |
| IID<br/>                      | WIA de CLSID \_<br/>                                                                                         |



 

 




