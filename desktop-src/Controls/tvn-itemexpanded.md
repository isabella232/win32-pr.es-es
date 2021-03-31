---
title: Código de notificación de TVN_ITEMEXPANDED (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario se ha expandido o contraído. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 18d9d61d-6ec5-4d3b-9c02-36d0e61ed232
keywords:
- TVN_ITEMEXPANDED controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDED
- TVN_ITEMEXPANDEDA
- TVN_ITEMEXPANDEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f193e9a0ff029ca607748fe4bbb6d61f781c1248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151041"
---
# <a name="tvn_itemexpanded-notification-code"></a><span data-ttu-id="d69c3-105">Código de notificación de ITEMEXPANDED de TVN \_</span><span class="sxs-lookup"><span data-stu-id="d69c3-105">TVN\_ITEMEXPANDED notification code</span></span>

<span data-ttu-id="d69c3-106">Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario se ha expandido o contraído.</span><span class="sxs-lookup"><span data-stu-id="d69c3-106">Notifies a tree-view control's parent window that a parent item's list of child items has expanded or collapsed.</span></span> <span data-ttu-id="d69c3-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="d69c3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDED 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="d69c3-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d69c3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d69c3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d69c3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d69c3-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="d69c3-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="d69c3-111">El miembro **itemNew** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento primario en los miembros **hItem**, **State** y **lParam** .</span><span class="sxs-lookup"><span data-stu-id="d69c3-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="d69c3-112">El miembro de **acción** indica si la lista está expandida o contraída.</span><span class="sxs-lookup"><span data-stu-id="d69c3-112">The **action** member indicates whether the list expanded or collapsed.</span></span> <span data-ttu-id="d69c3-113">Para obtener una lista de los valores posibles, vea la descripción del mensaje de [**\_ expansión TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="d69c3-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d69c3-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d69c3-114">Return value</span></span>

<span data-ttu-id="d69c3-115">Se omite el valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="d69c3-115">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d69c3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d69c3-116">Requirements</span></span>



| <span data-ttu-id="d69c3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d69c3-117">Requirement</span></span> | <span data-ttu-id="d69c3-118">Value</span><span class="sxs-lookup"><span data-stu-id="d69c3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d69c3-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d69c3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d69c3-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="d69c3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d69c3-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d69c3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d69c3-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="d69c3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d69c3-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d69c3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d69c3-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="d69c3-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="d69c3-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="d69c3-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d69c3-126">**TVN \_ ITEMEXPANDEDW** (Unicode) y **TVN \_ ITEMEXPANDEDA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="d69c3-126">**TVN\_ITEMEXPANDEDW** (Unicode) and **TVN\_ITEMEXPANDEDA** (ANSI)</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="d69c3-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="d69c3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d69c3-128">TVN \_ ITEMEXPANDING</span><span class="sxs-lookup"><span data-stu-id="d69c3-128">TVN\_ITEMEXPANDING</span></span>](tvn-itemexpanding.md)
</dt> </dl>

 

 





