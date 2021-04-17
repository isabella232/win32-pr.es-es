---
title: Mensaje de WM_KEYDOWN (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando se presiona una tecla que no es del sistema. Una clave no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT.
ms.assetid: 0e37149f-445c-4b20-ad68-fdf39428ac91
keywords:
- Entrada de mouse y teclado de mensaje de WM_KEYDOWN
topic_type:
- apiref
api_name:
- WM_KEYDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: ee6dc21b4fb90f0d02e80fce8ce6cc17099a0547
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700251"
---
# <a name="wm_keydown-message"></a><span data-ttu-id="7757d-105">\_Mensaje KEYDOWN de WM</span><span class="sxs-lookup"><span data-stu-id="7757d-105">WM\_KEYDOWN message</span></span>

<span data-ttu-id="7757d-106">Se envía a la ventana con el foco de teclado cuando se presiona una tecla que no es del sistema.</span><span class="sxs-lookup"><span data-stu-id="7757d-106">Posted to the window with the keyboard focus when a nonsystem key is pressed.</span></span> <span data-ttu-id="7757d-107">Una clave no del sistema es una tecla que se presiona cuando no se presiona la tecla ALT.</span><span class="sxs-lookup"><span data-stu-id="7757d-107">A nonsystem key is a key that is pressed when the ALT key is not pressed.</span></span>


```C++
#define WM_KEYDOWN                      0x0100
```



## <a name="parameters"></a><span data-ttu-id="7757d-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7757d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7757d-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7757d-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7757d-110">Código de tecla virtual de la clave que no es del sistema.</span><span class="sxs-lookup"><span data-stu-id="7757d-110">The virtual-key code of the nonsystem key.</span></span> <span data-ttu-id="7757d-111">Consulte [códigos de tecla virtual](virtual-key-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7757d-111">See [Virtual-Key Codes](virtual-key-codes.md).</span></span>

</dd> <dt>

<span data-ttu-id="7757d-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7757d-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7757d-113">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, como se muestra a continuación.</span><span class="sxs-lookup"><span data-stu-id="7757d-113">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown following.</span></span>



| <span data-ttu-id="7757d-114">Bits</span><span class="sxs-lookup"><span data-stu-id="7757d-114">Bits</span></span>  | <span data-ttu-id="7757d-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7757d-115">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7757d-116">0-15</span><span class="sxs-lookup"><span data-stu-id="7757d-116">0-15</span></span>  | <span data-ttu-id="7757d-117">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="7757d-117">The repeat count for the current message.</span></span> <span data-ttu-id="7757d-118">El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="7757d-118">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="7757d-119">Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="7757d-119">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="7757d-120">Sin embargo, el número de repeticiones no es acumulativo.</span><span class="sxs-lookup"><span data-stu-id="7757d-120">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="7757d-121">16-23</span><span class="sxs-lookup"><span data-stu-id="7757d-121">16-23</span></span> | <span data-ttu-id="7757d-122">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="7757d-122">The scan code.</span></span> <span data-ttu-id="7757d-123">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="7757d-123">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="7757d-124">24</span><span class="sxs-lookup"><span data-stu-id="7757d-124">24</span></span>    | <span data-ttu-id="7757d-125">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="7757d-125">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="7757d-126">El valor es 1 si es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="7757d-126">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="7757d-127">25-28</span><span class="sxs-lookup"><span data-stu-id="7757d-127">25-28</span></span> | <span data-ttu-id="7757d-128">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="7757d-128">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="7757d-129">29</span><span class="sxs-lookup"><span data-stu-id="7757d-129">29</span></span>    | <span data-ttu-id="7757d-130">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="7757d-130">The context code.</span></span> <span data-ttu-id="7757d-131">El valor siempre es 0 para un mensaje de **\_ KEYDOWN de WM** .</span><span class="sxs-lookup"><span data-stu-id="7757d-131">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                                |
| <span data-ttu-id="7757d-132">30</span><span class="sxs-lookup"><span data-stu-id="7757d-132">30</span></span>    | <span data-ttu-id="7757d-133">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="7757d-133">The previous key state.</span></span> <span data-ttu-id="7757d-134">El valor es 1 si la tecla está inactiva antes de que se envíe el mensaje o es cero si la clave está activa.</span><span class="sxs-lookup"><span data-stu-id="7757d-134">The value is 1 if the key is down before the message is sent, or it is zero if the key is up.</span></span>                                                                                                                                                 |
| <span data-ttu-id="7757d-135">31</span><span class="sxs-lookup"><span data-stu-id="7757d-135">31</span></span>    | <span data-ttu-id="7757d-136">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="7757d-136">The transition state.</span></span> <span data-ttu-id="7757d-137">El valor siempre es 0 para un mensaje de **\_ KEYDOWN de WM** .</span><span class="sxs-lookup"><span data-stu-id="7757d-137">The value is always 0 for a **WM\_KEYDOWN** message.</span></span>                                                                                                                                                                                            |

<span data-ttu-id="7757d-138">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="7757d-138">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7757d-139">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7757d-139">Return value</span></span>

<span data-ttu-id="7757d-140">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="7757d-140">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="7757d-141">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="7757d-141">Example</span></span>

```cpp
LRESULT CALLBACK HostWndProc(HWND hWnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message) 
    {
    case WM_KEYDOWN:
        if (wParam == VK_ESCAPE)
        {
            if (isFullScreen) 
            {
                GoPartialScreen();
            }
        }
        break;

    // ...
    default:
        return DefWindowProc(hWnd, message, wParam, lParam);
    }
    return 0;  
}

```

<span data-ttu-id="7757d-142">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) en github.</span><span class="sxs-lookup"><span data-stu-id="7757d-142">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Magnification/cpp/Windowed/MagnifierSample.cpp) on GitHub.</span></span>


