---
UID: ''
title: Función de devolución de llamada KeyboardProc
description: El sistema llama a esta función obtiene una función de mensaje y hay un mensaje de teclado para procesar.
old-location: ''
ms.assetid: na
ms.date: 04/05/2019
ms.keywords: ''
ms.topic: reference
req.header: ''
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location: ''
api_name: ''
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: a042a1a92900713bdf49ba8d866031bfdcb5c6a8
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105665779"
---
# <a name="keyboardproc-function"></a><span data-ttu-id="69ac8-103">KeyboardProc función)</span><span class="sxs-lookup"><span data-stu-id="69ac8-103">KeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="69ac8-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ac8-104">Description</span></span>

<span data-ttu-id="69ac8-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="69ac8-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="69ac8-106">El sistema llama a esta función cada vez que una aplicación llama a la función [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) y hay un mensaje de teclado ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) o [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="69ac8-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a keyboard message ([WM_KEYUP](/windows/desktop/inputdev/wm-keyup) or [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown)) to be processed.</span></span>

<span data-ttu-id="69ac8-107">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="69ac8-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="69ac8-108">**KeyboardProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="69ac8-108">**KeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK KeyboardProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="69ac8-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69ac8-109">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="69ac8-110">código [in]</span><span class="sxs-lookup"><span data-stu-id="69ac8-110">code [in]</span></span>

<span data-ttu-id="69ac8-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="69ac8-111">Type: **int**</span></span>

<span data-ttu-id="69ac8-112">Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="69ac8-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="69ac8-113">Si el *código* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="69ac8-113">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="69ac8-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="69ac8-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="69ac8-115">Valor</span><span class="sxs-lookup"><span data-stu-id="69ac8-115">Value</span></span> | <span data-ttu-id="69ac8-116">Significado</span><span class="sxs-lookup"><span data-stu-id="69ac8-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="69ac8-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="69ac8-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="69ac8-118">Los parámetros *wParam* e *lParam* contienen información sobre un mensaje de pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="69ac8-118">The *wParam* and *lParam* parameters contain information about a keystroke message.</span></span> |
| <span data-ttu-id="69ac8-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="69ac8-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="69ac8-120">Los parámetros *wParam* y *lParam* contienen información sobre un mensaje de pulsación de tecla y el mensaje de pulsación de tecla no se ha quitado de la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="69ac8-120">The *wParam* and *lParam* parameters contain information about a keystroke message, and the keystroke message has not been removed from the message queue.</span></span> <span data-ttu-id="69ac8-121">(Una aplicación llamada la función **PeekMessage** , que especifica la marca **PM_NOREMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="69ac8-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="69ac8-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="69ac8-122">wParam [in]</span></span>

<span data-ttu-id="69ac8-123">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="69ac8-123">Type: **WPARAM**</span></span>

<span data-ttu-id="69ac8-124">[Código de tecla virtual](/windows/desktop/inputdev/virtual-key-codes) de la clave que generó el mensaje de pulsación de tecla.</span><span class="sxs-lookup"><span data-stu-id="69ac8-124">The [virtual-key code](/windows/desktop/inputdev/virtual-key-codes) of the key that generated the keystroke message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="69ac8-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="69ac8-125">lParam [in]</span></span>

<span data-ttu-id="69ac8-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="69ac8-126">Type: **LPARAM**</span></span>

<span data-ttu-id="69ac8-127">El número de repeticiones, el código de digitalización, la marca de clave extendida, el código de contexto, la marca de estado de clave anterior y la marca de estado de transición.</span><span class="sxs-lookup"><span data-stu-id="69ac8-127">The repeat count, scan code, extended-key flag, context code, previous key-state flag, and transition-state flag.</span></span>
<span data-ttu-id="69ac8-128">Para obtener más información sobre el parámetro *lParam* , consulte [marcas de mensajes de pulsación de teclas](/windows/desktop/inputdev/about-keyboard-input).</span><span class="sxs-lookup"><span data-stu-id="69ac8-128">For more information about The *lParam* parameter, see [Keystroke Message Flags](/windows/desktop/inputdev/about-keyboard-input).</span></span>
<span data-ttu-id="69ac8-129">En la tabla siguiente se describen los bits de este valor.</span><span class="sxs-lookup"><span data-stu-id="69ac8-129">The following table describes the bits of this value.</span></span>

| <span data-ttu-id="69ac8-130">Bits</span><span class="sxs-lookup"><span data-stu-id="69ac8-130">Bits</span></span> | <span data-ttu-id="69ac8-131">Descripción</span><span class="sxs-lookup"><span data-stu-id="69ac8-131">Description</span></span> |
|-------|---------|
| <span data-ttu-id="69ac8-132">0-15</span><span class="sxs-lookup"><span data-stu-id="69ac8-132">0-15</span></span> | <span data-ttu-id="69ac8-133">Número de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="69ac8-133">The repeat count.</span></span> <span data-ttu-id="69ac8-134">El valor es el número de veces que la pulsación de tecla se repite como resultado de que el usuario mantiene presionada la tecla.</span><span class="sxs-lookup"><span data-stu-id="69ac8-134">The value is the number of times the keystroke is repeated as a result of the user's holding down the key.</span></span> |
| <span data-ttu-id="69ac8-135">16-23</span><span class="sxs-lookup"><span data-stu-id="69ac8-135">16-23</span></span> | <span data-ttu-id="69ac8-136">Código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="69ac8-136">The scan code.</span></span> <span data-ttu-id="69ac8-137">El valor depende del OEM.</span><span class="sxs-lookup"><span data-stu-id="69ac8-137">The value depends on the OEM.</span></span> |
| <span data-ttu-id="69ac8-138">24</span><span class="sxs-lookup"><span data-stu-id="69ac8-138">24</span></span> | <span data-ttu-id="69ac8-139">Indica si la tecla es una clave extendida, como una tecla de función o una tecla del teclado numérico.</span><span class="sxs-lookup"><span data-stu-id="69ac8-139">Indicates whether the key is an extended key, such as a function key or a key on the numeric keypad.</span></span> <span data-ttu-id="69ac8-140">El valor es 1 si la clave es una clave extendida; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="69ac8-140">The value is 1 if the key is an extended key; otherwise, it is 0.</span></span> |
| <span data-ttu-id="69ac8-141">25-28</span><span class="sxs-lookup"><span data-stu-id="69ac8-141">25-28</span></span> | <span data-ttu-id="69ac8-142">Reservado.</span><span class="sxs-lookup"><span data-stu-id="69ac8-142">Reserved.</span></span> |
| <span data-ttu-id="69ac8-143">29</span><span class="sxs-lookup"><span data-stu-id="69ac8-143">29</span></span> | <span data-ttu-id="69ac8-144">Código de contexto.</span><span class="sxs-lookup"><span data-stu-id="69ac8-144">The context code.</span></span> <span data-ttu-id="69ac8-145">El valor es 1 si la tecla ALT está presionada; de lo contrario, es 0.</span><span class="sxs-lookup"><span data-stu-id="69ac8-145">The value is 1 if the ALT key is down; otherwise, it is 0.</span></span> |
| <span data-ttu-id="69ac8-146">30</span><span class="sxs-lookup"><span data-stu-id="69ac8-146">30</span></span> | <span data-ttu-id="69ac8-147">Estado de la clave anterior.</span><span class="sxs-lookup"><span data-stu-id="69ac8-147">The previous key state.</span></span> <span data-ttu-id="69ac8-148">El valor es 1 si la tecla está inactiva antes de que se envíe el mensaje; es 0 si la clave está activa.</span><span class="sxs-lookup"><span data-stu-id="69ac8-148">The value is 1 if the key is down before the message is sent; it is 0 if the key is up.</span></span> |
| <span data-ttu-id="69ac8-149">31</span><span class="sxs-lookup"><span data-stu-id="69ac8-149">31</span></span> | <span data-ttu-id="69ac8-150">Estado de transición.</span><span class="sxs-lookup"><span data-stu-id="69ac8-150">The transition state.</span></span> <span data-ttu-id="69ac8-151">El valor es 0 si se presiona la tecla y 1 si se está liberando.</span><span class="sxs-lookup"><span data-stu-id="69ac8-151">The value is 0 if the key is being pressed and 1 if it is being released.</span></span> |

## <a name="returns"></a><span data-ttu-id="69ac8-152">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="69ac8-152">Returns</span></span>

<span data-ttu-id="69ac8-153">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="69ac8-153">Type: **LRESULT**</span></span>

<span data-ttu-id="69ac8-154">Si el *código* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="69ac8-154">If *code* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="69ac8-155">Si el *código* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_KEYBOARD](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.</span><span class="sxs-lookup"><span data-stu-id="69ac8-155">If *code* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="69ac8-156">Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="69ac8-156">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="69ac8-157">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69ac8-157">Remarks</span></span>

<span data-ttu-id="69ac8-158">Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de **WH_KEYBOARD** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="69ac8-158">An application installs the hook procedure by specifying the **WH_KEYBOARD** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="69ac8-159">Este enlace se puede llamar en el contexto del subproceso que lo instaló.</span><span class="sxs-lookup"><span data-stu-id="69ac8-159">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="69ac8-160">La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.</span><span class="sxs-lookup"><span data-stu-id="69ac8-160">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="69ac8-161">Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="69ac8-161">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="69ac8-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="69ac8-162">See also</span></span>

[<span data-ttu-id="69ac8-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="69ac8-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="69ac8-164">GetMessage</span><span class="sxs-lookup"><span data-stu-id="69ac8-164">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="69ac8-165">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="69ac8-165">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="69ac8-166">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="69ac8-166">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="69ac8-167">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="69ac8-167">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="69ac8-168">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="69ac8-168">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="69ac8-169">Enlaces</span><span class="sxs-lookup"><span data-stu-id="69ac8-169">Hooks</span></span>](hooks.md)
