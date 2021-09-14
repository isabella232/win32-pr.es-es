---
title: Interfaz IMsRdpClientNonScriptable4
description: Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la interfaz IMsRdpClientNonScriptable3.
ms.assetid: 570a5722-94b9-4195-846a-10233d56002d
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto
- Interfaz IMsRdpClientNonScriptable4 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aedea56733a2a98db4b966bd91d9337e38e61d0d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071032"
---
# <a name="imsrdpclientnonscriptable4-interface"></a>Interfaz IMsRdpClientNonScriptable4

Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la [**interfaz IMsRdpClientNonScriptable3.**](imsrdpclientnonscriptable3.md) Solo se puede acceder a los métodos de esta interfaz a través de vtable; no están disponibles para su uso en clientes que pueden incluir scripts.

## <a name="members"></a>Members

La **interfaz IMsRdpClientNonScriptable4** hereda de [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md). **IMsRdpClientNonScriptable4** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientNonScriptable4** tiene estas propiedades.



| Propiedad.                                                                                                         | Tipo de acceso           | Descripción                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AllowCredentialSaving**](imsrdpclientnonscriptable4-allowcredentialsaving.md)<br/>                     | Lectura y escritura<br/> | Especifica si el cuadro de diálogo credenciales muestra una casilla para habilitar el guardado de credenciales.<br/>                                                                                        |
| [**LaunchedViaClientShellInterface**](imsrdpclientnonscriptable4-launchedviaclientshellinterface.md)<br/> | Lectura y escritura<br/> | Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto.<br/>                                                                                                  |
| [**MarkRdpSettingsSecure**](imsrdpclientnonscriptable4-markrdpsettingssecure.md)<br/>                     | Lectura y escritura<br/> | Especifica si la configuración de RDP se marca como segura.<br/>                                                                                                                                          |
| [**PromptForCredsOnClient**](imsrdpclientnonscriptable4-promptforcredsonclient.md)<br/>                   | Lectura y escritura<br/> | Especifica si el control de cliente muestra un cuadro de diálogo que solicita credenciales.<br/>                                                                                                      |
| [**PublisherCertificateChain**](imsrdpclientnonscriptable4-publishercertificatechain.md)<br/>             | Lectura y escritura<br/> | Especifica la cadena de certificados del publicador. La cadena se almacena en una variante de tipo VT \_ BYREF que contiene un puntero a una [**estructura CERT CHAIN \_ \_ CONTEXT.**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)<br/> |
| [**RedirectionWarningType**](imsrdpclientnonscriptable4-redirectionwarningtype.md)<br/>                   | Lectura y escritura<br/> | Controla la presencia y la apariencia del cuadro de diálogo de redirección.<br/>                                                                                                                           |
| [**TrustedZoneSite**](imsrdpclientnonscriptable4-trustedzonesite.md)<br/>                                 | Lectura y escritura<br/> | Especifica si el sitio web desde el que el usuario inició la conexión está en la lista de sitios de confianza del equipo cliente.<br/>                                                                |
| [**WarnAboutPrinterRedirection**](imsrdpclientnonscriptable4-warnaboutprinterredirection.md)<br/>         | Lectura y escritura<br/> | Especifica si el cuadro de diálogo de redireccionamiento muestra un mensaje sobre el redireccionamiento de impresoras antes de iniciar una sesión.<br/>                                                                          |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID MsRdpClient7 se define como \_ A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> <dt>

[**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
</dt> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

