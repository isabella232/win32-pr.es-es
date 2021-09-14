---
title: Interfaz IMsRdpClient8
description: Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la interfaz IMsRdpClient7.
ms.assetid: 5ff54392-48f2-49a9-a264-88db08ec1770
ms.tgt_platform: multiple
keywords:
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto
- Interfaz IMsRdpClient8 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- IMsRdpClient8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6575e50bd85cfe96888f6c5924d1875b48d544ea
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968376"
---
# <a name="imsrdpclient8-interface"></a>Interfaz IMsRdpClient8

Proporciona los métodos y propiedades necesarios para configurar y usar el control de cliente. Deriva de la [**interfaz IMsRdpClient7.**](imsrdpclient7.md)

## <a name="members"></a>Members

La **interfaz IMsRdpClient8** hereda de [**IMsRdpClient7**](imsrdpclient7.md). **IMsRdpClient8** también tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **interfaz IMsRdpClient8** tiene estos métodos.



| Método                                                                    | Descripción                                                                                                                                                                                 |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                       | Inicia una conexión con las propiedades establecidas actualmente en el control .<br/>                                                                                                        |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)           | Crea un objeto de canal virtual del lado cliente para cada nombre de canal virtual especificado.<br/>                                                                                            |
| [**Desconectar**](imstscax-disconnect.md)                                 | Desconecta la conexión activa.<br/>                                                                                                                                               |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)          | Recupera la descripción del error para los eventos de desconexión de sesión.<br/>                                                                                                               |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                      | Recupera el texto de estado del código de estado especificado.<br/>                                                                                                                         |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md) | Recupera las opciones establecidas para un canal virtual.<br/>                                                                                                                                 |
| [**Volver a conectar**](imsrdpclient8-reconnect.md)                              | Se vuelve a conectar a la sesión remota con el nuevo ancho y alto del escritorio.<br/>                                                                                                          |
| [**RequestClose**](imsrdpclient-requestclose.md)                         | Solicita un cierre correcto del control de Escritorio remoto ActiveX.<br/>                                                                                                              |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)             | Envía datos al servidor host de sesión de Escritorio remoto a través de un canal virtual que se creó anteriormente mediante el [**método CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/> |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                | Hace que se realice una acción en la sesión remota.<br/>                                                                                                                          |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md) | Establece las opciones de canal virtual para el control Escritorio remoto ActiveX virtual.<br/>                                                                                                         |



 

### <a name="properties"></a>Propiedades

La **interfaz IMsRdpClient8** tiene estas propiedades.



