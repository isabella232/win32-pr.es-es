---
title: Mensaje de WM_NOTIFY (Winuser. h)
description: Lo envía un control común a su ventana primaria cuando se ha producido un evento o el control requiere cierta información.
ms.assetid: vs|controls|~\controls\common\messages\wm_notify.htm
keywords:
- WM_NOTIFY controles de mensajes de Windows
topic_type:
- apiref
api_name:
- WM_NOTIFY
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1905954e7fb164f8436216fa918cc6f243f4b17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996635"
---
# <a name="wm_notify-message"></a><span data-ttu-id="800da-104">Mensaje de notificación de WM \_</span><span class="sxs-lookup"><span data-stu-id="800da-104">WM\_NOTIFY message</span></span>

<span data-ttu-id="800da-105">Lo envía un control común a su ventana primaria cuando se ha producido un evento o el control requiere cierta información.</span><span class="sxs-lookup"><span data-stu-id="800da-105">Sent by a common control to its parent window when an event has occurred or the control requires some information.</span></span>

## <a name="parameters"></a><span data-ttu-id="800da-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="800da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="800da-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="800da-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="800da-108">Identificador del control común que envía el mensaje.</span><span class="sxs-lookup"><span data-stu-id="800da-108">The identifier of the common control sending the message.</span></span> <span data-ttu-id="800da-109">No se garantiza que este identificador sea único.</span><span class="sxs-lookup"><span data-stu-id="800da-109">This identifier is not guaranteed to be unique.</span></span> <span data-ttu-id="800da-110">Una aplicación debe usar el miembro **hwndFrom** o **idFrom** de la estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) (pasada como el parámetro *lParam* ) para identificar el control.</span><span class="sxs-lookup"><span data-stu-id="800da-110">An application should use the **hwndFrom** or **idFrom** member of the [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure (passed as the *lParam* parameter) to identify the control.</span></span>

</dd> <dt>

<span data-ttu-id="800da-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="800da-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="800da-112">Puntero a una estructura [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) que contiene el código de notificación e información adicional.</span><span class="sxs-lookup"><span data-stu-id="800da-112">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains the notification code and additional information.</span></span> <span data-ttu-id="800da-113">En algunos mensajes de notificación, este parámetro apunta a una estructura más grande que tiene la estructura **NMHDR** como primer miembro.</span><span class="sxs-lookup"><span data-stu-id="800da-113">For some notification messages, this parameter points to a larger structure that has the **NMHDR** structure as its first member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="800da-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="800da-114">Return value</span></span>

<span data-ttu-id="800da-115">El valor devuelto se omite excepto para los mensajes de notificación que especifican lo contrario.</span><span class="sxs-lookup"><span data-stu-id="800da-115">The return value is ignored except for notification messages that specify otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="800da-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="800da-116">Remarks</span></span>

<span data-ttu-id="800da-117">El destino del mensaje debe ser el **hWnd** del elemento primario del control.</span><span class="sxs-lookup"><span data-stu-id="800da-117">The destination of the message must be the **HWND** of the parent of the control.</span></span> <span data-ttu-id="800da-118">Este valor se puede obtener mediante [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), tal como se muestra en el ejemplo siguiente, donde *m \_ controlHwnd* es el **hWnd** del propio control.</span><span class="sxs-lookup"><span data-stu-id="800da-118">This value can be obtained by using [**GetParent**](/windows/desktop/api/winuser/nf-winuser-getparent), as shown in the following example, where *m\_controlHwnd* is the **HWND** of the control itself.</span></span>


```
NMHDR nmh;
nmh.code = CUSTOM_SELCHANGE;    // Message type defined by control.
nmh.idFrom = GetDlgCtrlID(m_controlHwnd);
nmh.hwndFrom = m_controlHwnd;
SendMessage(GetParent(m_controlHwnd), 
    WM_NOTIFY, 
    nmh.idFrom, 
    (LPARAM)&nmh);
```



