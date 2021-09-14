---
title: Clase MsRdpClient6
description: 'Control de cliente RDP de Microsoft (redistribuible): versión 7.'
ms.assetid: 1E8F5EBE-AF25-481D-8F41-13AAAF9B4A34
ms.tgt_platform: multiple
keywords:
- Clase MsRdpClient6 Servicios de Escritorio remoto
- Clase MsRdpClient6 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- MsRdpClient6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db831abf9e421601230b8f459799f7ac574417ee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968055"
---
# <a name="msrdpclient6-class"></a>Clase MsRdpClient6

Control de cliente RDP de Microsoft (redistribuible): versión 7

Esta clase implementa las interfaces siguientes.

-   [**IMsRdpClient6**](imsrdpclient6.md)
-   [**IMsRdpClient5**](imsrdpclient5.md)
-   [**IMsRdpClient4**](imsrdpclient4.md)
-   [**IMsRdpClient3**](imsrdpclient3.md)
-   [**IMsRdpClient2**](imsrdpclient2.md)
-   [**IMsRdpClient**](imsrdpclientshell2.md)
-   [**IMsTscAx**](imstscax-interface.md)
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)
-   [**IMsTscAxEvents**](imstscaxevents-interface.md)
-   [**IMsTscNonScriptable**](imstscnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable**](imsrdpclientnonscriptable-interface.md)
-   [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)
-   [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
-   [**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)

**MsRdpClient6** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MsRdpClient6** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Conectar**](imstscax-connect.md)                                                         | Inicia una conexión con las propiedades establecidas actualmente en el control .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un objeto de canal virtual del lado cliente para cada nombre de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta la conexión activa.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Recupera los códigos de error y los mensajes de error.<br/>                                                                                                                                                                                                                                      |
| [**GetVirtualChannelOptions**](imsrdpclient-getvirtualchanneloptions.md)                   | Recupera las opciones establecidas para un canal virtual.<br/>                                                                                                                                                                                                                                   |
| [**NotifyRedirectDeviceChange**](imsrdpclientnonscriptable-notifyredirectdevicechange.md)  | Notifica al módulo de redirección de dispositivos Escritorio remoto ActiveX control que se ha producido un cambio de dispositivo en el sistema. Este método pasa [**notificaciones DE WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) al control .<br/>                                                        |
| [**OnAuthenticationWarningDismissed**](imstscaxevents-onauthenticationwarningdismissed.md) | Se llama después de ActiveX control muestra un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo de error de certificado).<br/>                                                                                                                                                             |
| [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) | Se llama antes de ActiveX control muestra un cuadro de diálogo de autenticación (por ejemplo, el cuadro de diálogo de error de certificado).<br/>                                                                                                                                                            |
| [**OnAutoReconnected**](imstscaxevents-onautoreconnected.md)                               | Se llama cuando el control de cliente se ha vuelto a conectar automáticamente a una sesión remota.<br/>                                                                                                                                                                                                  |
| [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md)                           | Se llama cuando un cliente está en proceso de volver a conectar automáticamente una sesión con un servidor host de sesión de Escritorio remoto.<br/>                                                                                                                                                                      |
| [**OnAutoReconnecting2**](imstscaxevents-onautoreconnecting2.md)                           | Se llama cuando un cliente está en proceso de volver a conectar automáticamente una sesión con un servidor host de sesión de Escritorio remoto.<br/>                                                                                                                                                                      |
| [**OnChannelReceivedData**](imstscaxevents-onchannelreceiveddata.md)                       | Se llama cuando el cliente recibe datos en un canal virtual que puede incluir scripts.<br/>                                                                                                                                                                                                              |
| [**OnConfirmClose**](imstscaxevents-onconfirmclose.md)                                     | Se llama cuando el cliente llama [**al método IMsRdpClient::RequestClose.**](imsrdpclient-requestclose.md)<br/>                                                                                                                                                                           |
| [**OnConnected**](imstscaxevents-onconnected.md)                                           | Se llama cuando el control de cliente está en proceso de establecer una conexión con un servidor host de sesión de Escritorio remoto.<br/>                                                                                                                                                                       |
| [**OnConnecting**](imstscaxevents-onconnecting.md)                                         | Se llama cuando el control de cliente comienza a conectarse a un servidor en respuesta a una llamada a [**IMsTscAx::Conectar**](imstscax-connect.md).<br/>                                                                                                                                               |
| [**OnConnectionBarPullDown**](imstscaxevents-onconnectionbarpulldown.md)                   | Se llama cuando el usuario se ha arrastrado hacia abajo en la barra de conexión.<br/>                                                                                                                                                                                                                       |
| [**OnDevicesButtonPressed**](imstscaxevents-ondevicesbuttonpressed.md)                     | Se llama cuando se presiona el botón dispositivos de la barra de conexión.<br/>                                                                                                                                                                                                             |
| [**OnDisconnected**](imstscaxevents-ondisconnected.md)                                     | Se llama cuando el control de cliente se ha desconectado del servidor host de sesión de Escritorio remoto.<br/>                                                                                                                                                                                              |
| [**OnEnterFullScreenMode**](imstscaxevents-onenterfullscreenmode.md)                       | Se llama cuando el cliente entra en modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado de modo [de pantalla](terminal-services-shortcut-keys.md) completa (CTRL+ALT+BREAK).<br/>                                                                     |
| [**OnFatalError**](imstscaxevents-onfatalerror.md)                                         | Se llama cuando el control de cliente encuentra un error grave.<br/>                                                                                                                                                                                                                           |
| [**OnFocusReleased**](imstscaxevents-onfocusreleased.md)                                   | Se llama cuando se presiona la combinación de teclas de enfoque de liberación. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas CTRL+ALT+FLECHA IZQUIERDA o CTRL+ALT+FLECHA DERECHA.<br/>                                                                                             |
| [**OnIdleTimeoutNotification**](imstscaxevents-onidletimeoutnotification.md)               | Se llama cuando el usuario no ha realizado ninguna entrada de mouse o teclado durante el período de tiempo establecido por el método [**IMsRdpClientAdvancedSettings::p ut \_ MinutesToIdleTimeout.**](imsrdpclientadvancedsettings-minutestoidletimeout.md)<br/>                                                |
| [**OnLeaveFullScreenMode**](imstscaxevents-onleavefullscreenmode.md)                       | Se llama cuando el cliente sale del modo de pantalla completa. Por ejemplo, se llama a este evento cuando el usuario presiona la combinación de teclas de método abreviado de modo [de pantalla](terminal-services-shortcut-keys.md) completa (CTRL+ALT+BREAK).<br/>                                                                     |
| [**OnLoginComplete**](imstscaxevents-onlogincomplete.md)                                   | Se llama cuando el control de cliente ha iniciado sesión correctamente en un servidor host de sesión de Escritorio remoto, siguiendo la presentación del cuadro de diálogo Windows inicio de sesión.<br/>                                                                                                                                      |
| [**OnLogonError**](imstscaxevents-onlogonerror.md)                                         | Se llama cuando se produce un error de inicio de sesión u otro evento de inicio de sesión.<br/>                                                                                                                                                                                                                             |
| [**OnMouseInputModeChanged**](imstscaxevents-onmouseinputmodechanged.md)                   | Se llama cuando cambia el modo de entrada del mouse.<br/>                                                                                                                                                                                                                                      |
| [**OnNetworkStatusChanged**](imstscaxevents-onnetworkstatuschanged.md)                     | Se llama cuando el estado de la red ha cambiado.<br/>                                                                                                                                                                                                                                        |
| [**OnReceivedTSPublicKey**](imstscaxevents-onreceivedtspublickey.md)                       | Se llama durante la secuencia de conexión cuando el cliente recupera la clave pública del servidor. Este evento solo se llama si la propiedad **NotifyTSPublicKey** es **VARIANT \_ TRUE.**<br/>                                                                                              |
| [**OnRemoteDesktopSizeChange**](imstscaxevents-onremotedesktopsizechange.md)               | Se llama para indicar que el tamaño del control de cliente en el Escritorio remoto ha cambiado en respuesta a una operación de control de cliente.<br/>                                                                                                                                                |
| [**OnRemoteProgramDisplayed**](imstscaxevents-onremoteprogramdisplayed.md)                 | Se llama cuando se muestra un programa RemoteApp.<br/>                                                                                                                                                                                                                                      |
| [**OnRemoteProgramResult**](imstscaxevents-onremoteprogramresult.md)                       | Se llama cuando un programa RemoteApp devuelve un resultado al control de cliente.<br/>                                                                                                                                                                                                            |
| [**OnRemoteWindowDisplayed**](imstscaxevents-onremotewindowdisplayed.md)                   | Se llama cuando se muestra una ventana remoteapp.<br/>                                                                                                                                                                                                                                       |
| [**OnRequestContainerMinimize**](imstscaxevents-onrequestcontainerminimize.md)             | Se llama cuando el usuario presiona el botón **Minimizar** en la barra de conexión en modo de pantalla completa. La activación de este evento es una solicitud que la aplicación contenedora minimiza.<br/>                                                                                              |
| [**OnRequestGoFullScreen**](imstscaxevents-onrequestgofullscreen.md)                       | Se llama cuando el cliente solicita cambiar al modo de pantalla completa y se llama al método [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) para establecer la propiedad **ContainerHandledFullScreen** en un valor distinto de cero.<br/> |
| [**OnRequestLeaveFullScreen**](imstscaxevents-onrequestleavefullscreen.md)                 | Se llama cuando el cliente solicita salir del modo de pantalla completa y la propiedad [**IMsTscAdvancedSettings::p ut \_ ContainerHandledFullScreen**](imstscadvancedsettings-containerhandledfullscreen.md) se ha establecido en un valor distinto de cero.<br/>                                                   |
| [**OnServiceMessageReceived**](imstscaxevents-onservicemessagereceived.md)                 | Se llama cuando el cliente recibe un mensaje del sistema.<br/>                                                                                                                                                                                                                                  |
| [**OnUserNameAcquired**](imstscaxevents-onusernameacquired.md)                             | Se llama cuando el control ha adquirido el nombre de usuario.<br/>                                                                                                                                                                                                                        |
| [**OnWarning**](imstscaxevents-onwarning.md)                                               | Se llama cuando el control de cliente encuentra una condición de error que no es grave.<br/>                                                                                                                                                                                                    |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita un cierre correcto del control de cliente.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Restablece todos los estados de contraseña del control .<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envía una serie de pulsaciones de tecla al control. Las pulsaciones de tecla están en formato de código de examen, que son los datos del teclado de las teclas físicas reales.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envía datos al servidor host de sesión de Escritorio remoto a través de un canal virtual que se creó anteriormente mediante el método [**IMsTscAx::CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/>                                                                                         |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Establece las opciones de canal virtual para el control de cliente.<br/>                                                                                                                                                                                                                           |



 

### <a name="properties"></a>Propiedades

La **clase MsRdpClient6** tiene estas propiedades.




| Propiedad | Tipo de acceso | Descripción | 
|----------|-------------|-------------|
| <a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br /> | Solo lectura<br /> | Puntero <a href="imstscadvancedsettings-interface.md"><strong>de interfaz IMsTscAdvancedSettings.</strong></a><br /> | 
| <a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br /> | Solo lectura<br /> | Puntero a la <a href="imsrdpclientadvancedsettings-interface.md"><strong>interfaz IMsRdpClientAdvancedSettings,</strong></a> que se usa para establecer la configuración avanzada para el control de cliente.<br /> | 
| <a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br /> | Solo lectura<br /> | Puntero a la <a href="imsrdpclientadvancedsettings2.md"><strong>interfaz IMsRdpClientAdvancedSettings2,</strong></a> que se usa para establecer la configuración avanzada del control de cliente.<br /> | 
| <a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br /> | Solo lectura<br /> | Puntero a la <a href="imsrdpclientadvancedsettings3.md"><strong>interfaz IMsRdpClientAdvancedSettings3,</strong></a> que se usa para establecer la configuración avanzada para el control de cliente.<br /> | 
| <a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br /> | Solo lectura<br /> | Puntero <a href="imsrdpclientadvancedsettings4.md"><strong>de interfaz IMsRdpClientAdvancedSettings4.</strong></a><br /> | 
| <a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br /> | Solo lectura<br /> | Interfaz de <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br /> | 
| <a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br /> | Solo lectura<br /> | Interfaz de <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>.<br /> | 
| <a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br /> | Lectura y escritura<br /> | Especifica si el cuadro de diálogo credenciales muestra una casilla para habilitar el guardado de credenciales.<br /> | 
| <a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br /> | Lectura y escritura<br /> | Esta propiedad no es compatible.<br /> | 
| <a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br /> | Lectura y escritura<br /> | Esta propiedad no es compatible.<br /> | 
| <a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br /> | Solo lectura<br /> | La intensidad de cifrado máxima del control actual.<br /> | 
| <a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br /> | Solo escritura<br /> | La Escritorio remoto ActiveX de control, en formato de texto no cifrado.<br /> | 
| <a href="imsrdpclient-colordepth.md"><strong>Colordepth</strong></a><br /> | Lectura y escritura<br /> | Profundidad de color del control actual.<br /> | 
| <a href="imstscax-connected.md"><strong>Conectado</strong></a><br /> | Solo lectura<br /> | Estado de conexión del control actual.<br /> | 
| <a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br /> | Lectura y escritura<br /> | Texto que se muestra en el área de cliente del control mientras el control está en estado conectado.<br /> | 
| <a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br /> | Lectura y escritura<br /> | Texto que aparece centrado en el control mientras se conecta el control.<br /> | 
| <a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br /> | Lectura y escritura<br /> | Cadena de texto que se mostrará para la barra de conexión.<br /> | 
| <a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br /> | Lectura y escritura<br /> | Alto del control actual, en píxeles, en el escritorio remoto inicial.<br /> | 
| <a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br /> | Lectura y escritura<br /> | Ancho del control actual, en píxeles, en el escritorio remoto inicial.<br /> | 
| <a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br /> | Solo lectura<br /> | Colección de dispositivos PnP que están disponibles para el redireccionamiento.<br /> | 
| <a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br /> | Lectura y escritura<br /> | Texto que aparece centrado en el control antes de finalizar una conexión.<br /> | 
| <a href="imstscax-domain.md"><strong>Dominio</strong></a><br /> | Lectura y escritura<br /> | Dominio en el que el usuario actual inicia sesión.<br /> | 
| <a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br /> | Solo lectura<br /> | Colección de unidades de disco que está disponible para el redireccionamiento.<br /> | 
| <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br /> | Lectura y escritura<br /> | Especifica si CredSSP está habilitado para esta conexión.<br /> | 
| <a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br /> | Solo lectura<br /> | Información extendida sobre el motivo de desconexión del control de cliente.<br /> | 
| <a href="imsrdpclient-fullscreen.md"><strong>Fullscreen</strong></a><br /> | Lectura y escritura<br /> | Indica si el control está en modo de pantalla completa.<br /> | 
| <a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br /> | Solo escritura<br /> | Título de la ventana que se muestra cuando el control está en modo de pantalla completa.<br /> | 
| <a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br /> | Solo lectura<br /> | Indica si el control ha mostrado una barra de desplazamiento horizontal.<br /> | 
| <a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br /> | Lectura y escritura<br /> | Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto.<br /> | 
| <a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br /> | Lectura y escritura<br /> | Especifica si la configuración de RDP se marca como segura.<br /> | 
| <a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br /> | Solo lectura<br /> | Configuración de cliente para el iniciador del portal web.<br /> | 
| <a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br /> | Lectura y escritura<br /> | Especifica si el valor NegotiateSecurityLayer es compatible con esta conexión.<br /><blockquote>[!Note]<br />Cuando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> está habilitado y presente en el cliente, o cuando Capa de sockets seguros (SSL) está habilitado con la autenticación de usuario, NegotiateSecurityLayer se omite.</blockquote><br /> | 
| <a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br /> | Lectura y escritura<br /> | Esta propiedad no es compatible.<br /> | 
| <a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br /> | Lectura y escritura<br /> | Esta propiedad no es compatible.<br /> | 
| <a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br /> | Lectura y escritura<br /> | Especifica si se debe mostrar el cuadro de diálogo solicitar credenciales.<br /> | 
| <a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br /> | Lectura y escritura<br /> | Especifica si el control de cliente muestra un cuadro de diálogo que solicita credenciales.<br /> | 
| <a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br /> | Lectura y escritura<br /> | Especifica la cadena de certificados del publicador. La cadena se almacena en una variante de tipo VT_BYREF que contiene un puntero a una <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> estructura.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br /> | Lectura y escritura<br /> | Especifica si los dispositivos PnP conectados dinámicamente que se enumeran mientras están en una sesión están disponibles para el redireccionamiento.<br /> | 
| <a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br /> | Lectura y escritura<br /> | Especifica si las unidades PnP conectadas dinámicamente que se enumeran mientras están en una sesión están disponibles para el redireccionamiento.<br /> | 
| <a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br /> | Lectura y escritura<br /> | Controla la presencia y la apariencia del cuadro de diálogo de redirección.<br /> | 
| <a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br /> | Solo lectura<br /> | La configuración de RemoteApp del cliente.<br /> | 
| <a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br /> | Solo lectura<br /> | Puntero <a href="imstscsecuredsettings-interface.md"><strong>de interfaz IMsTscSecuredSettings.</strong></a><br /> | 
| <a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br /> | Solo lectura<br /> | Puntero a la <a href="imsrdpclientsecuredsettings-interface.md"><strong>interfaz IMsRdpClientSecuredSettings,</strong></a> que se usa para establecer la configuración protegida para el control de cliente.<br /> | 
| <a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br /> | Solo lectura<br /> | Indica si la <a href="imstscsecuredsettings-interface.md"><strong>interfaz IMsTscSecuredSettings</strong></a> está disponible.<br /> | 
| <a href="imstscax-server.md"><strong>Servidor</strong></a><br /> | Lectura y escritura<br /> | Nombre del servidor al que está conectado el control actual.<br /> | 
| <a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br /> | Lectura y escritura<br /> | Especifica si se debe mostrar el cuadro de diálogo de advertencia de seguridad de redireccionamiento antes de iniciar una sesión.<br /> | 
| <a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br /> | Lectura y escritura<br /> | Indica si el control establecerá la conexión del servidor host de sesión de Escritorio remoto inmediatamente después del inicio.<br /> | 
| <a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br /> | Solo lectura<br /> | La configuración de puerta de enlace de Escritorio remoto del cliente.<br /> | 
| <a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br /> | Solo lectura<br /> | Interfaz de <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>.<br /> | 
| <a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br /> | Lectura y escritura<br /> | Especifica si el sitio web desde el que el usuario inició la conexión está en la lista de sitios de confianza del equipo cliente.<br /> | 
| <a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br /> | Lectura y escritura<br /> | Identificador de ventana que va a ser la ventana primaria del control. Esto permite que las ventanas mostradas por el control sean modales correctamente con respecto a las ventanas mostradas por la aplicación primaria.<br /> | 
| <a href="imstscax-username.md"><strong>Nombre de usuario</strong></a><br /> | Lectura y escritura<br /> | Credencial de inicio de sesión de nombre de usuario.<br /> | 
| <a href="imstscax-version.md"><strong>Versión</strong></a><br /> | Solo lectura<br /> | Número de versión del control actual.<br /> | 
| <a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br /> | Solo lectura<br /> | Indica si el control muestra una barra de desplazamiento vertical.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br /> | Lectura y escritura<br /> | Especifica si el cuadro de diálogo de advertencia de seguridad debe incluir una advertencia sobre el redireccionamiento del Portapapeles antes de iniciar una sesión.<br /> | 
| <a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br /> | Lectura y escritura<br /> | Especifica si el cuadro de diálogo de redireccionamiento muestra un mensaje sobre el redireccionamiento de impresoras antes de iniciar una sesión.<br /> | 
| <a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br /> | Lectura y escritura<br /> | Especifica si la advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.<br /> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID MsRdpClient6 se define como \_ 7390F3D8-0439-4C05-91E3-CF5CB290C3D0<br/>      |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Escritorio remoto ActiveX clases de control](remote-desktop-activex-control-classes.md)
</dt> </dl>

