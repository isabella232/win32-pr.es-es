---
title: Mensaje de TBM_SETSELSTART (commctrl. h)
description: Establece la posición lógica inicial del intervalo de selección actual en una barra de inicio. Este mensaje se omite si TrackBar no tiene el \_ estilo ENABLESELRANGE de TBS.
ms.assetid: eec1019c-6dbe-48c4-9c9d-72d657e80b83
keywords:
- TBM_SETSELSTART controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETSELSTART
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 445cb97c73f8e6483b5d4dd76bc3ccf64322e579
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078851"
---
# <a name="tbm_setselstart-message"></a><span data-ttu-id="ecb1e-105">TBM \_ SETSELSTART</span><span class="sxs-lookup"><span data-stu-id="ecb1e-105">TBM\_SETSELSTART message</span></span>

<span data-ttu-id="ecb1e-106">Establece la posición lógica inicial del intervalo de selección actual en una barra de inicio.</span><span class="sxs-lookup"><span data-stu-id="ecb1e-106">Sets the starting logical position of the current selection range in a trackbar.</span></span> <span data-ttu-id="ecb1e-107">Este mensaje se omite si TrackBar no tiene el estilo [**\_ ENABLESELRANGE de TBS**](trackbar-control-styles.md) .</span><span class="sxs-lookup"><span data-stu-id="ecb1e-107">This message is ignored if the trackbar does not have the [**TBS\_ENABLESELRANGE**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="ecb1e-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ecb1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecb1e-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ecb1e-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb1e-110">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="ecb1e-110">Redraw flag.</span></span> <span data-ttu-id="ecb1e-111">Si este parámetro es **true**, el mensaje vuelve a dibujar el TrackBar después de establecer el intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="ecb1e-111">If this parameter is **TRUE**, the message redraws the trackbar after the selection range is set.</span></span> <span data-ttu-id="ecb1e-112">Si este parámetro es **false**, el mensaje establece el intervalo de selección, pero no vuelve a dibujar el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="ecb1e-112">If this parameter is **FALSE**, the message sets the selection range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="ecb1e-113">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ecb1e-113">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ecb1e-114">Posición inicial del intervalo de selección.</span><span class="sxs-lookup"><span data-stu-id="ecb1e-114">Starting position of the selection range.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecb1e-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ecb1e-115">Return value</span></span>

<span data-ttu-id="ecb1e-116">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="ecb1e-116">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ecb1e-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ecb1e-117">Requirements</span></span>



| <span data-ttu-id="ecb1e-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="ecb1e-118">Requirement</span></span> | <span data-ttu-id="ecb1e-119">Value</span><span class="sxs-lookup"><span data-stu-id="ecb1e-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ecb1e-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecb1e-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ecb1e-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="ecb1e-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ecb1e-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ecb1e-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ecb1e-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="ecb1e-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ecb1e-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ecb1e-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecb1e-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecb1e-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ecb1e-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="ecb1e-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="ecb1e-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="ecb1e-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ecb1e-128">**TBM \_ GETSELEND**</span><span class="sxs-lookup"><span data-stu-id="ecb1e-128">**TBM\_GETSELEND**</span></span>](tbm-getselend.md)
</dt> <dt>

[<span data-ttu-id="ecb1e-129">**TBM \_ GETSELSTART**</span><span class="sxs-lookup"><span data-stu-id="ecb1e-129">**TBM\_GETSELSTART**</span></span>](tbm-getselstart.md)
</dt> <dt>

[<span data-ttu-id="ecb1e-130">**TBM \_ SETSEL**</span><span class="sxs-lookup"><span data-stu-id="ecb1e-130">**TBM\_SETSEL**</span></span>](tbm-setsel.md)
</dt> <dt>

[<span data-ttu-id="ecb1e-131">**TBM \_ SETSELEND**</span><span class="sxs-lookup"><span data-stu-id="ecb1e-131">**TBM\_SETSELEND**</span></span>](tbm-setselend.md)
</dt> </dl>

 

 





