---
UID: ''
title: Función de devolución de llamada JournalPlaybackProc
description: Reproduce una serie de mensajes de teclado y del mouse grabados anteriormente.
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
ms.openlocfilehash: 9bceede3cd6ab009aace4679dfb3d4d85bd37276
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "104420504"
---
# <a name="journalplaybackproc-function"></a><span data-ttu-id="353aa-103">JournalPlaybackProc función)</span><span class="sxs-lookup"><span data-stu-id="353aa-103">JournalPlaybackProc function</span></span>

## <a name="description"></a><span data-ttu-id="353aa-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="353aa-104">Description</span></span>

<span data-ttu-id="353aa-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="353aa-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="353aa-106">Normalmente, una aplicación usa esta función para reproducir una serie de mensajes del mouse y del teclado grabados previamente por el procedimiento de enlace **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="353aa-106">Typically, an application uses this function to play back a series of mouse and keyboard messages recorded previously by the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="353aa-107">Siempre que se instale un procedimiento de enlace **JournalPlaybackProc** , se deshabilitará la entrada normal del mouse y del teclado.</span><span class="sxs-lookup"><span data-stu-id="353aa-107">As long as a **JournalPlaybackProc** hook procedure is installed, regular mouse and keyboard input is disabled.</span></span>

<span data-ttu-id="353aa-108">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="353aa-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="353aa-109">**JournalPlaybackProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="353aa-109">**JournalPlaybackProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalPlaybackProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="353aa-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="353aa-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="353aa-111">código [in]</span><span class="sxs-lookup"><span data-stu-id="353aa-111">code [in]</span></span>

<span data-ttu-id="353aa-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="353aa-112">Type: **int**</span></span>

