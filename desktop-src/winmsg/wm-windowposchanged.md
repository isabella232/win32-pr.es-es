---
description: Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z ha cambiado como resultado de una llamada a la función SetWindowPos u otra función de administración de ventanas.
ms.assetid: 1eabd0b1-1f92-4576-b7fb-8af50fb04526
title: Mensaje de WM_WINDOWPOSCHANGED (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d9bda353a1c7546727818a8a3975696000da0e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154166"
---
# <a name="wm_windowposchanged-message"></a><span data-ttu-id="1a884-103">Mensaje de WINDOWPOSCHANGED de WM \_</span><span class="sxs-lookup"><span data-stu-id="1a884-103">WM\_WINDOWPOSCHANGED message</span></span>

<span data-ttu-id="1a884-104">Se envía a una ventana cuyo tamaño, posición o lugar en el orden Z ha cambiado como resultado de una llamada a la función [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) u otra función de administración de ventanas.</span><span class="sxs-lookup"><span data-stu-id="1a884-104">Sent to a window whose size, position, or place in the Z order has changed as a result of a call to the [**SetWindowPos**](/windows/win32/api/winuser/nf-winuser-setwindowpos) function or another window-management function.</span></span>

<span data-ttu-id="1a884-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1a884-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_WINDOWPOSCHANGED             0x0047
```



## <a name="parameters"></a><span data-ttu-id="1a884-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a884-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a884-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="1a884-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a884-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1a884-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="1a884-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1a884-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1a884-110">Puntero a una estructura [**windowpos (**](/windows/win32/api/winuser/ns-winuser-windowpos) que contiene información sobre el nuevo tamaño y la posición de la ventana.</span><span class="sxs-lookup"><span data-stu-id="1a884-110">A pointer to a [**WINDOWPOS**](/windows/win32/api/winuser/ns-winuser-windowpos) structure that contains information about the window's new size and position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a884-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a884-111">Return value</span></span>

<span data-ttu-id="1a884-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="1a884-112">Type: **LRESULT**</span></span>

<span data-ttu-id="1a884-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="1a884-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a884-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a884-114">Remarks</span></span>

<span data-ttu-id="1a884-115">De forma predeterminada, la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) envía los mensajes de [**\_ tamaño de WM**](wm-size.md) y de [**\_ movimiento de WM**](wm-move.md) a la ventana.</span><span class="sxs-lookup"><span data-stu-id="1a884-115">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function sends the [**WM\_SIZE**](wm-size.md) and [**WM\_MOVE**](wm-move.md) messages to the window.</span></span> <span data-ttu-id="1a884-116">Los mensajes de **\_ tamaño de WM** y **\_ movimiento de WM** no se envían si una aplicación controla el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="1a884-116">The **WM\_SIZE** and **WM\_MOVE** messages are not sent if an application handles the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span> <span data-ttu-id="1a884-117">Es más eficaz realizar cualquier procesamiento de cambios de movimiento o de tamaño durante el mensaje de **\_ WINDOWPOSCHANGED de WM** sin llamar a **DefWindowProc**.</span><span class="sxs-lookup"><span data-stu-id="1a884-117">It is more efficient to perform any move or size change processing during the **WM\_WINDOWPOSCHANGED** message without calling **DefWindowProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a884-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a884-118">Requirements</span></span>



| <span data-ttu-id="1a884-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a884-119">Requirement</span></span> | <span data-ttu-id="1a884-120">Value</span><span class="sxs-lookup"><span data-stu-id="1a884-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a884-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a884-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1a884-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1a884-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="1a884-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a884-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1a884-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a884-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="1a884-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a884-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a884-126"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a884-126"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a884-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1a884-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="1a884-128">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="1a884-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="1a884-129">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="1a884-129">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="1a884-130">**EndDeferWindowPos**</span><span class="sxs-lookup"><span data-stu-id="1a884-130">**EndDeferWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-enddeferwindowpos)
</dt> <dt>

[<span data-ttu-id="1a884-131">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="1a884-131">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="1a884-132">**WINDOWPOS (**</span><span class="sxs-lookup"><span data-stu-id="1a884-132">**WINDOWPOS**</span></span>](/windows/win32/api/winuser/ns-winuser-windowpos)
</dt> <dt>

[<span data-ttu-id="1a884-133">**movimiento de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1a884-133">**WM\_MOVE**</span></span>](wm-move.md)
</dt> <dt>

[<span data-ttu-id="1a884-134">**tamaño de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1a884-134">**WM\_SIZE**</span></span>](wm-size.md)
</dt> <dt>

[<span data-ttu-id="1a884-135">**WINDOWPOSCHANGING de WM \_**</span><span class="sxs-lookup"><span data-stu-id="1a884-135">**WM\_WINDOWPOSCHANGING**</span></span>](wm-windowposchanging.md)
</dt> <dt>

<span data-ttu-id="1a884-136">**Vista**</span><span class="sxs-lookup"><span data-stu-id="1a884-136">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="1a884-137">Windows</span><span class="sxs-lookup"><span data-stu-id="1a884-137">Windows</span></span>](windows.md)
</dt> </dl>

 

 
