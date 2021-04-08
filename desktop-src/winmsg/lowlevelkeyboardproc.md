---
UID: ''
title: Función de devolución de llamada LowLevelKeyboardProc
description: El sistema llama a esta función cada vez que se va a publicar un nuevo evento de entrada de teclado en una cola de entrada del subproceso.
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
ms.openlocfilehash: f33acbb6888bad97a03b610c513cbaf9c3750684
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "104077474"
---
# <a name="lowlevelkeyboardproc-function"></a><span data-ttu-id="15871-103">LowLevelKeyboardProc función)</span><span class="sxs-lookup"><span data-stu-id="15871-103">LowLevelKeyboardProc function</span></span>

## <a name="description"></a><span data-ttu-id="15871-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="15871-104">Description</span></span>

<span data-ttu-id="15871-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="15871-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="15871-106">El sistema llama a esta función cada vez que se va a publicar un nuevo evento de entrada de teclado en una cola de entrada del subproceso.</span><span class="sxs-lookup"><span data-stu-id="15871-106">The system calls this function every time a new keyboard input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="15871-107">**Nota:**  Cuando se llama a esta función de devolución de llamada en respuesta a un cambio en el estado de una clave, se llama a la función de devolución de llamada antes de que se actualice el estado asincrónico de la clave.</span><span class="sxs-lookup"><span data-stu-id="15871-107">**Note:**  When this callback function is called in response to a change in the state of a key, the callback function is called before the asynchronous state of the key is updated.</span></span>
<span data-ttu-id="15871-108">Por consiguiente, el estado asincrónico de la clave no se puede determinar mediante una llamada a [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) desde dentro de la función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="15871-108">Consequently, the asynchronous state of the key cannot be determined by calling [GetAsyncKeyState](/windows/desktop/api/winuser/nf-winuser-getasynckeystate) from within the callback function.</span></span>

<span data-ttu-id="15871-109">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="15871-109">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="15871-110">**LowLevelKeyboardProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="15871-110">**LowLevelKeyboardProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelKeyboardProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="15871-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="15871-111">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="15871-112">código [in]</span><span class="sxs-lookup"><span data-stu-id="15871-112">code [in]</span></span>

<span data-ttu-id="15871-113">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="15871-113">Type: **int**</span></span>

<span data-ttu-id="15871-114">Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="15871-114">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="15871-115">Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="15871-115">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="15871-116">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="15871-116">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="15871-117">Valor</span><span class="sxs-lookup"><span data-stu-id="15871-117">Value</span></span> | <span data-ttu-id="15871-118">Significado</span><span class="sxs-lookup"><span data-stu-id="15871-118">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="15871-119">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="15871-119">**HC_ACTION** 0</span></span> | <span data-ttu-id="15871-120">Los parámetros *wParam* e *lParam* contienen información sobre un mensaje de teclado.</span><span class="sxs-lookup"><span data-stu-id="15871-120">The *wParam* and *lParam* parameters contain information about a keyboard message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="15871-121">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="15871-121">wParam [in]</span></span>

<span data-ttu-id="15871-122">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="15871-122">Type: **WPARAM**</span></span>

