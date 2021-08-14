---
title: Clase MsRdpClient10
description: 'Control de cliente RDP de Microsoft (redistribuible): versión 11.'
ms.assetid: 9D0F2312-0D85-402D-874D-9FA477435210
ms.tgt_platform: multiple
keywords:
- Clase MsRdpClient10 Servicios de Escritorio remoto
- Clase MsRdpClient10 Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- MsRdpClient10
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45c39ae5718227095ade406f13a0103e053cb09f2661d009964f6e7e2570583d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119989025"
---
# <a name="msrdpclient10-class"></a>Clase MsRdpClient10

Control de cliente RDP de Microsoft (redistribuible): versión 11

Esta clase implementa las interfaces siguientes.

-   [**IMsRdpClient10**](imsrdpclient10.md)
-   [**IMsRdpClient9**](imsrdpclient9.md)
-   [**IMsRdpClient8**](imsrdpclient8.md)
-   [**IMsRdpClient7**](imsrdpclient7.md)
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
-   [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
-   [**IMsRdpPreferredRedirectionInfo**](imsrdppreferredredirectioninfo.md)

**MsRdpClient10** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase MsRdpClient10** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](imsrdpclient9-attachevent.md)                                            | Asocia un evento. <br/>                                                                                                                                                                                                                                                                |
| [**Conectar**](imstscax-connect.md)                                                         | Inicia una conexión con las propiedades establecidas actualmente en el control .<br/>                                                                                                                                                                                                          |
| [**CreateVirtualChannels**](imstscax-createvirtualchannels.md)                             | Crea un objeto de canal virtual del lado cliente para cada nombre de canal virtual especificado.<br/>                                                                                                                                                                                              |
| [**detachEvent**](imsrdpclient9-detachevent.md)                                            | Desasoja un evento. <br/>                                                                                                                                                                                                                                                                |
| [**Desconectar**](imstscax-disconnect.md)                                                   | Desconecta la conexión activa.<br/>                                                                                                                                                                                                                                                 |
| [**GetErrorDescription**](imsrdpclient5-geterrordescription.md)                            | Recupera los códigos de error y los mensajes de error.<br/>                                                                                                                                                                                                                                      |
| [**GetStatusText**](imsrdpclient7-getstatustext.md)                                        | Recupera el texto de estado del código de estado especificado.<br/>                                                                                                                                                                                                                           |
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
| [**Volver a conectar**](imsrdpclient8-reconnect.md)                                                | Se vuelve a conectar a la sesión remota con el nuevo ancho y alto del escritorio.<br/>                                                                                                                                                                                                            |
| [**RequestClose**](imsrdpclient-requestclose.md)                                           | Solicita un cierre correcto del control de cliente.<br/>                                                                                                                                                                                                                                |
| [**ResetPassword**](imstscnonscriptable-resetpassword.md)                                  | Restablece todos los estados de contraseña del control .<br/>                                                                                                                                                                                                                                         |
| [**SendKeys**](imsrdpclientnonscriptable-sendkeys.md)                                      | Envía una serie de pulsaciones de tecla al control. Las pulsaciones de tecla están en formato de código de examen, que son los datos del teclado de las teclas físicas reales.<br/>                                                                                                                                       |
| [**SendOnVirtualChannel**](imstscax-sendonvirtualchannel.md)                               | Envía datos al servidor host de sesión de Escritorio remoto a través de un canal virtual que se creó anteriormente mediante el método [**IMsTscAx::CreateVirtualChannels.**](imstscax-createvirtualchannels.md)<br/>                                                                                         |
| [**SendRemoteAction**](imsrdpclient8-sendremoteaction.md)                                  | Hace que se realice una acción en la sesión remota.<br/>                                                                                                                                                                                                                            |
| [**SetVirtualChannelOptions**](imsrdpclient-setvirtualchanneloptions.md)                   | Establece las opciones de canal virtual para el control de cliente.<br/>                                                                                                                                                                                                                           |
| [**SyncSessionDisplaySettings**](imsrdpclient9-syncsessiondisplaysettings.md)              | Sincroniza la configuración de visualización de la sesión. <br/>                                                                                                                                                                                                                                            |
| [**UpdateSessionDisplaySettings**](/previous-versions/windows/desktop/legacy/mt703457(v=vs.85))          | Actualiza la configuración de visualización de la sesión. <br/>                                                                                                                                                                                                                                                 |



 

