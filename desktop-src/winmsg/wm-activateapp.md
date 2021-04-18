---
description: Se envía cuando se va a activar una ventana que pertenece a una aplicación diferente de la ventana activa. El mensaje se envía a la aplicación cuya ventana se está activando y a la aplicación cuya ventana se está desactivando.
ms.assetid: fc3626ac-8f19-4aa6-8fe9-5020d00c09db
title: Mensaje de WM_ACTIVATEAPP (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee2d64b90426e004a3c18fdc60538fd21862c42f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706679"
---
# <a name="wm_activateapp-message"></a><span data-ttu-id="92681-104">Mensaje de ACTIVATEAPP de WM \_</span><span class="sxs-lookup"><span data-stu-id="92681-104">WM\_ACTIVATEAPP message</span></span>

<span data-ttu-id="92681-105">Se envía cuando se va a activar una ventana que pertenece a una aplicación diferente de la ventana activa.</span><span class="sxs-lookup"><span data-stu-id="92681-105">Sent when a window belonging to a different application than the active window is about to be activated.</span></span> <span data-ttu-id="92681-106">El mensaje se envía a la aplicación cuya ventana se está activando y a la aplicación cuya ventana se está desactivando.</span><span class="sxs-lookup"><span data-stu-id="92681-106">The message is sent to the application whose window is being activated and to the application whose window is being deactivated.</span></span>

<span data-ttu-id="92681-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="92681-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ACTIVATEAPP                  0x001C
```



## <a name="parameters"></a><span data-ttu-id="92681-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="92681-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92681-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="92681-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92681-110">Indica si la ventana se está activando o desactivando.</span><span class="sxs-lookup"><span data-stu-id="92681-110">Indicates whether the window is being activated or deactivated.</span></span> <span data-ttu-id="92681-111">Este parámetro es **true** si la ventana se está activando; es **false** si la ventana se está desactivando.</span><span class="sxs-lookup"><span data-stu-id="92681-111">This parameter is **TRUE** if the window is being activated; it is **FALSE** if the window is being deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="92681-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92681-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92681-113">Identificador de subproceso.</span><span class="sxs-lookup"><span data-stu-id="92681-113">The thread identifier.</span></span> <span data-ttu-id="92681-114">Si el parámetro *wParam* es **true**, *lParam* es el identificador del subproceso que posee la ventana que se va a desactivar.</span><span class="sxs-lookup"><span data-stu-id="92681-114">If the *wParam* parameter is **TRUE**, *lParam* is the identifier of the thread that owns the window being deactivated.</span></span> <span data-ttu-id="92681-115">Si *wParam* es **false**, *lParam* es el identificador del subproceso que posee la ventana que se está activando.</span><span class="sxs-lookup"><span data-stu-id="92681-115">If *wParam* is **FALSE**, *lParam* is the identifier of the thread that owns the window being activated.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92681-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="92681-116">Return value</span></span>

<span data-ttu-id="92681-117">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="92681-117">Type: **LRESULT**</span></span>

<span data-ttu-id="92681-118">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="92681-118">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="92681-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92681-119">Requirements</span></span>



| <span data-ttu-id="92681-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="92681-120">Requirement</span></span> | <span data-ttu-id="92681-121">Value</span><span class="sxs-lookup"><span data-stu-id="92681-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92681-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92681-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92681-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="92681-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="92681-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92681-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92681-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="92681-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="92681-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92681-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92681-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="92681-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92681-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="92681-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="92681-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="92681-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="92681-130">**activación de WM \_**</span><span class="sxs-lookup"><span data-stu-id="92681-130">**WM\_ACTIVATE**</span></span>](../inputdev/wm-activate.md)
</dt> <dt>

<span data-ttu-id="92681-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="92681-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="92681-132">Windows</span><span class="sxs-lookup"><span data-stu-id="92681-132">Windows</span></span>](windows.md)
</dt> </dl>

 

 
