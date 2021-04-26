---
description: Marcas de funcionalidad del sombreador de píxeles.
ms.assetid: 41a8939f-eba5-47ca-8628-94b606b6f43d
title: D3DD3DPSHADERCAPS2_0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa2326b8f5066d34087fb543c7771a0cd547b98f
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995272"
---
# <a name="d3dd3dpshadercaps2_0"></a><span data-ttu-id="0cff7-103">D3DD3DPSHADERCAPS2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0cff7-103">D3DD3DPSHADERCAPS2\_0</span></span>

<span data-ttu-id="0cff7-104">Marcas de funcionalidad del sombreador de píxeles.</span><span class="sxs-lookup"><span data-stu-id="0cff7-104">Pixel shader capability flags.</span></span>



| <span data-ttu-id="0cff7-105">\#Definir</span><span class="sxs-lookup"><span data-stu-id="0cff7-105">\#define</span></span>                                     | <span data-ttu-id="0cff7-106">Value</span><span class="sxs-lookup"><span data-stu-id="0cff7-106">Value</span></span>          | <span data-ttu-id="0cff7-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="0cff7-107">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cff7-108">D3DD3DPSHADERCAPS2 \_ 0 \_ ARBITRARYSWAPILE</span><span class="sxs-lookup"><span data-stu-id="0cff7-108">D3DD3DPSHADERCAPS2\_0\_ARBITRARYSWIZZLE</span></span>      | <span data-ttu-id="0cff7-109">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="0cff7-109">(1 << 0)</span></span> | <span data-ttu-id="0cff7-110">Se admite el desdobado arbitrario.</span><span class="sxs-lookup"><span data-stu-id="0cff7-110">Arbitrary swizzling is supported.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="0cff7-111">D3DD3DPSHADERCAPS2 \_ 0 \_ GRADIENTINSTRUCTIONS</span><span class="sxs-lookup"><span data-stu-id="0cff7-111">D3DD3DPSHADERCAPS2\_0\_GRADIENTINSTRUCTIONS</span></span>  | <span data-ttu-id="0cff7-112">(1 << 1)</span><span class="sxs-lookup"><span data-stu-id="0cff7-112">(1 << 1)</span></span> | <span data-ttu-id="0cff7-113">Se admiten instrucciones de degradado.</span><span class="sxs-lookup"><span data-stu-id="0cff7-113">Gradient instructions are supported.</span></span>                                                                                                                                                                              |
| <span data-ttu-id="0cff7-114">D3DD3DPSHADERCAPS2 \_ 0 \_ PREDICATION</span><span class="sxs-lookup"><span data-stu-id="0cff7-114">D3DD3DPSHADERCAPS2\_0\_PREDICATION</span></span>           | <span data-ttu-id="0cff7-115">(1 << 2)</span><span class="sxs-lookup"><span data-stu-id="0cff7-115">(1 << 2)</span></span> | <span data-ttu-id="0cff7-116">Se admite el predicado de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="0cff7-116">Instruction predication is supported.</span></span> <span data-ttu-id="0cff7-117">Consulte [setp \_ comp - ps](../direct3dhlsl/setp-comp---ps.md).</span><span class="sxs-lookup"><span data-stu-id="0cff7-117">See [setp\_comp - ps](../direct3dhlsl/setp-comp---ps.md).</span></span>                                                                                                                         |
| <span data-ttu-id="0cff7-118">D3DD3DPSHADERCAPS2 \_ 0 \_ NODEPENDENTREADLIMIT</span><span class="sxs-lookup"><span data-stu-id="0cff7-118">D3DD3DPSHADERCAPS2\_0\_NODEPENDENTREADLIMIT</span></span>  | <span data-ttu-id="0cff7-119">(1 << 3)</span><span class="sxs-lookup"><span data-stu-id="0cff7-119">(1 << 3)</span></span> | <span data-ttu-id="0cff7-120">No hay ningún límite en el número de lecturas dependientes por instrucción.</span><span class="sxs-lookup"><span data-stu-id="0cff7-120">There is no limit on the number of dependent reads per instruction.</span></span>                                                                                                                                               |
| <span data-ttu-id="0cff7-121">D3DD3DPSHADERCAPS2 \_ 0 \_ NOTESTRUCTIONLIMIT</span><span class="sxs-lookup"><span data-stu-id="0cff7-121">D3DD3DPSHADERCAPS2\_0\_NOTEXINSTRUCTIONLIMIT</span></span> | <span data-ttu-id="0cff7-122">(1 << 4)</span><span class="sxs-lookup"><span data-stu-id="0cff7-122">(1 << 4)</span></span> | <span data-ttu-id="0cff7-123">No hay ningún límite en el número de instrucciones de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="0cff7-123">There is no limit on the number of tex instructions.</span></span>                                                                                                                                                              |
| <span data-ttu-id="0cff7-124">D3DPS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="0cff7-124">D3DPS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="0cff7-125">24</span><span class="sxs-lookup"><span data-stu-id="0cff7-125">24</span></span>             | <span data-ttu-id="0cff7-126">El nivel máximo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, ifc).</span><span class="sxs-lookup"><span data-stu-id="0cff7-126">The maximum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="0cff7-127">D3DPS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="0cff7-127">D3DPS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span>        | <span data-ttu-id="0cff7-128">0</span><span class="sxs-lookup"><span data-stu-id="0cff7-128">0</span></span>              | <span data-ttu-id="0cff7-129">El nivel mínimo de anidamiento de instrucciones de control de flujo dinámico (break, breakc, ifc).</span><span class="sxs-lookup"><span data-stu-id="0cff7-129">The minimum level of nesting of dynamic flow control instructions (break, breakc, ifc).</span></span>                                                                                                                           |
| <span data-ttu-id="0cff7-130">D3DPS20 \_ MAX \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="0cff7-130">D3DPS20\_MAX\_NUMTEMPS</span></span>                       | <span data-ttu-id="0cff7-131">32</span><span class="sxs-lookup"><span data-stu-id="0cff7-131">32</span></span>             | <span data-ttu-id="0cff7-132">El controlador admitirá como máximo este gran número de registros temporales.</span><span class="sxs-lookup"><span data-stu-id="0cff7-132">The driver will support at most this many temporary register.</span></span>                                                                                                                                                     |
| <span data-ttu-id="0cff7-133">D3DPS20 \_ MIN \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="0cff7-133">D3DPS20\_MIN\_NUMTEMPS</span></span>                       | <span data-ttu-id="0cff7-134">12</span><span class="sxs-lookup"><span data-stu-id="0cff7-134">12</span></span>             | <span data-ttu-id="0cff7-135">El controlador admitirá al menos este número de registros temporales.</span><span class="sxs-lookup"><span data-stu-id="0cff7-135">The driver will support at least this many temporary register.</span></span>                                                                                                                                                    |
| <span data-ttu-id="0cff7-136">D3DPS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="0cff7-136">D3DPS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="0cff7-137">4</span><span class="sxs-lookup"><span data-stu-id="0cff7-137">4</span></span>              | <span data-ttu-id="0cff7-138">La profundidad máxima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions).</span><span class="sxs-lookup"><span data-stu-id="0cff7-138">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="0cff7-139">D3DPS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="0cff7-139">D3DPS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>         | <span data-ttu-id="0cff7-140">1</span><span class="sxs-lookup"><span data-stu-id="0cff7-140">1</span></span>              | <span data-ttu-id="0cff7-141">La profundidad mínima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions).</span><span class="sxs-lookup"><span data-stu-id="0cff7-141">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span> |
| <span data-ttu-id="0cff7-142">D3DPS20 \_ MAX \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="0cff7-142">D3DPS20\_MAX\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="0cff7-143">512</span><span class="sxs-lookup"><span data-stu-id="0cff7-143">512</span></span>            | <span data-ttu-id="0cff7-144">El controlador admitirá como máximo estas muchas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="0cff7-144">The driver will support at most this many instructions.</span></span>                                                                                                                                                           |
| <span data-ttu-id="0cff7-145">D3DPS20 \_ MIN \_ NUMINSTRUCTIONSLOTS</span><span class="sxs-lookup"><span data-stu-id="0cff7-145">D3DPS20\_MIN\_NUMINSTRUCTIONSLOTS</span></span>            | <span data-ttu-id="0cff7-146">96</span><span class="sxs-lookup"><span data-stu-id="0cff7-146">96</span></span>             | <span data-ttu-id="0cff7-147">El controlador admitirá al menos estas muchas instrucciones.</span><span class="sxs-lookup"><span data-stu-id="0cff7-147">The driver will support at least this many instructions.</span></span>                                                                                                                                                          |



 

<span data-ttu-id="0cff7-148">El miembro D3DPSHADERCAPS2 \_ 0 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="0cff7-148">These constants are used by the D3DPSHADERCAPS2\_0 member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>

## <a name="constant-information"></a><span data-ttu-id="0cff7-149">Información constante</span><span class="sxs-lookup"><span data-stu-id="0cff7-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="0cff7-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0cff7-150">Header</span></span>                   | <span data-ttu-id="0cff7-151">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="0cff7-151">d3d9caps.h</span></span> |
| <span data-ttu-id="0cff7-152">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="0cff7-152">Minimum operating system</span></span> | <span data-ttu-id="0cff7-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0cff7-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0cff7-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0cff7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0cff7-155">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="0cff7-155">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="0cff7-156">**D3DPSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="0cff7-156">**D3DPSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dpshadercaps2_0)
</dt> </dl>

 

 
