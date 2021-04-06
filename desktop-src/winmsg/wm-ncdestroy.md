---
description: Notifica a una ventana que se está destruyendo su área no cliente. La función DestroyWindow envía el mensaje de NCDESTROY de WM \_ a la ventana después del mensaje de destrucción de WM \_ .
ms.assetid: 64ab268d-0e90-4401-81d3-a4da64196001
title: Mensaje de WM_NCDESTROY (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a462f679a29f471638299e037749adaf32a85dea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104002026"
---
# <a name="wm_ncdestroy-message"></a><span data-ttu-id="35fde-104">Mensaje de NCDESTROY de WM \_</span><span class="sxs-lookup"><span data-stu-id="35fde-104">WM\_NCDESTROY message</span></span>

<span data-ttu-id="35fde-105">Notifica a una ventana que se está destruyendo su área no cliente.</span><span class="sxs-lookup"><span data-stu-id="35fde-105">Notifies a window that its nonclient area is being destroyed.</span></span> <span data-ttu-id="35fde-106">La función [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) envía el mensaje de **\_ NCDESTROY de WM** a la ventana después del mensaje de [**\_ destrucción de WM**](wm-destroy.md) .[**WM \_ Destroy**](wm-destroy.md) se usa para liberar el objeto de memoria asignado asociado a la ventana.</span><span class="sxs-lookup"><span data-stu-id="35fde-106">The [**DestroyWindow**](/windows/win32/api/winuser/nf-winuser-destroywindow) function sends the **WM\_NCDESTROY** message to the window following the [**WM\_DESTROY**](wm-destroy.md) message.[**WM\_DESTROY**](wm-destroy.md) is used to free the allocated memory object associated with the window.</span></span>

<span data-ttu-id="35fde-107">El mensaje de **\_ NCDESTROY de WM** se envía después de que se hayan destruido las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="35fde-107">The **WM\_NCDESTROY** message is sent after the child windows have been destroyed.</span></span> <span data-ttu-id="35fde-108">En cambio, [**la \_ destrucción de WM**](wm-destroy.md) se envía antes de que se destruyan las ventanas secundarias.</span><span class="sxs-lookup"><span data-stu-id="35fde-108">In contrast, [**WM\_DESTROY**](wm-destroy.md) is sent before the child windows are destroyed.</span></span>

<span data-ttu-id="35fde-109">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="35fde-109">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_NCDESTROY                    0x0082
```



## <a name="parameters"></a><span data-ttu-id="35fde-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35fde-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35fde-111">*wParam*</span><span class="sxs-lookup"><span data-stu-id="35fde-111">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35fde-112">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="35fde-112">This parameter is not used.</span></span>

</dd> <dt>

<span data-ttu-id="35fde-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="35fde-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="35fde-114">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="35fde-114">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35fde-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35fde-115">Return value</span></span>

<span data-ttu-id="35fde-116">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="35fde-116">Type: **LRESULT**</span></span>

<span data-ttu-id="35fde-117">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="35fde-117">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="35fde-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35fde-118">Remarks</span></span>

<span data-ttu-id="35fde-119">Este mensaje libera cualquier memoria asignada internamente para la ventana.</span><span class="sxs-lookup"><span data-stu-id="35fde-119">This message frees any memory internally allocated for the window.</span></span>

## <a name="requirements"></a><span data-ttu-id="35fde-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35fde-120">Requirements</span></span>



| <span data-ttu-id="35fde-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="35fde-121">Requirement</span></span> | <span data-ttu-id="35fde-122">Value</span><span class="sxs-lookup"><span data-stu-id="35fde-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35fde-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35fde-123">Minimum supported client</span></span><br/> | <span data-ttu-id="35fde-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="35fde-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="35fde-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="35fde-125">Minimum supported server</span></span><br/> | <span data-ttu-id="35fde-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="35fde-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="35fde-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="35fde-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="35fde-128"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35fde-128"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35fde-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="35fde-129">See also</span></span>

<dl> <dt>

<span data-ttu-id="35fde-130">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="35fde-130">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="35fde-131">**DestroyWindow**</span><span class="sxs-lookup"><span data-stu-id="35fde-131">**DestroyWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-destroywindow)
</dt> <dt>

[<span data-ttu-id="35fde-132">**destrucción de WM \_**</span><span class="sxs-lookup"><span data-stu-id="35fde-132">**WM\_DESTROY**</span></span>](wm-destroy.md)
</dt> <dt>

[<span data-ttu-id="35fde-133">**NCCREATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="35fde-133">**WM\_NCCREATE**</span></span>](wm-nccreate.md)
</dt> <dt>

<span data-ttu-id="35fde-134">**Vista**</span><span class="sxs-lookup"><span data-stu-id="35fde-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="35fde-135">Windows</span><span class="sxs-lookup"><span data-stu-id="35fde-135">Windows</span></span>](windows.md)
</dt> </dl>

 

 
