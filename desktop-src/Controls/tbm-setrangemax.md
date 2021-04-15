---
title: Mensaje de TBM_SETRANGEMAX (commctrl. h)
description: Establece la posición lógica máxima para el control deslizante en una barra de desplazamiento.
ms.assetid: 8e9d8fd3-2ee3-4fb6-aa1f-9d6e999ef330
keywords:
- TBM_SETRANGEMAX controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43997725e2fa88db3f9d4dc2fec1d51255cbb0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489028"
---
# <a name="tbm_setrangemax-message"></a><span data-ttu-id="b33e6-104">TBM \_ SETRANGEMAX</span><span class="sxs-lookup"><span data-stu-id="b33e6-104">TBM\_SETRANGEMAX message</span></span>

<span data-ttu-id="b33e6-105">Establece la posición lógica máxima para el control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="b33e6-105">Sets the maximum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="b33e6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b33e6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b33e6-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="b33e6-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b33e6-108">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="b33e6-108">Redraw flag.</span></span> <span data-ttu-id="b33e6-109">Si este parámetro es **true**, el TrackBar se vuelve a dibujar una vez establecido el intervalo.</span><span class="sxs-lookup"><span data-stu-id="b33e6-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="b33e6-110">Si este parámetro es **false**, el mensaje establece el intervalo pero no vuelve a dibujar el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="b33e6-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="b33e6-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="b33e6-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="b33e6-112">Posición máxima del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="b33e6-112">Maximum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b33e6-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b33e6-113">Return value</span></span>

<span data-ttu-id="b33e6-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="b33e6-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b33e6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b33e6-115">Remarks</span></span>

<span data-ttu-id="b33e6-116">Si la posición del control deslizante actual es mayor que el nuevo máximo, el mensaje **TBM \_ SETRANGEMAX** establece la posición del control deslizante en el nuevo valor máximo.</span><span class="sxs-lookup"><span data-stu-id="b33e6-116">If the current slider position is greater than the new maximum, the **TBM\_SETRANGEMAX** message sets the slider position to the new maximum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b33e6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b33e6-117">Requirements</span></span>



| <span data-ttu-id="b33e6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="b33e6-118">Requirement</span></span> | <span data-ttu-id="b33e6-119">Value</span><span class="sxs-lookup"><span data-stu-id="b33e6-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b33e6-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b33e6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="b33e6-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="b33e6-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b33e6-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b33e6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="b33e6-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b33e6-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b33e6-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b33e6-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="b33e6-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b33e6-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b33e6-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="b33e6-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="b33e6-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="b33e6-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b33e6-128">**TBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="b33e6-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="b33e6-129">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="b33e6-129">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

 





