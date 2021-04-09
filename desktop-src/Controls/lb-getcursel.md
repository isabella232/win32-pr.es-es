---
title: Mensaje de LB_GETCURSEL (Winuser. h)
description: Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- LB_GETCURSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079717"
---
# <a name="lb_getcursel-message"></a><span data-ttu-id="cd751-104">\_Mensaje lb GETCURSEL</span><span class="sxs-lookup"><span data-stu-id="cd751-104">LB\_GETCURSEL message</span></span>

<span data-ttu-id="cd751-105">Obtiene el índice del elemento seleccionado actualmente, si existe, en un cuadro de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="cd751-105">Gets the index of the currently selected item, if any, in a single-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="cd751-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="cd751-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd751-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cd751-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd751-108">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cd751-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="cd751-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cd751-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cd751-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="cd751-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd751-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="cd751-111">Return value</span></span>

<span data-ttu-id="cd751-112">En un cuadro de lista de selección única, el valor devuelto es el índice de base cero del elemento actualmente seleccionado.</span><span class="sxs-lookup"><span data-stu-id="cd751-112">In a single-selection list box, the return value is the zero-based index of the currently selected item.</span></span> <span data-ttu-id="cd751-113">Si no hay ninguna selección, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="cd751-113">If there is no selection, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd751-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cd751-114">Remarks</span></span>

<span data-ttu-id="cd751-115">Para recuperar los índices de los elementos seleccionados en un cuadro de lista de selección múltiple, use el mensaje [**lb \_ GETSELITEMS**](lb-getselitems.md) .</span><span class="sxs-lookup"><span data-stu-id="cd751-115">To retrieve the indexes of the selected items in a multiple-selection list box, use the [**LB\_GETSELITEMS**](lb-getselitems.md) message.</span></span> <span data-ttu-id="cd751-116">Para determinar si el elemento que tiene el rectángulo de foco en un cuadro de lista de selección múltiple está seleccionado, use el mensaje [**lb \_ GETSEL**](lb-getsel.md) .</span><span class="sxs-lookup"><span data-stu-id="cd751-116">To determine whether the item that has the focus rectangle in a multiple selection list box is selected, use the [**LB\_GETSEL**](lb-getsel.md) message.</span></span>

<span data-ttu-id="cd751-117">Si se envía a un cuadro de lista de selección múltiple, **lb \_ GETCURSEL** devuelve el índice del elemento que tiene el rectángulo de foco.</span><span class="sxs-lookup"><span data-stu-id="cd751-117">If sent to a multiple-selection list box, **LB\_GETCURSEL** returns the index of the item that has the focus rectangle.</span></span> <span data-ttu-id="cd751-118">Si no se selecciona ningún elemento, devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="cd751-118">If no items are selected, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd751-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd751-119">Requirements</span></span>



| <span data-ttu-id="cd751-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="cd751-120">Requirement</span></span> | <span data-ttu-id="cd751-121">Value</span><span class="sxs-lookup"><span data-stu-id="cd751-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd751-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd751-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd751-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="cd751-123">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="cd751-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="cd751-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd751-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="cd751-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cd751-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="cd751-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd751-127"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cd751-127"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd751-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="cd751-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd751-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="cd751-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cd751-130">**LB \_ GETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="cd751-130">**LB\_GETCARETINDEX**</span></span>](lb-getcaretindex.md)
</dt> <dt>

[<span data-ttu-id="cd751-131">**LB \_ GETSEL**</span><span class="sxs-lookup"><span data-stu-id="cd751-131">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="cd751-132">**LB \_ GETSELITEMS**</span><span class="sxs-lookup"><span data-stu-id="cd751-132">**LB\_GETSELITEMS**</span></span>](lb-getselitems.md)
</dt> <dt>

[<span data-ttu-id="cd751-133">**LB \_ SETCURSEL**</span><span class="sxs-lookup"><span data-stu-id="cd751-133">**LB\_SETCURSEL**</span></span>](lb-setcursel.md)
</dt> </dl>

 

 