| Propiedad                                                                             | Tipo de acceso           | Descripción                                                                                                                                                                                                                                            |
|:-------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AdvancedSettings**](imstscax-advancedsettings.md)<br/>                     | Solo lectura<br/>  | Recupera un puntero [**de interfaz IMsTscAdvancedSettings.**](imstscadvancedsettings-interface.md)<br/>                                                                                                                                          |
| [**AdvancedSettings2**](imsrdpclient-advancedsettings2.md)<br/>               | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings.**](imsrdpclientadvancedsettings-interface.md) La interfaz se puede usar para establecer la configuración avanzada del control de cliente.<br/>                                             |
| [**AdvancedSettings3**](imsrdpclient2-advancedsettings3.md)<br/>              | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings2.**](imsrdpclientadvancedsettings2.md) La interfaz se puede usar para establecer la configuración avanzada del control de cliente.<br/>                                                     |
| [**AdvancedSettings4**](imsrdpclient3-advancedsettings4.md)<br/>              | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientAdvancedSettings3.**](imsrdpclientadvancedsettings3.md)<br/>                                                                                                                                |
| [**AdvancedSettings5**](imsrdpclient4-advancedsettings5.md)<br/>              | Solo lectura<br/>  | Recupera un puntero a una [**interfaz IMsRdpClientAdvancedSettings4.**](imsrdpclientadvancedsettings4.md)<br/>                                                                                                                                 |
| [**AdvancedSettings6**](imsrdpclient5-advancedsettings6.md)<br/>              | Solo lectura<br/>  | Recupera la [**interfaz IMsRdpClientAdvancedSettings5.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                                                             |
| [**AdvancedSettings7**](imsrdpclient6-advancedsettings7.md)<br/>              | Solo lectura<br/>  | Recupera la [**interfaz IMsRdpClientAdvancedSettings6.**](imsrdpclientadvancedsettings5.md)<br/>                                                                                                                                             |
| [**AdvancedSettings8**](imsrdpclient7-advancedsettings8.md)<br/>              | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientAdvancedSettings7.**](imsrdpclientadvancedsettings7.md)<br/>                                                                                                                     |
| [**AdvancedSettings9**](imsrdpclient8-advancedsettings9.md)<br/>              | Solo lectura<br/>  | Contiene un objeto que admite la [**interfaz IMsRdpClientAdvancedSettings8.**](imsrdpclientadvancedsettings8.md)<br/>                                                                                                                      |
| [**CipherStrength**](imstscax-cipherstrength.md)<br/>                         | Solo lectura<br/>  | Recupera la intensidad de cifrado máxima del control actual.<br/>                                                                                                                                                                           |
| [**Colordepth**](imsrdpclient-colordepth.md)<br/>                             | Lectura y escritura<br/> | Profundidad de color (en bits por píxel) para la conexión del control.<br/>                                                                                                                                                                           |
| [**Conectado**](imstscax-connected.md)<br/>                                   | Solo lectura<br/>  | Recupera el estado de conexión del control actual.<br/>                                                                                                                                                                                      |
| [**ConnectedStatusText**](imsrdpclient2-connectedstatustext.md)<br/>          | Lectura y escritura<br/> | Contiene el texto que se muestra en el área de cliente del control mientras el control está en estado conectado.<br/>                                                                                                                          |
| [**ConnectingText**](imstscax-connectingtext.md)<br/>                         | Lectura y escritura<br/> | Especifica el texto que aparece centrado en el control mientras se conecta el control.<br/>                                                                                                                                                    |
| [**DesktopHeight**](imstscax-desktopheight.md)<br/>                           | Lectura y escritura<br/> | Especifica el alto del control actual, en píxeles, en el escritorio remoto inicial.<br/>                                                                                                                                                           |
| [**DesktopWidth**](imstscax-desktopwidth.md)<br/>                             | Lectura y escritura<br/> | Especifica el ancho del control actual, en píxeles, en el escritorio remoto inicial.<br/>                                                                                                                                                            |
| [**DisconnectedText**](imstscax-disconnectedtext.md)<br/>                     | Lectura y escritura<br/> | Especifica el texto que aparece centrado en el control antes de finalizar una conexión.<br/>                                                                                                                                                  |
| [**Dominio**](imstscax-domain.md)<br/>                                         | Lectura y escritura<br/> | Especifica el dominio en el que el usuario actual inicia sesión.<br/>                                                                                                                                                                                     |
| [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md)<br/> | Solo lectura<br/>  | Contiene información extendida sobre el motivo de desconexión del control.<br/>                                                                                                                                                                 |
| [**Fullscreen**](imsrdpclient-fullscreen.md)<br/>                             | Lectura y escritura<br/> | Determina si el control de cliente está en modo de pantalla completa.<br/>                                                                                                                                                                               |
| [**FullScreenTitle**](imstscax-fullscreentitle.md)<br/>                       | Solo escritura<br/> | Especifica el título de la ventana que se muestra cuando el control está en modo de pantalla completa.<br/>                                                                                                                                                               |
| [**HorizontalScrollBarVisible**](imstscax-horizontalscrollbarvisible.md)<br/> | Solo lectura<br/>  | Indica si el control ha mostrado una barra de desplazamiento horizontal.<br/>                                                                                                                                                                        |
| [**MsRdpClientShell**](imsrdpclient5-msrdpclientshell.md)<br/>                | Solo lectura<br/>  | Recupera la interfaz de configuración de cliente que admite scripts [**IMsRdpClientShell**](imsrdpclientshell.md).<br/>                                                                                                                                           |
| [**RemoteProgram**](imsrdpclient5-remoteprogram.md)<br/>                      | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz ITSRemoteProgram.**](itsremoteprogram.md)<br/>                                                                                                                                               |
| [**RemoteProgram2**](imsrdpclient7-remoteprogram2.md)<br/>                    | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz ITSRemoteProgram2.**](itsremoteprogram2.md)<br/>                                                                                                                                             |
| [**SecuredSettings**](imstscax-securedsettings.md)<br/>                       | Solo lectura<br/>  | Recupera un puntero [**de interfaz IMsTscSecuredSettings.**](imstscsecuredsettings-interface.md)<br/>                                                                                                                                            |
| [**SecuredSettings2**](imsrdpclient-securedsettings2.md)<br/>                 | Solo lectura<br/>  | Recupera un puntero a la [**interfaz IMsRdpClientSecuredSettings.**](imsrdpclientsecuredsettings-interface.md) Esta interfaz se puede usar para establecer la configuración segura para el control de cliente.<br/>                                               |
| [**SecuredSettings3**](imsrdpclient7-securedsettings3.md)<br/>                | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientSecuredSettings2.**](imsrdpclientsecuredsettings2.md)<br/>                                                                                                                       |
| [**SecuredSettingsEnabled**](imstscax-securedsettingsenabled.md)<br/>         | Solo lectura<br/>  | Indica si la [**interfaz IMsTscSecuredSettings**](imstscsecuredsettings-interface.md) está disponible. Es decir, si la página web que contiene el control se encuentra actualmente en una de las zonas de seguridad Internet Explorer URL permitidas.<br/> |
| [**Servidor**](imstscax-server.md)<br/>                                         | Lectura y escritura<br/> | Especifica el nombre del servidor al que está conectado el control actual.<br/>                                                                                                                                                                 |
| [**StartConnected**](imstscax-startconnected.md)<br/>                         | Lectura y escritura<br/> | Indica si el control establecerá la conexión del servidor host de sesión de Escritorio remoto inmediatamente después del inicio.<br/>                                                                                                                                |
| [**TransportSettings**](imsrdpclient5-transportsettings.md)<br/>              | Solo lectura<br/>  | Recupera lo que se pasó a través de un script a la [**interfaz IMsRdpClientTransportSettings.**](imsrdpclienttransportsettings.md)<br/>                                                                                                         |
| [**TransportSettings2**](imsrdpclient6-transportsettings2.md)<br/>            | Solo lectura<br/>  | Recupera la [**interfaz IMsRdpClientTransportSettings2.**](imsrdpclienttransportsettings2.md)<br/>                                                                                                                                           |
| [**TransportSettings3**](imsrdpclient7-transportsettings3.md)<br/>            | Solo lectura<br/>  | Recupera un objeto que admite la [**interfaz IMsRdpClientTransportSettings3.**](imsrdpclienttransportsettings3.md)<br/>                                                                                                                   |
| [**Nombre de usuario**](imstscax-username.md)<br/>                                     | Lectura y escritura<br/> | Especifica la credencial de inicio de sesión de nombre de usuario.<br/>                                                                                                                                                                                                   |
| [**Versión**](imstscax-version.md)<br/>                                       | Solo lectura<br/>  | Especifica el número de versión del control actual.<br/>                                                                                                                                                                                        |
| [**VerticalScrollBarVisible**](imstscax-verticalscrollbarvisible.md)<br/>     | Solo lectura<br/>  | Indica si el control muestra una barra de desplazamiento vertical.<br/>                                                                                                                                                                               |



 

## <a name="remarks"></a>Observaciones

Las interfaces siguientes han ampliado la interfaz **IMsRdpClient8,** donde cada nueva interfaz hereda todos los métodos y propiedades de las interfaces anteriores:

-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient10**](imsrdpclient10.md)

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/> CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D<br/> CLSID MsRdpClient8 se define como \_ 5F681803-2900-4C43-A1CC-CF405404A676<br/> CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5<br/> CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> |
| IID<br/>                      | IID \_ IMsRdpClient8 se define como 4247E044-9271-43A9-BC49-E2AD9E855D62<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

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

 

 





