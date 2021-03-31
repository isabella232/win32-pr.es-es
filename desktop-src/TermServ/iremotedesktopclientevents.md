---
title: Interfaz IRemoteDesktopClientEvents
description: Proporciona métodos que reciben información del servidor relacionada con los eventos de control de cliente.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IRemoteDesktopClientEvents
- Servicios de Escritorio remoto de la interfaz IRemoteDesktopClientEvents, descrito
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7533ee7fea7c522b6129bda06891630c3e5ad15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079375"
---
# <a name="iremotedesktopclientevents-interface"></a>Interfaz IRemoteDesktopClientEvents

Proporciona métodos que reciben información del servidor relacionada con los eventos de control de cliente. Los eventos incluyen la conexión y desconexión, las solicitudes del modo de pantalla completa, el inicio de sesión correcto y las condiciones de error.

## <a name="members"></a>Miembros

La interfaz **IRemoteDesktopClientEvents** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IRemoteDesktopClientEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IRemoteDesktopClientEvents** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Se llama cuando el control de cliente recibe un mensaje administrativo. <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Se llama cuando el control de cliente se vuelve a conectar automáticamente a una sesión remota. <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota. <br/>                                                  |
| [**Conectado**](iremotedesktopclientevents-onconnected.md)                               | Se llama cuando el control de cliente se ha conectado a una sesión remota.<br/>                                                                                        |
| [**Conectar**](iremotedesktopclientevents-onconnecting.md)                             | Se llama cuando el control de cliente intenta establecer una conexión a una sesión remota. <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Se llama después de que se descarte un cuadro de diálogo que muestra el control de cliente. <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Se llama antes de que el control muestre un cuadro de diálogo. <br/>                                                                                                        |
| [**OnDisconnection**](iremotedesktopclientevents-ondisconnected.md)                         | Se llama cuando el control de cliente se ha desconectado de una sesión remota. <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Se le llama cuando se presionan combinaciones de teclas especiales en la sesión remota. <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Se llama cuando el control de cliente ha iniciado sesión correctamente en una sesión remota. <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Se llama cuando el estado de la red ha cambiado. <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Se llama cuando el tamaño del escritorio remoto ha cambiado. <br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Se llama cuando el control de cliente ha actualizado su estado. <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Se llama cuando se ha cambiado el cursor del puntero táctil y la propiedad [**EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) está establecida en true. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID \_ RemoteDesktopClient se define como EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Referencia de controles ActiveX Escritorio remoto](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

