---
title: Interfaz IMsRdpClientAdvancedSettings5
description: Administra la configuración avanzada del cliente. Deriva de la interfaz IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49ad2b26697cd3985cc0e39a8ed7345bc4bbe941
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2021
ms.locfileid: "122622351"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a>Interfaz IMsRdpClientAdvancedSettings5

Administra la configuración avanzada del cliente. Deriva de la [**interfaz IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)

Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md) A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings5** a **QueryInterface**.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientAdvancedSettings5** hereda de [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md). **IMsRdpClientAdvancedSettings5** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientAdvancedSettings5** tiene estas propiedades.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Propiedad</th>
<th >Tipo de acceso</th>
<th >Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Modo de redireccionamiento de audio. La <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>propiedad AudioRedirectionMode</strong></a> tiene los siguientes valores posibles.<br/>
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (la redirección de audio está habilitada y la opción para el redireccionamiento es &quot; Bring to this computer &quot; . Este es el modo predeterminado).<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (la redirección de audio está habilitada y la opción &quot; es Salir en el equipo &quot; remoto). La opción Salir en equipo remoto solo se admite cuando se conecta de forma remota a un equipo host que &quot; &quot; ejecuta Windows Vista. Si la conexión es a un equipo host que ejecuta Windows Server 2008, la opción Dejar en el equipo remoto cambia a &quot; &quot; No &quot; &quot; reproducir).<br/> </dt> <dd></dd> <dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (la redirección de audio está habilitada y el modo es &quot; No &quot; reproducir).<br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Especifica el tamaño del archivo de caché virtual para los mapas de bits de 32 bits por píxel (bpp). El valor máximo es 48 megabytes (MB).<br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Especifica si el botón anclar debe mostrarse en la barra de conexión. De forma predeterminada, el valor es <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Especifica si el modo público debe habilitarse o deshabilitarse. De forma predeterminada, el modo público se establece en <strong>FALSE.</strong><br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Especifica si el redireccionamiento del Portapapeles debe habilitarse o deshabilitarse. De forma predeterminada, el modo de redirección del Portapapeles está establecido <strong>en TRUE</strong> (habilitado).<br/></td>
</tr>
<tr class="even">
<td ><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Especifica si los dispositivos redirigidos deben estar habilitados o deshabilitados. De forma predeterminada, el modo de dispositivos redirigidos está establecido en <strong>FALSE.</strong><br/></td>
</tr>
<tr class="odd">
<td ><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a><br/></td>
<td >Lectura/escritura<br/></td>
<td >Especifica si los dispositivos redirigidos de punto de servicio deben estar habilitados o deshabilitados. De forma predeterminada, el modo de dispositivos redirigidos de punto de servicio está establecido en <strong>FALSE.</strong><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentarios

Esta interfaz se ha ampliado mediante las interfaces siguientes, y cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
-   [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
-   [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                         |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                   |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>           |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

