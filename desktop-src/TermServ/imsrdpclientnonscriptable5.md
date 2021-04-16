---
title: Interfaz IMsRdpClientNonScriptable5
description: Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz IMsRdpClientNonScriptable4.
ms.assetid: 41b8c624-0451-4a7e-bc80-d0bf269e33c6
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0ec338dbe07c4733bf80207298f23f388bf8f77c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104493175"
---
# <a name="imsrdpclientnonscriptable5-interface"></a>Interfaz IMsRdpClientNonScriptable5

Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md) . Solo se puede tener acceso a los métodos de esta interfaz a través de vtable; no están disponibles para los clientes con scripts.

Una instancia de esta interfaz se obtiene llamando a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el objeto [**IMsTscAx**](imstscax-interface.md) y pasando **IID \_ IMsRdpClientNonScriptable5**.

## <a name="members"></a>Miembros

La interfaz **IMsRdpClientNonScriptable5** hereda de [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md). **IMsRdpClientNonScriptable5** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClientNonScriptable5** tiene estas propiedades.



| Propiedad                                                                                                         | Tipo de acceso           | Descripción                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**AllowPromptingForCredentials**](imsrdpclientnonscriptable5-allowpromptingforcredentials.md)<br/>       | Lectura/escritura<br/> | Especifica si el control ActiveX Escritorio remoto puede solicitar las credenciales al usuario.<br/>                    |
| [**DisableConnectionBar**](imsrdpclientnonscriptable5-disableconnectionbar.md)<br/>                       | Solo escritura<br/> | Especifica si el control ActiveX Escritorio remoto debe deshabilitar la barra de conexión.<br/>                      |
| [**DisableRemoteAppCapsCheck**](imsrdpclientnonscriptable5-disableremoteappcapscheck.md)<br/>             | Lectura/escritura<br/> | Especifica si el control ActiveX Escritorio remoto no debe comprobar las capacidades de RemoteApp en el servidor.<br/> |
| [**GetRemoteMonitorsBoundingBox**](imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md)<br/>       | Solo lectura<br/>  | Especifica el rectángulo delimitador del monitor remoto.<br/>                                                      |
| [**RemoteMonitorCount**](imsrdpclientnonscriptable5-remotemonitorcount.md)<br/>                           | Solo lectura<br/>  | Especifica el número de monitores remotos.<br/>                                                                     |
| [**RemoteMonitorLayoutMatchesLocal**](imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md)<br/> | Solo lectura<br/>  | Especifica si el diseño del monitor remoto es idéntico al diseño del monitor local.<br/>                             |
| [**UseMultimon**](imsrdpclientnonscriptable5-usemultimon.md)<br/>                                         | Lectura/escritura<br/> | Especifica si el control ActiveX Escritorio remoto debe usar varios monitores.<br/>                           |
| [**WarnAboutDirectXRedirection**](imsrdpclientnonscriptable5-warnaboutdirectxredirection.md)<br/>         | Lectura/escritura<br/> | No se usa esta propiedad.<br/>                                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 se define como A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 se define como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412C-b0ff-063718566907<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