<span data-ttu-id="800da-119">Las aplicaciones controlan el mensaje en el procedimiento de ventana de la ventana primaria, como se muestra en el ejemplo siguiente, que controla el mensaje de notificación enviado por el control personalizado en el ejemplo anterior.</span><span class="sxs-lookup"><span data-stu-id="800da-119">Applications handle the message in the window procedure of the parent window, as shown in the following example, which handles the notification message sent by the custom control in the previous example.</span></span>


```
INT_PTR CALLBACK DlgProc(HWND hDlg, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
    case WM_NOTIFY:
        switch (((LPNMHDR)lParam)->code)
        {
        case CUSTOM_SELCHANGE:
            if (((LPNMHDR)lParam)->idFrom == IDC_CUSTOMLISTBOX1)
            {
                ...   // Respond to message.
                return TRUE;
            }
            break; 
        ... // More cases on WM_NOTIFY switch.
        break;
        }
    ...  // More cases on message switch.
    }
    return FALSE;
}
```



<span data-ttu-id="800da-120">Algunas notificaciones, principalmente las que han estado en la API durante mucho tiempo, se envían como mensajes de [**\_ comandos de WM**](/windows/desktop/menurc/wm-command) .</span><span class="sxs-lookup"><span data-stu-id="800da-120">Some notifications, chiefly those that have been in the API for a long time, are sent as [**WM\_COMMAND**](/windows/desktop/menurc/wm-command) messages.</span></span> <span data-ttu-id="800da-121">Para obtener más información, consulte [control de mensajes](control-messages.md).</span><span class="sxs-lookup"><span data-stu-id="800da-121">For more information, see [Control Messages](control-messages.md).</span></span>

<span data-ttu-id="800da-122">Si el controlador de mensajes está en un procedimiento de cuadro de diálogo, debe usar la función [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) con DWL \_ MSGRESULT para establecer un valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="800da-122">If the message handler is in a dialog box procedure, you must use the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with DWL\_MSGRESULT to set a return value.</span></span>

<span data-ttu-id="800da-123">En Windows Vista y sistemas posteriores, no se puede enviar el mensaje de **\_ notificación de WM** entre procesos.</span><span class="sxs-lookup"><span data-stu-id="800da-123">For Windows Vista and later systems, the **WM\_NOTIFY** message cannot be sent between processes.</span></span>

<span data-ttu-id="800da-124">Muchas notificaciones están disponibles en los formatos ANSI y Unicode.</span><span class="sxs-lookup"><span data-stu-id="800da-124">Many notifications are available in both ANSI and Unicode formats.</span></span> <span data-ttu-id="800da-125">La ventana que envía el mensaje de **\_ notificación de WM** usa el mensaje de [**\_ NOTIFYFORMAT de WM**](wm-notifyformat.md) para determinar qué formato se debe usar.</span><span class="sxs-lookup"><span data-stu-id="800da-125">The window sending the **WM\_NOTIFY** message uses the [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message to determine which format should be used.</span></span> <span data-ttu-id="800da-126">Consulte **WM \_ NOTIFYFORMAT** para más información.</span><span class="sxs-lookup"><span data-stu-id="800da-126">See **WM\_NOTIFYFORMAT** for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="800da-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="800da-127">Requirements</span></span>



| <span data-ttu-id="800da-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="800da-128">Requirement</span></span> | <span data-ttu-id="800da-129">Value</span><span class="sxs-lookup"><span data-stu-id="800da-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="800da-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="800da-130">Minimum supported client</span></span><br/> | <span data-ttu-id="800da-131">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="800da-131">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="800da-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="800da-132">Minimum supported server</span></span><br/> | <span data-ttu-id="800da-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="800da-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="800da-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="800da-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="800da-135"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="800da-135"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="800da-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="800da-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="800da-137">**NOTIFYFORMAT de WM \_**</span><span class="sxs-lookup"><span data-stu-id="800da-137">**WM\_NOTIFYFORMAT**</span></span>](wm-notifyformat.md)
</dt> </dl>

 

