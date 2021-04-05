---
title: Interfaz IMsRdpClientNonScriptable3
description: Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz IMsRdpClientNonScriptable2.
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c456393ee00c06bcd16135a7fbc73b0f1686259f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996597"
---
# <a name="imsrdpclientnonscriptable3-interface"></a>Interfaz IMsRdpClientNonScriptable3

Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) . Solo se puede tener acceso a los métodos de esta interfaz a través de vtable; no están disponibles para los clientes con scripts.

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientNonScriptable3** hereda de [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md). **IMsRdpClientNonScriptable3** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientNonScriptable3** tiene estas propiedades.



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
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Cadena de texto que se va a mostrar para la barra de conexión.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>Recopilación</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La colección de dispositivos PnP que están disponibles para la redirección.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La colección de unidades de disco que está disponible para la redirección.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si CredSSP está habilitado para esta conexión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si la configuración NegotiateSecurityLayer es compatible con esta conexión.<br/>
<blockquote>
[!Note]<br />
Cuando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> está habilitado y presente en el cliente, o cuando capa de sockets seguros (SSL) está habilitado con la autenticación de usuario, NegotiateSecurityLayer se omite.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si se debe mostrar el cuadro de diálogo solicitar credenciales.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si los dispositivos PnP conectados dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si las unidades PnP conectadas dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si se debe mostrar el cuadro de diálogo Advertencia de seguridad de redirección antes de iniciar una sesión.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre la redirección del portapapeles antes de iniciar una sesión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si la advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient5 se define como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 se define como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 se define como A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 se define como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





