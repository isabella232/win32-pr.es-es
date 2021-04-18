---
title: Mensaje de WM_TOUCH (Winuser. h)
description: Notifica a la ventana cuando uno o más puntos táctiles, como un dedo o un lápiz, tocan una superficie del digitalizador sensible al tacto.
ms.assetid: 5dee8bab-34fa-4dd9-a65b-35883757ec80
keywords:
- Mensaje de WM_TOUCH de Windows Touch
topic_type:
- apiref
api_name:
- WM_TOUCH
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b6242d43b661240d946d2883237640d1bc92b3f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422452"
---
# <a name="wm_touch-message"></a><span data-ttu-id="60922-104">\_Mensaje táctil de WM</span><span class="sxs-lookup"><span data-stu-id="60922-104">WM\_TOUCH message</span></span>

<span data-ttu-id="60922-105">Notifica a la ventana cuando uno o más puntos táctiles, como un dedo o un lápiz, tocan una superficie del digitalizador sensible al tacto.</span><span class="sxs-lookup"><span data-stu-id="60922-105">Notifies the window when one or more touch points, such as a finger or pen, touches a touch-sensitive digitizer surface.</span></span>

## <a name="parameters"></a><span data-ttu-id="60922-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="60922-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60922-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="60922-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60922-108">La palabra de orden inferior contiene el número de puntos de toque asociados a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="60922-108">The low-order word contains the number of touch points associated with this message.</span></span> <span data-ttu-id="60922-109">La palabra de orden superior se reserva para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="60922-109">The high-order word is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="60922-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="60922-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="60922-111">Contiene un identificador de entrada táctil que se puede usar en una llamada a [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) para recuperar información detallada sobre los puntos de toque asociados a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="60922-111">Contains a touch input handle that can be used in a call to [**GetTouchInputInfo**](/windows/desktop/api/winuser/nf-winuser-gettouchinputinfo) to retrieve detailed information about the touch points associated with this message.</span></span>

<span data-ttu-id="60922-112">Este identificador solo es válido en el proceso actual y no se debe pasar entre procesos salvo como **lParam** en una llamada **SendMessage** o **PostMessage** .</span><span class="sxs-lookup"><span data-stu-id="60922-112">This handle is valid only within the current process and should not be passed cross-process except as the **LPARAM** in a **SendMessage** or **PostMessage** call.</span></span>

<span data-ttu-id="60922-113">Cuando la aplicación ya no requiere este identificador, la aplicación debe llamar a **CloseTouchInputHandle** para liberar la memoria de proceso asociada a este identificador.</span><span class="sxs-lookup"><span data-stu-id="60922-113">When the application no longer requires this handle, the application must call **CloseTouchInputHandle** to free the process memory associated with this handle.</span></span> <span data-ttu-id="60922-114">Si no lo hace, puede producirse una pérdida de memoria de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="60922-114">Failing to do so can result in an application memory leak.</span></span>

