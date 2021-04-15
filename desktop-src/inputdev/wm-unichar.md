---
title: Mensaje de WM_UNICHAR (Winuser. h)
description: '\_Una aplicación puede utilizar el mensaje UNIchar de WM para publicar la entrada en otras ventanas.'
ms.assetid: edbfcf14-0371-43ce-9676-eb10d964d0b7
keywords:
- Entrada de mouse y teclado de mensaje de WM_UNICHAR
topic_type:
- apiref
api_name:
- WM_UNICHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 833b5cb59095f5aecc8c0172857c8761fd92449a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695938"
---
# <a name="wm_unichar-message"></a><span data-ttu-id="b0832-104">Message de WM \_ UNIchar</span><span class="sxs-lookup"><span data-stu-id="b0832-104">WM\_UNICHAR message</span></span>

<span data-ttu-id="b0832-105">Una aplicación puede utilizar el mensaje **\_ UNICHAR de WM** para publicar la entrada en otras ventanas.</span><span class="sxs-lookup"><span data-stu-id="b0832-105">The **WM\_UNICHAR** message can be used by an application to post input to other windows.</span></span> <span data-ttu-id="b0832-106">Este mensaje contiene el código de carácter de la tecla que se presionó.</span><span class="sxs-lookup"><span data-stu-id="b0832-106">This message contains the character code of the key that was pressed.</span></span> <span data-ttu-id="b0832-107">(Compruebe si una aplicación de destino puede procesar mensajes de **WM \_ UNICHAR** enviando el mensaje con *wParam* establecido en **Unicode \_ nochar**).</span><span class="sxs-lookup"><span data-stu-id="b0832-107">(Test whether a target app can process **WM\_UNICHAR** messages by sending the message with *wParam* set to **UNICODE\_NOCHAR**.)</span></span>


```C++
#define WM_UNICHAR                      0x0109
```



## <a name="parameters"></a><span data-ttu-id="b0832-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0832-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0832-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b0832-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0832-110">Código de carácter de la clave.</span><span class="sxs-lookup"><span data-stu-id="b0832-110">The character code of the key.</span></span>

<span data-ttu-id="b0832-111">Si *wParam* es **Unicode \_ nochar** y la aplicación procesa este mensaje, devuelve **true**.</span><span class="sxs-lookup"><span data-stu-id="b0832-111">If *wParam* is **UNICODE\_NOCHAR** and the application processes this message, then return **TRUE**.</span></span> <span data-ttu-id="b0832-112">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devolverá **false** (el valor predeterminado).</span><span class="sxs-lookup"><span data-stu-id="b0832-112">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function will return **FALSE** (the default).</span></span>

<span data-ttu-id="b0832-113">Si *wParam* no es **Unicode \_**, devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="b0832-113">If *wParam* is not **UNICODE\_NOCHAR**, return **FALSE**.</span></span> <span data-ttu-id="b0832-114">El  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) de Unicode envía un mensaje de [**\_ carácter de WM**](wm-char.md) con los mismos parámetros y la función ANSI **DefWindowProc** envía uno o dos mensajes de **WM \_ Char** con los caracteres ANSI correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b0832-114">The Unicode  [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) posts a [**WM\_CHAR**](wm-char.md) message with the same parameters and the ANSI **DefWindowProc** function posts either one or two **WM\_CHAR** messages with the corresponding ANSI character(s).</span></span>

</dd> <dt>

<span data-ttu-id="b0832-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b0832-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b0832-116">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición, tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="b0832-116">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag, as shown in the following table.</span></span>



