---
description: Se envía cuando una aplicación cambia el estado habilitado de una ventana.
ms.assetid: df2cf953-121f-43bb-a06c-d10e445bfb5e
title: Mensaje de WM_ENABLE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82bc83b84cbbf8e0c0145ef7d2730179cab54a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697374"
---
# <a name="wm_enable-message"></a><span data-ttu-id="6dce5-103">\_Mensaje de habilitación de WM</span><span class="sxs-lookup"><span data-stu-id="6dce5-103">WM\_ENABLE message</span></span>

<span data-ttu-id="6dce5-104">Se envía cuando una aplicación cambia el estado habilitado de una ventana.</span><span class="sxs-lookup"><span data-stu-id="6dce5-104">Sent when an application changes the enabled state of a window.</span></span> <span data-ttu-id="6dce5-105">Se envía a la ventana cuyo estado habilitado está cambiando.</span><span class="sxs-lookup"><span data-stu-id="6dce5-105">It is sent to the window whose enabled state is changing.</span></span> <span data-ttu-id="6dce5-106">Este mensaje se envía antes de que se devuelva la función [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) , pero después de que se haya cambiado el estado habilitado (bit de estilo [**WS \_ Disabled**](window-styles.md) ) de la ventana.</span><span class="sxs-lookup"><span data-stu-id="6dce5-106">This message is sent before the [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) function returns, but after the enabled state ([**WS\_DISABLED**](window-styles.md) style bit) of the window has changed.</span></span>

<span data-ttu-id="6dce5-107">Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="6dce5-107">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ENABLE                       0x000A
```



## <a name="parameters"></a><span data-ttu-id="6dce5-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6dce5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6dce5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6dce5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dce5-110">Indica si la ventana se ha habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="6dce5-110">Indicates whether the window has been enabled or disabled.</span></span> <span data-ttu-id="6dce5-111">Este parámetro es **true** si se ha habilitado la ventana o **false** si se ha deshabilitado la ventana.</span><span class="sxs-lookup"><span data-stu-id="6dce5-111">This parameter is **TRUE** if the window has been enabled or **FALSE** if the window has been disabled.</span></span>

</dd> <dt>

<span data-ttu-id="6dce5-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6dce5-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6dce5-113">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="6dce5-113">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6dce5-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6dce5-114">Return value</span></span>

<span data-ttu-id="6dce5-115">Tipo: **LRESULT**</span><span class="sxs-lookup"><span data-stu-id="6dce5-115">Type: **LRESULT**</span></span>

<span data-ttu-id="6dce5-116">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="6dce5-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="6dce5-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6dce5-117">Requirements</span></span>



| <span data-ttu-id="6dce5-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6dce5-118">Requirement</span></span> | <span data-ttu-id="6dce5-119">Value</span><span class="sxs-lookup"><span data-stu-id="6dce5-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dce5-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dce5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6dce5-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6dce5-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="6dce5-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6dce5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6dce5-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6dce5-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="6dce5-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6dce5-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6dce5-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6dce5-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6dce5-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6dce5-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="6dce5-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="6dce5-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="6dce5-128">**EnableWindow**</span><span class="sxs-lookup"><span data-stu-id="6dce5-128">**EnableWindow**</span></span>](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

<span data-ttu-id="6dce5-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="6dce5-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6dce5-130">Windows</span><span class="sxs-lookup"><span data-stu-id="6dce5-130">Windows</span></span>](windows.md)
</dt> </dl>

 

 
