---
title: Mensaje de WM_SYSKEYDOWN (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla.
ms.assetid: a3c03dbf-1be7-49ff-b931-1981786b74ce
keywords:
- Entrada de mouse y teclado de mensaje de WM_SYSKEYDOWN
topic_type:
- apiref
api_name:
- WM_SYSKEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3053c5933a0388e3c8522b0d7201b491aaa4fa2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695939"
---
# <a name="wm_syskeydown-message"></a><span data-ttu-id="965cb-104">Mensaje de SYSKEYDOWN de WM \_</span><span class="sxs-lookup"><span data-stu-id="965cb-104">WM\_SYSKEYDOWN message</span></span>

<span data-ttu-id="965cb-105">Se envía a la ventana con el foco de teclado cuando el usuario presiona la tecla F10 (que activa la barra de menús) o mantiene presionada la tecla ALT y, a continuación, presiona otra tecla.</span><span class="sxs-lookup"><span data-stu-id="965cb-105">Posted to the window with the keyboard focus when the user presses the F10 key (which activates the menu bar) or holds down the ALT key and then presses another key.</span></span> <span data-ttu-id="965cb-106">También se produce cuando no hay ninguna ventana que tenga actualmente el foco de teclado; en este caso, el mensaje de **\_ SYSKEYDOWN de WM** se envía a la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="965cb-106">It also occurs when no window currently has the keyboard focus; in this case, the **WM\_SYSKEYDOWN** message is sent to the active window.</span></span> <span data-ttu-id="965cb-107">La ventana que recibe el mensaje puede distinguir entre estos dos contextos comprobando el código de contexto en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="965cb-107">The window that receives the message can distinguish between these two contexts by checking the context code in the *lParam* parameter.</span></span>


```C++
#define WM_SYSKEYDOWN                   0x0104
```



## <a name="parameters"></a><span data-ttu-id="965cb-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="965cb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="965cb-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="965cb-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="965cb-110">Código de tecla virtual de la tecla que se va a presionar.</span><span class="sxs-lookup"><span data-stu-id="965cb-110">The virtual-key code of the key being pressed.</span></span> <span data-ttu-id="965cb-111">Consulte [**códigos de tecla virtual**](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="965cb-111">See [**Virtual-Key Codes**](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="965cb-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="965cb-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="965cb-113">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="965cb-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="965cb-114">Bits</span><span class="sxs-lookup"><span data-stu-id="965cb-114">Bits</span></span>  | <span data-ttu-id="965cb-115">Significado</span><span class="sxs-lookup"><span data-stu-id="965cb-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965cb-116">0-15</span><span class="sxs-lookup"><span data-stu-id="965cb-116">0-15</span></span>  | <span data-ttu-id="965cb-117">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="965cb-117">The repeat count for the current message.</span></span> <span data-ttu-id="965cb-118">El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="965cb-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="965cb-119">Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="965cb-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="965cb-120">Sin embargo, el número de repeticiones no es acumulativo.</span><span class="sxs-lookup"><span data-stu-id="965cb-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="965cb-121">16-23</span><span class="sxs-lookup"><span data-stu-id="965cb-121">16-23</span></span> | <span data-ttu-id="965cb-122">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="965cb-122">The scan code.</span></span> <span data-ttu-id="965cb-123">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="965cb-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="965cb-124">24</span><span class="sxs-lookup"><span data-stu-id="965cb-124">24</span></span>    | <span data-ttu-id="965cb-125">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="965cb-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="965cb-126">El valor es 1 si es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="965cb-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="965cb-127">25-28</span><span class="sxs-lookup"><span data-stu-id="965cb-127">25-28</span></span> | <span data-ttu-id="965cb-128">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="965cb-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="965cb-129">29</span><span class="sxs-lookup"><span data-stu-id="965cb-129">29</span></span>    | <span data-ttu-id="965cb-130">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="965cb-130">The context code.</span></span> <span data-ttu-id="965cb-131">El valor es 1 si la tecla ALT está presionada mientras se presiona la tecla; es 0 si el mensaje **de \_ SYSKEYDOWN de WM** se envía a la ventana activa porque ninguna ventana tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="965cb-131">The value is 1 if the ALT key is down while the key is pressed; it is 0 if the **WM\_SYSKEYDOWN** message is posted to the active window because no window has the keyboard focus.</span></span>                                                                  |
| <span data-ttu-id="965cb-132">30</span><span class="sxs-lookup"><span data-stu-id="965cb-132">30</span></span>    | <span data-ttu-id="965cb-133">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="965cb-133">The previous key state.</span></span> <span data-ttu-id="965cb-134">El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.</span><span class="sxs-lookup"><span data-stu-id="965cb-134">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="965cb-135">31</span><span class="sxs-lookup"><span data-stu-id="965cb-135">31</span></span>    | <span data-ttu-id="965cb-136">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="965cb-136">The transition state.</span></span> <span data-ttu-id="965cb-137">El valor es siempre 0 para un mensaje de **\_ SYSKEYDOWN de WM** .</span><span class="sxs-lookup"><span data-stu-id="965cb-137">The value is always 0 for a **WM\_SYSKEYDOWN** message.</span></span>                                                                                                                                                                                         |

<span data-ttu-id="965cb-138">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="965cb-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="965cb-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="965cb-139">Return value</span></span>

<span data-ttu-id="965cb-140">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="965cb-140">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="965cb-141">Observaciones</span><span class="sxs-lookup"><span data-stu-id="965cb-141">Remarks</span></span>

<span data-ttu-id="965cb-142">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) examina la clave especificada y genera un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) si la clave es TAB o entrar.</span><span class="sxs-lookup"><span data-stu-id="965cb-142">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function examines the specified key and generates a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message if the key is either TAB or ENTER.</span></span>

