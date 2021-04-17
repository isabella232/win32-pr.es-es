---
description: Se envía a una aplicación cuando un usuario cancela las actividades de registro en diario de la aplicación. El mensaje se envía con un identificador de ventana nulo.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Mensaje de WM_CANCELJOURNAL (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706677"
---
# <a name="wm_canceljournal-message"></a><span data-ttu-id="6b2b9-104">Mensaje de CANCELJOURNAL de WM \_</span><span class="sxs-lookup"><span data-stu-id="6b2b9-104">WM\_CANCELJOURNAL message</span></span>

<span data-ttu-id="6b2b9-105">Se envía a una aplicación cuando un usuario cancela las actividades de registro en diario de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-105">Posted to an application when a user cancels the application's journaling activities.</span></span> <span data-ttu-id="6b2b9-106">El mensaje se envía con un identificador de ventana **nulo** .</span><span class="sxs-lookup"><span data-stu-id="6b2b9-106">The message is posted with a **NULL** window handle.</span></span>


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a><span data-ttu-id="6b2b9-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6b2b9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b2b9-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b2b9-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b2b9-109">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-109">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="6b2b9-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b2b9-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b2b9-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b2b9-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6b2b9-112">Return value</span></span>

<span data-ttu-id="6b2b9-113">Tipo: **void**</span><span class="sxs-lookup"><span data-stu-id="6b2b9-113">Type: **void**</span></span>

<span data-ttu-id="6b2b9-114">Este mensaje no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-114">This message does not return a value.</span></span> <span data-ttu-id="6b2b9-115">Está pensada para ser procesada desde el bucle principal de una aplicación o un procedimiento de enlace [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , no desde un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-115">It is meant to be processed from within an application's main loop or a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) hook procedure, not from a window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b2b9-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6b2b9-116">Remarks</span></span>

<span data-ttu-id="6b2b9-117">Los modos de reproducción y registro del diario son modos impuestos en el sistema que permiten a una aplicación grabar o reproducir de forma secuencial datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-117">Journal record and playback modes are modes imposed on the system that let an application sequentially record or play back user input.</span></span> <span data-ttu-id="6b2b9-118">El sistema entra en estos modos cuando una aplicación instala un procedimiento de enlace [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) o [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6b2b9-118">The system enters these modes when an application installs a [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) or [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) hook procedure.</span></span> <span data-ttu-id="6b2b9-119">Cuando el sistema se encuentra en cualquiera de estos modos de registro en diario, las aplicaciones deben realizar la lectura de la entrada de la cola de entrada.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-119">When the system is in either of these journaling modes, applications must take turns reading input from the input queue.</span></span> <span data-ttu-id="6b2b9-120">Si una aplicación deja de leer la entrada mientras el sistema está en un modo de registro en diario, se fuerza a otras aplicaciones a esperar.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-120">If any one application stops reading input while the system is in a journaling mode, other applications are forced to wait.</span></span>

<span data-ttu-id="6b2b9-121">Para garantizar un sistema sólido, uno que no puede dejar de responder a ninguna aplicación, el sistema cancela automáticamente las actividades de registro en diario cuando un usuario presiona CTRL + ESC o CTRL + ALT + SUPR.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-121">To ensure a robust system, one that cannot be made unresponsive by any one application, the system automatically cancels any journaling activities when a user presses CTRL+ESC or CTRL+ALT+DEL.</span></span> <span data-ttu-id="6b2b9-122">Después, el sistema desenlaza los procedimientos de enlace de registro en diario y envía un mensaje de **WM \_ CANCELJOURNAL** , con un identificador de ventana **nulo** , a la aplicación que establece el enlace de registro en diario.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-122">The system then unhooks any journaling hook procedures, and posts a **WM\_CANCELJOURNAL** message, with a **NULL** window handle, to the application that set the journaling hook.</span></span>

<span data-ttu-id="6b2b9-123">El mensaje de **\_ CANCELJOURNAL de WM** tiene un identificador de ventana **nulo** , por lo que no se puede enviar a un procedimiento de ventana.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-123">The **WM\_CANCELJOURNAL** message has a **NULL** window handle, therefore it cannot be dispatched to a window procedure.</span></span> <span data-ttu-id="6b2b9-124">Hay dos maneras de que una aplicación vea un mensaje **de \_ CANCELJOURNAL de WM** : Si la aplicación se ejecuta en su propio bucle principal, debe detectar el mensaje entre su llamada a [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) o [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) y su llamada a [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span><span class="sxs-lookup"><span data-stu-id="6b2b9-124">There are two ways for an application to see a **WM\_CANCELJOURNAL** message: If the application is running in its own main loop, it must catch the message between its call to [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) or [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) and its call to [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage).</span></span> <span data-ttu-id="6b2b9-125">Si la aplicación no se ejecuta en su propio bucle principal, debe establecer un procedimiento de enlace [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (a través de una llamada a [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) que especifique el tipo de enlace de **\_ GETMESSAGE** ) que inspecciona el mensaje.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-125">If the application is not running in its own main loop, it must set a [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) hook procedure (through a call to [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) specifying the **WH\_GETMESSAGE** hook type) that watches for the message.</span></span>

<span data-ttu-id="6b2b9-126">Cuando una aplicación ve un mensaje de **\_ CANCELJOURNAL de WM** , puede suponer dos cosas: el usuario canceló intencionadamente el registro del diario o el modo de reproducción, y el sistema ya ha desenlazado los procedimientos de registro del diario o del enlace de reproducción.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-126">When an application sees a **WM\_CANCELJOURNAL** message, it can assume two things: the user has intentionally canceled the journal record or playback mode, and the system has already unhooked any journal record or playback hook procedures.</span></span>

<span data-ttu-id="6b2b9-127">Tenga en cuenta que las combinaciones de teclas mencionadas anteriormente (CTRL + ESC o CTRL + ALT + Supr) hacen que el sistema cancele el registro en diario.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-127">Note that the key combinations mentioned above (CTRL+ESC or CTRL+ALT+DEL) cause the system to cancel journaling.</span></span> <span data-ttu-id="6b2b9-128">Si una aplicación deja de responder, proporciona al usuario un medio de recuperación.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-128">If any one application is made unresponsive, they give the user a means of recovery.</span></span> <span data-ttu-id="6b2b9-129">El código de la clave virtual de [**\_ cancelación de VK**](../inputdev/virtual-key-codes.md) (normalmente implementado como combinación de teclas Ctrl + Inter) es lo que una aplicación que está en modo de registro de diario debe supervisar como una señal de que el usuario desea cancelar la actividad de diario.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-129">The [**VK\_CANCEL**](../inputdev/virtual-key-codes.md) virtual key code (usually implemented as the CTRL+BREAK key combination) is what an application that is in journal record mode should watch for as a signal that the user wishes to cancel the journaling activity.</span></span> <span data-ttu-id="6b2b9-130">La diferencia es que supervisar la **\_ cancelación de VK** es un comportamiento sugerido para las aplicaciones de registro en diario, mientras que Ctrl + ESC o Ctrl + Alt + Supr hacen que el sistema cancele el registro en diario, independientemente del comportamiento de la aplicación de registro en diario.</span><span class="sxs-lookup"><span data-stu-id="6b2b9-130">The difference is that watching for **VK\_CANCEL** is a suggested behavior for journaling applications, whereas CTRL+ESC or CTRL+ALT+DEL cause the system to cancel journaling regardless of a journaling application's behavior.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b2b9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6b2b9-131">Requirements</span></span>



| <span data-ttu-id="6b2b9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b2b9-132">Requirement</span></span> | <span data-ttu-id="6b2b9-133">Value</span><span class="sxs-lookup"><span data-stu-id="6b2b9-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b2b9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b2b9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6b2b9-135">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6b2b9-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6b2b9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6b2b9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6b2b9-137">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6b2b9-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6b2b9-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6b2b9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b2b9-139"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6b2b9-139"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b2b9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="6b2b9-140">See also</span></span>

<dl> <dt>

<span data-ttu-id="6b2b9-141">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6b2b9-141">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="6b2b9-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b2b9-142">[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6b2b9-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b2b9-143">[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="6b2b9-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="6b2b9-144">[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="6b2b9-145">**SetWindowsHookEx**</span><span class="sxs-lookup"><span data-stu-id="6b2b9-145">**SetWindowsHookEx**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

<span data-ttu-id="6b2b9-146">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6b2b9-146">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6b2b9-147">Enlaces</span><span class="sxs-lookup"><span data-stu-id="6b2b9-147">Hooks</span></span>](hooks.md)
</dt> </dl>

 

 
