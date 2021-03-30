---
title: Mensaje de WM_INITMENUPOPUP (Winuser. h)
description: Se envía cuando un menú desplegable o un submenú está a punto de activarse. Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e02bf0f9b8e196c27990cc1bc839daed4c92f8c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079088"
---
# <a name="wm_initmenupopup-message"></a><span data-ttu-id="f52fe-105">Mensaje de INITMENUPOPUP de WM \_</span><span class="sxs-lookup"><span data-stu-id="f52fe-105">WM\_INITMENUPOPUP message</span></span>

<span data-ttu-id="f52fe-106">Se envía cuando un menú desplegable o un submenú está a punto de activarse.</span><span class="sxs-lookup"><span data-stu-id="f52fe-106">Sent when a drop-down menu or submenu is about to become active.</span></span> <span data-ttu-id="f52fe-107">Esto permite que una aplicación modifique el menú antes de que se muestre, sin cambiar todo el menú.</span><span class="sxs-lookup"><span data-stu-id="f52fe-107">This allows an application to modify the menu before it is displayed, without changing the entire menu.</span></span>


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a><span data-ttu-id="f52fe-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f52fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f52fe-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f52fe-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f52fe-110">Identificador del menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="f52fe-110">A handle to the drop-down menu or submenu.</span></span>

</dd> <dt>

<span data-ttu-id="f52fe-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f52fe-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f52fe-112">La palabra de orden inferior especifica la posición relativa de base cero del elemento de menú que abre el menú desplegable o submenú.</span><span class="sxs-lookup"><span data-stu-id="f52fe-112">The low-order word specifies the zero-based relative position of the menu item that opens the drop-down menu or submenu.</span></span>

<span data-ttu-id="f52fe-113">La palabra de orden superior indica si el menú desplegable es el menú ventana.</span><span class="sxs-lookup"><span data-stu-id="f52fe-113">The high-order word indicates whether the drop-down menu is the window menu.</span></span> <span data-ttu-id="f52fe-114">Si el menú es el menú ventana, este parámetro es **true**; de lo contrario, es **false**.</span><span class="sxs-lookup"><span data-stu-id="f52fe-114">If the menu is the window menu, this parameter is **TRUE**; otherwise, it is **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f52fe-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f52fe-115">Return value</span></span>

<span data-ttu-id="f52fe-116">Si una aplicación procesa este mensaje, debe devolver cero.</span><span class="sxs-lookup"><span data-stu-id="f52fe-116">If an application processes this message, it should return zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f52fe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f52fe-117">Requirements</span></span>



| <span data-ttu-id="f52fe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f52fe-118">Requirement</span></span> | <span data-ttu-id="f52fe-119">Value</span><span class="sxs-lookup"><span data-stu-id="f52fe-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f52fe-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f52fe-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="f52fe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="f52fe-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f52fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f52fe-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="f52fe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f52fe-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f52fe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f52fe-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f52fe-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f52fe-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f52fe-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f52fe-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f52fe-127">**Reference**</span></span>
</dt> <dt>

<span data-ttu-id="f52fe-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f52fe-128">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="f52fe-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f52fe-129">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f52fe-130">**INITMENU de WM \_**</span><span class="sxs-lookup"><span data-stu-id="f52fe-130">**WM\_INITMENU**</span></span>](wm-initmenu.md)
</dt> <dt>

<span data-ttu-id="f52fe-131">**Vista**</span><span class="sxs-lookup"><span data-stu-id="f52fe-131">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f52fe-132">Aceleradores de teclado</span><span class="sxs-lookup"><span data-stu-id="f52fe-132">Keyboard Accelerators</span></span>](keyboard-accelerators.md)
</dt> </dl>

 

