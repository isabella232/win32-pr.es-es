---
title: Mensaje de WM_ENTERMENULOOP (Winuser. h)
description: Notifica al procedimiento de ventana principal de una aplicación que se ha especificado un bucle modal de menú.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a7b325719c428dc7310503320b53f3a5f96182e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714553"
---
# <a name="wm_entermenuloop-message"></a><span data-ttu-id="98c2d-104">Mensaje de ENTERMENULOOP de WM \_</span><span class="sxs-lookup"><span data-stu-id="98c2d-104">WM\_ENTERMENULOOP message</span></span>

<span data-ttu-id="98c2d-105">Notifica al procedimiento de ventana principal de una aplicación que se ha especificado un bucle modal de menú.</span><span class="sxs-lookup"><span data-stu-id="98c2d-105">Notifies an application's main window procedure that a menu modal loop has been entered.</span></span>


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a><span data-ttu-id="98c2d-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98c2d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98c2d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="98c2d-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98c2d-108">Especifica si el menú ventana se ha especificado mediante la función [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) .</span><span class="sxs-lookup"><span data-stu-id="98c2d-108">Specifies whether the window menu was entered using the [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) function.</span></span> <span data-ttu-id="98c2d-109">Este parámetro tiene un valor **true** si el menú ventana se escribió con **TrackPopupMenu** y **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="98c2d-109">This parameter has a value of **TRUE** if the window menu was entered using **TrackPopupMenu**, and **FALSE** if it was not.</span></span>

</dd> <dt>

<span data-ttu-id="98c2d-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="98c2d-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="98c2d-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="98c2d-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98c2d-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98c2d-112">Return value</span></span>

<span data-ttu-id="98c2d-113">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="98c2d-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="98c2d-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98c2d-114">Remarks</span></span>

<span data-ttu-id="98c2d-115">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="98c2d-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="98c2d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98c2d-116">Requirements</span></span>



| <span data-ttu-id="98c2d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="98c2d-117">Requirement</span></span> | <span data-ttu-id="98c2d-118">Value</span><span class="sxs-lookup"><span data-stu-id="98c2d-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="98c2d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c2d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="98c2d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="98c2d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="98c2d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98c2d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="98c2d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="98c2d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="98c2d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="98c2d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="98c2d-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="98c2d-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98c2d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="98c2d-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="98c2d-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="98c2d-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="98c2d-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="98c2d-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="98c2d-128">**EXITMENULOOP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="98c2d-128">**WM\_EXITMENULOOP**</span></span>](wm-exitmenuloop.md)
</dt> <dt>

<span data-ttu-id="98c2d-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="98c2d-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="98c2d-130">Menús</span><span class="sxs-lookup"><span data-stu-id="98c2d-130">Menus</span></span>](menus.md)
</dt> </dl>

 