### <a name="properties"></a>Propiedades

La **clase MsRdpClient10** tiene estas propiedades.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propiedad</th>
<th style="text-align: left;">Tipo de acceso</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-advancedsettings.md"><strong>AdvancedSettings</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero <a href="imstscadvancedsettings-interface.md"><strong>de interfaz IMsTscAdvancedSettings.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-advancedsettings2.md"><strong>AdvancedSettings2</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero a la <a href="imsrdpclientadvancedsettings-interface.md"><strong>interfaz IMsRdpClientAdvancedSettings,</strong></a> que se usa para establecer la configuración avanzada para el control de cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient2-advancedsettings3.md"><strong>AdvancedSettings3</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero a la <a href="imsrdpclientadvancedsettings2.md"><strong>interfaz IMsRdpClientAdvancedSettings2,</strong></a> que se usa para establecer la configuración avanzada del control de cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient3-advancedsettings4.md"><strong>AdvancedSettings4</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero a la <a href="imsrdpclientadvancedsettings3.md"><strong>interfaz IMsRdpClientAdvancedSettings3,</strong></a> que se usa para establecer la configuración avanzada para el control de cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient4-advancedsettings5.md"><strong>AdvancedSettings5</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero <a href="imsrdpclientadvancedsettings4.md"><strong>de interfaz IMsRdpClientAdvancedSettings4.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient5-advancedsettings6.md"><strong>AdvancedSettings6</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Interfaz de <a href="imsrdpclientadvancedsettings5.md"><strong>IMsRdpClientAdvancedSettings5</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient6-advancedsettings7.md"><strong>AdvancedSettings7</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Interfaz de <a href="imsrdpclientadvancedsettings6.md"><strong>IMsRdpClientAdvancedSettings6</strong></a>.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-advancedsettings8.md"><strong>AdvancedSettings8</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Objeto que admite la <a href="imsrdpclientadvancedsettings7.md"><strong>interfaz IMsRdpClientAdvancedSettings7.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient8-advancedsettings9.md"><strong>AdvancedSettings9</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Interfaz <a href="imsrdpclientadvancedsettings8.md"><strong>IMsRdpClientAdvancedSettings8</strong></a> que representa el objeto de configuración.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-allowcredentialsaving.md"><strong>AllowCredentialSaving</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el cuadro de diálogo credenciales muestra una casilla para habilitar el guardado de credenciales.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-allowpromptingforcredentials.md"><strong>AllowPromptingForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el control Escritorio remoto ActiveX puede solicitar credenciales al usuario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-binarypassword.md"><strong>BinaryPassword</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Esta propiedad no es compatible.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-binarysalt.md"><strong>BinarySalt</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Esta propiedad no es compatible.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-cipherstrength.md"><strong>CipherStrength</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La intensidad de cifrado máxima del control actual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-cleartextpassword.md"><strong>ClearTextPassword</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">La Escritorio remoto ActiveX de control, en formato de texto no cifrado.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-colordepth.md"><strong>Colordepth</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Profundidad de color del control actual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connected.md"><strong>Conectado</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Estado de conexión del control actual.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient2-connectedstatustext.md"><strong>ConnectedStatusText</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Texto que se muestra en el área de cliente del control mientras el control está en estado conectado.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-connectingtext.md"><strong>ConnectingText</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Texto que aparece centrado en el control mientras se conecta el control.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Cadena de texto que se mostrará para la barra de conexión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-desktopheight.md"><strong>DesktopHeight</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Alto del control actual, en píxeles, en el escritorio remoto inicial.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-desktopwidth.md"><strong>DesktopWidth</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Ancho del control actual, en píxeles, en el escritorio remoto inicial.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La colección de dispositivos PnP que están disponibles para el redireccionamiento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableconnectionbar.md"><strong>DisableConnectionBar</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">Especifica si el control Escritorio remoto ActiveX debe deshabilitar la barra de conexión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-disableremoteappcapscheck.md"><strong>DisableRemoteAppCapsCheck</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el control Escritorio remoto ActiveX no debe comprobar las funcionalidades de RemoteApp del servidor.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-disconnectedtext.md"><strong>DisconnectedText</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Texto que aparece centrado en el control antes de finalizar una conexión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-domain.md"><strong>Domain</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Dominio en el que el usuario actual inicia sesión.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Colección de unidades de disco que está disponible para el redireccionamiento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si CredSSP está habilitado para esta conexión.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient-extendeddisconnectreason.md"><strong>ExtendedDisconnectReason</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Información ampliada sobre el motivo de la desconexión del control de cliente.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-fullscreen.md"><strong>Fullscreen</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Indica si el control está en modo de pantalla completa.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-fullscreentitle.md"><strong>FullScreenTitle</strong></a><br/></td>
<td style="text-align: left;">Solo escritura<br/></td>
<td style="text-align: left;">Título de la ventana que se muestra cuando el control está en modo de pantalla completa.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-getremotemonitorsboundingbox.md"><strong>GetRemoteMonitorsBoundingBox</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Especifica el rectángulo delimitador del monitor remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-horizontalscrollbarvisible.md"><strong>HorizontalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Indica si el control ha mostrado una barra de desplazamiento horizontal.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-launchedviaclientshellinterface.md"><strong>LaunchedViaClientShellInterface</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el usuario inició el control de cliente mediante la interfaz de acceso web de Escritorio remoto.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-markrdpsettingssecure.md"><strong>MarkRdpSettingsSecure</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si la configuración de RDP está marcada como segura.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-msrdpclientshell.md"><strong>MsRdpClientShell</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La configuración de cliente para el iniciador del portal web.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si se admite la configuración NegotiateSecurityLayer para esta conexión.<br/>
<blockquote>
[!Note]<br />
Cuando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> está habilitado y presente en el cliente, o cuando Capa de sockets seguros (SSL) está habilitado con la autenticación de usuario, NegotiateSecurityLayer se omite.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscnonscriptable-portablepassword.md"><strong>PortablePassword</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Esta propiedad no es compatible.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscnonscriptable-portablesalt.md"><strong>PortableSalt</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Esta propiedad no es compatible.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si se debe mostrar el cuadro de diálogo solicitar credenciales.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-promptforcredsonclient.md"><strong>PromptForCredsOnClient</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el control de cliente muestra un cuadro de diálogo que solicita credenciales.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-publishercertificatechain.md"><strong>PublisherCertificateChain</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica la cadena de certificados del publicador. La cadena se almacena en una variante de tipo VT_BYREF que contiene un puntero a una <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context"><strong>CERT_CHAIN_CONTEXT</strong></a> estructura.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si los dispositivos PnP conectados dinámicamente que se enumeran mientras están en una sesión están disponibles para el redireccionamiento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si las unidades PnP conectadas dinámicamente que se enumeran mientras están en una sesión están disponibles para el redireccionamiento.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-redirectionwarningtype.md"><strong>RedirectionWarningType</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Controla la presencia y la apariencia del cuadro de diálogo de redireccionamiento.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorcount.md"><strong>RemoteMonitorCount</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Especifica el número de monitores remotos.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-remotemonitorlayoutmatcheslocal.md"><strong>RemoteMonitorLayoutMatchesLocal</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Especifica si el diseño del monitor remoto es idéntico al diseño del monitor local.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-remoteprogram.md"><strong>RemoteProgram</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La configuración de RemoteApp del cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-remoteprogram2.md"><strong>RemoteProgram2</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Objeto que admite la <a href="itsremoteprogram2.md"><strong>interfaz ITSRemoteProgram2.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient10-remoteprogram3.md"><strong>RemoteProgram3</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Objeto que admite la <a href="itsremoteprogram3.md"><strong>interfaz ITSRemoteProgram3.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-securedsettings.md"><strong>SecuredSettings</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero <a href="imstscsecuredsettings-interface.md"><strong>de interfaz IMsTscSecuredSettings.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient-securedsettings2.md"><strong>SecuredSettings2</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Puntero a la <a href="imsrdpclientsecuredsettings-interface.md"><strong>interfaz IMsRdpClientSecuredSettings,</strong></a> que se usa para establecer la configuración protegida para el control de cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient7-securedsettings3.md"><strong>SecuredSettings3</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Objeto que admite la <a href="imsrdpclientsecuredsettings2.md"><strong>interfaz IMsRdpClientSecuredSettings2.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-securedsettingsenabled.md"><strong>SecuredSettingsEnabled</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Indica si la <a href="imstscsecuredsettings-interface.md"><strong>interfaz IMsTscSecuredSettings</strong></a> está disponible.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-server.md"><strong>Servidor</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Nombre del servidor al que está conectado el control actual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si se debe mostrar el cuadro de diálogo de advertencia de seguridad de redireccionamiento antes de iniciar una sesión.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-startconnected.md"><strong>StartConnected</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Indica si el control establecerá la conexión del servidor host de sesión de Escritorio remoto inmediatamente después del inicio.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient5-transportsettings.md"><strong>TransportSettings</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">La configuración de puerta de enlace de Escritorio remoto del cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient6-transportsettings2.md"><strong>TransportSettings2</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Interfaz de <a href="imsrdpclienttransportsettings2.md"><strong>IMsRdpClientTransportSettings2</strong></a>.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclient7-transportsettings3.md"><strong>TransportSettings3</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Objeto que admite la <a href="imsrdpclienttransportsettings3.md"><strong>interfaz IMsRdpClientTransportSettings3.</strong></a><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclient9-transportsettings4.md"><strong>TransportSettings4</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Objeto que admite la <a href="imsrdpclienttransportsettings4.md"><strong>interfaz IMsRdpClientTransportSettings4.</strong></a><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-trustedzonesite.md"><strong>TrustedZoneSite</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el sitio web desde el que el usuario inició la conexión está en la lista de sitios de confianza del equipo cliente.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable2-uiparentwindowhandle.md"><strong>UIParentWindowHandle</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Identificador de ventana que va a ser la ventana primaria del control. Esto permite que las ventanas mostradas por el control sean modales correctamente con respecto a las ventanas mostradas por la aplicación primaria.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-usemultimon.md"><strong>UseMultimon</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el control Escritorio remoto ActiveX debe usar varios monitores.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdppreferredredirectioninfo-useredirectionservername.md"><strong>UseRedirectionServerName</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Si se va a usar el nombre del servidor de redirección.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-username.md"><strong>nombre de usuario</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Credencial de inicio de sesión de nombre de usuario.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imstscax-version.md"><strong>Versión</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Número de versión del control actual.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imstscax-verticalscrollbarvisible.md"><strong>VerticalScrollBarVisible</strong></a><br/></td>
<td style="text-align: left;">Solo lectura<br/></td>
<td style="text-align: left;">Indica si el control muestra una barra de desplazamiento vertical.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el cuadro de diálogo de advertencia de seguridad debe incluir una advertencia sobre el redireccionamiento del Portapapeles antes de iniciar una sesión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable5-warnaboutdirectxredirection.md"><strong>WarnAboutDirectXRedirection</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">No se usa esta propiedad.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable4-warnaboutprinterredirection.md"><strong>WarnAboutPrinterRedirection</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si el cuadro de diálogo de redireccionamiento muestra un mensaje sobre el redireccionamiento de impresoras antes de iniciar una sesión.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a><br/></td>
<td style="text-align: left;">Lectura/escritura<br/></td>
<td style="text-align: left;">Especifica si la advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| CLSID<br/>                    | CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24<br/>     |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Escritorio remoto ActiveX clases de control](remote-desktop-activex-control-classes.md)
</dt> </dl>

