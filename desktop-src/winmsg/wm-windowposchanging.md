---
description: Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z está a punto de cambiar como resultado de una llamada a la función SetWindowPos u otra función de administración de ventanas.
ms.assetid: 45ecd966-5222-4738-9e99-8a6edbdd435a
title: Mensaje de WM_WINDOWPOSCHANGING (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015a31aac31d38506d1798f83c8dd7f9aa646f85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816307"
---
# <a name="wm_windowposchanging-message"></a><span data-ttu-id="5ac50-103">Mensaje de WINDOWPOSCHANGING de WM \_</span><span class="sxs-lookup"><span data-stu-id="5ac50-103">WM\_WINDOWPOSCHANGING message</span></span>

<span data-ttu-id="5ac50-104">Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z está a punto de cambiar como resultado de una llamada a la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) u otra función de administración de ventanas.</span><span class="sxs-lookup"><span data-stu-id="5ac50-104">Sent to a window whose size, position, or place in the Z order is about to change as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="5ac50-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="5ac50-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGING            0x0046
```



## <a name="parameters"></a><span data-ttu-id="5ac50-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ac50-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ac50-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5ac50-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac50-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="5ac50-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="5ac50-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5ac50-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5ac50-110">Puntero a una estructura [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) que contiene información sobre el nuevo tamaño y la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="5ac50-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ac50-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ac50-111">Return value</span></span>

<span data-ttu-id="5ac50-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="5ac50-112">Type: **LRESULT**</span></span>

<span data-ttu-id="5ac50-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="5ac50-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ac50-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ac50-114">Remarks</span></span>

<span data-ttu-id="5ac50-115">En el caso de una ventana con el estilo [**WS \_ OVERLAPPED**](window-styles.md) o **WS \_ THICKFRAME** , la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía el mensaje de [**WM \_ GETMINMAXINFO**](wm-getminmaxinfo.md) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="5ac50-115">For a window with the [**WS\_OVERLAPPED**](window-styles.md) or **WS\_THICKFRAME** style, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_GETMINMAXINFO**](wm-getminmaxinfo.md) message to the window.</span></span> <span data-ttu-id="5ac50-116">Esto se hace para validar el nuevo tamaño y la posición de la ventana y aplicar los estilos [CS \_ BYTEALIGNCLIENT](about-window-classes.md) y CS \_ BYTEALIGNWINDOW Client.</span><span class="sxs-lookup"><span data-stu-id="5ac50-116">This is done to validate the new size and position of the window and to enforce the [CS\_BYTEALIGNCLIENT](about-window-classes.md) and CS\_BYTEALIGNWINDOW client styles.</span></span> <span data-ttu-id="5ac50-117">Al no pasar el mensaje de **\_ WINDOWPOSCHANGING de WM** a la función **DefWindowProc** , una aplicación puede invalidar estos valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="5ac50-117">By not passing the **WM\_WINDOWPOSCHANGING** message to the **DefWindowProc** function, an application can override these defaults.</span></span>

<span data-ttu-id="5ac50-118">Mientras se está procesando este mensaje, la modificación de los valores de [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) afecta al nuevo tamaño, posición o lugar en el orden Z.</span><span class="sxs-lookup"><span data-stu-id="5ac50-118">While this message is being processed, modifying any of the values in [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) affects the window's new size, position, or place in the Z order.</span></span> <span data-ttu-id="5ac50-119">Una aplicación puede evitar cambios en la ventana estableciendo o borrando los bits adecuados en el miembro **Flags** de **windowpos (**.</span><span class="sxs-lookup"><span data-stu-id="5ac50-119">An application can prevent changes to the window by setting or clearing the appropriate bits in the **flags** member of **WINDOWPOS**.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ac50-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ac50-120">Requirements</span></span>



| <span data-ttu-id="5ac50-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ac50-121">Requirement</span></span> | <span data-ttu-id="5ac50-122">Value</span><span class="sxs-lookup"><span data-stu-id="5ac50-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ac50-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ac50-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5ac50-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="5ac50-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5ac50-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ac50-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5ac50-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="5ac50-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ac50-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ac50-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ac50-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5ac50-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ac50-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ac50-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="5ac50-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="5ac50-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="5ac50-131">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5ac50-131">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="5ac50-132">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="5ac50-132">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="5ac50-133">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="5ac50-133">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="5ac50-134">**WINDOWPOS (**</span><span class="sxs-lookup"><span data-stu-id="5ac50-134">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="5ac50-135">**GETMINMAXINFO de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5ac50-135">**WM\_GETMINMAXINFO**</span></span>](wm-getminmaxinfo.md)
</dt> <dt>

[<span data-ttu-id="5ac50-136">**movimiento de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5ac50-136">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="5ac50-137">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5ac50-137">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="5ac50-138">**WINDOWPOSCHANGED de WM \_**</span><span class="sxs-lookup"><span data-stu-id="5ac50-138">**WM\_WINDOWPOSCHANGED**</span></span>](wm-windowposchanged.md)
</dt> <dt>

<span data-ttu-id="5ac50-139">**Vista**</span><span class="sxs-lookup"><span data-stu-id="5ac50-139">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5ac50-140">Windows</span><span class="sxs-lookup"><span data-stu-id="5ac50-140">Windows</span></span>](windows.md)
</dt> </dl>

 

 
