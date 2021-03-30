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
# <a name="wm_wtssession_change-message"></a><span data-ttu-id="6641e-104">Mensaje de cambio de \_ WTSSESSION de WM \_</span><span class="sxs-lookup"><span data-stu-id="6641e-104">WM\_WTSSESSION\_CHANGE message</span></span>

<span data-ttu-id="6641e-105">Notifica a las aplicaciones los cambios en el estado de la sesión.</span><span class="sxs-lookup"><span data-stu-id="6641e-105">Notifies applications of changes in session state.</span></span>

<span data-ttu-id="6641e-106">La ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6641e-106">The window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
LRESULT CALLBACK WindowProc(
  HWND hWnd,       // handle to window
  UINT Msg,        // WM_WTSSESSION_CHANGE
  WPARAM wParam,   // session state change event
  LPARAM lParam    // session ID
);
```



## <a name="parameters"></a><span data-ttu-id="6641e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6641e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6641e-108">*hWnd* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6641e-108">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641e-109">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6641e-109">Handle to the window.</span></span>

</dd> <dt>

<span data-ttu-id="6641e-110">*Mensaje* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="6641e-110">*Msg* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641e-111">Especifica el mensaje (**\_ \_ cambio de WTSSESSION de WM**).</span><span class="sxs-lookup"><span data-stu-id="6641e-111">Specifies the message (**WM\_WTSSESSION\_CHANGE**).</span></span>

</dd> <dt>

<span data-ttu-id="6641e-112">*wParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6641e-112">*wParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641e-113">Código de estado que describe el motivo por el que se envió la notificación de cambio de estado de sesión.</span><span class="sxs-lookup"><span data-stu-id="6641e-113">Status code describing the reason the session state change notification was sent.</span></span> <span data-ttu-id="6641e-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="6641e-114">This parameter can be one of the following values.</span></span>

<dt>

<span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>

<span data-ttu-id="6641e-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS \_ \_Conexión** de la consola (0x1)</span><span class="sxs-lookup"><span data-stu-id="6641e-115"><span id="WTS_CONSOLE_CONNECT"></span><span id="wts_console_connect"></span>**WTS\_CONSOLE\_CONNECT** (0x1)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-116">La sesión identificada por *lParam* estaba conectada al terminal de la consola o a la sesión de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6641e-116">The session identified by *lParam* was connected to the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>

<span data-ttu-id="6641e-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS \_ \_Desconexión de consola** (0X2)</span><span class="sxs-lookup"><span data-stu-id="6641e-117"><span id="WTS_CONSOLE_DISCONNECT"></span><span id="wts_console_disconnect"></span>**WTS\_CONSOLE\_DISCONNECT** (0x2)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-118">La sesión identificada por *lParam* se desconectó del terminal de la consola o de la sesión de RemoteFX.</span><span class="sxs-lookup"><span data-stu-id="6641e-118">The session identified by *lParam* was disconnected from the console terminal or RemoteFX session.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>

<span data-ttu-id="6641e-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS \_ \_Conexión remota** (0X3)</span><span class="sxs-lookup"><span data-stu-id="6641e-119"><span id="WTS_REMOTE_CONNECT"></span><span id="wts_remote_connect"></span>**WTS\_REMOTE\_CONNECT** (0x3)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-120">La sesión identificada por *lParam* estaba conectada al terminal remoto.</span><span class="sxs-lookup"><span data-stu-id="6641e-120">The session identified by *lParam* was connected to the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>

<span data-ttu-id="6641e-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS \_ \_Desconexión remota** (0x4)</span><span class="sxs-lookup"><span data-stu-id="6641e-121"><span id="WTS_REMOTE_DISCONNECT"></span><span id="wts_remote_disconnect"></span>**WTS\_REMOTE\_DISCONNECT** (0x4)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-122">La sesión identificada por *lParam* se desconectó del terminal remoto.</span><span class="sxs-lookup"><span data-stu-id="6641e-122">The session identified by *lParam* was disconnected from the remote terminal.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>

<span data-ttu-id="6641e-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS \_ \_Inicio** de sesión (0X5)</span><span class="sxs-lookup"><span data-stu-id="6641e-123"><span id="WTS_SESSION_LOGON"></span><span id="wts_session_logon"></span>**WTS\_SESSION\_LOGON** (0x5)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-124">Un usuario ha iniciado sesión en la sesión identificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6641e-124">A user has logged on to the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>

<span data-ttu-id="6641e-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS \_ \_Cerrar sesión** (0x6)</span><span class="sxs-lookup"><span data-stu-id="6641e-125"><span id="WTS_SESSION_LOGOFF"></span><span id="wts_session_logoff"></span>**WTS\_SESSION\_LOGOFF** (0x6)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-126">Un usuario ha cerrado la sesión identificada por *lParam*.</span><span class="sxs-lookup"><span data-stu-id="6641e-126">A user has logged off the session identified by *lParam*.</span></span>

</dd> <dt>

<span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>

<span data-ttu-id="6641e-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS \_ \_Bloqueo de sesión** (0X7)</span><span class="sxs-lookup"><span data-stu-id="6641e-127"><span id="WTS_SESSION_LOCK"></span><span id="wts_session_lock"></span>**WTS\_SESSION\_LOCK** (0x7)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-128">La sesión identificada por *lParam* se ha bloqueado.</span><span class="sxs-lookup"><span data-stu-id="6641e-128">The session identified by *lParam* has been locked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>

<span data-ttu-id="6641e-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS \_ \_Desbloqueo de sesión** (0x8)</span><span class="sxs-lookup"><span data-stu-id="6641e-129"><span id="WTS_SESSION_UNLOCK"></span><span id="wts_session_unlock"></span>**WTS\_SESSION\_UNLOCK** (0x8)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-130">Se ha desbloqueado la sesión identificada por *lParam* .</span><span class="sxs-lookup"><span data-stu-id="6641e-130">The session identified by *lParam* has been unlocked.</span></span>

</dd> <dt>

<span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>

<span data-ttu-id="6641e-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS \_ \_ \_ Control remoto de sesión** (0x9)</span><span class="sxs-lookup"><span data-stu-id="6641e-131"><span id="WTS_SESSION_REMOTE_CONTROL"></span><span id="wts_session_remote_control"></span>**WTS\_SESSION\_REMOTE\_CONTROL** (0x9)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-132">La sesión identificada por *lParam* ha cambiado su estado controlado remoto.</span><span class="sxs-lookup"><span data-stu-id="6641e-132">The session identified by *lParam* has changed its remote controlled status.</span></span> <span data-ttu-id="6641e-133">Para determinar el estado, llame a [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) y Compruebe la métrica **SM \_ REMOTECONTROL** .</span><span class="sxs-lookup"><span data-stu-id="6641e-133">To determine the status, call [**GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) and check the **SM\_REMOTECONTROL** metric.</span></span>

</dd> <dt>

<span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>

<span data-ttu-id="6641e-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS \_ \_Creación** de la sesión (0xA)</span><span class="sxs-lookup"><span data-stu-id="6641e-134"><span id="WTS_SESSION_CREATE"></span><span id="wts_session_create"></span>**WTS\_SESSION\_CREATE** (0xA)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-135">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6641e-135">Reserved for future use.</span></span>

</dd> <dt>

<span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>

<span data-ttu-id="6641e-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS \_ \_Finalización** de la sesión (0xB)</span><span class="sxs-lookup"><span data-stu-id="6641e-136"><span id="WTS_SESSION_TERMINATE"></span><span id="wts_session_terminate"></span>**WTS\_SESSION\_TERMINATE** (0xB)</span></span>


</dt> <dd>

<span data-ttu-id="6641e-137">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6641e-137">Reserved for future use.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6641e-138">*lParam* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="6641e-138">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6641e-139">Identificador de la sesión.</span><span class="sxs-lookup"><span data-stu-id="6641e-139">The identifier of the session.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6641e-140">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6641e-140">Return value</span></span>

<span data-ttu-id="6641e-141">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="6641e-141">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="6641e-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6641e-142">Remarks</span></span>

<span data-ttu-id="6641e-143">Este mensaje se envía únicamente a las aplicaciones que se han registrado para recibir este mensaje mediante una llamada a [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span><span class="sxs-lookup"><span data-stu-id="6641e-143">This message is sent only to applications that have registered to receive this message by calling [**WTSRegisterSessionNotification**](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification).</span></span>

<span data-ttu-id="6641e-144">Entre los ejemplos de cómo las aplicaciones pueden responder a este mensaje se incluyen la liberación o adquisición de recursos específicos de la consola, la determinación del modo de pintar una pantalla o la activación de los efectos de animación de la consola.</span><span class="sxs-lookup"><span data-stu-id="6641e-144">Examples of how applications can respond to this message include releasing or acquiring console-specific resources, determining how a screen is to be painted, or triggering console animation effects.</span></span>

## <a name="requirements"></a><span data-ttu-id="6641e-145">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6641e-145">Requirements</span></span>



| <span data-ttu-id="6641e-146">Requisito</span><span class="sxs-lookup"><span data-stu-id="6641e-146">Requirement</span></span> | <span data-ttu-id="6641e-147">Value</span><span class="sxs-lookup"><span data-stu-id="6641e-147">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6641e-148">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6641e-148">Minimum supported client</span></span><br/> | <span data-ttu-id="6641e-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6641e-149">Windows Vista</span></span><br/>                                                                                 |
| <span data-ttu-id="6641e-150">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6641e-150">Minimum supported server</span></span><br/> | <span data-ttu-id="6641e-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6641e-151">Windows Server 2008</span></span><br/>                                                                           |
| <span data-ttu-id="6641e-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6641e-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="6641e-153"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6641e-153"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6641e-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="6641e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6641e-155">**WTSRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="6641e-155">**WTSRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsregistersessionnotification)
</dt> <dt>

[<span data-ttu-id="6641e-156">**WTSUnRegisterSessionNotification**</span><span class="sxs-lookup"><span data-stu-id="6641e-156">**WTSUnRegisterSessionNotification**</span></span>](/windows/desktop/api/Wtsapi32/nf-wtsapi32-wtsunregistersessionnotification)
</dt> </dl>

 

