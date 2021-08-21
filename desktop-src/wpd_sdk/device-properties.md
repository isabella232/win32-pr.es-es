---
description: Windows Dispositivos portátiles admite las siguientes propiedades de dispositivo.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Propiedades del dispositivo (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 5490323e60d353fade6dfb7f517533ecb5fa26ca9e78ae221b9ff584d8c13a52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431009"
---
# <a name="device-properties-portabledeviceh"></a>Propiedades del dispositivo (PortableDevice.h)

Windows Dispositivos portátiles admite las siguientes propiedades de dispositivo.



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
<td><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></td>
<td><strong>VT_DATE</strong></td>
<td>Fecha y hora actuales del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Versión de firmware del dispositivo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Identificador único de 16 bytes que es común en varios transportes compatibles con el dispositivo. Si un único dispositivo admite varios transportes, esta propiedad se puede usar para asociar los distintos controladores WPD de transporte a ese dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Un nombre de fabricante de dispositivos legible.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>El modelo del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></td>
<td><strong>VT_VECTOR | VT_UI1</strong></td>
<td>Identificador único de 16 bytes que se usa para diferenciar entre diferentes modelos de un dispositivo.</td>
</tr>
<tr class="odd">
<td><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></td>
<td><strong>VT_UI8</strong></td>
<td>Valor que especifica el identificador de red EUI-64 del dispositivo; esta propiedad se usa para operaciones de red fuera de banda. Si el dispositivo tiene direcciones de red físicas MAC-48 (típicas de las redes IPv4), la dirección MAC-48 se codifica en la dirección EUI-64 como las dos mitades de la dirección MAC-48 separadas por FF-FF. El valor EUI-64 se almacena en orden de red o big-endian, donde una dirección &quot; &quot; &quot; &quot; EUI-64 de 01-02-03-FF-FF-04-05-06 se colocaría en el VT_UI8 de forma que el valor decimal sea 72624942021346566. Esta propiedad es necesaria en cualquier dispositivo que admita la autenticación nominal o segura. Esta propiedad se recomienda en dispositivos que solo admiten la autenticación cero. El host puede usar el valor para establecer automáticamente el acceso al dispositivo sin intervención del usuario.<br/></td>
</tr>
<tr class="even">
<td><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valor de 0 a 100 que especifica el nivel de energía de la batería del dispositivo, siendo 0 ninguno y 100 totalmente cargado.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></td>
<td>VT_UI4</td>
<td>Una <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeración que especifica la fuente de alimentación del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Protocolo de dispositivo que se está utilizando.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>El número de serie del dispositivo.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></td>
<td><strong>VT_UNKNOWN</strong></td>
<td>Valor que especifica si los formatos admitidos devueltos desde el dispositivo están en el orden preferido. El dispositivo prefiere el primer formato de la lista, mientras que el último es el menos preferido. Las aplicaciones pueden usar esta propiedad para determinar si los formatos admitidos de un dispositivo se muestran en el orden preferido.<br/></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valor booleano que especifica si los formatos admitidos devueltos desde el dispositivo están en el orden preferido; Es decir, el primer formato devuelto es el más preferido, mientras que el último formato devuelto es el menos preferido.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valor booleano que especifica si el dispositivo admite objetos no consumibles. Se trata de objetos que el dispositivo solo está diseñado para almacenar, no reproducir ni usar de ninguna manera.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Descripción legible del asociado de sincronización <em>de un dispositivo.</em> Se trata de un dispositivo, aplicación o servidor con el que el dispositivo se comunica para mantener un estado o un grupo de archivos comunes entre ambos asociados. Algunos ejemplos son los programas de correo electrónico y las bibliotecas de música.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valor que representa el nombre descriptivo establecido por el usuario en el dispositivo.</td>
</tr>
<tr class="odd">
<td><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></td>
<td><strong>VT_UI4</strong></td>
<td>el transporte admitido por el dispositivo, como USB, IP o Bluetooth. Los valores válidos son del tipo <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeración.</td>
</tr>
<tr class="even">
<td><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valor que especifica el tipo de dispositivo; las aplicaciones usan esta propiedad solo con fines de representación. Las características funcionales del dispositivo se deciden a través de objetos funcionales. Los dispositivos que no proporcionen un <strong></strong> icono de dispositivo, por ejemplo, un WPD_RESOURCE_ICON para el objeto de dispositivo, se representarán en el espacio de nombres de WPD con un icono genérico. Este icono dependerá del tipo de dispositivo especificado; por ejemplo, si el tipo de dispositivo es un teléfono móvil, se usa el icono de teléfono genérico. En la primera instalación del dispositivo, el Instalador de clase WPD consultará este valor de propiedad y lo almacenará en el registro de dispositivos en el valor PORTABLE_DEVICE_TYPE como REG_DWORD.<br/> Los valores posibles de este parámetro son de la <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeración definida en PortableDevice.h. Los valores son:<br/> <dl> <strong>WPD_DEVICE_TYPE_GENERIC</strong><br />
<strong>WPD_DEVICE_TYPE_CAMERA</strong><br />
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong><br />
<strong>WPD_DEVICE_TYPE_PHONE</strong><br />
<strong>WPD_DEVICE_TYPE_VIDEO</strong><br />
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong><br />
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Si esta propiedad existe y se establece en <strong>TRUE,</strong>el dispositivo se puede usar con la fase de dispositivo . Está pensado para dispositivos que no pueden almacenar metadatos mediante el Metadata Service <strong>dispositivo,</strong>pero que proporcionarán metadatos en los servidores de Microsoft.</td>
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

 

 




