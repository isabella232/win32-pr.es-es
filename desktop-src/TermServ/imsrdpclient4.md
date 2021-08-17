---
title: Interfaz IMsRdpClient4
description: Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la interfaz IMsRdpClient3.
ms.assetid: c3382a86-f044-4924-b69b-5907f2506eb6
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto
- Interfaz IMsRdpClient4 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClient4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ac9660384e15827b3a1bc6949e448ff2f9ce99c3d034de02c86a3831cc219ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119475595"
---
# <a name="imsrdpclient4-interface"></a>Interfaz IMsRdpClient4

Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la [**interfaz IMsRdpClient3.**](imsrdpclient3.md)

## <a name="members"></a>Miembros

La **interfaz IMsRdpClient4** hereda de [**IMsRdpClient3.**](imsrdpclient3.md) **IMsRdpClient4** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClient4** tiene estas propiedades.



| Propiedad                                                                | Tipo de acceso          | Descripción                                                                                             |
|:------------------------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/> | Solo lectura<br/> | Puntero [**de interfaz IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/> |



 

## <a name="remarks"></a>Comentarios

La **interfaz IMsRdpClient4** se ha ampliado mediante las interfaces siguientes, y cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient4 se define como \_ 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a se define como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting se define como 6AE29350-321B-42BE-MID5-12FB5270C0DE<br/> CLSID MsRdpClient5 se define como \_ 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID MsRdpClient7 se define como \_ A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID IMsRdpClient4 se define como \_ 095E0738-D97D-488b-B9F6-DD0E8D66C0DE<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient3**](imsrdpclient3.md)
</dt> <dt>

[**IMsRdpClient2**](imsrdpclient2.md)
</dt> <dt>

[**IMsRdpClient**](imsrdpclient-interface.md)
</dt> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





