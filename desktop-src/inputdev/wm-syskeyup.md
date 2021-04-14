---
title: Mensaje de WM_SYSKEYUP (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando el usuario suelta una tecla que se presionó mientras se mantenía presionada la tecla ALT.
ms.assetid: a4f62575-fb84-4390-a1d1-1a62629de55f
keywords:
- Entrada de mouse y teclado de mensaje de WM_SYSKEYUP
topic_type:
- apiref
api_name:
- WM_SYSKEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2139c11558eccc3fb3b225f0cc1a87bcf6fb084d
ms.sourcegitcommit: cea2889abb43350c38cd120e877d8471dae78beb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362010"
---
# <a name="wm_syskeyup-message"></a><span data-ttu-id="5e139-104">Mensaje de SYSKEYUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="5e139-104">WM\_SYSKEYUP message</span></span>

<span data-ttu-id="5e139-105">Se envía a la ventana con el foco de teclado cuando el usuario suelta una tecla que se presionó mientras se mantenía presionada la tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="5e139-105">Posted to the window with the keyboard focus when the user releases a key that was pressed while the ALT key was held down.</span></span> <span data-ttu-id="5e139-106">También se produce cuando no hay ninguna ventana que tenga actualmente el foco de teclado; en este caso, el mensaje de **\_ SYSKEYUP de WM** se envía a la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="5e139-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYUP** message is sent to the active window.</span></span> <span data-ttu-id="5e139-107">La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5e139-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>

<span data-ttu-id="5e139-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5e139-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SYSKEYUP                     0x0105
```



## <a name="parameters"></a><span data-ttu-id="5e139-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5e139-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e139-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e139-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e139-111">Código de tecla virtual de la clave que se va a liberar.</span><span class="sxs-lookup"><span data-stu-id="5e139-111">The virtual-key code of the key being released.</span></span> <span data-ttu-id="5e139-112">Consulte [**códigos de tecla virtual**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="5e139-112">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="5e139-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e139-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e139-114">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="5e139-114">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="5e139-115">Bits</span><span class="sxs-lookup"><span data-stu-id="5e139-115">Bits</span></span>  | <span data-ttu-id="5e139-116">Significado</span><span class="sxs-lookup"><span data-stu-id="5e139-116">Meaning</span></span>                                                                                                                                                                                                                       |
|-------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e139-117">0-15</span><span class="sxs-lookup"><span data-stu-id="5e139-117">0-15</span></span>  | <span data-ttu-id="5e139-118">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="5e139-118">The repeat count for the current message.</span></span> <span data-ttu-id="5e139-119">El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="5e139-119">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="5e139-120">El número de repeticiones siempre es uno para un mensaje de **\_ SYSKEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="5e139-120">The repeat count is always one for a **WM\_SYSKEYUP** message.</span></span>         |
| <span data-ttu-id="5e139-121">16-23</span><span class="sxs-lookup"><span data-stu-id="5e139-121">16-23</span></span> | <span data-ttu-id="5e139-122">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="5e139-122">The scan code.</span></span> <span data-ttu-id="5e139-123">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="5e139-123">The value depends on the OEM.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="5e139-124">24</span><span class="sxs-lookup"><span data-stu-id="5e139-124">24</span></span>    | <span data-ttu-id="5e139-125">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="5e139-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="5e139-126">El valor es 1 si es una clave extendida; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="5e139-126">The value is 1 if it is an extended key; otherwise, it is zero.</span></span>                   |
| <span data-ttu-id="5e139-127">25-28</span><span class="sxs-lookup"><span data-stu-id="5e139-127">25-28</span></span> | <span data-ttu-id="5e139-128">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="5e139-128">Reserved; do not use.</span></span>                                                                                                                                                                                                         |
| <span data-ttu-id="5e139-129">29</span><span class="sxs-lookup"><span data-stu-id="5e139-129">29</span></span>    | <span data-ttu-id="5e139-130">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="5e139-130">The context code.</span></span> <span data-ttu-id="5e139-131">El valor es 1 si la tecla ALT está presionada mientras se suelta la tecla; es cero si el mensaje **de \_ SYSKEYUP de WM** se envía a la ventana activa porque ninguna ventana tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="5e139-131">The value is 1 if the ALT key is down while the key is released; it is zero if the **WM\_SYSKEYUP** message is posted to the active window because no window has the keyboard focus.</span></span> |
| <span data-ttu-id="5e139-132">30</span><span class="sxs-lookup"><span data-stu-id="5e139-132">30</span></span>    | <span data-ttu-id="5e139-133">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="5e139-133">The previous key state.</span></span> <span data-ttu-id="5e139-134">El valor es siempre 1 para un mensaje de **\_ SYSKEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="5e139-134">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                 |
| <span data-ttu-id="5e139-135">31</span><span class="sxs-lookup"><span data-stu-id="5e139-135">31</span></span>    | <span data-ttu-id="5e139-136">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="5e139-136">The transition state.</span></span> <span data-ttu-id="5e139-137">El valor es siempre 1 para un mensaje de **\_ SYSKEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="5e139-137">The value is always 1 for a **WM\_SYSKEYUP** message.</span></span>                                                                                                                                                   |

<span data-ttu-id="5e139-138">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="5e139-138">For more details, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e139-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5e139-139">Return value</span></span>

<span data-ttu-id="5e139-140">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="5e139-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e139-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5e139-141">Remarks</span></span>

<span data-ttu-id="5e139-142">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana de nivel superior si se liberó la tecla F10 o la tecla Alt.</span><span class="sxs-lookup"><span data-stu-id="5e139-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="5e139-143">El parámetro *wParam* del mensaje se establece en **SC \_ KEYMENU**.</span><span class="sxs-lookup"><span data-stu-id="5e139-143">The *wParam* parameter of the message is set to **SC\_KEYMENU**.</span></span>

<span data-ttu-id="5e139-144">Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres.</span><span class="sxs-lookup"><span data-stu-id="5e139-144">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="5e139-145">Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="5e139-145">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="5e139-146">Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="5e139-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="5e139-147">Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="5e139-147">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="5e139-148">Para los que no son de U. S. Teclados de clave mejorada 102, la tecla ALT derecha se trata como una tecla CTRL + ALT.</span><span class="sxs-lookup"><span data-stu-id="5e139-148">For non-U.S. enhanced 102-key keyboards, the right ALT key is handled as a CTRL+ALT key.</span></span> <span data-ttu-id="5e139-149">En la tabla siguiente se muestra la secuencia de mensajes que se produce cuando el usuario presiona y suelta esta clave.</span><span class="sxs-lookup"><span data-stu-id="5e139-149">The following table shows the sequence of messages that result when the user presses and releases this key.</span></span>



| <span data-ttu-id="5e139-150">Message</span><span class="sxs-lookup"><span data-stu-id="5e139-150">Message</span></span>                           | <span data-ttu-id="5e139-151">Código de tecla virtual</span><span class="sxs-lookup"><span data-stu-id="5e139-151">Virtual-key code</span></span> |
|-----------------------------------|------------------|
| [<span data-ttu-id="5e139-152">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e139-152">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="5e139-153">**\_control VK**</span><span class="sxs-lookup"><span data-stu-id="5e139-153">**VK\_CONTROL**</span></span>  |
| [<span data-ttu-id="5e139-154">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e139-154">**WM\_KEYDOWN**</span></span>](wm-keydown.md) | <span data-ttu-id="5e139-155">**\_menú VK**</span><span class="sxs-lookup"><span data-stu-id="5e139-155">**VK\_MENU**</span></span>     |
| [<span data-ttu-id="5e139-156">**KEYUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e139-156">**WM\_KEYUP**</span></span>](wm-keyup.md)     | <span data-ttu-id="5e139-157">**\_control VK**</span><span class="sxs-lookup"><span data-stu-id="5e139-157">**VK\_CONTROL**</span></span>  |
| <span data-ttu-id="5e139-158">**SYSKEYUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e139-158">**WM\_SYSKEYUP**</span></span>                  | <span data-ttu-id="5e139-159">**\_menú VK**</span><span class="sxs-lookup"><span data-stu-id="5e139-159">**VK\_MENU**</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="5e139-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5e139-160">Requirements</span></span>



| <span data-ttu-id="5e139-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="5e139-161">Requirement</span></span> | <span data-ttu-id="5e139-162">Value</span><span class="sxs-lookup"><span data-stu-id="5e139-162">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e139-163">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e139-163">Minimum supported client</span></span><br/> | <span data-ttu-id="5e139-164">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5e139-164">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5e139-165">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5e139-165">Minimum supported server</span></span><br/> | <span data-ttu-id="5e139-166">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5e139-166">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e139-167">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5e139-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e139-168"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5e139-168"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e139-169">Vea también</span><span class="sxs-lookup"><span data-stu-id="5e139-169">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e139-170">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5e139-170">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5e139-171">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5e139-171">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5e139-172">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="5e139-172">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="5e139-173">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e139-173">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="5e139-174">**SYSKEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5e139-174">**WM\_SYSKEYDOWN**</span></span>](wm-syskeydown.md)
</dt> <dt>

<span data-ttu-id="5e139-175">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5e139-175">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5e139-176">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="5e139-176">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

