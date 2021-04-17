---
UID: ''
title: Función de devolución de llamada MouseProc
description: El sistema llama a esta función cuando una aplicación llama a una función de mensaje y hay un mensaje de mouse que se va a procesar.
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
ms.openlocfilehash: abdd74b5fed93e2c2ddbc8d037a657b779a62a05
ms.sourcegitcommit: 61bde60d4c3bc09defc3dcdb64c0ddadf52b214e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/11/2020
ms.locfileid: "105704927"
---
# <a name="mouseproc-function"></a><span data-ttu-id="8ff2c-103">MouseProc función)</span><span class="sxs-lookup"><span data-stu-id="8ff2c-103">MouseProc function</span></span>

## <a name="description"></a><span data-ttu-id="8ff2c-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ff2c-104">Description</span></span>

<span data-ttu-id="8ff2c-105">Función de devolución de llamada definida por la aplicación o definida por la biblioteca que se usa con la función [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) .</span><span class="sxs-lookup"><span data-stu-id="8ff2c-105">An application-defined or library-defined callback function used with the [SetWindowsHookEx](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw) function.</span></span>
<span data-ttu-id="8ff2c-106">El sistema llama a esta función cada vez que una aplicación llama a la función [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) o [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) y hay un mensaje del mouse que se va a procesar.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-106">The system calls this function whenever an application calls the [GetMessage](/windows/desktop/api/winuser/nf-winuser-getmessage) or [PeekMessage](/windows/desktop/api/winuser/nf-winuser-peekmessagew) function and there is a mouse message to be processed.</span></span>

<span data-ttu-id="8ff2c-107">El tipo **HOOKPROC** define un puntero a esta función de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-107">The **HOOKPROC** type defines a pointer to this callback function.</span></span>
<span data-ttu-id="8ff2c-108">**MouseProc** es un marcador de posición para el nombre de la función definida por la aplicación o por la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-108">**MouseProc** is a placeholder for the application-defined or library-defined function name.</span></span>

```cpp
LRESULT CALLBACK MouseProc(
  _In_ int    nCode,
  _In_ WPARAM wParam,
  _In_ LPARAM lParam
);
```

## <a name="parameters"></a><span data-ttu-id="8ff2c-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ff2c-109">Parameters</span></span>

### <a name="ncode-in"></a><span data-ttu-id="8ff2c-110">nCode [in]</span><span class="sxs-lookup"><span data-stu-id="8ff2c-110">nCode [in]</span></span>

<span data-ttu-id="8ff2c-111">Tipo: **int**</span><span class="sxs-lookup"><span data-stu-id="8ff2c-111">Type: **int**</span></span>

<span data-ttu-id="8ff2c-112">Código que utiliza el procedimiento de enlace para determinar cómo procesar el mensaje.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-112">A code that the hook procedure uses to determine how to process the message.</span></span>
<span data-ttu-id="8ff2c-113">Si *nCode* es menor que cero, el procedimiento de enlace debe pasar el mensaje a la función [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) sin más procesamiento y debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-113">If *nCode* is less than zero, the hook procedure must pass the message to the [CallNextHookEx](/windows/desktop/api/winuser/nf-winuser-callnexthookex) function without further processing and should return the value returned by **CallNextHookEx**.</span></span>
<span data-ttu-id="8ff2c-114">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-114">This parameter can be one of the following values.</span></span>

| <span data-ttu-id="8ff2c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="8ff2c-115">Value</span></span> | <span data-ttu-id="8ff2c-116">Significado</span><span class="sxs-lookup"><span data-stu-id="8ff2c-116">Meaning</span></span> |
|-------|---------|
| <span data-ttu-id="8ff2c-117">**HC_ACTION** 0</span><span class="sxs-lookup"><span data-stu-id="8ff2c-117">**HC_ACTION** 0</span></span> | <span data-ttu-id="8ff2c-118">Los parámetros *wParam* e *lParam* contienen información sobre un mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-118">The *wParam* and *lParam* parameters contain information about a mouse message.</span></span> |
| <span data-ttu-id="8ff2c-119">**HC_NOREMOVE** 3</span><span class="sxs-lookup"><span data-stu-id="8ff2c-119">**HC_NOREMOVE** 3</span></span> | <span data-ttu-id="8ff2c-120">Los parámetros *wParam* e *lParam* contienen información sobre un mensaje del mouse y el mensaje del mouse no se ha quitado de la cola de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-120">The *wParam* and *lParam* parameters contain information about a mouse message, and the mouse message has not been removed from the message queue.</span></span> <span data-ttu-id="8ff2c-121">(Una aplicación llamada la función **PeekMessage** , que especifica la marca **PM_NOREMOVE** ).</span><span class="sxs-lookup"><span data-stu-id="8ff2c-121">(An application called the **PeekMessage** function, specifying the **PM_NOREMOVE** flag.)</span></span> |

### <a name="wparam-in"></a><span data-ttu-id="8ff2c-122">wParam [in]</span><span class="sxs-lookup"><span data-stu-id="8ff2c-122">wParam [in]</span></span>

<span data-ttu-id="8ff2c-123">Tipo: **wParam**</span><span class="sxs-lookup"><span data-stu-id="8ff2c-123">Type: **WPARAM**</span></span>

<span data-ttu-id="8ff2c-124">Identificador del mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-124">The identifier of the mouse message.</span></span>

