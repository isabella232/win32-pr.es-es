---
description: Se envía a una ventana cuando la ventana está a punto de ocultarse o mostrarse.
ms.assetid: dea7c9aa-eba7-4b93-a4c5-9b2d36999780
title: Mensaje de WM_SHOWWINDOW (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbca6cbb4c73ff1cad31754b1b581e0c892970e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360713"
---
# <a name="wm_showwindow-message"></a><span data-ttu-id="1b291-103">Mensaje de WM \_ SHOWWINDOW</span><span class="sxs-lookup"><span data-stu-id="1b291-103">WM\_SHOWWINDOW message</span></span>

<span data-ttu-id="1b291-104">Se envía a una ventana cuando la ventana está a punto de ocultarse o mostrarse.</span><span class="sxs-lookup"><span data-stu-id="1b291-104">Sent to a window when the window is about to be hidden or shown.</span></span>

<span data-ttu-id="1b291-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1b291-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_SHOWWINDOW                   0x0018
```



## <a name="parameters"></a><span data-ttu-id="1b291-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1b291-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b291-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1b291-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b291-108">Indica si se muestra una ventana.</span><span class="sxs-lookup"><span data-stu-id="1b291-108">Indicates whether a window is being shown.</span></span> <span data-ttu-id="1b291-109">Si *wParam* es **true**, se muestra la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b291-109">If *wParam* is **TRUE**, the window is being shown.</span></span> <span data-ttu-id="1b291-110">Si *wParam* es **false**, se oculta la ventana.</span><span class="sxs-lookup"><span data-stu-id="1b291-110">If *wParam* is **FALSE**, the window is being hidden.</span></span>

</dd> <dt>

<span data-ttu-id="1b291-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1b291-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1b291-112">Estado de la ventana que se va a mostrar.</span><span class="sxs-lookup"><span data-stu-id="1b291-112">The status of the window being shown.</span></span> <span data-ttu-id="1b291-113">Si *lParam* es cero, el mensaje se envió debido a una llamada a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) ; de lo contrario, *lParam* es uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="1b291-113">If *lParam* is zero, the message was sent because of a call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function; otherwise, *lParam* is one of the following values.</span></span>



| <span data-ttu-id="1b291-114">Value</span><span class="sxs-lookup"><span data-stu-id="1b291-114">Value</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="1b291-115">Significado</span><span class="sxs-lookup"><span data-stu-id="1b291-115">Meaning</span></span>                                                                                       |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="SW_OTHERUNZOOM"></span><span id="sw_otherunzoom"></span><dl> <span data-ttu-id="1b291-116"><dt>**SW \_ OTHERUNZOOM**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="1b291-116"><dt>**SW\_OTHERUNZOOM**</dt> <dt>4</dt></span></span> </dl>       | <span data-ttu-id="1b291-117">La ventana se está descubriendo porque se restauró o se minimizó una ventana de maximizar.</span><span class="sxs-lookup"><span data-stu-id="1b291-117">The window is being uncovered because a maximize window was restored or minimized.</span></span><br/> |
| <span id="SW_OTHERZOOM"></span><span id="sw_otherzoom"></span><dl> <span data-ttu-id="1b291-118"><dt>**SW \_ OTHERZOOM**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="1b291-118"><dt>**SW\_OTHERZOOM**</dt> <dt>2</dt></span></span> </dl>             | <span data-ttu-id="1b291-119">La ventana está en el ámbito de otra ventana que se ha maximizado.</span><span class="sxs-lookup"><span data-stu-id="1b291-119">The window is being covered by another window that has been maximized.</span></span><br/>             |
| <span id="SW_PARENTCLOSING"></span><span id="sw_parentclosing"></span><dl> <span data-ttu-id="1b291-120"><dt>**SW \_ PARENTCLOSING**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="1b291-120"><dt>**SW\_PARENTCLOSING**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="1b291-121">La ventana propietaria de la ventana se está minimizando.</span><span class="sxs-lookup"><span data-stu-id="1b291-121">The window's owner window is being minimized.</span></span><br/>                                      |
| <span id="SW_PARENTOPENING"></span><span id="sw_parentopening"></span><dl> <span data-ttu-id="1b291-122"><dt>**SW \_ PARENTOPENING**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="1b291-122"><dt>**SW\_PARENTOPENING**</dt> <dt>3</dt></span></span> </dl> | <span data-ttu-id="1b291-123">La ventana propietaria de la ventana se está restaurando.</span><span class="sxs-lookup"><span data-stu-id="1b291-123">The window's owner window is being restored.</span></span><br/>                                       |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b291-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1b291-124">Return value</span></span>

<span data-ttu-id="1b291-125">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1b291-125">Type: **LRESULT**</span></span>

<span data-ttu-id="1b291-126">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="1b291-126">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b291-127">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1b291-127">Remarks</span></span>

<span data-ttu-id="1b291-128">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) oculta o muestra la ventana, tal como se especifica en el mensaje.</span><span class="sxs-lookup"><span data-stu-id="1b291-128">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function hides or shows the window, as specified by the message.</span></span> <span data-ttu-id="1b291-129">Si una ventana tiene el [**estilo \_ visible de WS**](window-styles.md) cuando se crea, la ventana recibe este mensaje después de crearlo, pero antes de que se muestre.</span><span class="sxs-lookup"><span data-stu-id="1b291-129">If a window has the [**WS\_VISIBLE**](window-styles.md) style when it is created, the window receives this message after it is created, but before it is displayed.</span></span> <span data-ttu-id="1b291-130">Una ventana también recibe este mensaje cuando la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) o [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) cambia su estado de visibilidad.</span><span class="sxs-lookup"><span data-stu-id="1b291-130">A window also receives this message when its visibility state is changed by the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) or [**ShowOwnedPopups**](/windows/win32/api/winuser/nf-winuser-showownedpopups) function.</span></span>

<span data-ttu-id="1b291-131">El **mensaje \_ SHOWWINDOW de WM** no se envía en las siguientes circunstancias:</span><span class="sxs-lookup"><span data-stu-id="1b291-131">The **WM\_SHOWWINDOW** message is not sent under the following circumstances:</span></span>

-   <span data-ttu-id="1b291-132">Cuando se crea una ventana superpuesta de nivel superior con el estilo [**WS \_ Maximize**](window-styles.md) o **WS \_ miniMIZE** .</span><span class="sxs-lookup"><span data-stu-id="1b291-132">When a top-level, overlapped window is created with the [**WS\_MAXIMIZE**](window-styles.md) or **WS\_MINIMIZE** style.</span></span>
-   <span data-ttu-id="1b291-133">Cuando se especifica la marca **SW \_ SHOWNORMAL** en la llamada a la función [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) .</span><span class="sxs-lookup"><span data-stu-id="1b291-133">When the **SW\_SHOWNORMAL** flag is specified in the call to the [**ShowWindow**](/windows/win32/api/winuser/nf-winuser-showwindow) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b291-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1b291-134">Requirements</span></span>



| <span data-ttu-id="1b291-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="1b291-135">Requirement</span></span> | <span data-ttu-id="1b291-136">Value</span><span class="sxs-lookup"><span data-stu-id="1b291-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b291-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b291-137">Minimum supported client</span></span><br/> | <span data-ttu-id="1b291-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1b291-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1b291-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1b291-139">Minimum supported server</span></span><br/> | <span data-ttu-id="1b291-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1b291-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1b291-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1b291-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b291-142"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1b291-142"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b291-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="1b291-143">See also</span></span>

<dl> <dt>

<span data-ttu-id="1b291-144">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1b291-144">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1b291-145">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1b291-145">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1b291-146">**ShowOwnedPopups**</span><span class="sxs-lookup"><span data-stu-id="1b291-146">**ShowOwnedPopups**</span></span>](/windows/win32/api/winuser/nf-winuser-showownedpopups)
</dt> <dt>

[<span data-ttu-id="1b291-147">**ShowWindow**</span><span class="sxs-lookup"><span data-stu-id="1b291-147">**ShowWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-showwindow)
</dt> <dt>

<span data-ttu-id="1b291-148">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1b291-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1b291-149">Windows</span><span class="sxs-lookup"><span data-stu-id="1b291-149">Windows</span></span>](windows.md)
</dt> </dl>

 

 
