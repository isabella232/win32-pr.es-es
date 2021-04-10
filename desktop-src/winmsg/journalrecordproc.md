---
UID: ''
title: Función de devolución de llamada JournalRecordProc
description: La función registra los mensajes que el sistema elimina de la cola de mensajes del sistema.
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
ms.openlocfilehash: bc255441ca82c86542dd8dd4729564122df6c719
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "103995049"
---
# <a name="journalrecordproc-function"></a><span data-ttu-id="cfac4-103">JournalRecordProc función)</span><span class="sxs-lookup"><span data-stu-id="cfac4-103">JournalRecordProc function</span></span>

## <a name="description"></a><span data-ttu-id="cfac4-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="cfac4-104">Description</span></span>

<span data-ttu-id="cfac4-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="cfac4-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="cfac4-106">La función registra los mensajes que el sistema elimina de la cola de mensajes del sistema.</span><span class="sxs-lookup"><span data-stu-id="cfac4-106">The function records messages the system removes from the system message queue.</span></span>
<span data-ttu-id="cfac4-107">Más adelante, una aplicación puede utilizar un procedimiento de enlace [JournalPlaybackProc](journalplaybackproc.md) para reproducir los mensajes.</span><span class="sxs-lookup"><span data-stu-id="cfac4-107">Later, an application can use a [JournalPlaybackProc](journalplaybackproc.md) hook procedure to play back the messages.</span></span>

<span data-ttu-id="cfac4-108">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="cfac4-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="cfac4-109">**JournalRecordProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="cfac4-109">**JournalRecordProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK JournalRecordProc(
  _In_ int    code,
       WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="cfac4-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cfac4-110">Parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="cfac4-111">código [in]</span><span class="sxs-lookup"><span data-stu-id="cfac4-111">code [in]</span></span>

<span data-ttu-id="cfac4-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="cfac4-112">Type: **int**</span></span>

<span data-ttu-id="cfac4-113">Especifica cómo procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="cfac4-113">Specifies how to process the message.</span></span>
<span data-ttu-id="cfac4-114">Si el *código* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="cfac4-114">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="cfac4-115">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cfac4-115">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="cfac4-116">Valor</span><span class="sxs-lookup"><span data-stu-id="cfac4-116">Value</span></span> | <span data-ttu-id="cfac4-117">Significado</span><span class="sxs-lookup"><span data-stu-id="cfac4-117">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="cfac4-118">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="cfac4-118">**HC_ACTION** 0</span></span> | <span data-ttu-id="cfac4-119">El parámetro *lParam* es un puntero a una estructura [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) que contiene información sobre un mensaje que se ha quitado de la cola del sistema.</span><span class="sxs-lookup"><span data-stu-id="cfac4-119">The *lParam* parameter is a pointer to an [EVENTMSG](/windows/desktop/api/winuser/ns-winuser-eventmsg) structure containing information about a message removed from the system queue.</span></span> <span data-ttu-id="cfac4-120">El procedimiento de enlace debe registrar el contenido de la estructura copiándolos en un búfer o archivo.</span><span class="sxs-lookup"><span data-stu-id="cfac4-120">The hook procedure must record the contents of the structure by copying them to a buffer or file.</span></span> |
| <span data-ttu-id="cfac4-121">**HC_SYSMODALOFF** 5</span><span class="sxs-lookup"><span data-stu-id="cfac4-121">**HC_SYSMODALOFF** 5</span></span> | <span data-ttu-id="cfac4-122">Se ha destruido un cuadro de diálogo modal del sistema.</span><span class="sxs-lookup"><span data-stu-id="cfac4-122">A system-modal dialog box has been destroyed.</span></span> <span data-ttu-id="cfac4-123">El procedimiento de enlace debe reanudar la grabación.</span><span class="sxs-lookup"><span data-stu-id="cfac4-123">The hook procedure must resume recording.</span></span> |
| <span data-ttu-id="cfac4-124">**HC_SYSMODALON** 4</span><span class="sxs-lookup"><span data-stu-id="cfac4-124">**HC_SYSMODALON** 4</span></span> | <span data-ttu-id="cfac4-125">Se está mostrando un cuadro de diálogo modal del sistema.</span><span class="sxs-lookup"><span data-stu-id="cfac4-125">A system-modal dialog box is being displayed.</span></span> <span data-ttu-id="cfac4-126">Hasta que se destruya el cuadro de diálogo, el procedimiento de enlace debe dejar de grabar.</span><span class="sxs-lookup"><span data-stu-id="cfac4-126">Until the dialog box is destroyed, the hook procedure must stop recording.</span></span> |

