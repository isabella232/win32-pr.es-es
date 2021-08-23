---
title: Interfaz IMsRdpClient3
description: Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la interfaz IMsRdpClient2.
ms.assetid: 31e52de1-1fb0-47ef-aad5-fd06621f2b3c
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto
- Interfaz IMsRdpClient3 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClient3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 444f022c2f4db57c1c62f1405b30625bf7fed291674255ed6287026c9451e825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059013"
---
# <a name="imsrdpclient3-interface"></a>Interfaz IMsRdpClient3

Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la [**interfaz IMsRdpClient2.**](imsrdpclient2.md)

## <a name="members"></a>Miembros

La **interfaz IMsRdpClient3** hereda de [**IMsRdpClient2**](imsrdpclient2.md). **IMsRdpClient3** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClient3** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso          | Descripción                                                                                                                                                       |
|:------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/> | Solo lectura<br/> | Puntero a la [**interfaz IMsRdpClientAdvancedSettings3,**](imsrdpclientadvancedsettings3.md) que se usa para establecer la configuración avanzada para el control de cliente.<br/> |



 

## <a name="remarks"></a>Comentarios

Las interfaces siguientes han ampliado la interfaz **IMsRdpClient3,** y cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient3 se define como \_ 7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a se define como 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting se define como ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID MsRdpClient4 se define como \_ 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a se define como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting se define como 6AE29350-321B-42BE-MID5-12FB5270C0DE<br/> CLSID MsRdpClient5 se define como \_ 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID MsRdpClient7 se define como \_ A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient3 se define como 91b7cbc5-a72e-4fa0-9300-d647d7e897ff<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





