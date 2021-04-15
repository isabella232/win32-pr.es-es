---
title: Interfaz IMsRdpClient7
description: Proporciona los métodos y las propiedades necesarias para configurar y usar el control de cliente. Deriva de la interfaz IMsRdpClient6.
ms.assetid: f6bc5d50-f16a-44be-8244-5aec13c52066
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7
- Servicios de Escritorio remoto de la interfaz IMsRdpClient7, descrito
topic_type:
- apiref
api_name:
- IMsRdpClient7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e16375f9f1281f2cc34dac440373f95b828392f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105677013"
---
# <a name="imsrdpclient7-interface"></a>Interfaz IMsRdpClient7

Proporciona los métodos y las propiedades necesarias para configurar y usar el control de cliente. Deriva de la interfaz [**IMsRdpClient6**](imsrdpclient6.md) .

## <a name="members"></a>Miembros

La interfaz **IMsRdpClient7** hereda de [**IMsRdpClient6**](imsrdpclient6.md). **IMsRdpClient7** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpClient7** tiene estos métodos.



| Método                                               | Descripción                                                         |
|:-----------------------------------------------------|:--------------------------------------------------------------------|
| [**GetStatusText**](imsrdpclient7-getstatustext.md) | Recupera el texto de estado para el código de estado especificado.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClient7** tiene estas propiedades.



| Propiedad                                                                  | Tipo de acceso          | Descripción                                                                                                                |
|:--------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>   | Solo lectura<br/> | Objeto que admite la interfaz [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) .<br/>   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>         | Solo lectura<br/> | Objeto que admite la interfaz [**ITSRemoteProgram2**](itsremoteprogram2.md) .<br/>                           |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>     | Solo lectura<br/> | Objeto que admite la interfaz [**IMsRdpClientSecuredSettings2**](imsrdpclientsecuredsettings2.md) .<br/>     |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/> | Solo lectura<br/> | Objeto que admite la interfaz [**IMsRdpClientTransportSettings3**](imsrdpclienttransportsettings3.md) .<br/> |



 

## <a name="remarks"></a>Observaciones

La interfaz **IMsRdpClient7** se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient7 se define como A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 se define como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient7 se define como b2a5b5ce-3461-444A-91d4-add26d070638<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient6**](imsrdpclient6.md)
</dt> <dt>

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

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





