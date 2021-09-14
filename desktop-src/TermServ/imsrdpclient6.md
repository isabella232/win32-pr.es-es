---
title: Interfaz IMsRdpClient6
description: Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la interfaz IMsRdpClient5.
ms.assetid: 97ec885f-1c55-4293-84d0-2d1d804a9df8
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto
- Interfaz IMsRdpClient6 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClient6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ddb2b60d95650975955bc45abe23a354668c9bf
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968427"
---
# <a name="imsrdpclient6-interface"></a>Interfaz IMsRdpClient6

Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la [**interfaz IMsRdpClient5.**](imsrdpclient5.md)

## <a name="members"></a>Members

La **interfaz IMsRdpClient6** hereda de [**IMsRdpClient5.**](imsrdpclient5.md) **IMsRdpClient6** también tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClient6** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso          | Descripción                                                                                           |
|:--------------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>   | Solo lectura<br/> | Interfaz de [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md).<br/>   |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/> | Solo lectura<br/> | Interfaz de [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md).<br/> |



 

## <a name="remarks"></a>Observaciones

La **interfaz IMsRdpClient6** se ha ampliado mediante las siguientes interfaces, y cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista con SP1<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID MsRdpClient7 se define como \_ A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID IMsRdpClient6 se define como \_ d43b7d80-8517-4b6d-9eac-96ad6800d7f2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClient5**](imsrdpclient5.md)
</dt> <dt>

[**IMsRdpClient4**](imsrdpclient4.md)
</dt> <dt>

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

 

 