<span data-ttu-id="60922-115">Tenga en cuenta que el identificador de entrada táctil de este parámetro ya no es válido después de que el mensaje se haya pasado a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="60922-115">Note that the touch input handle in this parameter is no longer valid after the message has been passed to [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="60922-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) cerrará e invalidará este identificador.</span><span class="sxs-lookup"><span data-stu-id="60922-116">[DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca) will close and invalidate this handle.</span></span>

<span data-ttu-id="60922-117">Tenga en cuenta también que el identificador de entrada táctil de este parámetro ya no es válido después de que el mensaje se haya reenviado mediante [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage** o una de sus variantes.</span><span class="sxs-lookup"><span data-stu-id="60922-117">Note also that the touch input handle in this parameter is no longer valid after the message has been forwarded using [**PostMessage**](sendmessage--postmessage--and-related-functions.md), **SendMessage**, or one of their variants.</span></span> <span data-ttu-id="60922-118">Estas funciones cerrarán e invalidarán este identificador.</span><span class="sxs-lookup"><span data-stu-id="60922-118">These functions will close and invalidate this handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60922-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="60922-119">Return value</span></span>

<span data-ttu-id="60922-120">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="60922-120">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="60922-121">Si la aplicación no procesa el mensaje, debe llamar a [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="60922-121">If the application does not process the message, it must call [DefWindowProc](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span> <span data-ttu-id="60922-122">Si no lo hace, la aplicación perderá memoria porque el identificador de entrada táctil no está cerrado y no se libera la memoria de proceso asociada.</span><span class="sxs-lookup"><span data-stu-id="60922-122">Not doing so causes the application to leak memory because the touch input handle is not closed and associated process memory is not freed.</span></span>

## <a name="remarks"></a><span data-ttu-id="60922-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60922-123">Remarks</span></span>

<span data-ttu-id="60922-124">**WM \_ Los mensajes TÁCTILes** no respetan las regiones de **HTTRANSPARENT** de Windows.</span><span class="sxs-lookup"><span data-stu-id="60922-124">**WM\_TOUCH** messages do not respect **HTTRANSPARENT** regions of windows.</span></span> <span data-ttu-id="60922-125">Si una ventana devuelve **HTTRANSPARENT** en respuesta a un mensaje de **\_ NCHITTEST de WM** , los mensajes del mouse van al elemento primario y los mensajes **\_ táctiles de WM** van directamente a la ventana.</span><span class="sxs-lookup"><span data-stu-id="60922-125">If a window returns **HTTRANSPARENT** in response to a **WM\_NCHITTEST** message, mouse messages go to the parent, and **WM\_TOUCH** messages go directly to the window.</span></span>

## <a name="examples"></a><span data-ttu-id="60922-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="60922-126">Examples</span></span>

<span data-ttu-id="60922-127">El código siguiente es un ejemplo de cómo obtener información de entrada táctil detallada asociada a este mensaje.</span><span class="sxs-lookup"><span data-stu-id="60922-127">The following code is an example of how to obtain detailed touch input information associated with this message.</span></span>


```C++
UINT cInputs = LOWORD(wParam);
PTOUCHINPUT pInputs = new TOUCHINPUT[cInputs];
if (NULL != pInputs)
{
    if (GetTouchInputInfo((HTOUCHINPUT)lParam,
                          cInputs,
                          pInputs,
                          sizeof(TOUCHINPUT)))
    {
        // process pInputs
        if (!CloseTouchInputHandle((HTOUCHINPUT)lParam))
        {
            // error handling
        }
    }
    else
    {
        // GetLastError() and error handling
    }
    delete [] pInputs;
}
else
{
    // error handling, presumably out of memory
}
return DefWindowProc(hWnd, message, wParam, lParam);
```



## <a name="requirements"></a><span data-ttu-id="60922-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="60922-128">Requirements</span></span>



| <span data-ttu-id="60922-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="60922-129">Requirement</span></span> | <span data-ttu-id="60922-130">Value</span><span class="sxs-lookup"><span data-stu-id="60922-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60922-131">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60922-131">Minimum supported client</span></span><br/> | <span data-ttu-id="60922-132">Solo aplicaciones de escritorio de Windows 7 \[\]</span><span class="sxs-lookup"><span data-stu-id="60922-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="60922-133">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="60922-133">Minimum supported server</span></span><br/> | <span data-ttu-id="60922-134">Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="60922-134">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                  |
| <span data-ttu-id="60922-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="60922-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="60922-136"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="60922-136"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60922-137">Vea también</span><span class="sxs-lookup"><span data-stu-id="60922-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60922-138">Mensajes</span><span class="sxs-lookup"><span data-stu-id="60922-138">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="60922-139">Guía de programación de manipulaciones e inercia</span><span class="sxs-lookup"><span data-stu-id="60922-139">Manipulations and Inertia Programming Guide</span></span>](manipulation-and-inertia.md)
</dt> <dt>

[<span data-ttu-id="60922-140">Guía de programación de entrada táctil de Windows</span><span class="sxs-lookup"><span data-stu-id="60922-140">Windows Touch Input Programming Guide</span></span>](guide-multi-touch-input.md)
</dt> </dl>

 

