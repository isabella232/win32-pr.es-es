---
title: Mensaje de TBM_GETSELEND (commctrl. h)
description: Recupera la posición final del intervalo de selección actual en una barra de nivel.
ms.assetid: e365dd4d-eb49-4107-b6d4-cdb558d27fdb
keywords:
- TBM_GETSELEND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_GETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 486d66d3e7fc2dd4d23b89cb5e9406fa81b34638
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490696"
---
# <a name="tbm_getselend-message"></a><span data-ttu-id="3a911-104">TBM \_ GETSELEND</span><span class="sxs-lookup"><span data-stu-id="3a911-104">TBM\_GETSELEND message</span></span>

<span data-ttu-id="3a911-105">Recupera la posición final del intervalo de selección actual en una barra de nivel.</span><span class="sxs-lookup"><span data-stu-id="3a911-105">Retrieves the ending position of the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="3a911-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="3a911-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a911-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="3a911-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="3a911-108">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3a911-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="3a911-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3a911-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="3a911-110">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="3a911-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a911-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3a911-111">Return value</span></span>

<span data-ttu-id="3a911-112">Devuelve un valor de 32 bits que especifica la posición final del intervalo de selección actual.</span><span class="sxs-lookup"><span data-stu-id="3a911-112">Returns a 32-bit value that specifies the ending position of the current selection range.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a911-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3a911-113">Remarks</span></span>

<span data-ttu-id="3a911-114">Una barra de nivel solo puede tener un intervalo de selección si se especificó el estilo [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) al crearlo.</span><span class="sxs-lookup"><span data-stu-id="3a911-114">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a911-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a911-115">Requirements</span></span>



| <span data-ttu-id="3a911-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a911-116">Requirement</span></span> | <span data-ttu-id="3a911-117">Value</span><span class="sxs-lookup"><span data-stu-id="3a911-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3a911-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a911-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3a911-119">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="3a911-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3a911-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3a911-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3a911-121">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="3a911-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3a911-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3a911-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a911-123"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a911-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a911-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3a911-124">See also</span></span>

<dl> <dt>

<span data-ttu-id="3a911-125">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="3a911-125">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3a911-126">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="3a911-126">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="3a911-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="3a911-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="3a911-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="3a911-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="3a911-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="3a911-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