<span data-ttu-id="15871-123">Identificador del mensaje de teclado.</span><span class="sxs-lookup"><span data-stu-id="15871-123">The identifier of the keyboard message.</span></span>
<span data-ttu-id="15871-124">Este parámetro puede ser uno de los siguientes mensajes: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown)o [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span><span class="sxs-lookup"><span data-stu-id="15871-124">This parameter can be one of the following messages: [WM_KEYDOWN](/windows/desktop/inputdev/wm-keydown), [WM_KEYUP](/windows/desktop/inputdev/wm-keyup), [WM_SYSKEYDOWN](/windows/desktop/inputdev/wm-syskeydown), or [WM_SYSKEYUP](/windows/desktop/inputdev/wm-syskeyup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="15871-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="15871-125">lParam [in]</span></span>

<span data-ttu-id="15871-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="15871-126">Type: **LPARAM**</span></span>

<span data-ttu-id="15871-127">Puntero a una estructura [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="15871-127">A pointer to a [KBDLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="15871-128">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="15871-128">Returns</span></span>

<span data-ttu-id="15871-129">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="15871-129">Type: **LRESULT**</span></span>

<span data-ttu-id="15871-130">Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="15871-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="15871-131">Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_KEYBOARD_LL](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.</span><span class="sxs-lookup"><span data-stu-id="15871-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_KEYBOARD_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="15871-132">Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="15871-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="15871-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="15871-133">Remarks</span></span>

<span data-ttu-id="15871-134">Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de **WH_KEYBOARD_LL** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="15871-134">An application installs the hook procedure by specifying the **WH_KEYBOARD_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="15871-135">Este enlace se llama en el contexto del subproceso que lo instaló.</span><span class="sxs-lookup"><span data-stu-id="15871-135">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="15871-136">La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.</span><span class="sxs-lookup"><span data-stu-id="15871-136">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="15871-137">Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="15871-137">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="15871-138">La entrada del teclado puede proviene del controlador de teclado local o de las llamadas a la función [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) .</span><span class="sxs-lookup"><span data-stu-id="15871-138">The keyboard input can come from the local keyboard driver or from calls to the [keybd_event](/windows/desktop/api/winuser/nf-winuser-keybd_event) function.</span></span>
<span data-ttu-id="15871-139">Si la entrada procede de una llamada a **keybd_event**, la entrada se "insertó".</span><span class="sxs-lookup"><span data-stu-id="15871-139">If the input comes from a call to **keybd_event**, the input was "injected".</span></span>
<span data-ttu-id="15871-140">Sin embargo, el enlace de WH_KEYBOARD_LL no se inserta en otro proceso.</span><span class="sxs-lookup"><span data-stu-id="15871-140">However, the WH_KEYBOARD_LL hook is not injected into another process.</span></span>
<span data-ttu-id="15871-141">En su lugar, el contexto vuelve a cambiar al proceso que instaló el enlace y se llama en su contexto original.</span><span class="sxs-lookup"><span data-stu-id="15871-141">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="15871-142">A continuación, el contexto vuelve a la aplicación que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="15871-142">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="15871-143">El procedimiento de enlace debe procesar un mensaje en menos tiempo que la entrada de datos especificada en el valor **LowLevelHooksTimeout** en la siguiente clave del registro: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="15871-143">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="15871-144">El valor se expresa en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="15871-144">The value is in milliseconds.</span></span>
<span data-ttu-id="15871-145">Si el procedimiento de enlace agota el tiempo de espera, el sistema pasa el mensaje al siguiente enlace.</span><span class="sxs-lookup"><span data-stu-id="15871-145">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="15871-146">Sin embargo, en Windows 7 y versiones posteriores, el enlace se quita de forma silenciosa sin llamar a.</span><span class="sxs-lookup"><span data-stu-id="15871-146">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="15871-147">No hay ninguna manera de que la aplicación sepa si se quita el enlace.</span><span class="sxs-lookup"><span data-stu-id="15871-147">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="15871-148">Nota: los enlaces de depuración no pueden realizar un seguimiento de este tipo de enlaces de teclado de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="15871-148">Note:  Debug hooks cannot track this type of low level keyboard hooks.</span></span>
<span data-ttu-id="15871-149">Si la aplicación debe usar enlaces de nivel bajo, debe ejecutar los enlaces en un subproceso dedicado que pase el trabajo a un subproceso de trabajo y, a continuación, devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="15871-149">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="15871-150">En la mayoría de los casos en los que la aplicación necesita usar enlaces de nivel bajo, debe supervisar en su lugar la entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="15871-150">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="15871-151">Esto se debe a que la entrada sin formato puede supervisar de forma asincrónica los mensajes de teclado y del mouse que están destinados a otros subprocesos de forma más eficaz que los enlaces de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="15871-151">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="15871-152">Para obtener más información sobre la entrada sin formato, consulte [entrada sin formato](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="15871-152">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="15871-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="15871-153">See also</span></span>

[<span data-ttu-id="15871-154">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="15871-154">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="15871-155">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="15871-155">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="15871-156">keybd_event</span><span class="sxs-lookup"><span data-stu-id="15871-156">keybd_event</span></span>](/windows/desktop/api/winuser/nf-winuser-keybd_event)

[<span data-ttu-id="15871-157">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="15871-157">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="15871-158">WM_KEYDOWN</span><span class="sxs-lookup"><span data-stu-id="15871-158">WM_KEYDOWN</span></span>](/windows/desktop/inputdev/wm-keydown)

[<span data-ttu-id="15871-159">WM_KEYUP</span><span class="sxs-lookup"><span data-stu-id="15871-159">WM_KEYUP</span></span>](/windows/desktop/inputdev/wm-keyup)

[<span data-ttu-id="15871-160">WM_SYSKEYDOWN</span><span class="sxs-lookup"><span data-stu-id="15871-160">WM_SYSKEYDOWN</span></span>](/windows/desktop/inputdev/wm-syskeydown)

[<span data-ttu-id="15871-161">WM_SYSKEYUP</span><span class="sxs-lookup"><span data-stu-id="15871-161">WM_SYSKEYUP</span></span>](/windows/desktop/inputdev/wm-syskeyup)

[<span data-ttu-id="15871-162">Enlaces</span><span class="sxs-lookup"><span data-stu-id="15871-162">Hooks</span></span>](hooks.md)

[<span data-ttu-id="15871-163">Acerca de los enlaces</span><span class="sxs-lookup"><span data-stu-id="15871-163">About Hooks</span></span>](about-hooks.md)
