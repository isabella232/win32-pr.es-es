---
title: Mensaje de LB_SELITEMRANGE (Winuser. h)
description: Selecciona o anula la selección de uno o varios elementos consecutivos en un cuadro de lista de selección múltiple.
ms.assetid: 817d62df-98a3-40b3-8d62-86bf07ad797f
keywords:
- LB_SELITEMRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SELITEMRANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a137b90a817519cf23c894dc19417dd2d9b6b7f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079660"
---
# <a name="lb_selitemrange-message"></a><span data-ttu-id="b6262-104">\_Mensaje lb SELITEMRANGE</span><span class="sxs-lookup"><span data-stu-id="b6262-104">LB\_SELITEMRANGE message</span></span>

<span data-ttu-id="b6262-105">Selecciona o anula la selección de uno o varios elementos consecutivos en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="b6262-105">Selects or deselects one or more consecutive items in a multiple-selection list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="b6262-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b6262-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b6262-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b6262-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6262-108">**True** para seleccionar el intervalo de elementos o **false** para anular la selección.</span><span class="sxs-lookup"><span data-stu-id="b6262-108">**TRUE** to select the range of items, or **FALSE** to deselect it.</span></span>

</dd> <dt>

<span data-ttu-id="b6262-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b6262-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b6262-110">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica el índice de base cero del primer elemento que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="b6262-110">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the zero-based index of the first item to select.</span></span> <span data-ttu-id="b6262-111">[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica el índice de base cero del último elemento que se va a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="b6262-111">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the zero-based index of the last item to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b6262-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b6262-112">Return value</span></span>

<span data-ttu-id="b6262-113">Si se produce un error, el valor devuelto es LB \_ Err.</span><span class="sxs-lookup"><span data-stu-id="b6262-113">If an error occurs, the return value is LB\_ERR.</span></span>

## <a name="remarks"></a><span data-ttu-id="b6262-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b6262-114">Remarks</span></span>

<span data-ttu-id="b6262-115">Use este mensaje solo con cuadros de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="b6262-115">Use this message only with multiple-selection list boxes.</span></span>

<span data-ttu-id="b6262-116">Este mensaje puede seleccionar un intervalo solo dentro de los primeros 65.536 elementos.</span><span class="sxs-lookup"><span data-stu-id="b6262-116">This message can select a range only within the first 65,536 items.</span></span>

## <a name="requirements"></a><span data-ttu-id="b6262-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b6262-117">Requirements</span></span>



| <span data-ttu-id="b6262-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6262-118">Requirement</span></span> | <span data-ttu-id="b6262-119">Value</span><span class="sxs-lookup"><span data-stu-id="b6262-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6262-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6262-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b6262-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b6262-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="b6262-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b6262-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b6262-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b6262-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="b6262-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b6262-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b6262-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b6262-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6262-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b6262-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b6262-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b6262-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b6262-128">**LB \_ SELITEMRANGEEX**</span><span class="sxs-lookup"><span data-stu-id="b6262-128">**LB\_SELITEMRANGEEX**</span></span>](lb-selitemrangeex.md)
</dt> <dt>

[<span data-ttu-id="b6262-129">**LB \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="b6262-129">**LB\_SETSEL**</span></span>](lb-setsel.md)
</dt> <dt>

<span data-ttu-id="b6262-130">**Otros recursos**</span><span class="sxs-lookup"><span data-stu-id="b6262-130">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="b6262-131">**MAKELPARAM**</span><span class="sxs-lookup"><span data-stu-id="b6262-131">**MAKELPARAM**</span></span>](/windows/desktop/api/winuser/nf-winuser-makelparam)
</dt> </dl>

 

