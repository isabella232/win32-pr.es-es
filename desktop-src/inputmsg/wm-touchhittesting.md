---
title: Mensaje WM_TOUCHHITTESTING
description: Se envía a una ventana en un toque hacia abajo para determinar el destino táctil más probable.
ms.assetid: 741F9D67-A914-46CF-91A3-EF40447E7438
keywords:
- Mensajes y notificaciones de entrada de mensajes de WM_TOUCHHITTESTING
topic_type:
- apiref
api_name:
- WM_TOUCHHITTESTING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 83b6e564d692fb0223ec8871b99cefcb9fddf40b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150578"
---
# <a name="wm_touchhittesting-message"></a><span data-ttu-id="e7661-104">Mensaje WM_TOUCHHITTESTING</span><span class="sxs-lookup"><span data-stu-id="e7661-104">WM_TOUCHHITTESTING message</span></span>

<span data-ttu-id="e7661-105">Se envía a una ventana en un toque hacia abajo para determinar el destino táctil más probable.</span><span class="sxs-lookup"><span data-stu-id="e7661-105">Sent to a window on a touch down in order to determine the most probable touch target.</span></span>

> <span data-ttu-id="e7661-106">\[! Aún\]</span><span class="sxs-lookup"><span data-stu-id="e7661-106">\[!Important\]</span></span>  
> <span data-ttu-id="e7661-107">Las aplicaciones de escritorio deben tener en cuenta los ppp.</span><span class="sxs-lookup"><span data-stu-id="e7661-107">Desktop apps should be DPI aware.</span></span> <span data-ttu-id="e7661-108">Si la aplicación no tiene en cuenta los PPP, las coordenadas de pantalla contenidas en los mensajes de puntero y las estructuras relacionadas podrían aparecer inexactas debido a la virtualización de PPP.</span><span class="sxs-lookup"><span data-stu-id="e7661-108">If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization.</span></span> <span data-ttu-id="e7661-109">La virtualización de PPP proporciona compatibilidad con el escalado automático a las aplicaciones que no reconocen los PPP y está activo de forma predeterminada (los usuarios pueden desactivarla).</span><span class="sxs-lookup"><span data-stu-id="e7661-109">DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off).</span></span> <span data-ttu-id="e7661-110">Para obtener más información, vea [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="e7661-110">For more information, see [Writing High-DPI Win32 Applications](/previous-versions//dd464660(v=vs.85)).</span></span>

 


```C++
#define WM_TOUCHHITTESTING       0x024D
```



## <a name="parameters"></a><span data-ttu-id="e7661-111">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e7661-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7661-112">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e7661-112">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7661-113">Sin usar.</span><span class="sxs-lookup"><span data-stu-id="e7661-113">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="e7661-114">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e7661-114">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e7661-115">Puntero a la estructura de [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) que contiene los datos del área de contacto táctil.</span><span class="sxs-lookup"><span data-stu-id="e7661-115">Pointer to the [**TOUCH_HIT_TESTING_INPUT**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_input) structure that holds the touch contact area data.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7661-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e7661-116">Return value</span></span>

<span data-ttu-id="e7661-117">Si uno o más elementos están dentro del área de contacto táctil, una aplicación debe devolver el resultado de [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span><span class="sxs-lookup"><span data-stu-id="e7661-117">If one or more elements are within the touch contact area, an application should return the result of [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation).</span></span>

<span data-ttu-id="e7661-118">Si no hay elementos en el área de contacto táctil, una aplicación debe establecer el valor de **score** en [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) en [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) y llamar a [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) para obtener el valor devuelto de LRESULT.</span><span class="sxs-lookup"><span data-stu-id="e7661-118">If no elements are within the touch contact area, an application should set the value of **score** in [**TOUCH_HIT_TESTING_PROXIMITY_EVALUATION**](/windows/win32/api/winuser/ns-winuser-touch_hit_testing_proximity_evaluation) to [**TOUCH_HIT_TESTING_PROXIMITY_FARTHEST**](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores) and call [**PackTouchHitTestingProximityEvaluation**](/windows/win32/api/winuser/nf-winuser-packtouchhittestingproximityevaluation) to get the LRESULT return value.</span></span>

<span data-ttu-id="e7661-119">Si la aplicación no procesa este mensaje, debe llamar a [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span><span class="sxs-lookup"><span data-stu-id="e7661-119">If the application does not process this message, it must call [**DefWindowProc**](/windows/win32/api/winuser/nf-winuser-defwindowproca).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7661-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e7661-120">Remarks</span></span>

<span data-ttu-id="e7661-121">Este mensaje se envía a Windows que se registra a través de la función [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) .</span><span class="sxs-lookup"><span data-stu-id="e7661-121">This message is sent to windows that register through the [**RegisterTouchHitTestingWindow**](/windows/win32/api/winuser/nf-winuser-registertouchhittestingwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7661-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e7661-122">Requirements</span></span>



| <span data-ttu-id="e7661-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="e7661-123">Requirement</span></span> | <span data-ttu-id="e7661-124">Value</span><span class="sxs-lookup"><span data-stu-id="e7661-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7661-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7661-125">Minimum supported client</span></span><br/> | <span data-ttu-id="e7661-126">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7661-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="e7661-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e7661-127">Minimum supported server</span></span><br/> | <span data-ttu-id="e7661-128">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="e7661-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e7661-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e7661-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7661-130"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e7661-130"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7661-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="e7661-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7661-132">Mensajes</span><span class="sxs-lookup"><span data-stu-id="e7661-132">Messages</span></span>](messages.md)
</dt> <dt>

[<span data-ttu-id="e7661-133">**Puntuaciones de la prueba de posicionamiento táctil**</span><span class="sxs-lookup"><span data-stu-id="e7661-133">**Touch Hit Testing Scores**</span></span>](/previous-versions/windows/desktop/input_touchhittest/hit-testing-scores)
</dt> </dl>

 

