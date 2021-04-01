---
title: Mensaje de WM_ACTIVATE (Winuser. h)
description: Se envía a la ventana que se está activando y la ventana que se está desactivando.
ms.assetid: a62bb9f7-f286-4d0d-a1ca-370950c188b2
keywords:
- Entrada de mouse y teclado de mensaje de WM_ACTIVATE
topic_type:
- apiref
api_name:
- WM_ACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec28662aa2219ee9b3ad2e8cc8efac861d292f6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150157"
---
# <a name="wm_activate-message"></a><span data-ttu-id="dc6d7-104">Mensaje de activación de WM \_</span><span class="sxs-lookup"><span data-stu-id="dc6d7-104">WM\_ACTIVATE message</span></span>

<span data-ttu-id="dc6d7-105">Se envía a la ventana que se está activando y la ventana que se está desactivando.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-105">Sent to both the window being activated and the window being deactivated.</span></span> <span data-ttu-id="dc6d7-106">Si las ventanas utilizan la misma cola de entrada, el mensaje se envía de forma sincrónica, primero en el procedimiento de ventana de la ventana de nivel superior que se va a desactivar y, a continuación, en el procedimiento de ventana de la ventana de nivel superior que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-106">If the windows use the same input queue, the message is sent synchronously, first to the window procedure of the top-level window being deactivated, then to the window procedure of the top-level window being activated.</span></span> <span data-ttu-id="dc6d7-107">Si Windows usa colas de entrada diferentes, el mensaje se envía de forma asincrónica, por lo que la ventana se activa inmediatamente.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-107">If the windows use different input queues, the message is sent asynchronously, so the window is activated immediately.</span></span>


```C++
#define WM_ACTIVATE                     0x0006
```



## <a name="parameters"></a><span data-ttu-id="dc6d7-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dc6d7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc6d7-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="dc6d7-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc6d7-110">La palabra de orden inferior especifica si la ventana se está activando o desactivando.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-110">The low-order word specifies whether the window is being activated or deactivated.</span></span> <span data-ttu-id="dc6d7-111">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-111">This parameter can be one of the following values.</span></span> <span data-ttu-id="dc6d7-112">La palabra de orden superior especifica el estado minimizado de la ventana que se está activando o desactivando.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-112">The high-order word specifies the minimized state of the window being activated or deactivated.</span></span> <span data-ttu-id="dc6d7-113">Un valor distinto de cero indica que la ventana está minimizada.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-113">A nonzero value indicates the window is minimized.</span></span>



| <span data-ttu-id="dc6d7-114">Value</span><span class="sxs-lookup"><span data-stu-id="dc6d7-114">Value</span></span>                                                                                                                                                                                                                   | <span data-ttu-id="dc6d7-115">Significado</span><span class="sxs-lookup"><span data-stu-id="dc6d7-115">Meaning</span></span>                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WA_ACTIVE"></span><span id="wa_active"></span><dl> <span data-ttu-id="dc6d7-116"><dt>**Wa \_ ACTIVO**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="dc6d7-116"><dt>**WA\_ACTIVE**</dt> <dt>1</dt></span></span> </dl>                | <span data-ttu-id="dc6d7-117">Activado por algún método que no sea un clic del mouse (por ejemplo, mediante una llamada a la función [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) o mediante el uso de la interfaz de teclado para seleccionar la ventana).</span><span class="sxs-lookup"><span data-stu-id="dc6d7-117">Activated by some method other than a mouse click (for example, by a call to the [**SetActiveWindow**](/windows/win32/api/winuser/nf-winuser-setactivewindow) function or by use of the keyboard interface to select the window).</span></span><br/> |
| <span id="WA_CLICKACTIVE"></span><span id="wa_clickactive"></span><dl> <span data-ttu-id="dc6d7-118"><dt>**Wa \_ CLICKACTIVE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="dc6d7-118"><dt>**WA\_CLICKACTIVE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="dc6d7-119">Activado con un clic del mouse.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-119">Activated by a mouse click.</span></span><br/>                                                                                                                                                                     |
| <span id="WA_INACTIVE"></span><span id="wa_inactive"></span><dl> <span data-ttu-id="dc6d7-120"><dt>**Wa \_ Inactivo**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="dc6d7-120"><dt>**WA\_INACTIVE**</dt> <dt>0</dt></span></span> </dl>          | <span data-ttu-id="dc6d7-121">Desactivado.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-121">Deactivated.</span></span><br/>                                                                                                                                                                                    |



 

