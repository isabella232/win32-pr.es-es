---
UID: ''
title: Función de devolución de llamada LowLevelMouseProc
description: El sistema llama a esta función cada vez que se va a publicar un nuevo evento de entrada del mouse en una cola de entrada del subproceso.
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
ms.openlocfilehash: df6f246e5824099d01ab2a42f887464c7177cfa5
ms.sourcegitcommit: 36610cefb8577d0cf9aa2286c8000d8f31cc4ec2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/26/2020
ms.locfileid: "104078555"
---
# <a name="lowlevelmouseproc-function"></a><span data-ttu-id="0b787-103">LowLevelMouseProc función)</span><span class="sxs-lookup"><span data-stu-id="0b787-103">LowLevelMouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="0b787-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="0b787-104">Description</span></span>

<span data-ttu-id="0b787-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="0b787-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="0b787-106">El sistema llama a esta función cada vez que se va a publicar un nuevo evento de entrada del mouse en una cola de entrada del subproceso.</span><span class="sxs-lookup"><span data-stu-id="0b787-106">The system calls this function every time a new mouse input event is about to be posted into a thread input queue.</span></span>

<span data-ttu-id="0b787-107">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="0b787-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="0b787-108">**LowLevelMouseProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="0b787-108">**LowLevelMouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK LowLevelMouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="0b787-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0b787-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="0b787-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="0b787-110">nCode [in]</span></span>

<span data-ttu-id="0b787-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="0b787-111">Type: **int**</span></span>

<span data-ttu-id="0b787-112">Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="0b787-112">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="0b787-113">Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="0b787-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="0b787-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b787-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="0b787-115">Valor</span><span class="sxs-lookup"><span data-stu-id="0b787-115">Value</span></span> | <span data-ttu-id="0b787-116">Significado</span><span class="sxs-lookup"><span data-stu-id="0b787-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="0b787-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="0b787-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="0b787-118">Los parámetros *wParam* e *lParam* contienen información sobre un mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="0b787-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="0b787-119">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="0b787-119">wParam [in]</span></span>

<span data-ttu-id="0b787-120">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="0b787-120">Type: **WPARAM**</span></span>