<span data-ttu-id="965cb-143">Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) , que lo controlará como si fuera un mensaje de clave normal en lugar de un mensaje de clave de caracteres.</span><span class="sxs-lookup"><span data-stu-id="965cb-143">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a normal key message instead of a character-key message.</span></span> <span data-ttu-id="965cb-144">Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="965cb-144">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="965cb-145">Debido a la repetición automática, se puede producir más de un mensaje de **WM \_ SYSKEYDOWN** antes de que se envíe un mensaje de [**\_ SYSKEYUP de WM**](wm-syskeyup.md) .</span><span class="sxs-lookup"><span data-stu-id="965cb-145">Because of automatic repeat, more than one **WM\_SYSKEYDOWN** message may occur before a [**WM\_SYSKEYUP**](wm-syskeyup.md) message is sent.</span></span> <span data-ttu-id="965cb-146">El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje de **\_ SYSKEYDOWN de WM** indica la primera transición hacia abajo o una transición hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="965cb-146">The previous key state (bit 30) can be used to determine whether the **WM\_SYSKEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="965cb-147">Para los teclados mejorados de la clave 101-y 102, las teclas mejoradas son las teclas ALT y CTRL adecuadas en la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="965cb-147">For enhanced 101- and 102-key keyboards, enhanced keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="965cb-148">Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="965cb-148">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="965cb-149">Este mensaje también se envía cuando el usuario presiona la tecla F10 sin la tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="965cb-149">This message is also sent whenever the user presses the F10 key without the ALT key.</span></span>

## <a name="requirements"></a><span data-ttu-id="965cb-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="965cb-150">Requirements</span></span>



| <span data-ttu-id="965cb-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="965cb-151">Requirement</span></span> | <span data-ttu-id="965cb-152">Value</span><span class="sxs-lookup"><span data-stu-id="965cb-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="965cb-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="965cb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="965cb-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="965cb-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="965cb-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="965cb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="965cb-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="965cb-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="965cb-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="965cb-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="965cb-158"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="965cb-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="965cb-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="965cb-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="965cb-160">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="965cb-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="965cb-161">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="965cb-161">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="965cb-162">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="965cb-162">**TranslateAccelerator**</span></span>](/windows/desktop/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="965cb-163">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="965cb-163">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

[<span data-ttu-id="965cb-164">**SYSKEYUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="965cb-164">**WM\_SYSKEYUP**</span></span>](wm-syskeyup.md)
</dt> <dt>

<span data-ttu-id="965cb-165">**Vista**</span><span class="sxs-lookup"><span data-stu-id="965cb-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="965cb-166">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="965cb-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

