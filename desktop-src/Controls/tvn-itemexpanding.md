---
title: Código de notificación de TVN_ITEMEXPANDING (commctrl. h)
description: Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse. Este código de notificación se envía en forma de mensaje de \_ notificación de WM.
ms.assetid: 5ce256df-49e5-4fbf-9cdc-79dd2edbd8ec
keywords:
- TVN_ITEMEXPANDING controles de código de notificación de Windows
topic_type:
- apiref
api_name:
- TVN_ITEMEXPANDING
- TVN_ITEMEXPANDINGA
- TVN_ITEMEXPANDINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c9ed93eacb6d5b492d509b40cc789a803d04623
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997015"
---
# <a name="tvn_itemexpanding-notification-code"></a><span data-ttu-id="790c9-105">Código de notificación de ITEMEXPANDING de TVN \_</span><span class="sxs-lookup"><span data-stu-id="790c9-105">TVN\_ITEMEXPANDING notification code</span></span>

<span data-ttu-id="790c9-106">Notifica a la ventana primaria de un control de vista de árbol que la lista de elementos secundarios de un elemento primario está a punto de expandirse o contraerse.</span><span class="sxs-lookup"><span data-stu-id="790c9-106">Notifies a tree-view control's parent window that a parent item's list of child items is about to expand or collapse.</span></span> <span data-ttu-id="790c9-107">Este código de notificación se envía en forma de mensaje [**de \_ notificación de WM**](wm-notify.md) .</span><span class="sxs-lookup"><span data-stu-id="790c9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TVN_ITEMEXPANDING 

    pnmtv = (LPNMTREEVIEW) lParam 
```



## <a name="parameters"></a><span data-ttu-id="790c9-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="790c9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="790c9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="790c9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="790c9-110">Puntero a una estructura [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) .</span><span class="sxs-lookup"><span data-stu-id="790c9-110">Pointer to an [**NMTREEVIEW**](/windows/win32/api/commctrl/ns-commctrl-nmtreeviewa) structure.</span></span> <span data-ttu-id="790c9-111">El miembro **itemNew** es una estructura [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) que contiene información válida sobre el elemento primario en los miembros **hItem**, **State** y **lParam** .</span><span class="sxs-lookup"><span data-stu-id="790c9-111">The **itemNew** member is a [**TVITEM**](/windows/win32/api/commctrl/ns-commctrl-tvitema) structure that contains valid information about the parent item in the **hItem**, **state**, and **lParam** members.</span></span> <span data-ttu-id="790c9-112">El miembro de **acción** indica si la lista debe expandirse o contraerse.</span><span class="sxs-lookup"><span data-stu-id="790c9-112">The **action** member indicates whether the list is to expand or collapse.</span></span> <span data-ttu-id="790c9-113">Para obtener una lista de los valores posibles, vea la descripción del mensaje de [**\_ expansión TVM**](tvm-expand.md) .</span><span class="sxs-lookup"><span data-stu-id="790c9-113">For a list of possible values, see the description of the [**TVM\_EXPAND**](tvm-expand.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="790c9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="790c9-114">Return value</span></span>

<span data-ttu-id="790c9-115">Devuelve **true** para evitar que la lista se expanda o contraiga.</span><span class="sxs-lookup"><span data-stu-id="790c9-115">Returns **TRUE** to prevent the list from expanding or collapsing.</span></span>

## <a name="requirements"></a><span data-ttu-id="790c9-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="790c9-116">Requirements</span></span>



| <span data-ttu-id="790c9-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="790c9-117">Requirement</span></span> | <span data-ttu-id="790c9-118">Value</span><span class="sxs-lookup"><span data-stu-id="790c9-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="790c9-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="790c9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="790c9-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="790c9-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="790c9-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="790c9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="790c9-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="790c9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="790c9-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="790c9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="790c9-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="790c9-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="790c9-125">Nombres Unicode y ANSI</span><span class="sxs-lookup"><span data-stu-id="790c9-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="790c9-126">**TVN \_ ITEMEXPANDINGW** (Unicode) y **TVN \_ ITEMEXPANDINGA** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="790c9-126">**TVN\_ITEMEXPANDINGW** (Unicode) and **TVN\_ITEMEXPANDINGA** (ANSI)</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="790c9-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="790c9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="790c9-128">TVN \_ ITEMEXPANDED</span><span class="sxs-lookup"><span data-stu-id="790c9-128">TVN\_ITEMEXPANDED</span></span>](tvn-itemexpanded.md)
</dt> </dl>

 

 





