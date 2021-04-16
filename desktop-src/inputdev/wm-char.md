---
title: Mensaje de WM_CHAR (Winuser. h)
description: Se envía a la ventana con el foco de teclado cuando \_ la función TranslateMessage traduce un mensaje KEYDOWN de WM. El \_ mensaje de caracteres de WM contiene el código de carácter de la tecla que se presionó.
ms.assetid: 7e45dc6f-ff68-4534-9e52-46e5f4110532
keywords:
- Entrada de mouse y teclado de mensaje de WM_CHAR
topic_type:
- apiref
api_name:
- WM_CHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/28/2020
ms.openlocfilehash: 8d174f64fa776b506814540d4f2c97635fba38a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105718767"
---
# <a name="wm_char-message"></a><span data-ttu-id="e0d88-105">Mensaje de carácter de WM \_</span><span class="sxs-lookup"><span data-stu-id="e0d88-105">WM\_CHAR message</span></span>

<span data-ttu-id="e0d88-106">Se envía a la ventana con el foco de teclado cuando la función [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) traduce un mensaje [**\_ KEYDOWN de WM**](wm-keydown.md) .</span><span class="sxs-lookup"><span data-stu-id="e0d88-106">Posted to the window with the keyboard focus when a [**WM\_KEYDOWN**](wm-keydown.md) message is translated by the [**TranslateMessage**](/windows/desktop/api/winuser/nf-winuser-translatemessage) function.</span></span> <span data-ttu-id="e0d88-107">El mensaje de caracteres de **WM \_** contiene el código de carácter de la tecla que se presionó.</span><span class="sxs-lookup"><span data-stu-id="e0d88-107">The **WM\_CHAR** message contains the character code of the key that was pressed.</span></span>


```C++
#define WM_CHAR                         0x0102
```



## <a name="parameters"></a><span data-ttu-id="e0d88-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e0d88-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0d88-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e0d88-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d88-110">Código de carácter de la clave.</span><span class="sxs-lookup"><span data-stu-id="e0d88-110">The character code of the key.</span></span>

</dd> <dt>

<span data-ttu-id="e0d88-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e0d88-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e0d88-112">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="e0d88-112">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="e0d88-113">Bits</span><span class="sxs-lookup"><span data-stu-id="e0d88-113">Bits</span></span>  | <span data-ttu-id="e0d88-114">Significado</span><span class="sxs-lookup"><span data-stu-id="e0d88-114">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d88-115">0-15</span><span class="sxs-lookup"><span data-stu-id="e0d88-115">0-15</span></span>  | <span data-ttu-id="e0d88-116">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="e0d88-116">The repeat count for the current message.</span></span> <span data-ttu-id="e0d88-117">El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="e0d88-117">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="e0d88-118">Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="e0d88-118">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="e0d88-119">Sin embargo, el número de repeticiones no es acumulativo.</span><span class="sxs-lookup"><span data-stu-id="e0d88-119">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="e0d88-120">16-23</span><span class="sxs-lookup"><span data-stu-id="e0d88-120">16-23</span></span> | <span data-ttu-id="e0d88-121">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="e0d88-121">The scan code.</span></span> <span data-ttu-id="e0d88-122">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="e0d88-122">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="e0d88-123">24</span><span class="sxs-lookup"><span data-stu-id="e0d88-123">24</span></span>    | <span data-ttu-id="e0d88-124">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="e0d88-124">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="e0d88-125">El valor es 1 si es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="e0d88-125">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="e0d88-126">25-28</span><span class="sxs-lookup"><span data-stu-id="e0d88-126">25-28</span></span> | <span data-ttu-id="e0d88-127">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="e0d88-127">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="e0d88-128">29</span><span class="sxs-lookup"><span data-stu-id="e0d88-128">29</span></span>    | <span data-ttu-id="e0d88-129">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="e0d88-129">The context code.</span></span> <span data-ttu-id="e0d88-130">El valor es 1 si se mantiene presionada la tecla ALT mientras se presiona la tecla; de lo contrario, el valor es 0.</span><span class="sxs-lookup"><span data-stu-id="e0d88-130">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="e0d88-131">30</span><span class="sxs-lookup"><span data-stu-id="e0d88-131">30</span></span>    | <span data-ttu-id="e0d88-132">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="e0d88-132">The previous key state.</span></span> <span data-ttu-id="e0d88-133">El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.</span><span class="sxs-lookup"><span data-stu-id="e0d88-133">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="e0d88-134">31</span><span class="sxs-lookup"><span data-stu-id="e0d88-134">31</span></span>    | <span data-ttu-id="e0d88-135">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="e0d88-135">The transition state.</span></span> <span data-ttu-id="e0d88-136">El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.</span><span class="sxs-lookup"><span data-stu-id="e0d88-136">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="e0d88-137">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="e0d88-137">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>
 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0d88-138">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e0d88-138">Return value</span></span>

