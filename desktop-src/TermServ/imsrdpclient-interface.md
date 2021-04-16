---
title: Interfaz IMsRdpClient
description: Proporciona los métodos y las propiedades necesarias para configurar y usar el control de cliente. Deriva de la interfaz IMsTscAx.
ms.assetid: 6698c1d7-94d2-453c-96db-366113b95dd4
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClient
- Servicios de Escritorio remoto de la interfaz IMsRdpClient, descrito
topic_type:
- apiref
api_name:
- IMsRdpClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc6d3a1de6a6cd18004ff957ea0f8c4d7c23b14d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676563"
---
# <a name="imsrdpclient-interface"></a>Interfaz IMsRdpClient

Proporciona los métodos y las propiedades necesarias para configurar y usar el control de cliente. Deriva de la interfaz [**IMsTscAx**](imstscax-interface.md) .

## <a name="members"></a>Miembros

La interfaz **IMsRdpClient** hereda de [**IMsTscAx**](imstscax-interface.md). **IMsRdpClient** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La interfaz **IMsRdpClient** tiene estos métodos.



| Método                                                                    | Descripción                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md) | Recupera las opciones establecidas para un canal virtual.<br/>         |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | Solicita un cierre estable del control de cliente.<br/>      |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md) | Establece las opciones de canal virtual para el control de cliente.<br/> |



 

### <a name="properties"></a>Propiedades

La interfaz **IMsRdpClient** tiene estas propiedades.



| Propiedad                                                                             | Tipo de acceso           | Descripción                                                                                                                                                               |
|:-------------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Solo lectura<br/>  | Puntero a la interfaz [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) , que se usa para establecer la configuración avanzada del control de cliente.<br/> |
| [**ColorDepth**](imsrdpclient-colordepth.md)<br/>                             | Lectura/escritura<br/> | Profundidad de color del control actual.<br/>                                                                                                                            |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Solo lectura<br/>  | Información ampliada sobre el motivo del control de cliente para la desconexión.<br/>                                                                                      |
| [**FullScreen**](imsrdpclient-fullscreen.md)<br/>                             | Lectura/escritura<br/> | Indica si el control está en modo de pantalla completa.<br/>                                                                                                          |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Solo lectura<br/>  | Puntero a la interfaz [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) , que se usa para establecer la configuración segura para el control de cliente.<br/>    |



 

## <a name="remarks"></a>Observaciones

La interfaz **IMsRdpClient** se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| CLSID<br/>                    | CLSID \_ MsRdpClient se define como 791fa017-2de3-492e-acc5-53c67a2b94d0<br/> CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID \_ MsRdpClient2 se define como 9059F30F-4EB1-4BD2-9FDC-36F43A218F4A<br/> CLSID \_ MsRdpClient2a se define como 971127BB-259F-48C2-BD75-5F97A3331551<br/> CLSID \_ MsRdpClient2NotSafeForScripting se define como 3523C2FB-4031-44E4-9A3B-F1E94986EE7F<br/> CLSID \_ MsRdpClient3 se define como 7584C670-2274-4EFB-B00B-D6AABA6D3850<br/> CLSID \_ MsRdpClient3a se define como 6A6F4B83-45C5-4CA9-BDD9-0D81C12295E4<br/> CLSID \_ MsRdpClient3NotSafeForScripting se define como ACE575FD-1FCF-4074-9401-EBAB990FA9DE<br/> CLSID \_ MsRdpClient4 se define como 4EDCB26C-D24C-4E72-AF07-B576699AC0DE<br/> CLSID \_ MsRdpClient4a se define como 54CE37E0-9834-41AE-9896-4DAB69DC022B<br/> CLSID \_ MsRdpClient4NotSafeForScripting se define como 6AE29350-321B-42BE-BBE5-12FB5270C0DE<br/> CLSID \_ MsRdpClient5 se define como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2<br/> CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31<br/> CLSID \_ MsRdpClient6 se define como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/> CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399<br/> CLSID \_ MsRdpClient7 se define como A9D7038D-B5ED-472E-9C47-94BEA90A5910<br/> CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258<br/> CLSID \_ MsRdpClient8 se define como 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> CLSID \_ MsRdpClientNotSafeForScripting se define como 7CACBD7B-0D99-468F-AC33-22E495C0AFE5<br/> CLSID \_ MsTscAx se define como 1FB464C8-09BB-4017-A2F5-EB742F04392F<br/> CLSID \_ MsTscAxNotSafeForScripting se define como A41A4187-5A86-4E26-B40A-856F9035D9CB<br/> |
| IID<br/>                      | IID \_ IMsRdpClient se define como 92b4a539-7115-4b7c-a5a9-e5d9efc2780a<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAx**](imstscax-interface.md)
</dt> <dt>

[Referencia de Conexión web a Escritorio remoto](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





