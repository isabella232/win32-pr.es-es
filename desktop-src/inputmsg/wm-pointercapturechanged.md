---
title: Mensaje WM_POINTERCAPTURECHANGED
description: Se envía a una ventana que está perdiendo la captura de un puntero de entrada.
ms.assetid: 6eec37da-227c-4be1-bf0b-98704caa1322
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_POINTERCAPTURECHANGED
topic_type:
- apiref
api_name:
- WM_POINTERCAPTURECHANGED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 768dc81be57bb61a23acab7ebea450dba577d60a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105720233"
---
# <a name="wm_pointercapturechanged-message"></a><span data-ttu-id="91c8e-104">Mensaje WM_POINTERCAPTURECHANGED</span><span class="sxs-lookup"><span data-stu-id="91c8e-104">WM_POINTERCAPTURECHANGED message</span></span>

<span data-ttu-id="91c8e-105">Se envía a una ventana que está perdiendo la captura de un puntero de entrada.</span><span class="sxs-lookup"><span data-stu-id="91c8e-105">Sent to a window that is losing capture of an input pointer.</span></span>

<span data-ttu-id="91c8e-106">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="91c8e-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_POINTERCAPTURECHANGED           0x024C
```



## <a name="parameters"></a><span data-ttu-id="91c8e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="91c8e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91c8e-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91c8e-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91c8e-109">Contiene información sobre el puntero de entrada que se está perdida.</span><span class="sxs-lookup"><span data-stu-id="91c8e-109">Contains information about the input pointer that is being lost.</span></span> <span data-ttu-id="91c8e-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) para obtener el identificador de puntero.</span><span class="sxs-lookup"><span data-stu-id="91c8e-110">Use [**GET_POINTERID_WPARAM**](/previous-versions/windows/desktop/api) to get the pointer ID.</span></span>

</dd> <dt>

<span data-ttu-id="91c8e-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91c8e-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91c8e-112">Contiene un identificador de la ventana que está capturando el puntero de entrada.</span><span class="sxs-lookup"><span data-stu-id="91c8e-112">Contains a handle to the window that is capturing the input pointer.</span></span> <span data-ttu-id="91c8e-113">Este valor puede ser NULL si la ventana ya no captura el puntero.</span><span class="sxs-lookup"><span data-stu-id="91c8e-113">This value can be NULL if the pointer is no longer being captured by the window.</span></span>

<span data-ttu-id="91c8e-114">Si este mensaje se genera a partir del procesamiento interno, el valor puede ser el identificador de la ventana que recibe el mensaje.</span><span class="sxs-lookup"><span data-stu-id="91c8e-114">If this message is generated from internal processing, the value can be the handle of the window receiving the message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91c8e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="91c8e-115">Return value</span></span>

<span data-ttu-id="91c8e-116">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="91c8e-116">If an application processes this message, it should return zero.</span></span>

<span data-ttu-id="91c8e-117">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="91c8e-117">If the application does not process this message, it should call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="91c8e-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="91c8e-118">Remarks</span></span>

<span data-ttu-id="91c8e-119">Una ventana debe usar esta notificación para detener el procesamiento de mensajes posteriores e iniciar cualquier limpieza necesaria para que el puntero se pierda.</span><span class="sxs-lookup"><span data-stu-id="91c8e-119">A window should use this notification to stop processing subsequent messages and initiate any cleanup required for the pointer being lost.</span></span> <span data-ttu-id="91c8e-120">El procesamiento de gestos asociados al puntero también debe finalizar (por ejemplo, llamando a [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) y los contactos restantes se vuelven a asociar a la ventana.</span><span class="sxs-lookup"><span data-stu-id="91c8e-120">Processing of gestures associated with the pointer should also be terminated (for example, by calling [**StopInteractionContext**](/windows/win32/api/interactioncontext/nf-interactioncontext-stopinteractioncontext)) and remaining contacts re-associated with the window.</span></span>

<span data-ttu-id="91c8e-121">Normalmente, si una ventana recibe la notificación **WM_POINTERCAPTURECHANGED** , no se reciben notificaciones posteriores relacionadas con el puntero de entrada.</span><span class="sxs-lookup"><span data-stu-id="91c8e-121">Typically, if a window receives the **WM_POINTERCAPTURECHANGED** notification, no subsequent notifications related to the input pointer are received.</span></span> <span data-ttu-id="91c8e-122">Por este motivo, no dependa de las notificaciones emparejadas como [**WM_POINTERENTER**](wm-pointerenter.md) y [**WM_POINTERLEAVE**](wm-pointerleave.md).</span><span class="sxs-lookup"><span data-stu-id="91c8e-122">Because of this, do not depend on paired notifications such as [**WM_POINTERENTER**](wm-pointerenter.md) and [**WM_POINTERLEAVE**](wm-pointerleave.md).</span></span>

<span data-ttu-id="91c8e-123">**WM_POINTERCAPTURECHANGED** no incluye datos de [**POINTER_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="91c8e-123">**WM_POINTERCAPTURECHANGED** does not include [**POINTER_INFO**](/previous-versions/windows/desktop/api) data.</span></span> <span data-ttu-id="91c8e-124">Aparte de la marca [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) que se va a establecer, los datos devueltos por [**GetPointerInfo**](/previous-versions/windows/desktop/api) (o cualquier variante) son idénticos a los que se devolvieron antes de la notificación.</span><span class="sxs-lookup"><span data-stu-id="91c8e-124">Other than the [**POINTER_FLAG_CAPTURECHANGED**](pointer-flags-contants.md) flag being set, the data returned by [**GetPointerInfo**](/previous-versions/windows/desktop/api) (or any variant) is identical to that returned prior to the notification.</span></span>

<span data-ttu-id="91c8e-125">Si la aplicación no procesa esta notificación, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) puede generar uno o más mensajes [**WM_GESTURE**](../wintouch/wm-gesture.md) o, si no se reconoce un gesto, **DefWindowProc** puede generar la entrada del mouse.</span><span class="sxs-lookup"><span data-stu-id="91c8e-125">If the application does not process this notification, [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca) may generate one or more [**WM_GESTURE**](../wintouch/wm-gesture.md) messages or, if a gesture is not recognized, **DefWindowProc** may generate mouse input.</span></span>

<span data-ttu-id="91c8e-126">Si una aplicación usa selectivamente alguna entrada de puntero y pasa el resto a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), el comportamiento resultante es indefinido.</span><span class="sxs-lookup"><span data-stu-id="91c8e-126">If an application selectively consumes some pointer input and passes the rest to [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca), the resulting behavior is undefined.</span></span>

## <a name="requirements"></a><span data-ttu-id="91c8e-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="91c8e-127">Requirements</span></span>



| <span data-ttu-id="91c8e-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="91c8e-128">Requirement</span></span> | <span data-ttu-id="91c8e-129">Value</span><span class="sxs-lookup"><span data-stu-id="91c8e-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="91c8e-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91c8e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="91c8e-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="91c8e-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="91c8e-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="91c8e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="91c8e-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="91c8e-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="91c8e-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="91c8e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="91c8e-135"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="91c8e-135"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="91c8e-136">Vea también</span><span class="sxs-lookup"><span data-stu-id="91c8e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="91c8e-137">Mensajes</span><span class="sxs-lookup"><span data-stu-id="91c8e-137">Messages</span></span>](messages.md)
</dt> </dl>

 