<span data-ttu-id="0b787-121">Identificador del mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="0b787-121">The identifier of the mouse message.</span></span>
<span data-ttu-id="0b787-122">Este parámetro puede ser uno de los siguientes mensajes: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) o [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span><span class="sxs-lookup"><span data-stu-id="0b787-122">This parameter can be one of the following messages: [WM_LBUTTONDOWN](/windows/desktop/inputdev/wm-lbuttondown), [WM_LBUTTONUP](/windows/desktop/inputdev/wm-lbuttonup), [WM_MOUSEMOVE](/windows/desktop/inputdev/wm-mousemove), [WM_MOUSEWHEEL](/windows/desktop/inputdev/wm-mousewheel), [WM_RBUTTONDOWN](/windows/desktop/inputdev/wm-rbuttondown) or [WM_RBUTTONUP](/windows/desktop/inputdev/wm-rbuttonup).</span></span>

### <a name="lparam-in"></a><span data-ttu-id="0b787-123">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="0b787-123">lParam [in]</span></span>

<span data-ttu-id="0b787-124">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="0b787-124">Type: **LPARAM**</span></span>

<span data-ttu-id="0b787-125">Puntero a una estructura [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) .</span><span class="sxs-lookup"><span data-stu-id="0b787-125">A pointer to an [MSLLHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-msllhookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="0b787-126">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="0b787-126">Returns</span></span>

<span data-ttu-id="0b787-127">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0b787-127">Type: **LRESULT**</span></span>

<span data-ttu-id="0b787-128">Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="0b787-128">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="0b787-129">Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_MOUSE_LL](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.</span><span class="sxs-lookup"><span data-stu-id="0b787-129">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE_LL](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="0b787-130">Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al resto de la cadena de enlace o al procedimiento de ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="0b787-130">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the rest of the hook chain or the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b787-131">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b787-131">Remarks</span></span>

<span data-ttu-id="0b787-132">Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de **WH_MOUSE_LL** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="0b787-132">An application installs the hook procedure by specifying the **WH_MOUSE_LL** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="0b787-133">Este enlace se llama en el contexto del subproceso que lo instaló.</span><span class="sxs-lookup"><span data-stu-id="0b787-133">This hook is called in the context of the thread that installed it.</span></span>
<span data-ttu-id="0b787-134">La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.</span><span class="sxs-lookup"><span data-stu-id="0b787-134">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="0b787-135">Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="0b787-135">Therefore, the thread that installed the hook must have a message loop.</span></span>

<span data-ttu-id="0b787-136">La entrada del mouse puede proviene del controlador del mouse local o de las llamadas a la función [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) .</span><span class="sxs-lookup"><span data-stu-id="0b787-136">The mouse input can come from the local mouse driver or from calls to the [mouse_event](/windows/desktop/api/winuser/nf-winuser-mouse_event) function.</span></span>
<span data-ttu-id="0b787-137">Si la entrada procede de una llamada a **mouse_event**, la entrada se "insertó".</span><span class="sxs-lookup"><span data-stu-id="0b787-137">If the input comes from a call to **mouse_event**, the input was "injected".</span></span>
<span data-ttu-id="0b787-138">Sin embargo, el enlace de **WH_MOUSE_LL** no se inserta en otro proceso.</span><span class="sxs-lookup"><span data-stu-id="0b787-138">However, the **WH_MOUSE_LL** hook is not injected into another process.</span></span>
<span data-ttu-id="0b787-139">En su lugar, el contexto vuelve a cambiar al proceso que instaló el enlace y se llama en su contexto original.</span><span class="sxs-lookup"><span data-stu-id="0b787-139">Instead, the context switches back to the process that installed the hook and it is called in its original context.</span></span>
<span data-ttu-id="0b787-140">A continuación, el contexto vuelve a la aplicación que generó el evento.</span><span class="sxs-lookup"><span data-stu-id="0b787-140">Then the context switches back to the application that generated the event.</span></span>

<span data-ttu-id="0b787-141">El procedimiento de enlace debe procesar un mensaje en menos tiempo que la entrada de datos especificada en el valor **LowLevelHooksTimeout** en la siguiente clave del registro: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span><span class="sxs-lookup"><span data-stu-id="0b787-141">The hook procedure should process a message in less time than the data entry specified in the **LowLevelHooksTimeout** value in the following registry key: **HKEY_CURRENT_USER\Control Panel\Desktop**.</span></span>

<span data-ttu-id="0b787-142">El valor se expresa en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="0b787-142">The value is in milliseconds.</span></span>
<span data-ttu-id="0b787-143">Si el procedimiento de enlace agota el tiempo de espera, el sistema pasa el mensaje al siguiente enlace.</span><span class="sxs-lookup"><span data-stu-id="0b787-143">If the hook procedure times out, the system passes the message to the next hook.</span></span>
<span data-ttu-id="0b787-144">Sin embargo, en Windows 7 y versiones posteriores, el enlace se quita de forma silenciosa sin llamar a.</span><span class="sxs-lookup"><span data-stu-id="0b787-144">However, on Windows 7 and later, the hook is silently removed without being called.</span></span>
<span data-ttu-id="0b787-145">No hay ninguna manera de que la aplicación sepa si se quita el enlace.</span><span class="sxs-lookup"><span data-stu-id="0b787-145">There is no way for the application to know whether the hook is removed.</span></span>

<span data-ttu-id="0b787-146">**Nota:**  Los enlaces de depuración no pueden realizar un seguimiento de este tipo de enlaces de mouse de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="0b787-146">**Note:**  Debug hooks cannot track this type of low level mouse hooks.</span></span>
<span data-ttu-id="0b787-147">Si la aplicación debe usar enlaces de nivel bajo, debe ejecutar los enlaces en un subproceso dedicado que pase el trabajo a un subproceso de trabajo y, a continuación, devuelva inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="0b787-147">If the application must use low level hooks, it should run the hooks on a dedicated thread that passes the work off to a worker thread and then immediately returns.</span></span>
<span data-ttu-id="0b787-148">En la mayoría de los casos en los que la aplicación necesita usar enlaces de nivel bajo, debe supervisar en su lugar la entrada sin formato.</span><span class="sxs-lookup"><span data-stu-id="0b787-148">In most cases where the application needs to use low level hooks, it should monitor raw input instead.</span></span>
<span data-ttu-id="0b787-149">Esto se debe a que la entrada sin formato puede supervisar de forma asincrónica los mensajes de teclado y del mouse que están destinados a otros subprocesos de forma más eficaz que los enlaces de bajo nivel.</span><span class="sxs-lookup"><span data-stu-id="0b787-149">This is because raw input can asynchronously monitor mouse and keyboard messages that are targeted for other threads more effectively than low level hooks can.</span></span>
<span data-ttu-id="0b787-150">Para obtener más información sobre la entrada sin formato, consulte [entrada sin formato](/windows/desktop/inputdev/raw-input).</span><span class="sxs-lookup"><span data-stu-id="0b787-150">For more information on raw input, see [Raw Input](/windows/desktop/inputdev/raw-input).</span></span>

## <a name="see-also"></a><span data-ttu-id="0b787-151">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b787-151">See also</span></span>

[<span data-ttu-id="0b787-152">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="0b787-152">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="0b787-153">mouse_event</span><span class="sxs-lookup"><span data-stu-id="0b787-153">mouse_event</span></span>](/windows/desktop/api/winuser/nf-winuser-mouse_event)

[<span data-ttu-id="0b787-154">KBDLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="0b787-154">KBDLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-kbdllhookstruct)

[<span data-ttu-id="0b787-155">MSLLHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="0b787-155">MSLLHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-msllhookstruct)

[<span data-ttu-id="0b787-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="0b787-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="0b787-157">WM_LBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="0b787-157">WM_LBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-lbuttondown)

[<span data-ttu-id="0b787-158">WM_LBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="0b787-158">WM_LBUTTONUP</span></span>](/windows/desktop/inputdev/wm-lbuttonup)

[<span data-ttu-id="0b787-159">WM_MOUSEMOVE</span><span class="sxs-lookup"><span data-stu-id="0b787-159">WM_MOUSEMOVE</span></span>](/windows/desktop/inputdev/wm-mousemove)

[<span data-ttu-id="0b787-160">WM_MOUSEWHEEL</span><span class="sxs-lookup"><span data-stu-id="0b787-160">WM_MOUSEWHEEL</span></span>](/windows/desktop/inputdev/wm-mousewheel)

[<span data-ttu-id="0b787-161">WM_RBUTTONDOWN</span><span class="sxs-lookup"><span data-stu-id="0b787-161">WM_RBUTTONDOWN</span></span>](/windows/desktop/inputdev/wm-rbuttondown)

[<span data-ttu-id="0b787-162">WM_RBUTTONUP</span><span class="sxs-lookup"><span data-stu-id="0b787-162">WM_RBUTTONUP</span></span>](/windows/desktop/inputdev/wm-rbuttonup)

[<span data-ttu-id="0b787-163">Enlaces</span><span class="sxs-lookup"><span data-stu-id="0b787-163">Hooks</span></span>](hooks.md)

[<span data-ttu-id="0b787-164">Acerca de los enlaces</span><span class="sxs-lookup"><span data-stu-id="0b787-164">About Hooks</span></span>](about-hooks.md)
