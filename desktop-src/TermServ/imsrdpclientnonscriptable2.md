---
title: IMsRdpClientNonScriptable2 (interfaz)
description: Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la interfaz IMsRdpClientNonScriptable.
ms.assetid: 06a5ffc9-3c9e-44d6-a5b5-9ccb7488deff
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto
- Interfaz IMsRdpClientNonScriptable2 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 77df65d58ad2c3b479cac37a9ae543733d4c8c90bd4708c5e6e0273fcb142ae9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118352142"
---
# <a name="imsrdpclientnonscriptable2-interface"></a>IMsRdpClientNonScriptable2 (interfaz)

Proporciona acceso a las propiedades noscriptables de la sesión remota de un cliente en el control Escritorio remoto ActiveX cliente. Deriva de la [**interfaz IMsRdpClientNonScriptable.**](imsrdpclientnonscriptable-interface.md) Solo se puede acceder a los métodos de esta interfaz a través de la tabla virtual; no están disponibles para su uso en clientes que pueden incluir scripts.

## <a name="members"></a>Miembros

La **interfaz IMsRdpClientNonScriptable2** hereda de [**IMsRdpClientNonScriptable.**](imsrdpclientnonscriptable-interface.md) **IMsRdpClientNonScriptable2** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClientNonScriptable2** tiene estas propiedades.



| Propiedad                                                                                   | Tipo de acceso           | Descripción                                                                                                                                                                                                  |
|:-------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)<br/> | Lectura/escritura<br/> | Identificador de ventana que va a ser la ventana primaria del control. Esto permite que las ventanas mostradas por el control sean modales correctamente con respecto a las ventanas mostradas por la aplicación primaria.<br/> |



 

## <a name="remarks"></a>Comentarios

Esta interfaz se ha ampliado mediante las interfaces siguientes, donde cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008, Windows Server 2008 con SP1<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient4 se define como \_ 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a se define como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting se define como 6AE29350-321B-42BE- JAVASCRIPT5-12FB5270C0DE<br/> CLSID MsRdpClient5 se define como \_ 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID MsRdpClient7 se define como \_ A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable2 se define como 17A5E535-4072-4FA4-AF32-C8D0D47345E9<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





