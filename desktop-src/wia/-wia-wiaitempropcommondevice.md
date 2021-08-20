---
description: Además de las propiedades de información del dispositivo, Windows de adquisición de imágenes (WIA) tienen valores de propiedad almacenados en el registro que las aplicaciones leen y escriben.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Constantes comunes de propiedad de dispositivo (Wiadef.h)
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
ms.openlocfilehash: 7e647b969350173d751533c3f9d916e2fc1b0f82db399ad676801a3521899b61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117668978"
---
# <a name="common-device-property-constants"></a>Constantes comunes de propiedades de dispositivo

Además de las propiedades de información del dispositivo, Windows de adquisición de imágenes (WIA) tienen valores de propiedad almacenados en el registro que las aplicaciones leen y escriben. Están asociados al [**objeto IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o [**al objeto IWiaItem2.**](-wia-iwiaitem2.md) Las propiedades del dispositivo representan información del dispositivo, como el estado de conexión y la hora del dispositivo. Cada propiedad de dispositivo tiene una cadena de propiedad de dispositivo asociada.

Las constantes de propiedad de dispositivo enumeradas aquí son comunes a la mayoría o a todos los dispositivos de hardware WIA.

El prefijo "WIA DPA" indica una propiedad de dispositivo para todos los dispositivos y es la convención de nomenclatura usada \_ \_ en C/C++. Con fines de scripting, estas constantes usan el prefijo "Device" y forman parte del tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.



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
<td style="text-align: left;">El estado de conexión actual del dispositivo. El minidriver crea y mantiene esta propiedad.<br/> Tipo: <strong>VT_I4</strong>, Acceso: solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a><br/> La propiedad puede tener los siguientes valores posibles.<br/> 
<table>
<thead>
<tr class="header">
<th>Conectar Estado</th>
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
<td style="text-align: left;"><p>Hora del reloj actual que se almacena en el dispositivo. El minidriver crea y mantiene esta propiedad.</p>
<p>Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Acceso: Lectura/escritura o Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p>
<p>Esta propiedad solo es compatible con dispositivos que tienen un reloj interno. Si se puede establecer el reloj del dispositivo, esta propiedad es De lectura y escritura; de lo contrario, es de solo lectura.</p>
<p>Los dispositivos WIA informan de la hora <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">en una estructura SYSTEMTIME.</a></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </dl></td>
<td style="text-align: left;"><p>La versión de firmware del dispositivo. Este valor debe ser un valor de cadena, como &quot; 1.0.4 &quot; o &quot; 1.0abc &quot; . El minidriver crea y mantiene esta propiedad. Si el minidriver de WIA no proporciona un recurso de versión, el servicio WIA proporciona el valor &quot; 0.0.0.0 &quot; como valor predeterminado. Una aplicación lee esta propiedad para determinar la versión del archivo DLL de minidriver de WIA.</p>
<p>Tipo: <strong>VT_BSTR</strong>, Acceso: solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
