---
title: Mensaje de TBM_SETSELEND (commctrl. h)
description: Establece la posición lógica final del intervalo de selección actual en una barra de nivel. Este mensaje se omite si TrackBar no tiene el \_ estilo ENABLESELRANGE de TBS.
ms.assetid: 1feec14c-1607-49d5-a147-af2443f82dc1
keywords:
- TBM_SETSELEND controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETSELEND
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 146446df4daf8e8ac7c0f3499149ba0f46940880
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149884"
---
# <a name="tbm_setselend-message"></a><span data-ttu-id="19953-105">TBM \_ SETSELEND</span><span class="sxs-lookup"><span data-stu-id="19953-105">TBM\_SETSELEND message</span></span>

<span data-ttu-id="19953-106">Establece la posición lógica final del intervalo de selección actual en una barra de nivel.</span><span class="sxs-lookup"><span data-stu-id="19953-106">Sets the ending logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="19953-107">Este mensaje se omite si TrackBar no tiene el estilo [**\_ ENABLESELRANGE de TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="19953-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="19953-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19953-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19953-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="19953-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19953-110">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="19953-110">Redraw flag.</span></span> <span data-ttu-id="19953-111">Si este parámetro es **true**, el mensaje vuelve a dibujar el TrackBar después de establecer el intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="19953-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="19953-112">Si este parámetro es **false**, el mensaje establece el intervalo de selección, pero no vuelve a dibujar el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="19953-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="19953-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="19953-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="19953-114">Posición lógica de finalización del intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="19953-114">Ending logical position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19953-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19953-115">Return value</span></span>

<span data-ttu-id="19953-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="19953-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="19953-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="19953-117">Requirements</span></span>



| <span data-ttu-id="19953-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="19953-118">Requirement</span></span> | <span data-ttu-id="19953-119">Value</span><span class="sxs-lookup"><span data-stu-id="19953-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="19953-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19953-120">Minimum supported client</span></span><br/> | <span data-ttu-id="19953-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="19953-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="19953-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="19953-122">Minimum supported server</span></span><br/> | <span data-ttu-id="19953-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="19953-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="19953-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="19953-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="19953-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="19953-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19953-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="19953-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="19953-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="19953-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="19953-128">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="19953-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="19953-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="19953-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="19953-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="19953-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="19953-131">**TBM \_ SETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="19953-131">**TBM\_SETSELSTART**</span></span>](tbm-setselstart.md)
</dt> </dl>

 

 





