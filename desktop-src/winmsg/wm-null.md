---
description: No realiza ninguna operación. Una aplicación envía el mensaje de WM \_ null si desea publicar un mensaje que la ventana de destinatario omitirá.
ms.assetid: edbcfba6-7b79-4d53-84e3-2e4227e17369
title: Mensaje de WM_NULL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b445e13200bdeb2947e4d8fd363a1a39f0c86db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276849"
---
# <a name="wm_null-message"></a><span data-ttu-id="b02e9-104">\_Mensaje null de WM</span><span class="sxs-lookup"><span data-stu-id="b02e9-104">WM\_NULL message</span></span>

<span data-ttu-id="b02e9-105">No realiza ninguna operación.</span><span class="sxs-lookup"><span data-stu-id="b02e9-105">Performs no operation.</span></span> <span data-ttu-id="b02e9-106">Una aplicación envía el mensaje de **WM \_ null** si desea publicar un mensaje que la ventana de destinatario omitirá.</span><span class="sxs-lookup"><span data-stu-id="b02e9-106">An application sends the **WM\_NULL** message if it wants to post a message that the recipient window will ignore.</span></span>

<span data-ttu-id="b02e9-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="b02e9-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NULL                         0x0000
```



## <a name="parameters"></a><span data-ttu-id="b02e9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b02e9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b02e9-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b02e9-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b02e9-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b02e9-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="b02e9-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b02e9-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b02e9-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b02e9-112">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b02e9-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b02e9-113">Return value</span></span>

<span data-ttu-id="b02e9-114">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="b02e9-114">Type: **LRESULT**</span></span>

<span data-ttu-id="b02e9-115">Una aplicación devuelve cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b02e9-115">An application returns zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b02e9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b02e9-116">Remarks</span></span>

<span data-ttu-id="b02e9-117">Por ejemplo, si una aplicación ha instalado un enlace **qu \_ GETMESSAGE** y desea evitar que se procese un mensaje, la función de devolución de llamada [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) puede cambiar el número de mensaje a **WM \_ null** para que el destinatario lo ignore.</span><span class="sxs-lookup"><span data-stu-id="b02e9-117">For example, if an application has installed a **WH\_GETMESSAGE** hook and wants to prevent a message from being processed, the [**GetMsgProc**](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) callback function can change the message number to **WM\_NULL** so the recipient will ignore it.</span></span>

<span data-ttu-id="b02e9-118">Otro ejemplo: una aplicación puede comprobar si una ventana responde a los mensajes enviando el mensaje de **WM \_ null** con la función [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) .</span><span class="sxs-lookup"><span data-stu-id="b02e9-118">As another example, an application can check if a window is responding to messages by sending the **WM\_NULL** message with the [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b02e9-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b02e9-119">Requirements</span></span>



| <span data-ttu-id="b02e9-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="b02e9-120">Requirement</span></span> | <span data-ttu-id="b02e9-121">Value</span><span class="sxs-lookup"><span data-stu-id="b02e9-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b02e9-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b02e9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="b02e9-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b02e9-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b02e9-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b02e9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="b02e9-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b02e9-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b02e9-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b02e9-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="b02e9-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b02e9-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b02e9-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="b02e9-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02e9-129">Información general de Windows</span><span class="sxs-lookup"><span data-stu-id="b02e9-129">Windows Overview</span></span>](windows.md)
</dt> </dl>

 

 
