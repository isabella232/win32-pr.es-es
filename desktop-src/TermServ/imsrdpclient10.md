---
title: Interfaz IMsRdpClient10
description: Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la interfaz IMsRdpClient9.
ms.assetid: 601f70aa-85f1-4180-921b-9f1bb31d4def
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 561541f170fbe6dc5342b359e5deae69d0c92469ad2d692ee4ea3b9d59904885
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737245"
---
# <a name="imsrdpclient10-interface"></a>Interfaz IMsRdpClient10

Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la [**interfaz IMsRdpClient9.**](imsrdpclient9.md)

## <a name="members"></a>Miembros

La **interfaz IMsRdpClient10** hereda de [**IMsRdpClient9**](imsrdpclient9.md). **IMsRdpClient10** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpClient10** tiene estos métodos.



| Método                                                                             | Descripción                                                                         |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                   | Asocia un evento.<br/>                                                       |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                   | Desasocula un evento.<br/>                                                       |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                   | Recupera la descripción del error para los eventos de desconexión de sesión.<br/>       |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                               | Recupera el texto de estado del código de estado especificado.<br/>                 |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)          | Recupera las opciones establecidas para un canal virtual.<br/>                         |
| [**Volver a conectar**](imsrdpclient8-reconnect.md)                                       | Se vuelve a conectar a la sesión remota con el nuevo ancho y alto del escritorio.<br/>  |
| [**RequestClose**](imsrdpclient-requestclose.md)                                  | Solicita un cierre correcto del control Escritorio remoto ActiveX datos.<br/>      |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                         | Hace que se realice una acción en la sesión remota.<br/>                  |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)          | Establece las opciones de canal virtual para el control Escritorio remoto ActiveX virtual.<br/> |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)     | Sincroniza la configuración de visualización de la sesión.<br/>                                   |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85)) | Actualiza la configuración de visualización de la sesión.<br/>                                        |



 

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClient10** tiene estas propiedades.



| Propiedad                                                                             | Tipo de acceso           | Descripción                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) La interfaz se puede usar para establecer la configuración avanzada para el control de cliente.<br/> |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings2.**](imsrdpclientadvancedsettings2.md) La interfaz se puede usar para establecer la configuración avanzada para el control de cliente.<br/>         |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md)<br/>                                                                                    |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Solo lectura<br/>  | Recupera un puntero a una [**interfaz IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                     |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Solo lectura<br/>  | Recupera la [**interfaz IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                 |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Solo lectura<br/>  | Recupera la [**interfaz IMsRdpClientAdvancedSettings6.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                 |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientAdvancedSettings7.**](imsrdpclientadvancedsettings7.md)<br/>                                                                         |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Solo lectura<br/>  | Contiene un objeto que admite la [**interfaz IMsRdpClientAdvancedSettings8.**](imsrdpclientadvancedsettings8.md)<br/>                                                                          |
| [**Colordepth**](imsrdpclient-colordepth.md)<br/>                             | Lectura/escritura<br/> | Profundidad de color (en bits por píxel) de la conexión del control.<br/>                                                                                                                               |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lectura/escritura<br/> | Contiene el texto que se muestra en el área cliente del control mientras el control está en estado conectado.<br/>                                                                              |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Solo lectura<br/>  | Contiene información extendida sobre el motivo de desconexión del control.<br/>                                                                                                                     |
| [**Fullscreen**](imsrdpclient-fullscreen.md)<br/>                             | Lectura/escritura<br/> | Determina si el control de cliente está en modo de pantalla completa.<br/>                                                                                                                                   |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Solo lectura<br/>  | Recupera la interfaz de configuración de cliente que admite scripts [**IMsRdpClientShell**](imsrdpclientshell.md).<br/>                                                                                               |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz ITSRemoteProgram.**](itsremoteprogram.md)<br/>                                                                                                   |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz ITSRemoteProgram2.**](itsremoteprogram2.md)<br/>                                                                                                 |
| [**RemoteProgram3**](imsrdpclient10-remoteprogram3.md)<br/>                   | Solo lectura<br/>  | Objeto que admite la [**interfaz ITSRemoteProgram3.**](itsremoteprogram3.md)<br/>                                                                                                           |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md) Esta interfaz se puede usar para establecer la configuración segura para el control de cliente.<br/>   |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)<br/>                                                                           |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Solo lectura<br/>  | Recupera lo que se pasó a través de un script a la [**interfaz IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md)<br/>                                                             |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Solo lectura<br/>  | Recupera la [**interfaz IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/>                                                                                               |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientTransportSettings3.**](imsrdpclienttransportsettings3.md)<br/>                                                                       |
| [**TransportSettings4**](imsrdpclient9-transportsettings4.md)<br/>            | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientTransportSettings4.**](imsrdpclienttransportsettings4.md)<br/>                                                                       |



 

## <a name="remarks"></a>Comentarios

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                                                                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                                                                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                   |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> |
| IID<br/>                      | IID \_ IMsRdpClient10 se define como 7ED92C39-EB38-4927-A70A-708AC5A59321<br/>                                                                                                        |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> <dt>

[**IMsRdpClient8**](imsrdpclient8.md)
</dt> <dt>

[**IMsRdpClient7**](imsrdpclient7.md)
</dt> <dt>

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

[Conexión web a Escritorio remoto referencia](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

