---
UID: ''
title: Función de devolución de llamada GetMsgProc
description: El sistema llama a esta función cuando una función de mensaje recibe un mensaje de una cola de mensajes de aplicación.
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
ms.openlocfilehash: aa055e4184cdc9be5bb60a421ad5937bbfd15393
ms.sourcegitcommit: 4c00910ed754d7d0a68c9a833751d714c06e3b39
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/05/2021
ms.locfileid: "105696062"
---
# <a name="getmsgproc-function"></a><span data-ttu-id="20237-103">GetMsgProc función)</span><span class="sxs-lookup"><span data-stu-id="20237-103">GetMsgProc function</span></span>

## <a name="-description"></a><span data-ttu-id="20237-104">-Descripción</span><span class="sxs-lookup"><span data-stu-id="20237-104">-description</span></span>

<span data-ttu-id="20237-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="20237-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span> <span data-ttu-id="20237-106">El sistema llama a esta función siempre que la función [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) recupere un mensaje de una cola de mensajes de aplicación.</span><span class="sxs-lookup"><span data-stu-id="20237-106">The system calls this function whenever the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function has retrieved a message from an application message queue.</span></span>
<span data-ttu-id="20237-107">Antes de devolver el mensaje recuperado al autor de la llamada, el sistema pasa el mensaje al procedimiento de enlace.</span><span class="sxs-lookup"><span data-stu-id="20237-107">Before returning the retrieved message to the caller, the system passes the message to the hook procedure.</span></span>

<span data-ttu-id="20237-108">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="20237-108">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="20237-109">**GetMsgProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="20237-109">**GetMsgProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK GetMsgProc(
  _In_ int    code,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="-parameters"></a><span data-ttu-id="20237-110">parámetros de</span><span class="sxs-lookup"><span data-stu-id="20237-110">-parameters</span></span>

### <a name="code-in"></a><span data-ttu-id="20237-111">código [in]</span><span class="sxs-lookup"><span data-stu-id="20237-111">code [in]</span></span>

<span data-ttu-id="20237-112">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="20237-112">Type: **int**</span></span>

<span data-ttu-id="20237-113">Especifica si el procedimiento de enlace debe procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="20237-113">Specifies whether the hook procedure must process the message.</span></span>
<span data-ttu-id="20237-114">Si el *código* es **HC_ACTION**, el procedimiento de enlace debe procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="20237-114">If *code* is **HC_ACTION**, the hook procedure must process the message.</span></span>
<span data-ttu-id="20237-115">Si el *código* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="20237-115">If *code* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>

### <a name="wparam-in"></a><span data-ttu-id="20237-116">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="20237-116">wParam [in]</span></span>

<span data-ttu-id="20237-117">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="20237-117">Type: **WPARAM**</span></span>

<span data-ttu-id="20237-118">Especifica si el mensaje se ha quitado de la cola.</span><span class="sxs-lookup"><span data-stu-id="20237-118">Specifies whether the message has been removed from the queue.</span></span>
<span data-ttu-id="20237-119">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="20237-119">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="20237-120">Valor</span><span class="sxs-lookup"><span data-stu-id="20237-120">Value</span></span> | <span data-ttu-id="20237-121">Significado</span><span class="sxs-lookup"><span data-stu-id="20237-121">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="20237-122">**PM_NOREMOVE** 0x0000</span><span class="sxs-lookup"><span data-stu-id="20237-122">**PM_NOREMOVE** 0x0000</span></span> | <span data-ttu-id="20237-123">El mensaje no se ha quitado de la cola.</span><span class="sxs-lookup"><span data-stu-id="20237-123">The message has not been removed from the queue.</span></span> <span data-ttu-id="20237-124">(Una aplicación llamada la función **PeekMessage** , que especifica la marca **PM_NOREMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="20237-124">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |
| <span data-ttu-id="20237-125">**PM_REMOVE** 0x0001</span><span class="sxs-lookup"><span data-stu-id="20237-125">**PM_REMOVE** 0x0001</span></span> | <span data-ttu-id="20237-126">El mensaje se ha quitado de la cola.</span><span class="sxs-lookup"><span data-stu-id="20237-126">The message has been removed from the queue.</span></span> <span data-ttu-id="20237-127">(Una aplicación llamada **GetMessage**, o llamada a la función  **PeekMessage** , que especifica la marca de **PM_REMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="20237-127">(An application called **GetMessage**, or it called the  **PeekMessage** function, specifying the **PM_REMOVE** flag.)</span></span>|

### <a name="lparam-in"></a><span data-ttu-id="20237-128">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="20237-128">lParam [in]</span></span>

<span data-ttu-id="20237-129">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="20237-129">Type: **LPARAM**</span></span>

<span data-ttu-id="20237-130">Puntero a una estructura [MSG](/windows/desktop/api/winuser/ns-winuser-msg) que contiene detalles sobre el mensaje.</span><span class="sxs-lookup"><span data-stu-id="20237-130">A pointer to an [MSG](/windows/desktop/api/winuser/ns-winuser-msg) structure that contains details about the message.</span></span>

## <a name="-returns"></a><span data-ttu-id="20237-131">-Devuelve</span><span class="sxs-lookup"><span data-stu-id="20237-131">-returns</span></span>

<span data-ttu-id="20237-132">Si el *código* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span><span class="sxs-lookup"><span data-stu-id="20237-132">If *code* is less than zero, the hook procedure must return the value returned by [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex).</span></span>

<span data-ttu-id="20237-133">Si el *código* es mayor o igual que cero, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_GETMESSAGE](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.</span><span class="sxs-lookup"><span data-stu-id="20237-133">If *code* is greater than or equal to zero, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_GETMESSAGE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="20237-134">Si el procedimiento de enlace no llama a **CallNextHookEx**, el valor devuelto debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="20237-134">If the hook procedure does not call **CallNextHookEx**, the return value should be zero.</span></span>

## <a name="-remarks"></a><span data-ttu-id="20237-135">-Comentarios</span><span class="sxs-lookup"><span data-stu-id="20237-135">-remarks</span></span>

<span data-ttu-id="20237-136">El procedimiento de enlace **GetMsgProc** puede examinar o modificar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="20237-136">The **GetMsgProc** hook procedure can examine or modify the message.</span></span>
<span data-ttu-id="20237-137">Una vez que el procedimiento de enlace devuelve el control al sistema, la función **GetMessage** o **PeekMessage** devuelve el mensaje, junto con cualquier modificación, a la aplicación que lo llamó originalmente.</span><span class="sxs-lookup"><span data-stu-id="20237-137">After the hook procedure returns control to the system, the **GetMessage** or **PeekMessage** function returns the message, along with any modifications, to the application that originally called it.</span></span>

<span data-ttu-id="20237-138">Una aplicación instala este procedimiento de enlace especificando el tipo de enlace de **WH_GETMESSAGE** y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="20237-138">An application installs this hook procedure by specifying the **WH_GETMESSAGE** hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

## <a name="see-also"></a><span data-ttu-id="20237-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="20237-139">See also</span></span>

[<span data-ttu-id="20237-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="20237-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="20237-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="20237-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="20237-142">MENSAJE</span><span class="sxs-lookup"><span data-stu-id="20237-142">MSG</span></span>](/windows/desktop/api/winuser/ns-winuser-msg)

[<span data-ttu-id="20237-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="20237-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="20237-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="20237-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="20237-145">Enlaces</span><span class="sxs-lookup"><span data-stu-id="20237-145">Hooks</span></span>](hooks.md)
