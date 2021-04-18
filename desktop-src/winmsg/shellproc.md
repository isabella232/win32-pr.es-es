---
UID: ''
title: Función de devolución de llamada ShellProc
description: La función recibe notificaciones de eventos de Shell del sistema.
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
ms.openlocfilehash: 4add84011745aeb61659c39775b94fed91028d83
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105704929"
---
# <a name="shellproc-function"></a><span data-ttu-id="256c2-103">ShellProc función)</span><span class="sxs-lookup"><span data-stu-id="256c2-103">ShellProc function</span></span>

## <a name="description"></a><span data-ttu-id="256c2-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="256c2-104">Description</span></span>

<span data-ttu-id="256c2-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="256c2-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="256c2-106">La función recibe notificaciones de eventos de Shell del sistema.</span><span class="sxs-lookup"><span data-stu-id="256c2-106">The function receives notifications of Shell events from the system.</span></span>

<span data-ttu-id="256c2-107">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="256c2-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="256c2-108">**ShellProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="256c2-108">**ShellProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK ShellProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="256c2-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="256c2-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="256c2-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="256c2-110">nCode [in]</span></span>

<span data-ttu-id="256c2-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="256c2-111">Type: **int**</span></span>

<span data-ttu-id="256c2-112">Código de enlace.</span><span class="sxs-lookup"><span data-stu-id="256c2-112">The hook code.</span></span>
<span data-ttu-id="256c2-113">Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="256c2-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="256c2-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="256c2-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="256c2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="256c2-115">Value</span></span> | <span data-ttu-id="256c2-116">Significado</span><span class="sxs-lookup"><span data-stu-id="256c2-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="256c2-117">**HSHELL_ACCESSIBILITYSTATE** 11</span><span class="sxs-lookup"><span data-stu-id="256c2-117">**HSHELL_ACCESSIBILITYSTATE** 11</span></span> | <span data-ttu-id="256c2-118">El estado de accesibilidad ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="256c2-118">The accessibility state has changed.</span></span> |
| <span data-ttu-id="256c2-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span><span class="sxs-lookup"><span data-stu-id="256c2-119">**HSHELL_ACTIVATESHELLWINDOW** 3</span></span> | <span data-ttu-id="256c2-120">El shell debe activar su ventana principal.</span><span class="sxs-lookup"><span data-stu-id="256c2-120">The shell should activate its main window.</span></span> |
| <span data-ttu-id="256c2-121">**HSHELL_APPCOMMAND** 12</span><span class="sxs-lookup"><span data-stu-id="256c2-121">**HSHELL_APPCOMMAND** 12</span></span> | <span data-ttu-id="256c2-122">El usuario completó un evento de entrada (por ejemplo, presionó un botón de comando de la aplicación en el mouse o una tecla de comando de la aplicación en el teclado) y la aplicación no controló el mensaje de [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) generado por dicha entrada.</span><span class="sxs-lookup"><span data-stu-id="256c2-122">The user completed an input event (for example, pressed an application command button on the mouse or an application command key on the keyboard), and the application did not handle the [WM_APPCOMMAND](/windows/desktop/inputdev/wm-appcommand) message generated by that input.</span></span> <span data-ttu-id="256c2-123">Si el procedimiento de Shell controla el mensaje de [WM_COMMAND](/windows/desktop/menurc/wm-command) , no debe llamar a **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="256c2-123">If the Shell procedure handles the [WM_COMMAND](/windows/desktop/menurc/wm-command) message, it should not call **CallNextHookEx**.</span></span> <span data-ttu-id="256c2-124">Vea la sección valor devuelto para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="256c2-124">See the Return Value section for more information.</span></span> |
| <span data-ttu-id="256c2-125">**HSHELL_GETMINRECT** 5</span><span class="sxs-lookup"><span data-stu-id="256c2-125">**HSHELL_GETMINRECT** 5</span></span> | <span data-ttu-id="256c2-126">Una ventana está minimizada o maximizada.</span><span class="sxs-lookup"><span data-stu-id="256c2-126">A window is being minimized or maximized.</span></span> <span data-ttu-id="256c2-127">El sistema necesita las coordenadas del rectángulo minimizado para la ventana.</span><span class="sxs-lookup"><span data-stu-id="256c2-127">The system needs the coordinates of the minimized rectangle for the window.</span></span> |
| <span data-ttu-id="256c2-128">**HSHELL_LANGUAGE** 8</span><span class="sxs-lookup"><span data-stu-id="256c2-128">**HSHELL_LANGUAGE** 8</span></span> | <span data-ttu-id="256c2-129">El idioma del teclado ha cambiado o se ha cargado una nueva distribución del teclado.</span><span class="sxs-lookup"><span data-stu-id="256c2-129">Keyboard language was changed or a new keyboard layout was loaded.</span></span> |
| <span data-ttu-id="256c2-130">**HSHELL_REDRAW** 6</span><span class="sxs-lookup"><span data-stu-id="256c2-130">**HSHELL_REDRAW** 6</span></span> | <span data-ttu-id="256c2-131">Se ha redibujado el título de una ventana en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="256c2-131">The title of a window in the task bar has been redrawn.</span></span> |
| <span data-ttu-id="256c2-132">**HSHELL_TASKMAN** 7</span><span class="sxs-lookup"><span data-stu-id="256c2-132">**HSHELL_TASKMAN** 7</span></span> | <span data-ttu-id="256c2-133">El usuario ha seleccionado la lista de tareas.</span><span class="sxs-lookup"><span data-stu-id="256c2-133">The user has selected the task list.</span></span> <span data-ttu-id="256c2-134">Una aplicación de Shell que proporciona una lista de tareas debe devolver **true** para impedir que Windows inicie su lista de tareas.</span><span class="sxs-lookup"><span data-stu-id="256c2-134">A shell application that provides a task list should return **TRUE** to prevent Windows from starting its task list.</span></span> |
| <span data-ttu-id="256c2-135">**HSHELL_WINDOWACTIVATED** 4</span><span class="sxs-lookup"><span data-stu-id="256c2-135">**HSHELL_WINDOWACTIVATED** 4</span></span> | <span data-ttu-id="256c2-136">La activación ha cambiado a otra ventana sin propiedad de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="256c2-136">The activation has changed to a different top-level, unowned window.</span></span> |
| <span data-ttu-id="256c2-137">**HSHELL_WINDOWCREATED** 1</span><span class="sxs-lookup"><span data-stu-id="256c2-137">**HSHELL_WINDOWCREATED** 1</span></span> | <span data-ttu-id="256c2-138">Se ha creado una ventana sin propiedad de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="256c2-138">A top-level, unowned window has been created.</span></span> <span data-ttu-id="256c2-139">La ventana existe cuando el sistema llama a este enlace.</span><span class="sxs-lookup"><span data-stu-id="256c2-139">The window exists when the system calls this hook.</span></span> |
| <span data-ttu-id="256c2-140">**HSHELL_WINDOWDESTROYED** 2</span><span class="sxs-lookup"><span data-stu-id="256c2-140">**HSHELL_WINDOWDESTROYED** 2</span></span> | <span data-ttu-id="256c2-141">Una ventana sin propiedad de nivel superior está a punto de ser destruida.</span><span class="sxs-lookup"><span data-stu-id="256c2-141">A top-level, unowned window is about to be destroyed.</span></span> <span data-ttu-id="256c2-142">La ventana todavía existe cuando el sistema llama a este enlace.</span><span class="sxs-lookup"><span data-stu-id="256c2-142">The window still exists when the system calls this hook.</span></span> |
| <span data-ttu-id="256c2-143">**HSHELL_WINDOWREPLACED** 13</span><span class="sxs-lookup"><span data-stu-id="256c2-143">**HSHELL_WINDOWREPLACED** 13</span></span> | <span data-ttu-id="256c2-144">Se está reemplazando una ventana de nivel superior.</span><span class="sxs-lookup"><span data-stu-id="256c2-144">A top-level window is being replaced.</span></span> <span data-ttu-id="256c2-145">La ventana existe cuando el sistema llama a este enlace.</span><span class="sxs-lookup"><span data-stu-id="256c2-145">The window exists when the system calls this hook.</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="256c2-146">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="256c2-146">wParam [in]</span></span>

