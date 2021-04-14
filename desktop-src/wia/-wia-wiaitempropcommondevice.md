---
description: Además de las propiedades de información de dispositivos, los dispositivos de adquisición de imágenes de Windows (WIA) tienen valores de propiedad almacenados en el registro que las aplicaciones leen y escriben.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Constantes de propiedad de dispositivo comunes (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541891"
---
# <a name="common-device-property-constants"></a>Constantes de propiedad de dispositivo comunes

Además de las propiedades de información de dispositivos, los dispositivos de adquisición de imágenes de Windows (WIA) tienen valores de propiedad almacenados en el registro que las aplicaciones leen y escriben. Están asociados con el objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o el objeto [**IWiaItem2**](-wia-iwiaitem2.md) . Las propiedades del dispositivo representan información del dispositivo, como el estado de la conexión y la hora del dispositivo. Cada propiedad de dispositivo tiene una cadena de propiedad de dispositivo asociada.

Las constantes de propiedad de dispositivo enumeradas aquí son comunes a la mayoría o a todos los dispositivos de hardware WIA.

El prefijo "WIA \_ DPA \_ " indica una propiedad de dispositivo para todos los dispositivos y es la Convención de nomenclatura que se usa en C/C++. Con el fin de crear scripts, estas constantes usan el prefijo "Device" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante o valor</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </dl></td>
<td style="text-align: left;">El estado de la conexión actual para el dispositivo. El minicontrolador crea y mantiene esta propiedad.<br/> Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> La propiedad puede tener los siguientes valores posibles.<br/> 
<table>
<thead>
<tr class="header">
<th>Estado de conexión</th>
<th>Definición</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_DEVICE_NOT_CONNECTED</td>
<td>El dispositivo no está conectado.</td>
</tr>
<tr class="even">
<td>WIA_DEVICE_CONNECTED</td>
<td>El dispositivo está conectado y operativo.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </dl></td>
<td style="text-align: left;"><p>La hora actual del reloj que está almacenada en el dispositivo. El minicontrolador crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Access: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Esta propiedad solo es compatible con dispositivos que tienen un reloj interno. Si se puede establecer el reloj del dispositivo, esta propiedad es de lectura/escritura; de lo contrario, es de solo lectura.</p>
<p>Los dispositivos WIA informan del tiempo en una estructura <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td style="text-align: left;"><p>Versión de firmware del dispositivo. Este valor debe ser un valor de cadena, como &quot; 1.0.4 &quot; o &quot; 1.0 ABC &quot; . El minicontrolador crea y mantiene esta propiedad. Si el minicontrolador de WIA no proporciona un recurso de versión, el servicio WIA proporciona el valor &quot; 0.0.0.0 &quot; como valor predeterminado. Una aplicación Lee esta propiedad para determinar la versión de la DLL del minicontrolador de WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