| <span data-ttu-id="b0832-117">Bits</span><span class="sxs-lookup"><span data-stu-id="b0832-117">Bits</span></span>  | <span data-ttu-id="b0832-118">Significado</span><span class="sxs-lookup"><span data-stu-id="b0832-118">Meaning</span></span>                                                                                                                                                                                                                                                               |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0832-119">0-15</span><span class="sxs-lookup"><span data-stu-id="b0832-119">0-15</span></span>  | <span data-ttu-id="b0832-120">Número de repeticiones del mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="b0832-120">The repeat count for the current message.</span></span> <span data-ttu-id="b0832-121">El valor es el número de veces que se repite la pulsación de tecla como resultado del usuario que mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="b0832-121">The value is the number of times the keystroke is autorepeated as a result of the user holding down the key.</span></span> <span data-ttu-id="b0832-122">Si la pulsación de tecla se mantiene suficientemente larga, se envían varios mensajes.</span><span class="sxs-lookup"><span data-stu-id="b0832-122">If the keystroke is held long enough, multiple messages are sent.</span></span> <span data-ttu-id="b0832-123">Sin embargo, el número de repeticiones no es acumulativo.</span><span class="sxs-lookup"><span data-stu-id="b0832-123">However, the repeat count is not cumulative.</span></span> |
| <span data-ttu-id="b0832-124">16-23</span><span class="sxs-lookup"><span data-stu-id="b0832-124">16-23</span></span> | <span data-ttu-id="b0832-125">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="b0832-125">The scan code.</span></span> <span data-ttu-id="b0832-126">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="b0832-126">The value depends on the OEM.</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="b0832-127">24</span><span class="sxs-lookup"><span data-stu-id="b0832-127">24</span></span>    | <span data-ttu-id="b0832-128">Indica si la clave es una clave extendida, como las teclas ALT y CTRL de la derecha, que aparecen en un teclado mejorado de clave de 101 o 102.</span><span class="sxs-lookup"><span data-stu-id="b0832-128">Indicates whether the key is an extended key, such as the right-hand ALT and CTRL keys that appear on an enhanced 101- or 102-key keyboard.</span></span> <span data-ttu-id="b0832-129">El valor es 1 si es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="b0832-129">The value is 1 if it is an extended key; otherwise, it is 0.</span></span>                                                              |
| <span data-ttu-id="b0832-130">25-28</span><span class="sxs-lookup"><span data-stu-id="b0832-130">25-28</span></span> | <span data-ttu-id="b0832-131">Sector No use.</span><span class="sxs-lookup"><span data-stu-id="b0832-131">Reserved; do not use.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b0832-132">29</span><span class="sxs-lookup"><span data-stu-id="b0832-132">29</span></span>    | <span data-ttu-id="b0832-133">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="b0832-133">The context code.</span></span> <span data-ttu-id="b0832-134">El valor es 1 si se mantiene presionada la tecla ALT mientras se presiona la tecla; de lo contrario, el valor es 0.</span><span class="sxs-lookup"><span data-stu-id="b0832-134">The value is 1 if the ALT key is held down while the key is pressed; otherwise, the value is 0.</span></span>                                                                                                                                                     |
| <span data-ttu-id="b0832-135">30</span><span class="sxs-lookup"><span data-stu-id="b0832-135">30</span></span>    | <span data-ttu-id="b0832-136">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="b0832-136">The previous key state.</span></span> <span data-ttu-id="b0832-137">El valor es 1 si la tecla está presionada antes de que se envíe el mensaje o es 0 si la clave está activa.</span><span class="sxs-lookup"><span data-stu-id="b0832-137">The value is 1 if the key is down before the message is sent, or it is 0 if the key is up.</span></span>                                                                                                                                                    |
| <span data-ttu-id="b0832-138">31</span><span class="sxs-lookup"><span data-stu-id="b0832-138">31</span></span>    | <span data-ttu-id="b0832-139">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="b0832-139">The transition state.</span></span> <span data-ttu-id="b0832-140">El valor es 1 si se está liberando la tecla o es 0 si se presiona la tecla.</span><span class="sxs-lookup"><span data-stu-id="b0832-140">The value is 1 if the key is being released, or it is 0 if the key is being pressed.</span></span>                                                                                                                                                            |

