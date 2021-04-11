---
description: Especifica el intervalo usado en las búsquedas de movimiento.
ms.assetid: b2026f47-ac39-4276-8359-c939b202f00c
title: Propiedad MFPKEY_MOTIONSEARCHRANGE (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c557ea1a462192434222e425dccb8b9a0e291986
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276315"
---
# <a name="mfpkey_motionsearchrange-property"></a><span data-ttu-id="0b2c9-103">\_Propiedad MOTIONSEARCHRANGE de MFPKEY</span><span class="sxs-lookup"><span data-stu-id="0b2c9-103">MFPKEY\_MOTIONSEARCHRANGE Property</span></span>

<span data-ttu-id="0b2c9-104">Especifica el intervalo usado en las búsquedas de movimiento.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-104">Specifies the range used in motion searches.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="0b2c9-105">Constante para IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="0b2c9-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="0b2c9-106">g \_ wszWMVCMotionSearchRange</span><span class="sxs-lookup"><span data-stu-id="0b2c9-106">g\_wszWMVCMotionSearchRange</span></span>

## <a name="data-type"></a><span data-ttu-id="0b2c9-107">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="0b2c9-107">Data Type</span></span>

<span data-ttu-id="0b2c9-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="0b2c9-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="0b2c9-109">Valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="0b2c9-109">Default Value</span></span>

<span data-ttu-id="0b2c9-110">0</span><span class="sxs-lookup"><span data-stu-id="0b2c9-110">0</span></span>

## <a name="remarks"></a><span data-ttu-id="0b2c9-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0b2c9-111">Remarks</span></span>

<span data-ttu-id="0b2c9-112">Esta propiedad se puede establecer en uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-112">This property may be set to one of the following values.</span></span> <span data-ttu-id="0b2c9-113">H denota el intervalo horizontal y V denota el intervalo vertical.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-113">H denotes horizontal range and V denotes vertical range.</span></span> <span data-ttu-id="0b2c9-114">Todos los intervalos se proporcionan en píxeles.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-114">All ranges are given in pixels.</span></span>



| <span data-ttu-id="0b2c9-115">Value</span><span class="sxs-lookup"><span data-stu-id="0b2c9-115">Value</span></span> | <span data-ttu-id="0b2c9-116">Intervalo</span><span class="sxs-lookup"><span data-stu-id="0b2c9-116">Range</span></span>                                |
|-------|--------------------------------------|
| <span data-ttu-id="0b2c9-117">0</span><span class="sxs-lookup"><span data-stu-id="0b2c9-117">0</span></span>     | <span data-ttu-id="0b2c9-118">+ 63.75/-64 H, + 31.75/-32.0 V</span><span class="sxs-lookup"><span data-stu-id="0b2c9-118">+63.75/-64.0 H, +31.75/-32.0 V</span></span>       |
| <span data-ttu-id="0b2c9-119">1</span><span class="sxs-lookup"><span data-stu-id="0b2c9-119">1</span></span>     | <span data-ttu-id="0b2c9-120">+127,75/-128,0 H, +63,75/-64,0 V</span><span class="sxs-lookup"><span data-stu-id="0b2c9-120">+127.75/-128.0 H, +63.75/-64.0 V</span></span>     |
| <span data-ttu-id="0b2c9-121">2</span><span class="sxs-lookup"><span data-stu-id="0b2c9-121">2</span></span>     | <span data-ttu-id="0b2c9-122">+ 511.75/-512.0 H, + 127.75/-128.0 V</span><span class="sxs-lookup"><span data-stu-id="0b2c9-122">+511.75/-512.0 H, +127.75/-128.0 V</span></span>   |
| <span data-ttu-id="0b2c9-123">3</span><span class="sxs-lookup"><span data-stu-id="0b2c9-123">3</span></span>     | <span data-ttu-id="0b2c9-124">+ 1023.75/-1024.0 H, + 255.75/-256.0 V</span><span class="sxs-lookup"><span data-stu-id="0b2c9-124">+1023.75/-1024.0 H, +255.75/-256.0 V</span></span> |
| <span data-ttu-id="0b2c9-125">-1</span><span class="sxs-lookup"><span data-stu-id="0b2c9-125">-1</span></span>    | <span data-ttu-id="0b2c9-126">Adaptativo macrobloque: adaptable (automática)</span><span class="sxs-lookup"><span data-stu-id="0b2c9-126">Macroblock-adaptive (automatic)</span></span>      |



 

<span data-ttu-id="0b2c9-127">Esta propiedad controla el tamaño del área de marco en la que el códec buscará un elemento que pueda haber mostrado un movimiento entre fotogramas.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-127">This property controls the size of the frame area that the codec will search for an element that may have exhibited motion between frames.</span></span> <span data-ttu-id="0b2c9-128">Una ventana de búsqueda más grande le ayudará a encontrar un movimiento más rápido, pero requerirá más tiempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-128">A larger search window will help find faster motion but will require more CPU time.</span></span> <span data-ttu-id="0b2c9-129">Los requisitos de CPU se duplican aproximadamente en cada nivel.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-129">The CPU requirements are approximately doubled at each level.</span></span>

<span data-ttu-id="0b2c9-130">El modo automático (-1) seleccionará dinámicamente el modo más eficaz.</span><span class="sxs-lookup"><span data-stu-id="0b2c9-130">The automatic mode (-1) will dynamically select the most efficient mode.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b2c9-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b2c9-131">Requirements</span></span>



| <span data-ttu-id="0b2c9-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b2c9-132">Requirement</span></span> | <span data-ttu-id="0b2c9-133">Value</span><span class="sxs-lookup"><span data-stu-id="0b2c9-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0b2c9-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b2c9-134">Minimum supported client</span></span><br/> | <span data-ttu-id="0b2c9-135">Solo aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="0b2c9-135">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="0b2c9-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b2c9-136">Minimum supported server</span></span><br/> | <span data-ttu-id="0b2c9-137">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b2c9-137">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0b2c9-138">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0b2c9-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="0b2c9-139"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0b2c9-139"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b2c9-140">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b2c9-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b2c9-141">Propiedades de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0b2c9-141">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