<span data-ttu-id="256c2-147">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="256c2-147">Type: **WPARAM**</span></span>

<span data-ttu-id="256c2-148">Este parámetro depende del valor del parámetro *nCode* , tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="256c2-148">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="256c2-149">nCode</span><span class="sxs-lookup"><span data-stu-id="256c2-149">nCode</span></span> | <span data-ttu-id="256c2-150">wParam</span><span class="sxs-lookup"><span data-stu-id="256c2-150">wParam</span></span> |
|-------|---------|
| <span data-ttu-id="256c2-151">**HSHELL_ACCESSIBILITYSTATE**</span><span class="sxs-lookup"><span data-stu-id="256c2-151">**HSHELL_ACCESSIBILITYSTATE**</span></span> | <span data-ttu-id="256c2-152">Indica qué característica de accesibilidad ha cambiado de estado.</span><span class="sxs-lookup"><span data-stu-id="256c2-152">Indicates which accessibility feature has changed state.</span></span> <span data-ttu-id="256c2-153">Este valor es uno de los siguientes: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS** o **ACCESS_STICKYKEYS**.</span><span class="sxs-lookup"><span data-stu-id="256c2-153">This value is one of the following: **ACCESS_FILTERKEYS**, **ACCESS_MOUSEKEYS**, or **ACCESS_STICKYKEYS**.</span></span> |
| <span data-ttu-id="256c2-154">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="256c2-154">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="256c2-155">Indica dónde se envió originalmente el mensaje de **WM_APPCOMMAND** ; por ejemplo, el identificador de una ventana.</span><span class="sxs-lookup"><span data-stu-id="256c2-155">Indicates where the **WM_APPCOMMAND** message was originally sent; for example, the handle to a window.</span></span> <span data-ttu-id="256c2-156">Para obtener más información, vea el parámetro cmd en **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="256c2-156">For more information, see cmd parameter in **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="256c2-157">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="256c2-157">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="256c2-158">Identificador de la ventana minimizada o maximizada.</span><span class="sxs-lookup"><span data-stu-id="256c2-158">A handle to the minimized or maximized window.</span></span> |
| <span data-ttu-id="256c2-159">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="256c2-159">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="256c2-160">Identificador de la ventana.</span><span class="sxs-lookup"><span data-stu-id="256c2-160">A handle to the window.</span></span> |
| <span data-ttu-id="256c2-161">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="256c2-161">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="256c2-162">Identificador de la ventana redibujada.</span><span class="sxs-lookup"><span data-stu-id="256c2-162">A handle to the redrawn window.</span></span> |
| <span data-ttu-id="256c2-163">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="256c2-163">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="256c2-164">Identificador de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="256c2-164">A handle to the activated window.</span></span> |
| <span data-ttu-id="256c2-165">**HSHELL_WINDOWCREATED**</span><span class="sxs-lookup"><span data-stu-id="256c2-165">**HSHELL_WINDOWCREATED**</span></span> | <span data-ttu-id="256c2-166">Identificador de la ventana creada.</span><span class="sxs-lookup"><span data-stu-id="256c2-166">A handle to the created window.</span></span> |
| <span data-ttu-id="256c2-167">**HSHELL_WINDOWDESTROYED**</span><span class="sxs-lookup"><span data-stu-id="256c2-167">**HSHELL_WINDOWDESTROYED**</span></span> | <span data-ttu-id="256c2-168">Identificador de la ventana destruida.</span><span class="sxs-lookup"><span data-stu-id="256c2-168">A handle to the destroyed window.</span></span> |
| <span data-ttu-id="256c2-169">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="256c2-169">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="256c2-170">Identificador de la ventana que se va a reemplazar.</span><span class="sxs-lookup"><span data-stu-id="256c2-170">A handle to the window being replaced.</span></span> <span data-ttu-id="256c2-171">Windows 2000: no compatible.</span><span class="sxs-lookup"><span data-stu-id="256c2-171">Windows 2000:  Not supported.</span></span> |