<span data-ttu-id="b0832-141">Para obtener más información, consulte [marcas de mensajes de pulsación de teclas](about-keyboard-input.md#keystroke-message-flags).</span><span class="sxs-lookup"><span data-stu-id="b0832-141">For more detail, see [Keystroke Message Flags](about-keyboard-input.md#keystroke-message-flags).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0832-142">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0832-142">Return value</span></span>

<span data-ttu-id="b0832-143">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="b0832-143">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0832-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0832-144">Remarks</span></span>

<span data-ttu-id="b0832-145">El mensaje de **WM \_ UNICHAR** es similar a [**WM \_ Char**](wm-char.md), pero usa el formato de transformación unicode (UTF)-32, mientras que **WM \_ Char** usa UTF-16.</span><span class="sxs-lookup"><span data-stu-id="b0832-145">The **WM\_UNICHAR** message is similar to [**WM\_CHAR**](wm-char.md), but it uses Unicode Transformation Format (UTF)-32, whereas **WM\_CHAR** uses UTF-16.</span></span>

<span data-ttu-id="b0832-146">Este mensaje está diseñado para enviar o exponer caracteres Unicode en ventanas ANSI y puede controlar los caracteres de plano complementario Unicode.</span><span class="sxs-lookup"><span data-stu-id="b0832-146">This message is designed to send or post Unicode characters to ANSI windows and can handle Unicode Supplementary Plane characters.</span></span>

<span data-ttu-id="b0832-147">Dado que no hay necesariamente una correspondencia uno a uno entre las claves presionadas y los mensajes de caracteres generados, la información de la palabra de orden superior del parámetro *lParam* no suele ser útil para las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b0832-147">Because there is not necessarily a one-to-one correspondence between keys pressed and character messages generated, the information in the high-order word of the *lParam* parameter is generally not useful to applications.</span></span> <span data-ttu-id="b0832-148">La información de la palabra de orden superior solo se aplica al mensaje de [**\_ KEYDOWN de WM**](wm-keydown.md) más reciente que precede a la publicación del mensaje de **WM \_ UNICHAR** .</span><span class="sxs-lookup"><span data-stu-id="b0832-148">The information in the high-order word applies only to the most recent [**WM\_KEYDOWN**](wm-keydown.md) message that precedes the posting of the **WM\_UNICHAR** message.</span></span>

<span data-ttu-id="b0832-149">Para los teclados mejorados de clave 101-y 102, las teclas extendidas son la ALT derecha y las teclas CTRL derecha en la sección principal del teclado. las teclas INS, DEL, Inicio, fin, Re Pág, Av Pág y flecha abajo en los clústeres a la izquierda del teclado numérico. y la división (/) y escriba las teclas en el teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="b0832-149">For enhanced 101- and 102-key keyboards, extended keys are the right ALT and the right CTRL keys on the main section of the keyboard; the INS, DEL, HOME, END, PAGE UP, PAGE DOWN and arrow keys in the clusters to the left of the numeric keypad; and the divide (/) and ENTER keys in the numeric keypad.</span></span> <span data-ttu-id="b0832-150">Otros teclados pueden admitir el bit extendido-Key en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="b0832-150">Some other keyboards may support the extended-key bit in the *lParam* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0832-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0832-151">Requirements</span></span>



| <span data-ttu-id="b0832-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0832-152">Requirement</span></span> | <span data-ttu-id="b0832-153">Value</span><span class="sxs-lookup"><span data-stu-id="b0832-153">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0832-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0832-154">Minimum supported client</span></span><br/> | <span data-ttu-id="b0832-155">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="b0832-155">Windows XP \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="b0832-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0832-156">Minimum supported server</span></span><br/> | <span data-ttu-id="b0832-157">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b0832-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b0832-158">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0832-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0832-159"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0832-159"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0832-160">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0832-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="b0832-161">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b0832-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b0832-162">**TranslateMessage**</span><span class="sxs-lookup"><span data-stu-id="b0832-162">**TranslateMessage**</span></span>](/windows/desktop/api/winuser/nf-winuser-translatemessage)
</dt> <dt>

[<span data-ttu-id="b0832-163">**carácter de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b0832-163">**WM\_CHAR**</span></span>](wm-char.md)
</dt> <dt>

[<span data-ttu-id="b0832-164">**KEYDOWN de WM \_**</span><span class="sxs-lookup"><span data-stu-id="b0832-164">**WM\_KEYDOWN**</span></span>](wm-keydown.md)
</dt> <dt>

<span data-ttu-id="b0832-165">**Vista**</span><span class="sxs-lookup"><span data-stu-id="b0832-165">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0832-166">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="b0832-166">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

