---
title: Clase RemoteDesktopClient
description: Implementa la aplicación de la tienda Windows de Microsoft Escritorio remoto control de cliente-versión 1.
ms.assetid: 0910883A-BD49-4908-8423-1FC280E0FE0C
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la clase RemoteDesktopClient
- Servicios de Escritorio remoto de la clase RemoteDesktopClient, descrito
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
ms.openlocfilehash: fb10b23f52f53e2d89fd5a81449818a8fe374116
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996126"
---
# <a name="remotedesktopclient-class"></a>Clase RemoteDesktopClient

Implementa la aplicación Microsoft Windows Store Escritorio remoto control de cliente-versión 1

Esta clase implementa las interfaces siguientes.

-   [**IRemoteDesktopClient**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclient)
-   [**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)

**RemoteDesktopClient** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **RemoteDesktopClient** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                        |
|:--------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**attachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-attachevent)                                     | Adjunta un controlador de eventos a un evento.<br/>                                                                                                                  |
| [**Conectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-connect)                                             | Inicia una conexión mediante el uso de las propiedades establecidas actualmente en el control de cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).<br/>                         |
| [**DeleteSavedCredentials**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-deletesavedcredentials)               | Elimina las credenciales guardadas para el equipo remoto especificado.<br/>                                                                                            |
| [**detachEvent**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-detachevent)                                     | Desasocia un controlador de eventos de un evento.<br/>                                                                                                                |
| [**Desconectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-disconnect)                                       | Desconecta la conexión activa.<br/>                                                                                                                      |
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Se llama cuando el control de cliente recibe un mensaje administrativo.<br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Se llama cuando el control de cliente se vuelve a conectar automáticamente a una sesión remota.<br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.<br/>                                                  |
| [**Conectado**](iremotedesktopclientevents-onconnected.md)                               | Se llama cuando el control de cliente se ha conectado a una sesión remota.<br/>                                                                                       |
| [**Conectar**](iremotedesktopclientevents-onconnecting.md)                             | Se llama cuando el control de cliente intenta establecer una conexión a una sesión remota.<br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Se llama después de que se descarte un cuadro de diálogo que muestra el control de cliente.<br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Se llama antes de que el control muestre un cuadro de diálogo.<br/>                                                                                                        |
| [**OnDisconnection**](iremotedesktopclientevents-ondisconnected.md)                         | Se llama cuando el control de cliente se ha desconectado de una sesión remota.<br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Se le llama cuando se presionan combinaciones de teclas especiales en la sesión remota.<br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Se llama cuando el control de cliente ha iniciado sesión correctamente en una sesión remota.<br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Se llama cuando el estado de la red ha cambiado.<br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Se llama cuando el tamaño del escritorio remoto ha cambiado.<br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Se llama cuando el control de cliente ha actualizado su estado.<br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Se llama cuando se ha cambiado el cursor del puntero táctil y la propiedad [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está establecida en true.<br/> |
| [**Volver a conectar**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-reconnect)                                         | Inicia una reconexión automática del control de cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP) para ajustar la sesión al nuevo ancho y alto.<br/>   |
| [**UpdateSessionDisplaySettings**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-updatesessiondisplaysettings)   | Actualiza la configuración de ancho y alto del control de cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).<br/>                                               |



 

### <a name="properties"></a>Propiedades

La clase **RemoteDesktopClient** tiene estas propiedades.



| Propiedad                                                             | Tipo de acceso          | Descripción                                                                                                                                                            |
|:---------------------------------------------------------------------|:---------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Acciones**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_actions)<br/>           | Solo lectura<br/> | Recupera el objeto de acciones para el cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).<br/>                                                                    |
| [**Configuración**](iremotedesktopclient-settings.md)<br/>         | Solo lectura<br/> | Recupera el objeto de configuración para el cliente del contenedor de la aplicación Protocolo de escritorio remoto (RDP).<br/>                                                                   |
| [**TouchPointer**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclient-get_touchpointer)<br/> | Solo lectura<br/> | Contiene el objeto [**RemoteDesktopClientTouchPointer**](/windows/win32/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclienttouchpointer) para el cliente del contenedor de la aplicación protocolo de escritorio remoto (RDP).<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient se define como EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases de controles ActiveX Escritorio remoto](remote-desktop-activex-control-classes.md)
</dt> </dl>

 

