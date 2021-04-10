---
description: Marcas de capacidad del sombreador de píxeles.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a6da0dfc3fd09ce54e52b633066c6da09660c5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153454"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="86881-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="86881-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="86881-104">Marcas de capacidad del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="86881-104">Pixel shader capability flags.</span></span>



|                                              |                |                                                                                                                                                                                                                   |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="86881-105">\#define</span><span class="sxs-lookup"><span data-stu-id="86881-105">\#define</span></span>                                     | <span data-ttu-id="86881-106">Value</span><span class="sxs-lookup"><span data-stu-id="86881-106">Value</span></span>          | <span data-ttu-id="86881-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="86881-107">Description</span></span>                                                                                                                                                                                                       |
| <span data-ttu-id="86881-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWIZZLE</span><span class="sxs-lookup"><span data-stu-id="86881-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="86881-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="86881-109">(1 << 0)</span></span> | <span data-ttu-id="86881-110">Se admite permutación arbitrario.</span><span class="sxs-lookup"><span data-stu-id="86881-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="86881-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="86881-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="86881-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="86881-112">(1 << 1)</span></span> | <span data-ttu-id="86881-113">Se admiten las instrucciones de degradado.</span><span class="sxs-lookup"><span data-stu-id="86881-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="86881-114">D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION</span><span class="sxs-lookup"><span data-stu-id="86881-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="86881-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="86881-115">(1 << 2)</span></span> | <span data-ttu-id="86881-116">Se admite la instrucción predication.</span><span class="sxs-lookup"><span data-stu-id="86881-116">Instruction predication is supported.</span></span> <span data-ttu-id="86881-117">Consulte [SETP \_ COMP-PS](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="86881-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="86881-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="86881-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="86881-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="86881-119">(1 << 3)</span></span> | <span data-ttu-id="86881-120">No hay ningún límite en el número de lecturas dependientes por instrucción.</span><span class="sxs-lookup"><span data-stu-id="86881-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="86881-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTEXINSTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="86881-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="86881-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="86881-122">(1 << 4)</span></span> | <span data-ttu-id="86881-123">No hay ningún límite en el número de instrucciones Tex.</span><span class="sxs-lookup"><span data-stu-id="86881-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="86881-124">D3DPS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="86881-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="86881-125">24</span><span class="sxs-lookup"><span data-stu-id="86881-125">24</span></span>             | <span data-ttu-id="86881-126">El nivel máximo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="86881-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="86881-127">D3DPS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="86881-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="86881-128">0</span><span class="sxs-lookup"><span data-stu-id="86881-128">0</span></span>              | <span data-ttu-id="86881-129">Nivel mínimo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, IFC).</span><span class="sxs-lookup"><span data-stu-id="86881-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="86881-130">D3DPS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="86881-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="86881-131">32</span><span class="sxs-lookup"><span data-stu-id="86881-131">32</span></span>             | <span data-ttu-id="86881-132">El controlador admitirá como máximo este número de registro temporal.</span><span class="sxs-lookup"><span data-stu-id="86881-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="86881-133">D3DPS20 \_ min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="86881-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="86881-134">12</span><span class="sxs-lookup"><span data-stu-id="86881-134">12</span></span>             | <span data-ttu-id="86881-135">El controlador admitirá al menos este registro temporal.</span><span class="sxs-lookup"><span data-stu-id="86881-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="86881-136">D3DPS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="86881-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="86881-137">4</span><span class="sxs-lookup"><span data-stu-id="86881-137">4</span></span>              | <span data-ttu-id="86881-138">La profundidad máxima del anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="86881-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="86881-139">D3DPS20 \_ min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="86881-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="86881-140">1</span><span class="sxs-lookup"><span data-stu-id="86881-140">1</span></span>              | <span data-ttu-id="86881-141">La profundidad mínima de anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="86881-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="86881-142">D3DPS20 \_ Max \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="86881-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="86881-143">512</span><span class="sxs-lookup"><span data-stu-id="86881-143">512</span></span>            | <span data-ttu-id="86881-144">El controlador admitirá como máximo estas muchas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="86881-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="86881-145">D3DPS20 \_ min \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="86881-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="86881-146">96</span><span class="sxs-lookup"><span data-stu-id="86881-146">96</span></span>             | <span data-ttu-id="86881-147">El controlador admitirá al menos estas muchas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="86881-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="86881-148">El \_ miembro D3DPSHADERCAPS2 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="86881-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="86881-149">Información constante</span><span class="sxs-lookup"><span data-stu-id="86881-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="86881-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="86881-150">Header</span></span>                   | <span data-ttu-id="86881-151">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="86881-151">d3d9caps.h</span></span> |
| <span data-ttu-id="86881-152">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="86881-152">Minimum operating system</span></span> | <span data-ttu-id="86881-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="86881-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="86881-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="86881-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="86881-155">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="86881-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="86881-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="86881-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
