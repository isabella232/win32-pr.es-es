---
title: Mensaje de WM_KEYUP (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando se suelta una tecla que no es del sistema. Una clave no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT o una tecla del teclado presionada cuando una ventana tiene el foco de teclado.
ms.assetid: 67d9d82d-fab0-4aec-a337-7a9cb2b0b586
keywords:
- Entrada de mouse y teclado de mensaje de WM_KEYUP
topic_type:
- apiref
api_name:
- WM_KEYUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28aa02dd73f1706bb12ae30825f50241be7bb0d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422193"
---
# <a name="wm_keyup-message"></a><span data-ttu-id="f5aed-105">\_Mensaje KEYUP de WM</span><span class="sxs-lookup"><span data-stu-id="f5aed-105">WM\_KEYUP message</span></span>

<span data-ttu-id="f5aed-106">Se envía a la ventana con el foco de teclado cuando se suelta una tecla que no es del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5aed-106">Posted to the window with the keyboard focus when a nonsystem key is released.</span></span> <span data-ttu-id="f5aed-107">Una clave no del sistema es una tecla que se presiona cuando *no* se presiona la tecla Alt o una tecla del teclado presionada cuando una ventana tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="f5aed-107">A nonsystem key is a key that is pressed when the ALT key is *not* pressed, or a keyboard key that is pressed when a window has the keyboard focus.</span></span>


```C++
#define WM_KEYUP                        0x0101
```



## <a name="parameters"></a><span data-ttu-id="f5aed-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f5aed-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5aed-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f5aed-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5aed-110">Código de tecla virtual de la clave que no es del sistema.</span><span class="sxs-lookup"><span data-stu-id="f5aed-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="f5aed-111">Consulte [códigos de tecla virtual](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="f5aed-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="f5aed-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f5aed-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f5aed-113">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f5aed-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="f5aed-114">Bits</span><span class="sxs-lookup"><span data-stu-id="f5aed-114">Bits</span></span>  | <span data-ttu-id="f5aed-115">Significado</span><span class="sxs-lookup"><span data-stu-id="f5aed-115">Meaning</span></span>                                                                                                                                                                                                          |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aed-116">0-15</span><span class="sxs-lookup"><span data-stu-id="f5aed-116">0-15</span></span>  | <span data-ttu-id="f5aed-117">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="f5aed-117">The repeat count for the current message.</span></span> <span data-ttu-id="f5aed-118">El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="f5aed-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="f5aed-119">El número de repeticiones es siempre 1 para un mensaje de **\_ KEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="f5aed-119">The repeat count is always 1 for a **WM\_KEYUP** message.</span></span> |
| <span data-ttu-id="f5aed-120">16-23</span><span class="sxs-lookup"><span data-stu-id="f5aed-120">16-23</span></span> | <span data-ttu-id="f5aed-121">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="f5aed-121">The scan code.</span></span> <span data-ttu-id="f5aed-122">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="f5aed-122">The value depends on the OEM.</span></span>                                                                                                                                                                     |
| <span data-ttu-id="f5aed-123">24</span><span class="sxs-lookup"><span data-stu-id="f5aed-123">24</span></span>    | <span data-ttu-id="f5aed-124">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="f5aed-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="f5aed-125">El valor es 1 si es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="f5aed-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>         |
| <span data-ttu-id="f5aed-126">25-28</span><span class="sxs-lookup"><span data-stu-id="f5aed-126">25-28</span></span> | <span data-ttu-id="f5aed-127">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="f5aed-127">Reserved; do not use.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="f5aed-128">29</span><span class="sxs-lookup"><span data-stu-id="f5aed-128">29</span></span>    | <span data-ttu-id="f5aed-129">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="f5aed-129">The context code.</span></span> <span data-ttu-id="f5aed-130">El valor siempre es 0 para un mensaje de **\_ KEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="f5aed-130">The value is always 0 for a **WM\_KEYUP** message.</span></span>                                                                                                                                             |
| <span data-ttu-id="f5aed-131">30</span><span class="sxs-lookup"><span data-stu-id="f5aed-131">30</span></span>    | <span data-ttu-id="f5aed-132">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="f5aed-132">The previous key state.</span></span> <span data-ttu-id="f5aed-133">El valor es siempre 1 para un mensaje de **\_ KEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="f5aed-133">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                       |
| <span data-ttu-id="f5aed-134">31</span><span class="sxs-lookup"><span data-stu-id="f5aed-134">31</span></span>    | <span data-ttu-id="f5aed-135">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="f5aed-135">The transition state.</span></span> <span data-ttu-id="f5aed-136">El valor es siempre 1 para un mensaje de **\_ KEYUP de WM** .</span><span class="sxs-lookup"><span data-stu-id="f5aed-136">The value is always 1 for a **WM\_KEYUP** message.</span></span>                                                                                                                                         |

<span data-ttu-id="f5aed-137">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="f5aed-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5aed-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f5aed-138">Return value</span></span>

<span data-ttu-id="f5aed-139">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="f5aed-139">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5aed-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f5aed-140">Remarks</span></span>

<span data-ttu-id="f5aed-141">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana de nivel superior si se liberó la tecla F10 o la tecla Alt.</span><span class="sxs-lookup"><span data-stu-id="f5aed-141">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window if the F10 key or the ALT key was released.</span></span> <span data-ttu-id="f5aed-142">El parámetro *wParam* del mensaje se establece en SC \_ KEYMENU.</span><span class="sxs-lookup"><span data-stu-id="f5aed-142">The *wParam* parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="f5aed-143">Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="f5aed-143">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="f5aed-144">Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="f5aed-144">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="f5aed-145">Las aplicaciones deben pasar *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sin modificarlo.</span><span class="sxs-lookup"><span data-stu-id="f5aed-145">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5aed-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f5aed-146">Requirements</span></span>



| <span data-ttu-id="f5aed-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5aed-147">Requirement</span></span> | <span data-ttu-id="f5aed-148">Value</span><span class="sxs-lookup"><span data-stu-id="f5aed-148">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5aed-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5aed-149">Minimum supported client</span></span><br/> | <span data-ttu-id="f5aed-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f5aed-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f5aed-151">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f5aed-151">Minimum supported server</span></span><br/> | <span data-ttu-id="f5aed-152">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f5aed-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f5aed-153">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f5aed-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="f5aed-154"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5aed-154"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5aed-155">Vea también</span><span class="sxs-lookup"><span data-stu-id="f5aed-155">See also</span></span>

<dl> <dt>

<span data-ttu-id="f5aed-156">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f5aed-156">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f5aed-157">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="f5aed-157">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="f5aed-158">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="f5aed-158">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="f5aed-159">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f5aed-159">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="f5aed-160">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f5aed-160">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="f5aed-161">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f5aed-161">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f5aed-162">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="f5aed-162">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