### <a name="wparam"></a><span data-ttu-id="cfac4-127">wParam</span><span class="sxs-lookup"><span data-stu-id="cfac4-127">wParam</span></span>

<span data-ttu-id="cfac4-128">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="cfac4-128">Type: **WPARAM**</span></span>

<span data-ttu-id="cfac4-129">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="cfac4-129">This parameter is not used.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="cfac4-130">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="cfac4-130">lParam [in]</span></span>

<span data-ttu-id="cfac4-131">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="cfac4-131">Type: **LPARAM**</span></span>

<span data-ttu-id="cfac4-132">Puntero a una estructura **EVENTMSG** que contiene el mensaje que se va a registrar.</span><span class="sxs-lookup"><span data-stu-id="cfac4-132">A pointer to an **EVENTMSG** structure that contains the message to be recorded.</span></span>

## <a name="returns"></a><span data-ttu-id="cfac4-133">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="cfac4-133">Returns</span></span>

<span data-ttu-id="cfac4-134">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="cfac4-134">Type: **LRESULT**</span></span>

<span data-ttu-id="cfac4-135">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="cfac4-135">The return value is ignored.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfac4-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cfac4-136">Remarks</span></span>

<span data-ttu-id="cfac4-137">Un procedimiento de enlace **JournalRecordProc** debe copiar pero no modificar los mensajes.</span><span class="sxs-lookup"><span data-stu-id="cfac4-137">A **JournalRecordProc** hook procedure must copy but not modify the messages.</span></span>
<span data-ttu-id="cfac4-138">Una vez que el procedimiento de enlace devuelve el control al sistema, el mensaje continúa procesándose.</span><span class="sxs-lookup"><span data-stu-id="cfac4-138">After the hook procedure returns control to the system, the message continues to be processed.</span></span>

<span data-ttu-id="cfac4-139">Instale el procedimiento de enlace **JournalRecordProc** especificando el tipo de [WH_JOURNALRECORD](about-hooks.md) y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="cfac4-139">Install the **JournalRecordProc** hook procedure by specifying the [WH_JOURNALRECORD](about-hooks.md) type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="cfac4-140">No es necesario que un procedimiento de enlace **JournalRecordProc** esté activo en una biblioteca de vínculos dinámicos.</span><span class="sxs-lookup"><span data-stu-id="cfac4-140">A **JournalRecordProc** hook procedure does not need to live in a dynamic-link library.</span></span>
<span data-ttu-id="cfac4-141">Un procedimiento de enlace **JournalRecordProc** puede residir en la propia aplicación.</span><span class="sxs-lookup"><span data-stu-id="cfac4-141">A **JournalRecordProc** hook procedure can live in the application itself.</span></span>

<span data-ttu-id="cfac4-142">A diferencia de la mayoría de los demás procedimientos de enlace global, siempre se llama a los procedimientos de enlace **JournalRecordProc** y [JournalPlaybackProc](journalplaybackproc.md) en el contexto del subproceso que establece el enlace.</span><span class="sxs-lookup"><span data-stu-id="cfac4-142">Unlike most other global hook procedures, the **JournalRecordProc** and [JournalPlaybackProc](journalplaybackproc.md) hook procedures are always called in the context of the thread that set the hook.</span></span>

