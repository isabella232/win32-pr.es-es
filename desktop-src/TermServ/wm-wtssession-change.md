---
title: WM_WTSSESSION_CHANGE mensaje (Winuser.h)
description: Notifica a las aplicaciones los cambios en el estado de sesión.
ms.assetid: 758a130c-b75a-40fd-8530-3766aa86c5ba
ms.tgt_platform: multiple
keywords:
- WM_WTSSESSION_CHANGE mensaje Servicios de Escritorio remoto
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
ms.openlocfilehash: f29bef7eb7778602a256f80cb04e47eae905a245783906c3388b576aecedee18
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119419845"
---
# <a name="wm_wtssession_change-message"></a>Mensaje \_ DE CAMBIO DE WTSSESSION de WM \_

Notifica a las aplicaciones los cambios en el estado de sesión.

La ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


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

*hWnd* \[ En\]
</dt> <dd>

Identificador de la ventana.

</dd> <dt>

*Mensaje* \[ En\]
</dt> <dd>

Especifica el mensaje (**WM \_ WTSSESSION \_ CHANGE**).

</dd> <dt>

*wParam* \[ En\]
</dt> <dd>

Código de estado que describe el motivo por el que se envió la notificación de cambio de estado de sesión. Este parámetro puede ser uno de los valores siguientes.

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ CONSOLE \_ CONNECT** (0x1)


</dt> <dd>

La sesión identificada por *lParam se* conectó al terminal de la consola o a RemoteFX sesión.

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ CONSOLE \_ DISCONNECT** (0x2)


</dt> <dd>

La sesión identificada por *lParam se* desconectó del terminal de consola o RemoteFX sesión.

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ CONEXIÓN \_ REMOTA** (0x3)


</dt> <dd>

La sesión identificada por *lParam* se conectó al terminal remoto.

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ REMOTE \_ DISCONNECT** (0x4)


</dt> <dd>

La sesión identificada por *lParam* se desconectó del terminal remoto.

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ INICIO \_ DE SESIÓN** (0x5)


</dt> <dd>

Un usuario ha iniciado sesión en la sesión identificada por *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ SESSION \_ LOGOFF** (0x6)


</dt> <dd>

Un usuario ha cerrado la sesión identificada por *lParam*.

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ BLOQUEO \_ DE SESIÓN** (0x7)


</dt> <dd>

La sesión identificada por *lParam* se ha bloqueado.

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ DESBLOQUEO \_ DE SESIÓN** (0x8)


</dt> <dd>

La sesión identificada por *lParam* se ha desbloqueado.

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_CONTROL REMOTO DE \_ SESIÓN** (0x9)


</dt> <dd>

La sesión identificada por *lParam* ha cambiado su estado controlado remoto. Para determinar el estado, llame [**a GetSystemMetrics y**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) compruebe la **métrica SM \_ REMOTECONTROL.**

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ SESSION \_ CREATE** (0xA)


</dt> <dd>

Reservado para uso futuro.

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ SESSION \_ TERMINATE** (0xB)


</dt> <dd>

Reservado para uso futuro.

</dd> </dl> </dd> <dt>

*lParam* \[ En\]
</dt> <dd>

Identificador de la sesión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

Este mensaje solo se envía a las aplicaciones que se han registrado para recibir este mensaje mediante una llamada a [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).

Entre los ejemplos de cómo las aplicaciones pueden responder a este mensaje se incluyen la liberación o adquisición de recursos específicos de la consola, la determinación de cómo se va a pintar una pantalla o el desencadenamiento de efectos de animación de consola.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                           |
| Header<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[**WTSUnRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

