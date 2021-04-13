---
title: Mensaje de WM_SYSCHAR (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando \_ la función TranslateMessage traduce un mensaje de SYSKEYDOWN de WM.
ms.assetid: 55987105-3c53-42e5-8fab-a3c9f2ca7273
keywords:
- WM_SYSCHAR menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_SYSCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d14d2f8829cfd199049d3a1b254065918393c18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535547"
---
# <a name="wm_syschar-message"></a><span data-ttu-id="1253b-104">Mensaje de SYSCHAR de WM \_</span><span class="sxs-lookup"><span data-stu-id="1253b-104">WM\_SYSCHAR message</span></span>

<span data-ttu-id="1253b-105">Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje de [**\_ SYSKEYDOWN de WM**](/windows/desktop/inputdev/wm-syskeydown) .</span><span class="sxs-lookup"><span data-stu-id="1253b-105">Posted to the window with the keyboard focus when a [**WM\_SYSKEYDOWN**](/windows/desktop/inputdev/wm-syskeydown) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="1253b-106">Especifica el código de carácter de una tecla de carácter del sistema, que es una tecla de carácter que se presiona mientras la tecla ALT está presionada.</span><span class="sxs-lookup"><span data-stu-id="1253b-106">It specifies the character code of a system character key   that is, a character key that is pressed while the ALT key is down.</span></span>


```C++
#define WM_SYSCHAR                      0x0106
```



## <a name="parameters"></a><span data-ttu-id="1253b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1253b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1253b-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1253b-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1253b-109">Código de carácter de la tecla de menú de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1253b-109">The character code of the window menu key.</span></span>

</dd> <dt>

<span data-ttu-id="1253b-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1253b-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1253b-111">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="1253b-111">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="1253b-112">Bits</span><span class="sxs-lookup"><span data-stu-id="1253b-112">Bits</span></span>                                                                             | <span data-ttu-id="1253b-113">Significado</span><span class="sxs-lookup"><span data-stu-id="1253b-113">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1253b-114"><dt>0 15</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-114"><dt>0 15</dt></span></span> </dl>  | <span data-ttu-id="1253b-115">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="1253b-115">The repeat count for the current message.</span></span> <span data-ttu-id="1253b-116">El valor es el número de veces que la pulsación de tecla se repitió automáticamente como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="1253b-116">The value is the number of times the keystroke was auto-repeated as a result of the user holding down the key.</span></span> <span data-ttu-id="1253b-117">Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="1253b-117">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="1253b-118">Sin embargo, el número de repeticiones no es acumulativo.</span><span class="sxs-lookup"><span data-stu-id="1253b-118">However, the repeat count is not cumulative.</span></span><br/> |
| <dl> <span data-ttu-id="1253b-119"><dt>16 23</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-119"><dt>16 23</dt></span></span> </dl> | <span data-ttu-id="1253b-120">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="1253b-120">The scan code.</span></span> <span data-ttu-id="1253b-121">El valor depende del fabricante de equipos originales (OEM).</span><span class="sxs-lookup"><span data-stu-id="1253b-121">The value depends on the original equipment manufacturer (OEM).</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="1253b-122"><dt>24</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-122"><dt>24</dt></span></span> </dl>    | <span data-ttu-id="1253b-123">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="1253b-123">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="1253b-124">El valor es 1 si es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="1253b-124">The value is 1 if it is an extended key; otherwise, it is 0.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="1253b-125"><dt>25 28</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-125"><dt>25 28</dt></span></span> </dl> | <span data-ttu-id="1253b-126">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="1253b-126">Reserved; do not use.</span></span><br/>                                                                                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1253b-127"><dt>29</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-127"><dt>29</dt></span></span> </dl>    | <span data-ttu-id="1253b-128">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="1253b-128">The context code.</span></span> <span data-ttu-id="1253b-129">El valor es 1 si se mantiene presionada la tecla ALT mientras se presiona la tecla; de lo contrario, el valor es 0.</span><span class="sxs-lookup"><span data-stu-id="1253b-129">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="1253b-130"><dt>30</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-130"><dt>30</dt></span></span> </dl>    | <span data-ttu-id="1253b-131">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="1253b-131">The previous key state.</span></span> <span data-ttu-id="1253b-132">El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.</span><span class="sxs-lookup"><span data-stu-id="1253b-132">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span><br/>                                                                                                                                                      |
| <dl> <span data-ttu-id="1253b-133"><dt>31</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-133"><dt>31</dt></span></span> </dl>    | <span data-ttu-id="1253b-134">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="1253b-134">The transition state.</span></span> <span data-ttu-id="1253b-135">El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.</span><span class="sxs-lookup"><span data-stu-id="1253b-135">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span><br/>                                                                                                                                                              |

<span data-ttu-id="1253b-136">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="1253b-136">For more detail, see [Keystroke Message Flags](../inputdev/about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1253b-137">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1253b-137">Return value</span></span>

<span data-ttu-id="1253b-138">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="1253b-138">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="1253b-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1253b-139">Remarks</span></span>

<span data-ttu-id="1253b-140">Cuando el código de contexto es cero, el mensaje se puede pasar a la función [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) , que lo controlará como si fuera un mensaje de clave estándar en lugar de un mensaje de clave de carácter del sistema.</span><span class="sxs-lookup"><span data-stu-id="1253b-140">When the context code is zero, the message can be passed to the [**TranslateAccelerator**](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora) function, which will handle it as though it were a standard key message instead of a system character-key message.</span></span> <span data-ttu-id="1253b-141">Esto permite usar teclas de aceleración con la ventana activa incluso si la ventana activa no tiene el foco de teclado.</span><span class="sxs-lookup"><span data-stu-id="1253b-141">This allows accelerator keys to be used with the active window even if the active window does not have the keyboard focus.</span></span>

<span data-ttu-id="1253b-142">Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. tecla Impr Pant; tecla INTERRUMPIr; tecla Bloq Num; y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="1253b-142">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; the PRINT SCRN key; the BREAK key; the NUMLOCK key; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="1253b-143">Otros teclados pueden admitir el bit extendido-Key en el parámetro.</span><span class="sxs-lookup"><span data-stu-id="1253b-143">Other keyboards may support the extended-key bit in the parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="1253b-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1253b-144">Requirements</span></span>



| <span data-ttu-id="1253b-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="1253b-145">Requirement</span></span> | <span data-ttu-id="1253b-146">Value</span><span class="sxs-lookup"><span data-stu-id="1253b-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1253b-147">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1253b-147">Minimum supported client</span></span><br/> | <span data-ttu-id="1253b-148">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1253b-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1253b-149">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1253b-149">Minimum supported server</span></span><br/> | <span data-ttu-id="1253b-150">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1253b-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1253b-151">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1253b-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="1253b-152"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1253b-152"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1253b-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="1253b-153">See also</span></span>

<dl> <dt>

<span data-ttu-id="1253b-154">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1253b-154">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1253b-155">**TranslateAccelerator**</span><span class="sxs-lookup"><span data-stu-id="1253b-155">**TranslateAccelerator**</span></span>](/windows/desktop/api/Winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[<span data-ttu-id="1253b-156">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="1253b-156">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="1253b-157">**SYSKEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1253b-157">**WM\_SYSKEYDOWN**</span></span>](/windows/desktop/inputdev/wm-syskeydown)
</dt> <dt>

<span data-ttu-id="1253b-158">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1253b-158">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1253b-159">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="1253b-159">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

