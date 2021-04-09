---
title: Mensaje de LB_GETCARETINDEX (Winuser. h)
description: Recupera el índice del elemento que tiene el foco en un cuadro de lista de selección múltiple. El elemento puede estar o no seleccionado.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- LB_GETCARETINDEX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079718"
---
# <a name="lb_getcaretindex-message"></a><span data-ttu-id="3de6b-105">\_Mensaje lb GETCARETINDEX</span><span class="sxs-lookup"><span data-stu-id="3de6b-105">LB\_GETCARETINDEX message</span></span>

<span data-ttu-id="3de6b-106">Recupera el índice del elemento que tiene el foco en un cuadro de lista de selección múltiple.</span><span class="sxs-lookup"><span data-stu-id="3de6b-106">Retrieves the index of the item that has the focus in a multiple-selection list box.</span></span> <span data-ttu-id="3de6b-107">El elemento puede estar o no seleccionado.</span><span class="sxs-lookup"><span data-stu-id="3de6b-107">The item may or may not be selected.</span></span>

## <a name="parameters"></a><span data-ttu-id="3de6b-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3de6b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3de6b-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3de6b-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de6b-110">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3de6b-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="3de6b-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3de6b-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3de6b-112">No se utiliza; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3de6b-112">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3de6b-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3de6b-113">Return value</span></span>

<span data-ttu-id="3de6b-114">El valor devuelto es el índice de base cero del elemento de cuadro de lista enfocado, o 0 si ningún elemento tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="3de6b-114">The return value is the zero-based index of the focused list box item, or 0 if no item has the focus.</span></span>

## <a name="remarks"></a><span data-ttu-id="3de6b-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3de6b-115">Remarks</span></span>

<span data-ttu-id="3de6b-116">Este mensaje también se puede usar para obtener el índice del elemento seleccionado actualmente en un cuadro de lista de selección única.</span><span class="sxs-lookup"><span data-stu-id="3de6b-116">This message can also be used to get the index of the item that is currently selected in a single-selection list box.</span></span>

## <a name="requirements"></a><span data-ttu-id="3de6b-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3de6b-117">Requirements</span></span>



| <span data-ttu-id="3de6b-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="3de6b-118">Requirement</span></span> | <span data-ttu-id="3de6b-119">Value</span><span class="sxs-lookup"><span data-stu-id="3de6b-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3de6b-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3de6b-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3de6b-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3de6b-121">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3de6b-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3de6b-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3de6b-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3de6b-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3de6b-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3de6b-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3de6b-125"><dt>Winuser. h (incluir Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3de6b-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3de6b-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="3de6b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3de6b-127">**LB \_ SETCARETINDEX**</span><span class="sxs-lookup"><span data-stu-id="3de6b-127">**LB\_SETCARETINDEX**</span></span>](lb-setcaretindex.md)
</dt> </dl>

 

 