### <a name="lparam-in"></a><span data-ttu-id="256c2-172">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="256c2-172">lParam [in]</span></span>

<span data-ttu-id="256c2-173">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="256c2-173">Type: **LPARAM**</span></span>

<span data-ttu-id="256c2-174">Este parámetro depende del valor del parámetro *nCode* , tal y como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="256c2-174">This parameter depends on the value of the *nCode* parameter, as shown in the following table.</span></span>

| <span data-ttu-id="256c2-175">nCode</span><span class="sxs-lookup"><span data-stu-id="256c2-175">nCode</span></span> | <span data-ttu-id="256c2-176">lParam</span><span class="sxs-lookup"><span data-stu-id="256c2-176">lParam</span></span> |
|-------|---------|
| <span data-ttu-id="256c2-177">**HSHELL_APPCOMMAND**</span><span class="sxs-lookup"><span data-stu-id="256c2-177">**HSHELL_APPCOMMAND**</span></span> | <span data-ttu-id="256c2-178">`GET_APPCOMMAND_LPARAM(lParam)` es el comando de aplicación correspondiente al evento de entrada.</span><span class="sxs-lookup"><span data-stu-id="256c2-178">`GET_APPCOMMAND_LPARAM(lParam)` is the application command corresponding to the input event.</span></span> <span data-ttu-id="256c2-179">`GET_DEVICE_LPARAM(lParam)` indica qué generó el evento de entrada; por ejemplo, el mouse o el teclado.</span><span class="sxs-lookup"><span data-stu-id="256c2-179">`GET_DEVICE_LPARAM(lParam)` indicates what generated the input event; for example, the mouse or keyboard.</span></span> <span data-ttu-id="256c2-180">Para obtener más información, vea la descripción del parámetro *uDevice* en **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="256c2-180">For more information, see the *uDevice* parameter description under **WM_APPCOMMAND**.</span></span> <span data-ttu-id="256c2-181">`GET_FLAGS_LPARAM(lParam)` depende del valor de *cmd* en **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="256c2-181">`GET_FLAGS_LPARAM(lParam)` depends on the value of *cmd* in **WM_APPCOMMAND**.</span></span> <span data-ttu-id="256c2-182">Por ejemplo, podría indicar qué teclas virtuales se mantuvieron presionadas cuando el mensaje de **WM_APPCOMMAND** se envió originalmente.</span><span class="sxs-lookup"><span data-stu-id="256c2-182">For example, it might indicate which virtual keys were held down when the **WM_APPCOMMAND** message was originally sent.</span></span> <span data-ttu-id="256c2-183">Para obtener más información, consulte el parámetro *dwCmdFlags* Description en **WM_APPCOMMAND**.</span><span class="sxs-lookup"><span data-stu-id="256c2-183">For more information, see the *dwCmdFlags* description parameter under **WM_APPCOMMAND**.</span></span> |
| <span data-ttu-id="256c2-184">**HSHELL_GETMINRECT**</span><span class="sxs-lookup"><span data-stu-id="256c2-184">**HSHELL_GETMINRECT**</span></span> | <span data-ttu-id="256c2-185">Puntero a una estructura [Rect](/previous-versions/dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="256c2-185">A pointer to a [RECT](/previous-versions/dd162897(v=vs.85)) structure.</span></span> |
| <span data-ttu-id="256c2-186">**HSHELL_LANGUAGE**</span><span class="sxs-lookup"><span data-stu-id="256c2-186">**HSHELL_LANGUAGE**</span></span> | <span data-ttu-id="256c2-187">Identificador de una distribución del teclado.</span><span class="sxs-lookup"><span data-stu-id="256c2-187">A handle to a keyboard layout.</span></span> |
| <span data-ttu-id="256c2-188">**HSHELL_MONITORCHANGED**</span><span class="sxs-lookup"><span data-stu-id="256c2-188">**HSHELL_MONITORCHANGED**</span></span> | <span data-ttu-id="256c2-189">Identificador de la ventana que se ha desplace a otro monitor.</span><span class="sxs-lookup"><span data-stu-id="256c2-189">A handle to the window that moved to a different monitor.</span></span> |
| <span data-ttu-id="256c2-190">**HSHELL_REDRAW**</span><span class="sxs-lookup"><span data-stu-id="256c2-190">**HSHELL_REDRAW**</span></span> | <span data-ttu-id="256c2-191">El valor es **true** si la ventana parpadea o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="256c2-191">The value is **TRUE** if the window is flashing, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="256c2-192">**HSHELL_WINDOWACTIVATED**</span><span class="sxs-lookup"><span data-stu-id="256c2-192">**HSHELL_WINDOWACTIVATED**</span></span> | <span data-ttu-id="256c2-193">El valor es TRUE si la ventana está en modo de pantalla completa o **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="256c2-193">The value is TRUE if the window is in full-screen mode, or **FALSE** otherwise.</span></span> |
| <span data-ttu-id="256c2-194">**HSHELL_WINDOWREPLACED**</span><span class="sxs-lookup"><span data-stu-id="256c2-194">**HSHELL_WINDOWREPLACED**</span></span> | <span data-ttu-id="256c2-195">Identificador de la nueva ventana.</span><span class="sxs-lookup"><span data-stu-id="256c2-195">A handle to the new window.</span></span> <span data-ttu-id="256c2-196">Windows 2000: no compatible.</span><span class="sxs-lookup"><span data-stu-id="256c2-196">Windows 2000:  Not supported.</span></span> |

## <a name="returns"></a><span data-ttu-id="256c2-197">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="256c2-197">Returns</span></span>

<span data-ttu-id="256c2-198">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="256c2-198">Type: **LRESULT**</span></span>

<span data-ttu-id="256c2-199">El valor devuelto debe ser cero a menos que el valor de nCode sea **HSHELL_APPCOMMAND** y el procedimiento de Shell controle el mensaje de **WM_COMMAND** .</span><span class="sxs-lookup"><span data-stu-id="256c2-199">The return value should be zero unless the value of nCode is **HSHELL_APPCOMMAND** and the shell procedure handles the **WM_COMMAND** message.</span></span>
<span data-ttu-id="256c2-200">En este caso, el valor devuelto debe ser distinto de cero.</span><span class="sxs-lookup"><span data-stu-id="256c2-200">In this case, the return should be nonzero.</span></span>

## <a name="remarks"></a><span data-ttu-id="256c2-201">Observaciones</span><span class="sxs-lookup"><span data-stu-id="256c2-201">Remarks</span></span>

<span data-ttu-id="256c2-202">Instale este procedimiento de enlace especificando el tipo de enlace de [WH_SHELL](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="256c2-202">Install this hook procedure by specifying the [WH_SHELL](about-hooks.md) hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="256c2-203">Vea también</span><span class="sxs-lookup"><span data-stu-id="256c2-203">See also</span></span>

[<span data-ttu-id="256c2-204">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="256c2-204">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="256c2-205">SendMessage</span><span class="sxs-lookup"><span data-stu-id="256c2-205">SendMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-sendmessage)

[<span data-ttu-id="256c2-206">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="256c2-206">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="256c2-207">WM_APPCOMMAND</span><span class="sxs-lookup"><span data-stu-id="256c2-207">WM_APPCOMMAND</span></span>](/windows/desktop/inputdev/wm-appcommand)

[<span data-ttu-id="256c2-208">WM_COMMAND</span><span class="sxs-lookup"><span data-stu-id="256c2-208">WM_COMMAND</span></span>](/windows/desktop/menurc/wm-command)

[<span data-ttu-id="256c2-209">Enlaces</span><span class="sxs-lookup"><span data-stu-id="256c2-209">Hooks</span></span>](hooks.md)