<span data-ttu-id="cfac4-143">Una aplicación que ha instalado un procedimiento de enlace de **JournalRecordProc** debe ver el código de tecla virtual [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) (que se implementa como la combinación de teclas Ctrl + Inter en la mayoría de los teclados).</span><span class="sxs-lookup"><span data-stu-id="cfac4-143">An application that has installed a **JournalRecordProc** hook procedure should watch for the [VK_CANCEL](/windows/desktop/inputdev/virtual-key-codes) virtual key code (which is implemented as the CTRL+BREAK key combination on most keyboards).</span></span>
<span data-ttu-id="cfac4-144">La aplicación debe interpretar este código de tecla virtual como una señal de que el usuario desea detener la grabación del diario.</span><span class="sxs-lookup"><span data-stu-id="cfac4-144">This virtual key code should be interpreted by the application as a signal that the user wishes to stop journal recording.</span></span>
<span data-ttu-id="cfac4-145">La aplicación debe responder finalizando la secuencia de grabación y quitando el procedimiento de enlace **JournalRecordProc** .</span><span class="sxs-lookup"><span data-stu-id="cfac4-145">The application should respond by ending the recording sequence and removing the **JournalRecordProc** hook procedure.</span></span>
<span data-ttu-id="cfac4-146">La eliminación es importante.</span><span class="sxs-lookup"><span data-stu-id="cfac4-146">Removal is important.</span></span>
<span data-ttu-id="cfac4-147">Impide que una aplicación de registro en diario bloquee el sistema al bloquearse dentro de un procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="cfac4-147">It prevents a journaling application from locking up the system by hanging inside a hook procedure.</span></span>

<span data-ttu-id="cfac4-148">Este rol como una señal para detener la grabación de journl significa que no se puede grabar una combinación de teclas CTRL + INTER.</span><span class="sxs-lookup"><span data-stu-id="cfac4-148">This role as a signal to stop journl recording means that a CTRL+BREAK key combination cannot itself be recorded.</span></span>
<span data-ttu-id="cfac4-149">Dado que la combinación de teclas CTRL + C no tiene tal rol como una señal de registro en diario, se puede grabar.</span><span class="sxs-lookup"><span data-stu-id="cfac4-149">Since the CTRL+C key combination has no such role as a journaling signal, it can be recorded.</span></span>
<span data-ttu-id="cfac4-150">Hay otras dos combinaciones de teclas que no se pueden grabar: CTRL + ESC y CTRL + ALT + SUPR.</span><span class="sxs-lookup"><span data-stu-id="cfac4-150">There are two other key combinations that cannot be recorded: CTRL+ESC and CTRL+ALT+DEL.</span></span>
<span data-ttu-id="cfac4-151">Esas dos combinaciones de teclas hacen que el sistema detenga todas las actividades de registro en diario (grabación o reproducción), quite todos los enlaces de diario y publique un [WM_CANCELJOURNAL](wm-canceljournal.md) mensaje en la aplicación de registro en diario.</span><span class="sxs-lookup"><span data-stu-id="cfac4-151">Those two key combinations cause the system to stop all journaling activities (record or playback), remove all journaling hooks, and post a [WM_CANCELJOURNAL](wm-canceljournal.md) message to the journaling application.</span></span>

## <a name="see-also"></a><span data-ttu-id="cfac4-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="cfac4-152">See also</span></span>

[<span data-ttu-id="cfac4-153">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="cfac4-153">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="cfac4-154">EVENTMSG</span><span class="sxs-lookup"><span data-stu-id="cfac4-154">EVENTMSG</span></span>](/windows/desktop/api/winuser/ns-winuser-eventmsg)

[<span data-ttu-id="cfac4-155">JournalPlaybackProc</span><span class="sxs-lookup"><span data-stu-id="cfac4-155">JournalPlaybackProc</span></span>](journalplaybackproc.md)

[<span data-ttu-id="cfac4-156">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="cfac4-156">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="cfac4-157">WM_CANCELJOURNAL</span><span class="sxs-lookup"><span data-stu-id="cfac4-157">WM_CANCELJOURNAL</span></span>](wm-canceljournal.md)

[<span data-ttu-id="cfac4-158">Enlaces</span><span class="sxs-lookup"><span data-stu-id="cfac4-158">Hooks</span></span>](hooks.md)