<span data-ttu-id="e0d88-139">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e0d88-139">An application should return zero if it processes this message.</span></span>

## <a name="example"></a><span data-ttu-id="e0d88-140">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="e0d88-140">Example</span></span>

```cpp
LRESULT CALLBACK WndProc(HWND hwnd, UINT message, WPARAM wParam, LPARAM lParam)
{
    switch (message)
    {
   
    // ...

    case WM_CHAR:
        OnKeyPress(wParam);
        break;

    default:
        return DefWindowProc(hwnd, message, wParam, lParam);
    }
    return 0;
}
```
<span data-ttu-id="e0d88-141">Ejemplo de [ejemplos clásicos de Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) en github.</span><span class="sxs-lookup"><span data-stu-id="e0d88-141">Example from [Windows Classic Samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/multimedia/mediafoundation/protectedplayback/winmain.cpp) on GitHub.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0d88-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0d88-142">Remarks</span></span>

<span data-ttu-id="e0d88-143">El mensaje de **\_ carácter de WM** usa el formato de transformación Unicode (UTF)-16.</span><span class="sxs-lookup"><span data-stu-id="e0d88-143">The **WM\_CHAR** message uses Unicode Transformation Format (UTF)-16.</span></span>

<span data-ttu-id="e0d88-144">No hay necesariamente una correspondencia uno a uno entre las claves presionadas y los mensajes de caracteres generados, por lo que la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="e0d88-144">There is not necessarily a one-to-one correspondence between keys pressed and character messages generated, and so the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="e0d88-145">La información de la palabra de orden superior solo se aplica al mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) más reciente que precede a la publicación del mensaje de **\_ carácter de WM** .</span><span class="sxs-lookup"><span data-stu-id="e0d88-145">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_CHAR** message.</span></span>

<span data-ttu-id="e0d88-146">Para los teclados mejorados de clave 101-y 102, las teclas extendidas son la ALT derecha y las teclas CTRL derecha en la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="e0d88-146">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="e0d88-147">Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="e0d88-147">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

<span data-ttu-id="e0d88-148">El mensaje de conversión [**\_ UNICHAR de WM**](wm-unichar.md) es el mismo que el de **WM \_ Char**, salvo que usa UTF-32.</span><span class="sxs-lookup"><span data-stu-id="e0d88-148">The [**WM\_UNICHAR**](wm-unichar.md) message is the same as **WM\_CHAR**, except it uses UTF-32.</span></span> <span data-ttu-id="e0d88-149">Está diseñado para enviar o exponer caracteres Unicode en ventanas ANSI y puede controlar los caracteres de plano complementario Unicode.</span><span class="sxs-lookup"><span data-stu-id="e0d88-149">It is designed to send or post Unicode characters to ANSI windows, and it can handle Unicode Supplementary Plane characters.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0d88-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0d88-150">Requirements</span></span>



| <span data-ttu-id="e0d88-151">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0d88-151">Requirement</span></span> | <span data-ttu-id="e0d88-152">Value</span><span class="sxs-lookup"><span data-stu-id="e0d88-152">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0d88-153">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d88-153">Minimum supported client</span></span><br/> | <span data-ttu-id="e0d88-154">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e0d88-154">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e0d88-155">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e0d88-155">Minimum supported server</span></span><br/> | <span data-ttu-id="e0d88-156">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e0d88-156">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e0d88-157">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e0d88-157">Header</span></span><br/>                   | <dl> <span data-ttu-id="e0d88-158"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0d88-158"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0d88-159">Vea también</span><span class="sxs-lookup"><span data-stu-id="e0d88-159">See also</span></span>

<dl> <dt>

<span data-ttu-id="e0d88-160">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e0d88-160">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e0d88-161">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="e0d88-161">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="e0d88-162">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e0d88-162">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

[<span data-ttu-id="e0d88-163">**UNICHAR de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e0d88-163">**WM\_UNICHAR**</span></span>](wm-unichar.md)
</dt> <dt>

<span data-ttu-id="e0d88-164">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e0d88-164">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e0d88-165">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="e0d88-165">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

