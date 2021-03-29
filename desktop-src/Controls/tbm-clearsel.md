---
title: Mensaje de TBM_CLEARSEL (commctrl. h)
description: Borra el intervalo de selección actual en una barra de nivel.
ms.assetid: ccf69fb7-d616-4a7a-8c7c-7a82827758b1
keywords:
- TBM_CLEARSEL controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_CLEARSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9d2474f3978dc80b2611bd6b454c45e515ee159
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905677"
---
# <a name="tbm_clearsel-message"></a><span data-ttu-id="fde02-104">TBM \_ CLEARSEL</span><span class="sxs-lookup"><span data-stu-id="fde02-104">TBM\_CLEARSEL message</span></span>

<span data-ttu-id="fde02-105">Borra el intervalo de selección actual en una barra de nivel.</span><span class="sxs-lookup"><span data-stu-id="fde02-105">Clears the current selection range in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="fde02-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fde02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fde02-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="fde02-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="fde02-108">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="fde02-108">Redraw flag.</span></span> <span data-ttu-id="fde02-109">Si este parámetro es **true**, el TrackBar se vuelve a dibujar una vez desactivada la selección.</span><span class="sxs-lookup"><span data-stu-id="fde02-109">If this parameter is **TRUE**, the trackbar is redrawn after the selection is cleared.</span></span>

</dd> <dt>

<span data-ttu-id="fde02-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="fde02-110">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="fde02-111">Debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="fde02-111">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fde02-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fde02-112">Return value</span></span>

<span data-ttu-id="fde02-113">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="fde02-113">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fde02-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fde02-114">Remarks</span></span>

<span data-ttu-id="fde02-115">Una barra de nivel solo puede tener un intervalo de selección si se especificó el estilo [**TBS \_ ENABLESELRANGE**](trackbar-control-styles.md) al crearlo.</span><span class="sxs-lookup"><span data-stu-id="fde02-115">A trackbar can have a selection range only if you specified the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style when you created it.</span></span>

## <a name="requirements"></a><span data-ttu-id="fde02-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fde02-116">Requirements</span></span>



| <span data-ttu-id="fde02-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="fde02-117">Requirement</span></span> | <span data-ttu-id="fde02-118">Value</span><span class="sxs-lookup"><span data-stu-id="fde02-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fde02-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde02-119">Minimum supported client</span></span><br/> | <span data-ttu-id="fde02-120">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="fde02-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="fde02-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="fde02-121">Minimum supported server</span></span><br/> | <span data-ttu-id="fde02-122">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="fde02-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fde02-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="fde02-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="fde02-124"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="fde02-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fde02-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="fde02-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="fde02-126">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="fde02-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="fde02-127">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="fde02-127">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="fde02-128">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="fde02-128">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> <dt>

[<span data-ttu-id="fde02-129">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="fde02-129">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