## <a name="remarks"></a><span data-ttu-id="7757d-143">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7757d-143">Remarks</span></span>

<span data-ttu-id="7757d-144">Si se presiona la tecla F10, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece una marca interna.</span><span class="sxs-lookup"><span data-stu-id="7757d-144">If the F10 key is pressed, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets an internal flag.</span></span> <span data-ttu-id="7757d-145">Cuando **DefWindowProc** recibe el mensaje de [**\_ KEYUP de WM**](wm-keyup.md) , la función comprueba si se ha establecido la marca interna y, en caso afirmativo, envía un mensaje de [**WM \_ SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) a la ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="7757d-145">When **DefWindowProc** receives the [**WM\_KEYUP**](wm-keyup.md) message, the function checks whether the internal flag is set and, if so, sends a [**WM\_SYSCOMMAND**](/windows/desktop/menurc/wm-syscommand) message to the top-level window.</span></span> <span data-ttu-id="7757d-146">El parámetro **WM \_ SYSCOMMAND** del mensaje se establece en SC \_ KEYMENU.</span><span class="sxs-lookup"><span data-stu-id="7757d-146">The **WM\_SYSCOMMAND** parameter of the message is set to SC\_KEYMENU.</span></span>

<span data-ttu-id="7757d-147">Debido a la característica de repetición de la función, se puede publicar más de un mensaje de **\_ KEYDOWN de WM** antes de que se exponga un mensaje de [**\_ KEYUP de WM**](wm-keyup.md) .</span><span class="sxs-lookup"><span data-stu-id="7757d-147">Because of the autorepeat feature, more than one **WM\_KEYDOWN** message may be posted before a [**WM\_KEYUP**](wm-keyup.md) message is posted.</span></span> <span data-ttu-id="7757d-148">El estado de clave anterior (bit 30) se puede usar para determinar si el mensaje de **\_ KEYDOWN de WM** indica la primera transición o una transición hacia abajo.</span><span class="sxs-lookup"><span data-stu-id="7757d-148">The previous key state (bit 30) can be used to determine whether the **WM\_KEYDOWN** message indicates the first down transition or a repeated down transition.</span></span>

<span data-ttu-id="7757d-149">Para los teclados mejorados de la tecla 101 y 102, las teclas extendidas son las teclas ALT y CTRL correctas de la sección principal del teclado. las teclas INS, SUPR, Inicio, fin, Re Pág, Av Pág y flecha en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="7757d-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN, and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="7757d-150">Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="7757d-150">Other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="7757d-151">Las aplicaciones deben pasar *wParam* a [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) sin modificarlo.</span><span class="sxs-lookup"><span data-stu-id="7757d-151">Applications must pass *wParam* to [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) without altering it at all.</span></span>

## <a name="requirements"></a><span data-ttu-id="7757d-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7757d-152">Requirements</span></span>



| <span data-ttu-id="7757d-153">Requisito</span><span class="sxs-lookup"><span data-stu-id="7757d-153">Requirement</span></span> | <span data-ttu-id="7757d-154">Value</span><span class="sxs-lookup"><span data-stu-id="7757d-154">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7757d-155">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7757d-155">Minimum supported client</span></span><br/> | <span data-ttu-id="7757d-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7757d-156">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="7757d-157">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7757d-157">Minimum supported server</span></span><br/> | <span data-ttu-id="7757d-158">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7757d-158">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7757d-159">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7757d-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="7757d-160"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7757d-160"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7757d-161">Vea también</span><span class="sxs-lookup"><span data-stu-id="7757d-161">See also</span></span>

<dl> <dt>

<span data-ttu-id="7757d-162">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7757d-162">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7757d-163">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="7757d-163">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="7757d-164">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="7757d-164">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="7757d-165">**carácter de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7757d-165">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="7757d-166">**KEYUP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7757d-166">**WM\_KEYUP**</span></span>](wm-keyup.md)
</dt> <dt>

[<span data-ttu-id="7757d-167">**SYSCOMMAND de WM \_**</span><span class="sxs-lookup"><span data-stu-id="7757d-167">**WM\_SYSCOMMAND**</span></span>](/windows/desktop/menurc/wm-syscommand)
</dt> <dt>

<span data-ttu-id="7757d-168">**Vista**</span><span class="sxs-lookup"><span data-stu-id="7757d-168">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="7757d-169">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="7757d-169">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

