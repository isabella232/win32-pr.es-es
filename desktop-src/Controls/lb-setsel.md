---
title: Mensaje de LB_SETSEL (Winuser. h)
description: Selecciona un elemento en un cuadro de lista de selección múltiple y, si es necesario, desplaza el elemento a la vista.
ms.assetid: 643783f2-0e00-4b79-b957-47938bb9f8da
keywords:
- LB_SETSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd50f12c4190ba9ecafad11b167c1ac60adf691d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492430"
---
# <a name="lb_setsel-message"></a><span data-ttu-id="7845e-104">\_Mensaje lb SETSEL</span><span class="sxs-lookup"><span data-stu-id="7845e-104">LB\_SETSEL message</span></span>

<span data-ttu-id="7845e-105">Selecciona un elemento en un cuadro de lista de selección múltiple y, si es necesario, desplaza el elemento a la vista.</span><span class="sxs-lookup"><span data-stu-id="7845e-105">Selects an item in a multiple-selection list box and, if necessary, scrolls the item into view.</span></span>

## <a name="parameters"></a><span data-ttu-id="7845e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7845e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7845e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="7845e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7845e-108">Especifica cómo establecer la selección.</span><span class="sxs-lookup"><span data-stu-id="7845e-108">Specifies how to set the selection.</span></span> <span data-ttu-id="7845e-109">Si este parámetro es **true**, el elemento se selecciona y se resalta; Si es **false**, se quita el resaltado y ya no se selecciona el elemento.</span><span class="sxs-lookup"><span data-stu-id="7845e-109">If this parameter is **TRUE**, the item is selected and highlighted; if it is **FALSE**, the highlight is removed and the item is no longer selected.</span></span>

</dd> <dt>

<span data-ttu-id="7845e-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="7845e-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="7845e-111">Especifica el índice de base cero del elemento que se va a establecer.</span><span class="sxs-lookup"><span data-stu-id="7845e-111">Specifies the zero-based index of the item to set.</span></span> <span data-ttu-id="7845e-112">Si este parámetro es-1, la selección se agrega o se quita de todos los elementos, dependiendo del valor de *wParam*, y no se produce ningún desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="7845e-112">If this parameter is -1, the selection is added to or removed from all items, depending on the value of *wParam*, and no scrolling occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7845e-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7845e-113">Return value</span></span>

<span data-ttu-id="7845e-114">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="7845e-114">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="7845e-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7845e-115">Remarks</span></span>

<span data-ttu-id="7845e-116">Use este mensaje solo con cuadros de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="7845e-116">Use this message only with multiple-selection list boxes.</span></span>

## <a name="requirements"></a><span data-ttu-id="7845e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7845e-117">Requirements</span></span>



| <span data-ttu-id="7845e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7845e-118">Requirement</span></span> | <span data-ttu-id="7845e-119">Value</span><span class="sxs-lookup"><span data-stu-id="7845e-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7845e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7845e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7845e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="7845e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="7845e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7845e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7845e-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="7845e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="7845e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7845e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7845e-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7845e-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7845e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="7845e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="7845e-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="7845e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="7845e-128">**LB \_ GETSEL**</span><span class="sxs-lookup"><span data-stu-id="7845e-128">**LB\_GETSEL**</span></span>](lb-getsel.md)
</dt> <dt>

[<span data-ttu-id="7845e-129">**LB \_ SELITEMRANGE**</span><span class="sxs-lookup"><span data-stu-id="7845e-129">**LB\_SELITEMRANGE**</span></span>](lb-selitemrange.md)
</dt> </dl>

 

 





