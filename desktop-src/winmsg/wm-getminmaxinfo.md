---
description: Se envía a una ventana cuando el tamaño o la posición de la ventana está a punto de cambiar. Una aplicación puede usar este mensaje para invalidar el tamaño maximizado y la posición predeterminados de la ventana, o el tamaño de seguimiento máximo o mínimo predeterminado.
ms.assetid: af2295e0-2d0b-4ac0-b689-16138022f4b7
title: Mensaje de WM_GETMINMAXINFO (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a29cbca97d38f7fca90c93ef7bf0606ea49306da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911377"
---
# <a name="wm_getminmaxinfo-message"></a><span data-ttu-id="065f0-104">Mensaje de GETMINMAXINFO de WM \_</span><span class="sxs-lookup"><span data-stu-id="065f0-104">WM\_GETMINMAXINFO message</span></span>

<span data-ttu-id="065f0-105">Se envía a una ventana cuando el tamaño o la posición de la ventana está a punto de cambiar.</span><span class="sxs-lookup"><span data-stu-id="065f0-105">Sent to a window when the size or position of the window is about to change.</span></span> <span data-ttu-id="065f0-106">Una aplicación puede usar este mensaje para invalidar el tamaño maximizado y la posición predeterminados de la ventana, o el tamaño de seguimiento máximo o mínimo predeterminado.</span><span class="sxs-lookup"><span data-stu-id="065f0-106">An application can use this message to override the window's default maximized size and position, or its default minimum or maximum tracking size.</span></span>

<span data-ttu-id="065f0-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="065f0-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_GETMINMAXINFO                0x0024
```



## <a name="parameters"></a><span data-ttu-id="065f0-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="065f0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="065f0-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="065f0-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="065f0-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="065f0-110">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="065f0-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="065f0-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="065f0-112">Puntero a una estructura [**minmaxinfo (**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) que contiene las dimensiones y la posición maximizadas predeterminadas, y los tamaños de seguimiento mínimo y máximo predeterminados.</span><span class="sxs-lookup"><span data-stu-id="065f0-112">A pointer to a [**MINMAXINFO**](/windows/win32/api/winuser/ns-winuser-minmaxinfo) structure that contains the default maximized position and dimensions, and the default minimum and maximum tracking sizes.</span></span> <span data-ttu-id="065f0-113">Una aplicación puede invalidar los valores predeterminados estableciendo los miembros de esta estructura.</span><span class="sxs-lookup"><span data-stu-id="065f0-113">An application can override the defaults by setting the members of this structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="065f0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="065f0-114">Return value</span></span>

<span data-ttu-id="065f0-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="065f0-115">Type: **LRESULT**</span></span>

<span data-ttu-id="065f0-116">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="065f0-116">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="065f0-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="065f0-117">Remarks</span></span>

<span data-ttu-id="065f0-118">El tamaño máximo de seguimiento es el tamaño de ventana más grande que se puede generar mediante el uso de los bordes para ajustar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="065f0-118">The maximum tracking size is the largest window size that can be produced by using the borders to size the window.</span></span> <span data-ttu-id="065f0-119">El tamaño mínimo de seguimiento es el tamaño de ventana más pequeño que se puede generar mediante el uso de los bordes para ajustar el tamaño de la ventana.</span><span class="sxs-lookup"><span data-stu-id="065f0-119">The minimum tracking size is the smallest window size that can be produced by using the borders to size the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="065f0-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="065f0-120">Requirements</span></span>



| <span data-ttu-id="065f0-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="065f0-121">Requirement</span></span> | <span data-ttu-id="065f0-122">Value</span><span class="sxs-lookup"><span data-stu-id="065f0-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="065f0-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="065f0-123">Minimum supported client</span></span><br/> | <span data-ttu-id="065f0-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="065f0-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="065f0-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="065f0-125">Minimum supported server</span></span><br/> | <span data-ttu-id="065f0-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="065f0-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="065f0-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="065f0-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="065f0-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="065f0-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="065f0-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="065f0-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="065f0-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="065f0-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="065f0-131">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="065f0-131">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="065f0-132">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="065f0-132">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

[<span data-ttu-id="065f0-133">**MINMAXINFO (**</span><span class="sxs-lookup"><span data-stu-id="065f0-133">**MINMAXINFO**</span></span>](/windows/win32/api/winuser/ns-winuser-minmaxinfo)
</dt> <dt>

<span data-ttu-id="065f0-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="065f0-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="065f0-135">Windows</span><span class="sxs-lookup"><span data-stu-id="065f0-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
