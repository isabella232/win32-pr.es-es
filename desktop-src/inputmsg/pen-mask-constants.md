---
title: Máscara de lápiz
description: Valores que pueden aparecer en el campo penMask de la estructura POINTER_PEN_INFO.
ms.assetid: 6A44B701-55E1-41D4-9C4A-807E57441DA4
topic_type:
- apiref
api_name:
- PEN_MASK_NONE
- PEN_MASK_PRESSURE
- PEN_MASK_ROTATION
- PEN_MASK_TILT_X
- PEN_MASK_TILT_Y
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: bd181b5eafbe1cf6de56c95886deb04e5bd6d2b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150580"
---
# <a name="pen-mask"></a><span data-ttu-id="97596-103">Máscara de lápiz</span><span class="sxs-lookup"><span data-stu-id="97596-103">Pen Mask</span></span>

<span data-ttu-id="97596-104">Valores que pueden aparecer en el campo **penMask** de la estructura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="97596-104">Values that can appear in the **penMask** field of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="97596-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="97596-105"><span id="PEN_MASK_NONE"></span><span id="pen_mask_none"></span>**PEN_MASK_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97596-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="97596-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="97596-107">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="97596-107">Default.</span></span> <span data-ttu-id="97596-108">Ninguno de los campos opcionales es válido.</span><span class="sxs-lookup"><span data-stu-id="97596-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97596-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="97596-109"><span id="PEN_MASK_PRESSURE"></span><span id="pen_mask_pressure"></span>**PEN_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97596-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="97596-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="97596-111">la **presión** de la estructura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) es válida.</span><span class="sxs-lookup"><span data-stu-id="97596-111">**pressure** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97596-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span><span class="sxs-lookup"><span data-stu-id="97596-112"><span id="PEN_MASK_ROTATION"></span><span id="pen_mask_rotation"></span>**PEN_MASK_ROTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97596-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="97596-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="97596-114">el **giro** de la estructura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) es válido.</span><span class="sxs-lookup"><span data-stu-id="97596-114">**rotation** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97596-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span><span class="sxs-lookup"><span data-stu-id="97596-115"><span id="PEN_MASK_TILT_X____"></span><span id="pen_mask_tilt_x____"></span>**PEN_MASK_TILT_X**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="97596-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="97596-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="97596-117">el **tiltX** de la estructura de [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) es válido.</span><span class="sxs-lookup"><span data-stu-id="97596-117">**tiltX** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="97596-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span><span class="sxs-lookup"><span data-stu-id="97596-118"><span id="PEN_MASK_TILT_Y"></span><span id="pen_mask_tilt_y"></span>**PEN_MASK_TILT_Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="97596-119">0x00000008</span><span class="sxs-lookup"><span data-stu-id="97596-119">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="97596-120">la **inclinación** de la estructura [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) es válida.</span><span class="sxs-lookup"><span data-stu-id="97596-120">**tiltY** of the [**POINTER_PEN_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="97596-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="97596-121">Requirements</span></span>



| <span data-ttu-id="97596-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="97596-122">Requirement</span></span> | <span data-ttu-id="97596-123">Value</span><span class="sxs-lookup"><span data-stu-id="97596-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="97596-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97596-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97596-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="97596-125">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="97596-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="97596-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97596-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="97596-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="97596-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="97596-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="97596-129"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="97596-129"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97596-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="97596-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97596-131">Constantes</span><span class="sxs-lookup"><span data-stu-id="97596-131">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="97596-132">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="97596-132">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





