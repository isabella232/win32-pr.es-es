---
description: El sombreador de vértices encapsa las constantes. El miembro VS20Caps de D3DCAPS9 usa estas constantes.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bd0905a0996e2dc9df77adb0896c9397a93450
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342950"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="66dd8-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="66dd8-104">D3DVS20CAPS</span></span>

<span data-ttu-id="66dd8-105">El sombreador de vértices encapsa las constantes.</span><span class="sxs-lookup"><span data-stu-id="66dd8-105">Vertex shader caps constants.</span></span> <span data-ttu-id="66dd8-106">El miembro VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="66dd8-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="66dd8-107">\#Definir</span><span class="sxs-lookup"><span data-stu-id="66dd8-107">\#define</span></span>                              | <span data-ttu-id="66dd8-108">Valor</span><span class="sxs-lookup"><span data-stu-id="66dd8-108">Value</span></span>          | <span data-ttu-id="66dd8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="66dd8-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66dd8-110">PREDICADO D3DVS20CAPS \_</span><span class="sxs-lookup"><span data-stu-id="66dd8-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="66dd8-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="66dd8-111">(1 << 0)</span></span> | <span data-ttu-id="66dd8-112">Se admite el predicado de instrucciones.</span><span class="sxs-lookup"><span data-stu-id="66dd8-112">Instruction predication is supported.</span></span> <span data-ttu-id="66dd8-113">Vea [setp \_ comp - vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="66dd8-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="66dd8-114">D3DVS20 \_ MAX \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="66dd8-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="66dd8-115">24</span><span class="sxs-lookup"><span data-stu-id="66dd8-115">24</span></span>             | <span data-ttu-id="66dd8-116">El nivel máximo de anidamiento de instrucciones de control de flujo dinámico[(break - vs](../direct3dhlsl/break---vs.md), [break comp - \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="66dd8-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="66dd8-117">D3DVS20 \_ MIN \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="66dd8-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="66dd8-118">0</span><span class="sxs-lookup"><span data-stu-id="66dd8-118">0</span></span>              | <span data-ttu-id="66dd8-119">El nivel mínimo de anidamiento de instrucciones de control de flujo dinámico[(break - vs](../direct3dhlsl/break---vs.md), [break comp - \_ vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), if comp - [ \_ vs](../direct3dhlsl/if-comp---vs.md), if \_ comp - vs, if [pred - vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="66dd8-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="66dd8-120">NÚMERO MÁXIMO DE \_ NUMTEMPS D3DVS20 \_</span><span class="sxs-lookup"><span data-stu-id="66dd8-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="66dd8-121">32</span><span class="sxs-lookup"><span data-stu-id="66dd8-121">32</span></span>             | <span data-ttu-id="66dd8-122">Número máximo de registros temporales admitidos.</span><span class="sxs-lookup"><span data-stu-id="66dd8-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="66dd8-123">NUMTEMPS DE D3DVS20 \_ \_ MIN</span><span class="sxs-lookup"><span data-stu-id="66dd8-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="66dd8-124">12</span><span class="sxs-lookup"><span data-stu-id="66dd8-124">12</span></span>             | <span data-ttu-id="66dd8-125">Número mínimo de registros temporales admitidos.</span><span class="sxs-lookup"><span data-stu-id="66dd8-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="66dd8-126">D3DVS20 \_ MAX \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="66dd8-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="66dd8-127">4</span><span class="sxs-lookup"><span data-stu-id="66dd8-127">4</span></span>              | <span data-ttu-id="66dd8-128">La profundidad máxima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions).</span><span class="sxs-lookup"><span data-stu-id="66dd8-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="66dd8-129">D3DVS20 \_ MIN \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="66dd8-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="66dd8-130">1</span><span class="sxs-lookup"><span data-stu-id="66dd8-130">1</span></span>              | <span data-ttu-id="66dd8-131">La profundidad mínima de anidamiento del [bucle ( vs](../direct3dhlsl/loop---vs.md)rep - / [vs](../direct3dhlsl/rep---vs.md) y call - [vs](../direct3dhlsl/call---vs.md) / [callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions).</span><span class="sxs-lookup"><span data-stu-id="66dd8-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="66dd8-132">Información constante</span><span class="sxs-lookup"><span data-stu-id="66dd8-132">Constant Information</span></span>



| <span data-ttu-id="66dd8-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="66dd8-133">Requirement</span></span>                         | <span data-ttu-id="66dd8-134">Value</span><span class="sxs-lookup"><span data-stu-id="66dd8-134">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="66dd8-135">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66dd8-135">Header</span></span>                   | <span data-ttu-id="66dd8-136">d3d9caps.h</span><span class="sxs-lookup"><span data-stu-id="66dd8-136">d3d9caps.h</span></span> |
| <span data-ttu-id="66dd8-137">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="66dd8-137">Minimum operating system</span></span> | <span data-ttu-id="66dd8-138">Windows 98</span><span class="sxs-lookup"><span data-stu-id="66dd8-138">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="66dd8-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66dd8-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66dd8-140">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="66dd8-140">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="66dd8-141">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="66dd8-141">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