<span data-ttu-id="353aa-113">Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="353aa-113">A code the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="353aa-114">Si el *código* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="353aa-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="353aa-115">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="353aa-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="353aa-116">Valor</span><span class="sxs-lookup"><span data-stu-id="353aa-116">Value</span></span> | <span data-ttu-id="353aa-117">Significado</span><span class="sxs-lookup"><span data-stu-id="353aa-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="353aa-118">**HC_GETNEXT** 1</span><span class="sxs-lookup"><span data-stu-id="353aa-118">**HC_GETNEXT** 1</span></span> | <span data-ttu-id="353aa-119">El procedimiento de enlace debe copiar el mouse actual o el mensaje de teclado en la estructura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) señalada por el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="353aa-119">The hook procedure must copy the current mouse or keyboard message to the [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure pointed to by the *lParam* parameter.</span></span> |
| <span data-ttu-id="353aa-120">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="353aa-120">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="353aa-121">Una aplicación ha llamado a la función [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) con wRemoveMsg establecido en **PM_NOREMOVE**, lo que indica que el mensaje no se quita de la cola de mensajes después del procesamiento de **PeekMessage** .</span><span class="sxs-lookup"><span data-stu-id="353aa-121">An application has called the [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function with wRemoveMsg set to **PM_NOREMOVE**, indicating that the message is not removed from the message queue after **PeekMessage** processing.</span></span> |
| <span data-ttu-id="353aa-122">**HC_NOREMOVE** 2</span><span class="sxs-lookup"><span data-stu-id="353aa-122">**HC_NOREMOVE** 2</span></span> | <span data-ttu-id="353aa-123">El procedimiento de enlace debe prepararse para copiar el siguiente mensaje del mouse o del teclado en la estructura **EVENTMSG** a la que apunta *lParam*.</span><span class="sxs-lookup"><span data-stu-id="353aa-123">The hook procedure must prepare to copy the next mouse or keyboard message to the **EVENTMSG** structure pointed to by *lParam*.</span></span> <span data-ttu-id="353aa-124">Al recibir el código **HC_GETNEXT** , el procedimiento de enlace debe copiar el mensaje en la estructura.</span><span class="sxs-lookup"><span data-stu-id="353aa-124">Upon receiving the **HC_GETNEXT** code, the hook procedure must copy the message to the structure.</span></span> |
| <span data-ttu-id="353aa-125">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="353aa-125">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="353aa-126">Se ha destruido un cuadro de diálogo modal del sistema.</span><span class="sxs-lookup"><span data-stu-id="353aa-126">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="353aa-127">El procedimiento de enlace debe reanudar la reproducción de los mensajes.</span><span class="sxs-lookup"><span data-stu-id="353aa-127">The hook procedure must resume playing back the messages.</span></span> |
| <span data-ttu-id="353aa-128">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="353aa-128">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="353aa-129">Se está mostrando un cuadro de diálogo modal del sistema.</span><span class="sxs-lookup"><span data-stu-id="353aa-129">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="353aa-130">Hasta que se destruya el cuadro de diálogo, el procedimiento de enlace debe detener la reproducción de mensajes.</span><span class="sxs-lookup"><span data-stu-id="353aa-130">Until the dialog box is destroyed, the hook procedure must stop playing back messages.</span></span> |

### <a name="wparam"></a><span data-ttu-id="353aa-131">wParam</span><span class="sxs-lookup"><span data-stu-id="353aa-131">wParam</span></span>

<span data-ttu-id="353aa-132">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="353aa-132">Type: **WPARAM**</span></span>

<span data-ttu-id="353aa-133">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="353aa-133">This parameter is not used.</span></span>

### <a name="lparam"></a><span data-ttu-id="353aa-134">lParam</span><span class="sxs-lookup"><span data-stu-id="353aa-134">lParam</span></span>

<span data-ttu-id="353aa-135">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="353aa-135">Type: **LPARAM**</span></span>

<span data-ttu-id="353aa-136">Puntero a una estructura **EVENTMSG** que representa un mensaje procesado por el procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="353aa-136">A pointer to an **EVENTMSG** structure that represents a message being processed by the hook procedure.</span></span>
<span data-ttu-id="353aa-137">Este parámetro solo es válido cuando el parámetro de *código* es **HC_GETNEXT**.</span><span class="sxs-lookup"><span data-stu-id="353aa-137">This parameter is valid only when the *code* parameter is **HC_GETNEXT**.</span></span>

## <a name="returns"></a><span data-ttu-id="353aa-138">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="353aa-138">Returns</span></span>

<span data-ttu-id="353aa-139">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="353aa-139">Type: **LRESULT**</span></span>

<span data-ttu-id="353aa-140">Para que el sistema espere antes de procesar el mensaje, el valor devuelto debe ser la cantidad de tiempo, en ciclos de reloj, que el sistema debe esperar.</span><span class="sxs-lookup"><span data-stu-id="353aa-140">To have the system wait before processing the message, the return value must be the amount of time, in clock ticks, that the system should wait.</span></span>

<span data-ttu-id="353aa-141">(Este valor se puede calcular calculando la diferencia entre los miembros de hora de los mensajes de entrada actuales y anteriores).</span><span class="sxs-lookup"><span data-stu-id="353aa-141">(This value can be computed by calculating the difference between the time members in the current and previous input messages.)</span></span>

<span data-ttu-id="353aa-142">Para procesar el mensaje inmediatamente, el valor devuelto debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="353aa-142">To process the message immediately, the return value should be zero.</span></span> <span data-ttu-id="353aa-143">El valor devuelto se usa solo si el código de enlace es **HC_GETNEXT**; de lo contrario, se omite.</span><span class="sxs-lookup"><span data-stu-id="353aa-143">The return value is used only if the hook code is **HC_GETNEXT**; otherwise, it is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="353aa-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="353aa-144">Remarks</span></span>

<span data-ttu-id="353aa-145">Un procedimiento de enlace **JournalPlaybackProc** debe copiar un mensaje de entrada en el parámetro *lParam* .</span><span class="sxs-lookup"><span data-stu-id="353aa-145">A **JournalPlaybackProc** hook procedure should copy an input message to The *lParam* parameter.</span></span>
<span data-ttu-id="353aa-146">El mensaje se debe haber registrado previamente mediante un procedimiento de enlace **JournalRecordProc** , que no debe modificar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="353aa-146">The message must have been previously recorded by using a **JournalRecordProc** hook procedure, which should not modify the message.</span></span>

<span data-ttu-id="353aa-147">Para recuperar el mismo mensaje una y otra vez, se puede llamar varias veces al procedimiento de enlace con el parámetro de *código* establecido en **HC_GETNEXT** sin una llamada intermedia con el *código* establecido en **HC_SKIP**.</span><span class="sxs-lookup"><span data-stu-id="353aa-147">To retrieve the same message over and over, the hook procedure can be called several times with the *code* parameter set to **HC_GETNEXT** without an intervening call with *code* set to **HC_SKIP**.</span></span>

<span data-ttu-id="353aa-148">Si el *código* es **HC_GETNEXT** y el valor devuelto es mayor que cero, el sistema se suspende durante el número de milisegundos especificado por el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="353aa-148">If *code* is **HC_GETNEXT** and the return value is greater than zero, the system sleeps for the number of milliseconds specified by the return value.</span></span> <span data-ttu-id="353aa-149">Cuando el sistema continúa, llama de nuevo al procedimiento de enlace con el *código* establecido en **HC_GETNEXT** para recuperar el mismo mensaje.</span><span class="sxs-lookup"><span data-stu-id="353aa-149">When the system continues, it calls the hook procedure again with *code* set to **HC_GETNEXT** to retrieve the same message.</span></span>
<span data-ttu-id="353aa-150">El valor devuelto de esta nueva llamada a **JournalPlaybackProc** debe ser cero; de lo contrario, el sistema volverá a entrar en suspensión durante el número de milisegundos especificado por el valor devuelto, llamará de nuevo a **JournalPlaybackProc** , etc.</span><span class="sxs-lookup"><span data-stu-id="353aa-150">The return value from this new call to **JournalPlaybackProc** should be zero; otherwise, the system will go back to sleep for the number of milliseconds specified by the return value, call **JournalPlaybackProc** again, and so on.</span></span>
<span data-ttu-id="353aa-151">Parecerá que el sistema no responde.</span><span class="sxs-lookup"><span data-stu-id="353aa-151">The system will appear to be not responding.</span></span>

<span data-ttu-id="353aa-152">A diferencia de la mayoría de los demás procedimientos de enlace global, siempre se llama a los procedimientos de enlace **JournalRecordProc** y **JournalPlaybackProc** en el contexto del subproceso que establece el enlace.</span><span class="sxs-lookup"><span data-stu-id="353aa-152">Unlike most other global hook procedures, the **JournalRecordProc** and **JournalPlaybackProc** hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="353aa-153">Una vez que el procedimiento de enlace devuelve el control al sistema, el mensaje continúa procesándose.</span><span class="sxs-lookup"><span data-stu-id="353aa-153">After the hook procedure returns control to the system, the message continues to be processed.</span></span> <span data-ttu-id="353aa-154">Si el *código* es **HC_SKIP**, el procedimiento de enlace debe prepararse para devolver el siguiente mensaje de evento registrado en la siguiente llamada.</span><span class="sxs-lookup"><span data-stu-id="353aa-154">If *code* is **HC_SKIP**, the hook procedure must prepare to return the next recorded event message on its next call.</span></span>

<span data-ttu-id="353aa-155">Instale el procedimiento de enlace **JournalPlaybackProc** especificando el tipo de [WH_JOURNALPLAYBACK](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="353aa-155">Install the **JournalPlaybackProc** hook procedure by specifying the [WH_JOURNALPLAYBACK](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="353aa-156">Si el usuario presiona CTRL + ESC o CTRL + ALT + Supr durante la reproducción del diario, el sistema detiene la reproducción, desenlaza el procedimiento de reproducción del diario y envía un mensaje de [WM_CANCELJOURNAL](wm-canceljournal.md) a la aplicación de registro en diario.</span><span class="sxs-lookup"><span data-stu-id="353aa-156">If the user presses CTRL+ESC OR CTRL+ALT+DEL during journal playback, the system stops the playback, unhooks the journal playback procedure, and posts a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

<span data-ttu-id="353aa-157">Si el procedimiento de enlace devuelve un mensaje en el intervalo **WM_KEYFIRST** a **WM_KEYLAST**, se aplican las condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="353aa-157">If the hook procedure returns a message in the range **WM_KEYFIRST** to **WM_KEYLAST**, the following conditions apply:</span></span>

* <span data-ttu-id="353aa-158">El miembro **paraml** de la estructura **EVENTMSG** especifica el código de tecla virtual de la tecla que se presionó.</span><span class="sxs-lookup"><span data-stu-id="353aa-158">The **paramL** member of the **EVENTMSG** structure specifies the virtual key code of the key that was pressed.</span></span>
* <span data-ttu-id="353aa-159">El miembro **paramH** de la estructura **EVENTMSG** especifica el código de recorrido.</span><span class="sxs-lookup"><span data-stu-id="353aa-159">The **paramH** member of the **EVENTMSG** structure specifies the scan code.</span></span>
* <span data-ttu-id="353aa-160">No hay ninguna manera de especificar un número de repeticiones.</span><span class="sxs-lookup"><span data-stu-id="353aa-160">There's no way to specify a repeat count.</span></span>
<span data-ttu-id="353aa-161">Siempre se toma el evento para representar un evento de clave.</span><span class="sxs-lookup"><span data-stu-id="353aa-161">The event is always taken to represent one key event.</span></span>

## <a name="see-also"></a><span data-ttu-id="353aa-162">Vea también</span><span class="sxs-lookup"><span data-stu-id="353aa-162">See also</span></span>

[<span data-ttu-id="353aa-163">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="353aa-163">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="353aa-164">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="353aa-164">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="353aa-165">JournalRecordProc</span><span class="sxs-lookup"><span data-stu-id="353aa-165">JournalRecordProc</span></span>](journalrecordproc.md)

[<span data-ttu-id="353aa-166">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="353aa-166">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="353aa-167">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="353aa-167">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="353aa-168">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="353aa-168">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="353aa-169">Enlaces</span><span class="sxs-lookup"><span data-stu-id="353aa-169">Hooks</span></span>](hooks.md)
