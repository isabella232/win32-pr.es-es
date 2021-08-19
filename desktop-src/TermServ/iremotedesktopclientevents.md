---
title: Interfaz IRemoteDesktopClientEvents
description: Proporciona métodos que reciben información del servidor relacionada con eventos de control de cliente.
ms.assetid: CF1DA4C8-94A5-4E6A-AEB7-6F46117E9DF2
ms.tgt_platform: multiple
keywords:
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto , descrito
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
ms.openlocfilehash: 8bae11edf7e6c603c534afb75fe5c90bcc868f1e359f1d78748dd94b18b5627e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657075"
---
# <a name="iremotedesktopclientevents-interface"></a>Interfaz IRemoteDesktopClientEvents

Proporciona métodos que reciben información del servidor relacionada con eventos de control de cliente. Entre los eventos se incluyen la conexión y desconexión, las solicitudes de modo de pantalla completa, el inicio de sesión correcto y las condiciones de error.

## <a name="members"></a>Miembros

La **interfaz IRemoteDesktopClientEvents** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IRemoteDesktopClientEvents** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz IRemoteDesktopClientEvents** tiene estos métodos.



| Método                                                                                      | Descripción                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OnAdminMessageReceived**](iremotedesktopclientevents-onadminmessagereceived.md)         | Se llama cuando el control de cliente recibe un mensaje administrativo. <br/>                                                                                      |
| [**OnAutoReconnected**](iremotedesktopclientevents-onautoreconnected.md)                   | Se llama cuando el control de cliente se ha vuelto a conectar automáticamente a una sesión remota. <br/>                                                                       |
| [**OnAutoReconnecting**](iremotedesktopclientevents-onautoreconnecting.md)                 | Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota. <br/>                                                  |
| [**OnConnected**](iremotedesktopclientevents-onconnected.md)                               | Se llama cuando el control de cliente se ha conectado a una sesión remota.<br/>                                                                                        |
| [**OnConnecting**](iremotedesktopclientevents-onconnecting.md)                             | Se llama cuando el control de cliente intenta establecer una conexión a una sesión remota. <br/>                                                                  |
| [**OnDialogDismissed**](iremotedesktopclientevents-ondialogdismissed.md)                   | Se llama después de que se descarte un cuadro de diálogo mostrado por el control de cliente. <br/>                                                                                 |
| [**OnDialogDisplaying**](iremotedesktopclientevents-ondialogdisplaying.md)                 | Se llama antes de que el control muestre un cuadro de diálogo. <br/>                                                                                                        |
| [**OnDisconnected**](iremotedesktopclientevents-ondisconnected.md)                         | Se llama cuando el control de cliente se ha desconectado de una sesión remota. <br/>                                                                             |
| [**OnKeyCombinationPressed**](iremotedesktopclientevents-onkeycombinationpressed.md)       | Se llama cuando se presionan combinaciones de teclas especiales en la sesión remota. <br/>                                                                                 |
| [**OnLoginCompleted**](iremotedesktopclientevents-onlogincompleted.md)                     | Se llama cuando el control de cliente ha iniciado sesión correctamente en una sesión remota. <br/>                                                                          |
| [**OnNetworkStatusChanged**](iremotedesktopclientevents-onnetworkstatuschanged.md)         | Se llama cuando el estado de la red ha cambiado. <br/>                                                                                                             |
| [**OnRemoteDesktopSizeChanged**](iremotedesktopclientevents-onremotedesktopsizechanged.md) | Se llama cuando el tamaño del escritorio remoto ha cambiado. <br/>                                                                                                        |
| [**OnStatusChanged**](iremotedesktopclientevents-onstatuschanged.md)                       | Se llama cuando el control de cliente ha actualizado su estado. <br/>                                                                                                  |
| [**OnTouchPointerCursorMoved**](iremotedesktopclientevents-ontouchpointercursormoved.md)   | Se llama cuando se ha movido el cursor del puntero táctil y la [**propiedad EventsEnabled**](/windows/win32/api/rdpappcontainerclient/nf-rdpappcontainerclient-iremotedesktopclienttouchpointer-get_eventsenabled) se establece en true. <br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| CLSID<br/>                    | CLSID RemoteDesktopClient se define como \_ EAB16C5D-EED1-4E95-868B-0FBA1B42C092<br/>       |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Escritorio remoto ActiveX referencia de control](remote-desktop-activex-control-reference.md)
</dt> </dl>

 

