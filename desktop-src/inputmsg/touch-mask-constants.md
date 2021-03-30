---
title: Máscara táctil
description: Valores que pueden aparecer en el campo touchMask de la estructura POINTER_TOUCH_INFO.
ms.assetid: 23AD50C8-C769-48D6-9F27-DB2755C03D5C
topic_type:
- apiref
api_name:
- TOUCH_MASK_NONE
- TOUCH_MASK_CONTACTAREA
- TOUCH_MASK_ORIENTATION
- TOUCH_MASK_PRESSURE
api_location:
- winuser.h
api_type:
- HeaderDef
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 5ac389894d9096b389af127685feb9a2d81756ea
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492646"
---
# <a name="touch-mask"></a><span data-ttu-id="54545-103">Máscara táctil</span><span class="sxs-lookup"><span data-stu-id="54545-103">Touch Mask</span></span>

<span data-ttu-id="54545-104">Valores que pueden aparecer en el campo **touchMask** de la estructura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="54545-104">Values that can appear in the **touchMask** field of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure.</span></span>

<dl> <dt>

<span data-ttu-id="54545-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span><span class="sxs-lookup"><span data-stu-id="54545-105"><span id="TOUCH_MASK_NONE_"></span><span id="touch_mask_none_"></span>**TOUCH_MASK_NONE**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="54545-106">0x00000000</span><span class="sxs-lookup"><span data-stu-id="54545-106">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="54545-107">Predeterminada.</span><span class="sxs-lookup"><span data-stu-id="54545-107">Default.</span></span> <span data-ttu-id="54545-108">Ninguno de los campos opcionales es válido.</span><span class="sxs-lookup"><span data-stu-id="54545-108">None of the optional fields are valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54545-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span><span class="sxs-lookup"><span data-stu-id="54545-109"><span id="TOUCH_MASK_CONTACTAREA"></span><span id="touch_mask_contactarea"></span>**TOUCH_MASK_CONTACTAREA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54545-110">0x00000001</span><span class="sxs-lookup"><span data-stu-id="54545-110">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="54545-111">el **rcContact** de la estructura de [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) es válido.</span><span class="sxs-lookup"><span data-stu-id="54545-111">**rcContact** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54545-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span><span class="sxs-lookup"><span data-stu-id="54545-112"><span id="TOUCH_MASK_ORIENTATION"></span><span id="touch_mask_orientation"></span>**TOUCH_MASK_ORIENTATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54545-113">0x00000002</span><span class="sxs-lookup"><span data-stu-id="54545-113">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="54545-114">la **orientación** de la estructura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) es válida.</span><span class="sxs-lookup"><span data-stu-id="54545-114">**orientation** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="54545-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span><span class="sxs-lookup"><span data-stu-id="54545-115"><span id="TOUCH_MASK_PRESSURE"></span><span id="touch_mask_pressure"></span>**TOUCH_MASK_PRESSURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="54545-116">0x00000004</span><span class="sxs-lookup"><span data-stu-id="54545-116">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="54545-117">la **presión** de la estructura [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) es válida.</span><span class="sxs-lookup"><span data-stu-id="54545-117">**pressure** of the [**POINTER_TOUCH_INFO**](/previous-versions/windows/desktop/api) structure is valid.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="54545-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="54545-118">Requirements</span></span>



| <span data-ttu-id="54545-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="54545-119">Requirement</span></span> | <span data-ttu-id="54545-120">Value</span><span class="sxs-lookup"><span data-stu-id="54545-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="54545-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54545-121">Minimum supported client</span></span><br/> | <span data-ttu-id="54545-122">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="54545-122">Windows 8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="54545-123">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="54545-123">Minimum supported server</span></span><br/> | <span data-ttu-id="54545-124">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="54545-124">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="54545-125">Encabezado</span><span class="sxs-lookup"><span data-stu-id="54545-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="54545-126"><dt>Winuser. h</dt></span><span class="sxs-lookup"><span data-stu-id="54545-126"><dt>Winuser.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54545-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="54545-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54545-128">Constantes</span><span class="sxs-lookup"><span data-stu-id="54545-128">Constants</span></span>](constants.md)
</dt> <dt>

[<span data-ttu-id="54545-129">**POINTER_INFO**</span><span class="sxs-lookup"><span data-stu-id="54545-129">**POINTER_INFO**</span></span>](/previous-versions/windows/desktop/api)
</dt> </dl>

 

 