</dd> <dt>

<span data-ttu-id="dc6d7-122">*lParam*</span><span class="sxs-lookup"><span data-stu-id="dc6d7-122">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="dc6d7-123">Identificador de la ventana que se va a activar o desactivar, dependiendo del valor del parámetro *wParam* .</span><span class="sxs-lookup"><span data-stu-id="dc6d7-123">A handle to the window being activated or deactivated, depending on the value of the *wParam* parameter.</span></span> <span data-ttu-id="dc6d7-124">Si la palabra de orden inferior de *wParam* es **wa \_ inactiva**, *lParam* es el identificador de la ventana que se está activando.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-124">If the low-order word of *wParam* is **WA\_INACTIVE**, *lParam* is the handle to the window being activated.</span></span> <span data-ttu-id="dc6d7-125">Si la palabra de orden inferior de *wParam* es **wa \_ Active** o **wa \_ CLICKACTIVE**, *lParam* es el identificador de la ventana que se está desactivando.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-125">If the low-order word of *wParam* is **WA\_ACTIVE** or **WA\_CLICKACTIVE**, *lParam* is the handle to the window being deactivated.</span></span> <span data-ttu-id="dc6d7-126">Este identificador puede ser **null**.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-126">This handle can be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc6d7-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dc6d7-127">Return value</span></span>

<span data-ttu-id="dc6d7-128">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-128">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc6d7-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dc6d7-129">Remarks</span></span>

<span data-ttu-id="dc6d7-130">Si la ventana se está activando y no está minimizada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece el foco de teclado en la ventana.</span><span class="sxs-lookup"><span data-stu-id="dc6d7-130">If the window is being activated and is not minimized, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sets the keyboard focus to the window.</span></span> <span data-ttu-id="dc6d7-131">Si la ventana se activa con un clic del mouse, también recibe un mensaje de [**\_ MOUSEACTIVATE de WM**](wm-mouseactivate.md) .</span><span class="sxs-lookup"><span data-stu-id="dc6d7-131">If the window is activated by a mouse click, it also receives a [**WM\_MOUSEACTIVATE**](wm-mouseactivate.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="dc6d7-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dc6d7-132">Requirements</span></span>



| <span data-ttu-id="dc6d7-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc6d7-133">Requirement</span></span> | <span data-ttu-id="dc6d7-134">Value</span><span class="sxs-lookup"><span data-stu-id="dc6d7-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc6d7-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc6d7-135">Minimum supported client</span></span><br/> | <span data-ttu-id="dc6d7-136">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dc6d7-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dc6d7-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dc6d7-137">Minimum supported server</span></span><br/> | <span data-ttu-id="dc6d7-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dc6d7-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="dc6d7-139">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dc6d7-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc6d7-140"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="dc6d7-140"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dc6d7-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="dc6d7-141">See also</span></span>

<dl> <dt>

<span data-ttu-id="dc6d7-142">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="dc6d7-142">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6d7-143">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="dc6d7-143">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="dc6d7-144">**SetActiveWindow**</span><span class="sxs-lookup"><span data-stu-id="dc6d7-144">**SetActiveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-setactivewindow)
</dt> <dt>

[<span data-ttu-id="dc6d7-145">**MOUSEACTIVATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dc6d7-145">**WM\_MOUSEACTIVATE**</span></span>](wm-mouseactivate.md)
</dt> <dt>

[<span data-ttu-id="dc6d7-146">**NCACTIVATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="dc6d7-146">**WM\_NCACTIVATE**</span></span>](/windows/desktop/winmsg/wm-ncactivate)
</dt> <dt>

<span data-ttu-id="dc6d7-147">**Vista**</span><span class="sxs-lookup"><span data-stu-id="dc6d7-147">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6d7-148">Entrada de teclado</span><span class="sxs-lookup"><span data-stu-id="dc6d7-148">Keyboard Input</span></span>](keyboard-input.md)
</dt> </dl>

 

