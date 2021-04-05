---
title: Mensaje de WM_EXITMENULOOP (Winuser. h)
description: Notifica al procedimiento de ventana principal de una aplicación que se ha salido de un bucle modal de menú.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8440e1a255968eb3e1607b5d54375900f7b5de16
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802431"
---
# <a name="wm_exitmenuloop-message"></a><span data-ttu-id="e5476-104">Mensaje de EXITMENULOOP de WM \_</span><span class="sxs-lookup"><span data-stu-id="e5476-104">WM\_EXITMENULOOP message</span></span>

<span data-ttu-id="e5476-105">Notifica al procedimiento de ventana principal de una aplicación que se ha salido de un bucle modal de menú.</span><span class="sxs-lookup"><span data-stu-id="e5476-105">Notifies an application's main window procedure that a menu modal loop has been exited.</span></span>


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a><span data-ttu-id="e5476-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e5476-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5476-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="e5476-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5476-108">Especifica si el menú es un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="e5476-108">Specifies whether the menu is a shortcut menu.</span></span> <span data-ttu-id="e5476-109">Este parámetro tiene un valor **true** si se trata de un menú contextual, **false** en caso contrario.</span><span class="sxs-lookup"><span data-stu-id="e5476-109">This parameter has a value of **TRUE** if it is a shortcut menu, **FALSE** if it is not.</span></span>

</dd> <dt>

<span data-ttu-id="e5476-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="e5476-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="e5476-111">Este parámetro no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="e5476-111">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5476-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e5476-112">Return value</span></span>

<span data-ttu-id="e5476-113">Una aplicación debe devolver cero si procesa este mensaje.</span><span class="sxs-lookup"><span data-stu-id="e5476-113">An application should return zero if it processes this message.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5476-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5476-114">Remarks</span></span>

<span data-ttu-id="e5476-115">La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e5476-115">The [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5476-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e5476-116">Requirements</span></span>



| <span data-ttu-id="e5476-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e5476-117">Requirement</span></span> | <span data-ttu-id="e5476-118">Value</span><span class="sxs-lookup"><span data-stu-id="e5476-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5476-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5476-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e5476-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e5476-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="e5476-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e5476-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e5476-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e5476-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="e5476-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e5476-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="e5476-124"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e5476-124"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e5476-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="e5476-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="e5476-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="e5476-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="e5476-127">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="e5476-127">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[<span data-ttu-id="e5476-128">**ENTERMENULOOP de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e5476-128">**WM\_ENTERMENULOOP**</span></span>](wm-entermenuloop.md)
</dt> <dt>

<span data-ttu-id="e5476-129">**Vista**</span><span class="sxs-lookup"><span data-stu-id="e5476-129">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="e5476-130">Menús</span><span class="sxs-lookup"><span data-stu-id="e5476-130">Menus</span></span>](menus.md)
</dt> </dl>

 

