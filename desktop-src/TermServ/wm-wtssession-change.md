---
title: Mensaje de WM_WTSSESSION_CHANGE (Winuser. h)
description: Notifica a las aplicaciones los cambios en el estado de la sesión.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- WM_WTSSESSION_CHANGE Servicios de Escritorio remoto de mensaje
topic_type:
- apiref
api_name:
- WM_WTSSESSION_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f1dc421aa160824a194588711e84f961ea4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801279"
---
# <a name="wm_wtssession_change-message"></a>Mensaje de cambio de \_ WTSSESSION de WM \_

Notifica a las aplicaciones los cambios en el estado de la sesión.

La ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hWnd* \[ de\]
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*Mensaje* \[ de de\]
</dt> <dd>

Especifica el mensaje (**\_ \_ cambio de WTSSESSION de WM**).

</dd> <dt>

*wParam* \[ de\]
</dt> <dd>

Código de estado que describe el motivo por el que se envió la notificación de cambio de estado de sesión. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Conexión** de la consola (0x1)


</dt> <dd>

La sesión identificada por *lParam* estaba conectada al terminal de la consola o a la sesión de RemoteFX.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Desconexión de consola** (0X2)


</dt> <dd>

La sesión identificada por *lParam* se desconectó del terminal de la consola o de la sesión de RemoteFX.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Conexión remota** (0X3)


</dt> <dd>

La sesión identificada por *lParam* estaba conectada al terminal remoto.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Desconexión remota** (0x4)


</dt> <dd>

La sesión identificada por *lParam* se desconectó del terminal remoto.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Inicio** de sesión (0X5)


</dt> <dd>

Un usuario ha iniciado sesión en la sesión identificada por *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Cerrar sesión** (0x6)


</dt> <dd>

Un usuario ha cerrado la sesión identificada por *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Bloqueo de sesión** (0X7)


</dt> <dd>

La sesión identificada por *lParam* se ha bloqueado.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Desbloqueo de sesión** (0x8)


</dt> <dd>

Se ha desbloqueado la sesión identificada por *lParam* .

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Control remoto de sesión** (0x9)


</dt> <dd>

La sesión identificada por *lParam* ha cambiado su estado controlado remoto. Para determinar el estado, llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) y Compruebe la métrica **SM \_ REMOTECONTROL** .

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Creación** de la sesión (0xA)


</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Finalización** de la sesión (0xB)


</dt> <dd>

Reservado para uso futuro.

</dd> </dl> </dd> <dt>

*lParam* \[ de\]
</dt> <dd>

Identificador de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Este mensaje se envía únicamente a las aplicaciones que se han registrado para recibir este mensaje mediante una llamada a [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).

Entre los ejemplos de cómo las aplicaciones pueden responder a este mensaje se incluyen la liberación o adquisición de recursos específicos de la consola, la determinación del modo de pintar una pantalla o la activación de los efectos de animación de la consola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                           |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

