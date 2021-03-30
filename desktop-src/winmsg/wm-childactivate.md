---
description: Se envía a una ventana secundaria cuando el usuario hace clic en la barra de título de la ventana o cuando la ventana se activa, se mueve o se ajusta su tamaño.
ms.assetid: 6e60725d-aa01-48bb-86a5-f17f56b97d35
title: Mensaje de WM_CHILDACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a82564a63cfbbbfe5e3693e331c8e990fa934e53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815462"
---
# <a name="wm_childactivate-message"></a><span data-ttu-id="0c607-103">Mensaje de CHILDACTIVATE de WM \_</span><span class="sxs-lookup"><span data-stu-id="0c607-103">WM\_CHILDACTIVATE message</span></span>

<span data-ttu-id="0c607-104">Se envía a una ventana secundaria cuando el usuario hace clic en la barra de título de la ventana o cuando la ventana se activa, se mueve o se ajusta su tamaño.</span><span class="sxs-lookup"><span data-stu-id="0c607-104">Sent to a child window when the user clicks the window's title bar or when the window is activated, moved, or sized.</span></span>

<span data-ttu-id="0c607-105">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="0c607-105">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_CHILDACTIVATE                0x0022
```



## <a name="parameters"></a><span data-ttu-id="0c607-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0c607-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c607-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="0c607-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c607-108">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0c607-108">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="0c607-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="0c607-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="0c607-110">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="0c607-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c607-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0c607-111">Return value</span></span>

<span data-ttu-id="0c607-112">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="0c607-112">Type: **LRESULT**</span></span>

<span data-ttu-id="0c607-113">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="0c607-113">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c607-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c607-114">Requirements</span></span>



| <span data-ttu-id="0c607-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c607-115">Requirement</span></span> | <span data-ttu-id="0c607-116">Value</span><span class="sxs-lookup"><span data-stu-id="0c607-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c607-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c607-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0c607-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0c607-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="0c607-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0c607-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0c607-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0c607-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c607-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0c607-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c607-122"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c607-122"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c607-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="0c607-123">See also</span></span>

<dl> <dt>

<span data-ttu-id="0c607-124">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="0c607-124">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="0c607-125">**MoveWindow**</span><span class="sxs-lookup"><span data-stu-id="0c607-125">**MoveWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-movewindow)
</dt> <dt>

[<span data-ttu-id="0c607-126">**SetWindowPos**</span><span class="sxs-lookup"><span data-stu-id="0c607-126">**SetWindowPos**</span></span>](/windows/win32/api/winuser/nf-winuser-setwindowpos)
</dt> <dt>

<span data-ttu-id="0c607-127">**Vista**</span><span class="sxs-lookup"><span data-stu-id="0c607-127">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="0c607-128">Windows</span><span class="sxs-lookup"><span data-stu-id="0c607-128">Windows</span></span>](windows.md)
</dt> </dl>

 

 
