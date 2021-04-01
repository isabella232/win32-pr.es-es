---
title: Mensaje de WM_MOUSEACTIVATE (Winuser. h)
description: Se envía cuando el cursor está en una ventana inactiva y el usuario presiona un botón del mouse. La ventana primaria recibe este mensaje solo si la ventana secundaria lo pasa a la función DefWindowProc.
ms.assetid: 335c0819-a655-4dd1-9511-1f148b87271c
keywords:
- Entrada de mouse y teclado de mensaje de WM_MOUSEACTIVATE
topic_type:
- apiref
api_name:
- WM_MOUSEACTIVATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ba74141f8d519541d1e63327179fff2f27ad403
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150154"
---
# <a name="wm_mouseactivate-message"></a><span data-ttu-id="383ae-105">Mensaje de MOUSEACTIVATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="383ae-105">WM\_MOUSEACTIVATE message</span></span>

<span data-ttu-id="383ae-106">Se envía cuando el cursor está en una ventana inactiva y el usuario presiona un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-106">Sent when the cursor is in an inactive window and the user presses a mouse button.</span></span> <span data-ttu-id="383ae-107">La ventana primaria recibe este mensaje solo si la ventana secundaria lo pasa a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .</span><span class="sxs-lookup"><span data-stu-id="383ae-107">The parent window receives this message only if the child window passes it to the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function.</span></span>

<span data-ttu-id="383ae-108">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="383ae-108">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_MOUSEACTIVATE                0x0021
```



## <a name="parameters"></a><span data-ttu-id="383ae-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="383ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="383ae-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="383ae-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="383ae-111">Identificador de la ventana primaria de nivel superior de la ventana que se va a activar.</span><span class="sxs-lookup"><span data-stu-id="383ae-111">A handle to the top-level parent window of the window being activated.</span></span>

</dd> <dt>

<span data-ttu-id="383ae-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="383ae-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="383ae-113">La palabra de orden inferior especifica el valor de la prueba de posicionamiento devuelto por la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) como resultado del procesamiento del mensaje [**\_ NCHITTEST de WM**](wm-nchittest.md) .</span><span class="sxs-lookup"><span data-stu-id="383ae-113">The low-order word specifies the hit-test value returned by the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function as a result of processing the [**WM\_NCHITTEST**](wm-nchittest.md) message.</span></span> <span data-ttu-id="383ae-114">Para obtener una lista de los valores de las pruebas de posicionamiento, consulte **WM \_ NCHITTEST**.</span><span class="sxs-lookup"><span data-stu-id="383ae-114">For a list of hit-test values, see **WM\_NCHITTEST**.</span></span>

<span data-ttu-id="383ae-115">La palabra de orden superior especifica el identificador del mensaje de mouse que se genera cuando el usuario presionó un botón del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-115">The high-order word specifies the identifier of the mouse message generated when the user pressed a mouse button.</span></span> <span data-ttu-id="383ae-116">El mensaje del mouse se descarta o se envía a la ventana, dependiendo del valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="383ae-116">The mouse message is either discarded or posted to the window, depending on the return value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="383ae-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="383ae-117">Return value</span></span>

<span data-ttu-id="383ae-118">El valor devuelto especifica si se debe activar la ventana y si se debe descartar el identificador del mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-118">The return value specifies whether the window should be activated and whether the identifier of the mouse message should be discarded.</span></span> <span data-ttu-id="383ae-119">Debe ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="383ae-119">It must be one of the following values.</span></span>



| <span data-ttu-id="383ae-120">Código o valor devuelto</span><span class="sxs-lookup"><span data-stu-id="383ae-120">Return code/value</span></span>                                                                                                                                          | <span data-ttu-id="383ae-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="383ae-121">Description</span></span>                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="383ae-122"><dt>**MA \_ ACTIVAR**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="383ae-122"><dt>**MA\_ACTIVATE**</dt> <dt>1</dt></span></span> </dl>         | <span data-ttu-id="383ae-123">Activa la ventana y no descarta el mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-123">Activates the window, and does not discard the mouse message.</span></span><br/>         |
| <dl> <span data-ttu-id="383ae-124"><dt>**MA \_ ACTIVATEANDEAT**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="383ae-124"><dt>**MA\_ACTIVATEANDEAT**</dt> <dt>2</dt></span></span> </dl>   | <span data-ttu-id="383ae-125">Activa la ventana y descarta el mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-125">Activates the window, and discards the mouse message.</span></span><br/>                 |
| <dl> <span data-ttu-id="383ae-126"><dt>**MA \_ Noactivate**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="383ae-126"><dt>**MA\_NOACTIVATE**</dt> <dt>3</dt></span></span> </dl>       | <span data-ttu-id="383ae-127">No activa la ventana y no descarta el mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-127">Does not activate the window, and does not discard the mouse message.</span></span><br/> |
| <dl> <span data-ttu-id="383ae-128"><dt>**MA \_ NOACTIVATEANDEAT**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="383ae-128"><dt>**MA\_NOACTIVATEANDEAT**</dt> <dt>4</dt></span></span> </dl> | <span data-ttu-id="383ae-129">No activa la ventana, pero descarta el mensaje del mouse.</span><span class="sxs-lookup"><span data-stu-id="383ae-129">Does not activate the window, but discards the mouse message.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="383ae-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="383ae-130">Remarks</span></span>

<span data-ttu-id="383ae-131">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) pasa el mensaje a la ventana primaria de una ventana secundaria antes de que se produzca cualquier procesamiento.</span><span class="sxs-lookup"><span data-stu-id="383ae-131">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function passes the message to a child window's parent window before any processing occurs.</span></span> <span data-ttu-id="383ae-132">La ventana primaria determina si se debe activar la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="383ae-132">The parent window determines whether to activate the child window.</span></span> <span data-ttu-id="383ae-133">Si activa la ventana secundaria, la ventana primaria debe devolver **MA \_ noactivate** o **MA \_ NOACTIVATEANDEAT** para evitar que el sistema procese el mensaje más allá.</span><span class="sxs-lookup"><span data-stu-id="383ae-133">If it activates the child window, the parent window should return **MA\_NOACTIVATE** or **MA\_NOACTIVATEANDEAT** to prevent the system from processing the message further.</span></span>

## <a name="requirements"></a><span data-ttu-id="383ae-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="383ae-134">Requirements</span></span>



| <span data-ttu-id="383ae-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="383ae-135">Requirement</span></span> | <span data-ttu-id="383ae-136">Value</span><span class="sxs-lookup"><span data-stu-id="383ae-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="383ae-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="383ae-137">Minimum supported client</span></span><br/> | <span data-ttu-id="383ae-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="383ae-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="383ae-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="383ae-139">Minimum supported server</span></span><br/> | <span data-ttu-id="383ae-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="383ae-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="383ae-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="383ae-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="383ae-142"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="383ae-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="383ae-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="383ae-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="383ae-144">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="383ae-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="383ae-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="383ae-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

<span data-ttu-id="383ae-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="383ae-146">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="383ae-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="383ae-147">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="383ae-148">**NCHITTEST de WM \_**</span><span class="sxs-lookup"><span data-stu-id="383ae-148">**WM\_NCHITTEST**</span></span>](wm-nchittest.md)
</dt> <dt>

<span data-ttu-id="383ae-149">**Vista**</span><span class="sxs-lookup"><span data-stu-id="383ae-149">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="383ae-150">Entrada del mouse</span><span class="sxs-lookup"><span data-stu-id="383ae-150">Mouse Input</span></span>](mouse-input.md)
</dt> </dl>

 

