---
title: Mensaje de TBM_SETRANGEMIN (commctrl. h)
description: Establece la posición lógica mínima para el control deslizante en una barra de desplazamiento.
ms.assetid: 85071be2-4df3-4b54-9122-b6dc767f6cb9
keywords:
- TBM_SETRANGEMIN controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d34c2e70aa6247cb970e576c915bdcd28cd18d23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103995925"
---
# <a name="tbm_setrangemin-message"></a><span data-ttu-id="f00e1-104">TBM \_ SETRANGEMIN</span><span class="sxs-lookup"><span data-stu-id="f00e1-104">TBM\_SETRANGEMIN message</span></span>

<span data-ttu-id="f00e1-105">Establece la posición lógica mínima para el control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="f00e1-105">Sets the minimum logical position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="f00e1-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f00e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f00e1-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f00e1-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f00e1-108">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="f00e1-108">Redraw flag.</span></span> <span data-ttu-id="f00e1-109">Si este parámetro es **true**, el mensaje vuelve a dibujar el TrackBar una vez establecido el intervalo.</span><span class="sxs-lookup"><span data-stu-id="f00e1-109">If this parameter is **TRUE**, the message redraws the trackbar after the range is set.</span></span> <span data-ttu-id="f00e1-110">Si este parámetro es **false**, el mensaje establece el intervalo pero no vuelve a dibujar el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="f00e1-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="f00e1-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f00e1-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f00e1-112">Posición mínima del control deslizante.</span><span class="sxs-lookup"><span data-stu-id="f00e1-112">Minimum position for the slider.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f00e1-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f00e1-113">Return value</span></span>

<span data-ttu-id="f00e1-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="f00e1-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f00e1-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f00e1-115">Remarks</span></span>

<span data-ttu-id="f00e1-116">Si la posición del control deslizante actual es menor que el mínimo, el mensaje **TBM \_ SETRANGEMIN** establece la posición del control deslizante en el nuevo valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="f00e1-116">If the current slider position is less than the new minimum, the **TBM\_SETRANGEMIN** message sets the slider position to the new minimum value.</span></span>

## <a name="requirements"></a><span data-ttu-id="f00e1-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f00e1-117">Requirements</span></span>



| <span data-ttu-id="f00e1-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f00e1-118">Requirement</span></span> | <span data-ttu-id="f00e1-119">Value</span><span class="sxs-lookup"><span data-stu-id="f00e1-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f00e1-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f00e1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f00e1-121">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="f00e1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f00e1-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f00e1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f00e1-123">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="f00e1-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f00e1-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="f00e1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f00e1-125"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="f00e1-125"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f00e1-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="f00e1-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="f00e1-127">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="f00e1-127">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f00e1-128">**TBM \_ SetRange**</span><span class="sxs-lookup"><span data-stu-id="f00e1-128">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="f00e1-129">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="f00e1-129">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





