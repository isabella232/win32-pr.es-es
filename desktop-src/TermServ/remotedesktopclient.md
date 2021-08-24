---
title: RemoteDesktopClient (clase)
description: 'Implementa la aplicación de Microsoft Windows Store Escritorio remoto Client Control: versión 1.'
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- Clase RemoteDesktopClient Servicios de Escritorio remoto
- Clase RemoteDesktopClient Servicios de Escritorio remoto , descrito
topic_type:
- apiref
api_name:
- RemoteDesktopClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cad76c8c189854a28709765c5677d047590216ae8ab6271d44c595f7b24fdd88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865905"
---
# <a name="remotedesktopclient-class"></a>RemoteDesktopClient (clase)

Implementa la aplicación de Microsoft Windows Store Escritorio remoto Control de cliente: versión 1

Esta clase implementa las interfaces siguientes.

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase RemoteDesktopClient** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Asocia un controlador de eventos a un evento.<br/>                                                                                                                  |
| [**Conectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Inicia una conexión mediante las propiedades establecidas actualmente en el control de cliente Protocolo de escritorio remoto contenedor de aplicaciones (RDP).<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Elimina las credenciales guardadas para el equipo remoto especificado.<br/>                                                                                            |
| [**detachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Separa un controlador de eventos de un evento.<br/>                                                                                                                |
| [**Desconectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Desconecta la conexión activa.<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Se llama cuando el control de cliente recibe un mensaje administrativo.<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Se llama cuando el control de cliente se vuelve a conectar automáticamente a una sesión remota.<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.<br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Se llama cuando el control de cliente se ha conectado a una sesión remota.<br/>                                                                                       |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Se llama cuando el control de cliente intenta establecer una conexión a una sesión remota.<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Se llama después de descartar un cuadro de diálogo mostrado por el control de cliente.<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Se llama antes de que el control muestre un cuadro de diálogo.<br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Se llama cuando el control de cliente se ha desconectado de una sesión remota.<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Se llama cuando se presionan combinaciones de teclas especiales en la sesión remota.<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Se llama cuando el control de cliente ha iniciado sesión correctamente en una sesión remota.<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Se llama cuando el estado de la red ha cambiado.<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Se llama cuando cambia el tamaño del escritorio remoto.<br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Se llama cuando el control de cliente ha actualizado su estado.<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Se llama cuando se ha movido el cursor del puntero táctil y la [**propiedad EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) se establece en true.<br/> |
| [**Volver a conectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Inicia una reconexión automática del control de cliente del contenedor de aplicaciones Protocolo de escritorio remoto (RDP) para ajustar la sesión al nuevo ancho y alto.<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Actualiza la configuración de ancho y alto para el control de cliente Protocolo de escritorio remoto de contenedor de aplicaciones (RDP).<br/>                                               |



 

### <a name="properties"></a>Propiedades

La **clase RemoteDesktopClient** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acciones**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Solo lectura<br/> | Recupera el objeto actions para el cliente de contenedor de Protocolo de escritorio remoto (RDP).<br/>                                                                    |
| [**Configuración**](iremotedesktopclient-settings.md)<br/>         | Solo lectura<br/> | Recupera el objeto de configuración para el cliente Protocolo de escritorio remoto contenedor de aplicaciones (RDP).<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Solo lectura<br/> | Contiene el [**objeto RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) para el Protocolo de escritorio remoto contenedor de aplicaciones (RDP).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID RemoteDesktopClient se define como \_ EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto ActiveX clases de control](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

