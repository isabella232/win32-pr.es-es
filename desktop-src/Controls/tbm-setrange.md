---
title: Mensaje de TBM_SETRANGE (commctrl. h)
description: Establece el intervalo de posiciones lógicas mínima y máxima para el control deslizante en una barra de desplazamiento.
ms.assetid: 9c225742-8e5e-4f47-af8c-8243b6c90c1d
keywords:
- TBM_SETRANGE controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TBM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9d870df628b06031374260c679f792f0b7218a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079123"
---
# <a name="tbm_setrange-message"></a><span data-ttu-id="37453-104">\_Mensaje de SetRange TBM</span><span class="sxs-lookup"><span data-stu-id="37453-104">TBM\_SETRANGE message</span></span>

<span data-ttu-id="37453-105">Establece el intervalo de posiciones lógicas mínima y máxima para el control deslizante en una barra de desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="37453-105">Sets the range of minimum and maximum logical positions for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="37453-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="37453-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="37453-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="37453-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37453-108">Volver a dibujar el marcador.</span><span class="sxs-lookup"><span data-stu-id="37453-108">Redraw flag.</span></span> <span data-ttu-id="37453-109">Si este parámetro es **true**, el TrackBar se vuelve a dibujar una vez establecido el intervalo.</span><span class="sxs-lookup"><span data-stu-id="37453-109">If this parameter is **TRUE**, the trackbar is redrawn after the range is set.</span></span> <span data-ttu-id="37453-110">Si este parámetro es **false**, el mensaje establece el intervalo pero no vuelve a dibujar el TrackBar.</span><span class="sxs-lookup"><span data-stu-id="37453-110">If this parameter is **FALSE**, the message sets the range but does not redraw the trackbar.</span></span>

</dd> <dt>

<span data-ttu-id="37453-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="37453-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="37453-112">[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) especifica la posición mínima del control deslizante y [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) especifica la posición máxima.</span><span class="sxs-lookup"><span data-stu-id="37453-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the minimum position for the slider, and the [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the maximum position.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="37453-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="37453-113">Return value</span></span>

<span data-ttu-id="37453-114">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="37453-114">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="37453-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="37453-115">Remarks</span></span>

<span data-ttu-id="37453-116">Si la posición del control deslizante actual está fuera del nuevo intervalo, el mensaje de **\_ SetRange TBM** establece la posición del control deslizante en el nuevo valor máximo o mínimo.</span><span class="sxs-lookup"><span data-stu-id="37453-116">If the current slider position is outside the new range, the **TBM\_SETRANGE** message sets the slider position to the new maximum or minimum value.</span></span>

<span data-ttu-id="37453-117">Dado que este mensaje toma valores enteros de 2 16 bits sin signo, el intervalo máximo que puede especificar este mensaje es de 0 a 65.535.</span><span class="sxs-lookup"><span data-stu-id="37453-117">Because this message takes two 16-bit unsigned integer values, the maximum range that this message can specify is from 0 to 65,535.</span></span> <span data-ttu-id="37453-118">Para especificar valores de intervalo mayores, use los mensajes [**TBM \_ SETRANGEMIN**](tbm-setrangemin.md) y [**TBM \_ SETRANGEMAX**](tbm-setrangemax.md) .</span><span class="sxs-lookup"><span data-stu-id="37453-118">To specify larger range values, use the [**TBM\_SETRANGEMIN**](tbm-setrangemin.md) and [**TBM\_SETRANGEMAX**](tbm-setrangemax.md) messages.</span></span>

## <a name="requirements"></a><span data-ttu-id="37453-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37453-119">Requirements</span></span>



| <span data-ttu-id="37453-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="37453-120">Requirement</span></span> | <span data-ttu-id="37453-121">Value</span><span class="sxs-lookup"><span data-stu-id="37453-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="37453-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37453-122">Minimum supported client</span></span><br/> | <span data-ttu-id="37453-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="37453-123">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="37453-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="37453-124">Minimum supported server</span></span><br/> | <span data-ttu-id="37453-125">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="37453-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="37453-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="37453-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="37453-127"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="37453-127"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37453-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="37453-128">See also</span></span>

<dl> <dt>

<span data-ttu-id="37453-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="37453-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="37453-130">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="37453-130">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> <dt>

[<span data-ttu-id="37453-131">**TBM \_ SETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="37453-131">**TBM\_SETRANGEMIN**</span></span>](tbm-setrangemin.md)
</dt> </dl>

 