### <a name="lparam-in"></a><span data-ttu-id="8ff2c-125">lParam [in]</span><span class="sxs-lookup"><span data-stu-id="8ff2c-125">lParam [in]</span></span>

<span data-ttu-id="8ff2c-126">Tipo: **lParam**</span><span class="sxs-lookup"><span data-stu-id="8ff2c-126">Type: **LPARAM**</span></span>

<span data-ttu-id="8ff2c-127">Puntero a una estructura [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) .</span><span class="sxs-lookup"><span data-stu-id="8ff2c-127">A pointer to a [MOUSEHOOKSTRUCT](/windows/desktop/api/winuser/ns-winuser-mousehookstruct) structure.</span></span>

## <a name="returns"></a><span data-ttu-id="8ff2c-128">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="8ff2c-128">Returns</span></span>

<span data-ttu-id="8ff2c-129">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ff2c-129">Type: **LRESULT**</span></span>

<span data-ttu-id="8ff2c-130">Si *nCode* es menor que cero, el procedimiento de enlace debe devolver el valor devuelto por **CallNextHookEx**.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-130">If *nCode* is less than zero, the hook procedure must return the value returned by **CallNextHookEx**.</span></span>

<span data-ttu-id="8ff2c-131">Si *nCode* es mayor o igual que cero y el procedimiento de enlace no procese el mensaje, se recomienda encarecidamente llamar a **CallNextHookEx** y devolver el valor que devuelve; de lo contrario, otras aplicaciones que tengan instalado [WH_MOUSE](about-hooks.md) enlaces no recibirán notificaciones de enlace y se comportarán de forma incorrecta como resultado.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-131">If *nCode* is greater than or equal to zero, and the hook procedure did not process the message, it is highly recommended that you call **CallNextHookEx** and return the value it returns; otherwise, other applications that have installed [WH_MOUSE](about-hooks.md) hooks will not receive hook notifications and may behave incorrectly as a result.</span></span>
<span data-ttu-id="8ff2c-132">Si el procedimiento de enlace ha procesado el mensaje, es posible que devuelva un valor distinto de cero para evitar que el sistema pase el mensaje al procedimiento de ventana de destino.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-132">If the hook procedure processed the message, it may return a nonzero value to prevent the system from passing the message to the target window procedure.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ff2c-133">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8ff2c-133">Remarks</span></span>

<span data-ttu-id="8ff2c-134">Una aplicación instala el procedimiento de enlace especificando el tipo de enlace de WH_MOUSE y un puntero al procedimiento de enlace en una llamada a la función **SetWindowsHookEx** .</span><span class="sxs-lookup"><span data-stu-id="8ff2c-134">An application installs the hook procedure by specifying the WH_MOUSE hook type and a pointer to the hook procedure in a call to the **SetWindowsHookEx** function.</span></span>

<span data-ttu-id="8ff2c-135">El procedimiento de enlace no debe instalar una función de devolución de llamada [WH_JOURNALPLAYBACK](about-hooks.md) .</span><span class="sxs-lookup"><span data-stu-id="8ff2c-135">The hook procedure must not install a [WH_JOURNALPLAYBACK](about-hooks.md) callback function.</span></span>

<span data-ttu-id="8ff2c-136">Este enlace se puede llamar en el contexto del subproceso que lo instaló.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-136">This hook may be called in the context of the thread that installed it.</span></span>
<span data-ttu-id="8ff2c-137">La llamada se realiza mediante el envío de un mensaje al subproceso que instaló el enlace.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-137">The call is made by sending a message to the thread that installed the hook.</span></span>
<span data-ttu-id="8ff2c-138">Por lo tanto, el subproceso que instaló el enlace debe tener un bucle de mensajes.</span><span class="sxs-lookup"><span data-stu-id="8ff2c-138">Therefore, the thread that installed the hook must have a message loop.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ff2c-139">Vea también</span><span class="sxs-lookup"><span data-stu-id="8ff2c-139">See also</span></span>

[<span data-ttu-id="8ff2c-140">CallNextHookEx</span><span class="sxs-lookup"><span data-stu-id="8ff2c-140">CallNextHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-callnexthookex)

[<span data-ttu-id="8ff2c-141">GetMessage</span><span class="sxs-lookup"><span data-stu-id="8ff2c-141">GetMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-getmessage)

[<span data-ttu-id="8ff2c-142">MOUSEHOOKSTRUCT</span><span class="sxs-lookup"><span data-stu-id="8ff2c-142">MOUSEHOOKSTRUCT</span></span>](/windows/desktop/api/winuser/ns-winuser-mousehookstruct)

[<span data-ttu-id="8ff2c-143">PeekMessage</span><span class="sxs-lookup"><span data-stu-id="8ff2c-143">PeekMessage</span></span>](/windows/desktop/api/winuser/nf-winuser-peekmessagew)

[<span data-ttu-id="8ff2c-144">SetWindowsHookEx</span><span class="sxs-lookup"><span data-stu-id="8ff2c-144">SetWindowsHookEx</span></span>](/windows/desktop/api/winuser/nf-winuser-setwindowshookexw)

[<span data-ttu-id="8ff2c-145">Enlaces</span><span class="sxs-lookup"><span data-stu-id="8ff2c-145">Hooks</span></span>](hooks.md)

[<span data-ttu-id="8ff2c-146">Acerca de los enlaces</span><span class="sxs-lookup"><span data-stu-id="8ff2c-146">About Hooks</span></span>](about-hooks.md)
