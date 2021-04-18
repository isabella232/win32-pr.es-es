---
description: Constantes de mayúsculas del sombreador de vértices. El miembro VS20Caps de D3DCAPS9 usa estas constantes.
ms.assetid: c1321957-4ba5-45d0-984a-4f4267221c59
title: D3DVS20CAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8caccdebe3dc67b6299c038935e26c0dbac2be6d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105714845"
---
# <a name="d3dvs20caps"></a><span data-ttu-id="df0aa-104">D3DVS20CAPS</span><span class="sxs-lookup"><span data-stu-id="df0aa-104">D3DVS20CAPS</span></span>

<span data-ttu-id="df0aa-105">Constantes de mayúsculas del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="df0aa-105">Vertex shader caps constants.</span></span> <span data-ttu-id="df0aa-106">El miembro VS20Caps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)usa estas constantes.</span><span class="sxs-lookup"><span data-stu-id="df0aa-106">These constants are used by the VS20Caps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).</span></span>



| <span data-ttu-id="df0aa-107">\#define</span><span class="sxs-lookup"><span data-stu-id="df0aa-107">\#define</span></span>                              | <span data-ttu-id="df0aa-108">Value</span><span class="sxs-lookup"><span data-stu-id="df0aa-108">Value</span></span>          | <span data-ttu-id="df0aa-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="df0aa-109">Description</span></span>                                                                                                                                                                                                                                                                                                 |
|---------------------------------------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df0aa-110">D3DVS20CAPS \_ PREDICATION</span><span class="sxs-lookup"><span data-stu-id="df0aa-110">D3DVS20CAPS\_PREDICATION</span></span>              | <span data-ttu-id="df0aa-111">(1 << 0)</span><span class="sxs-lookup"><span data-stu-id="df0aa-111">(1 << 0)</span></span> | <span data-ttu-id="df0aa-112">Se admite la instrucción predication.</span><span class="sxs-lookup"><span data-stu-id="df0aa-112">Instruction predication is supported.</span></span> <span data-ttu-id="df0aa-113">Consulte [SETP \_ COMP-vs](../direct3dhlsl/setp-comp---vs.md).</span><span class="sxs-lookup"><span data-stu-id="df0aa-113">See [setp\_comp - vs](../direct3dhlsl/setp-comp---vs.md).</span></span>                                                                                                                                                                                                                   |
| <span data-ttu-id="df0aa-114">D3DVS20 \_ Max \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="df0aa-114">D3DVS20\_MAX\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="df0aa-115">24</span><span class="sxs-lookup"><span data-stu-id="df0aa-115">24</span></span>             | <span data-ttu-id="df0aa-116">El nivel máximo de anidamiento de instrucciones de control de flujo dinámico ([break-vs](../direct3dhlsl/break---vs.md), [break \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [If \_ COMP-vs](../direct3dhlsl/if-comp---vs.md), if \_ COMP-vs, [si es Pred-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="df0aa-116">The maximum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="df0aa-117">D3DVS20 \_ min \_ DYNAMICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="df0aa-117">D3DVS20\_MIN\_DYNAMICFLOWCONTROLDEPTH</span></span> | <span data-ttu-id="df0aa-118">0</span><span class="sxs-lookup"><span data-stu-id="df0aa-118">0</span></span>              | <span data-ttu-id="df0aa-119">El nivel mínimo de anidamiento de instrucciones de control de flujo dinámico ([break-vs](../direct3dhlsl/break---vs.md), [break \_ COMP-vs](../direct3dhlsl/break-comp---vs.md), [breakp-vs](../direct3dhlsl/breakp---vs.md), [If \_ COMP-vs](../direct3dhlsl/if-comp---vs.md), if \_ COMP-vs, [si es Pred-vs](../direct3dhlsl/if-pred---vs.md)).</span><span class="sxs-lookup"><span data-stu-id="df0aa-119">The minimum level of nesting of dynamic flow control instructions ([break - vs](../direct3dhlsl/break---vs.md), [break\_comp - vs](../direct3dhlsl/break-comp---vs.md), [breakp - vs](../direct3dhlsl/breakp---vs.md), [if\_comp - vs](../direct3dhlsl/if-comp---vs.md), if\_comp - vs, [if pred - vs](../direct3dhlsl/if-pred---vs.md)).</span></span> |
| <span data-ttu-id="df0aa-120">D3DVS20 \_ Max \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="df0aa-120">D3DVS20\_MAX\_NUMTEMPS</span></span>                | <span data-ttu-id="df0aa-121">32</span><span class="sxs-lookup"><span data-stu-id="df0aa-121">32</span></span>             | <span data-ttu-id="df0aa-122">Número máximo de registros temporales admitidos.</span><span class="sxs-lookup"><span data-stu-id="df0aa-122">The maximum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="df0aa-123">D3DVS20 \_ min \_ NUMTEMPS</span><span class="sxs-lookup"><span data-stu-id="df0aa-123">D3DVS20\_MIN\_NUMTEMPS</span></span>                | <span data-ttu-id="df0aa-124">12</span><span class="sxs-lookup"><span data-stu-id="df0aa-124">12</span></span>             | <span data-ttu-id="df0aa-125">El número mínimo de registros temporales admitidos.</span><span class="sxs-lookup"><span data-stu-id="df0aa-125">The minimum number of temporary registers supported.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="df0aa-126">D3DVS20 \_ Max \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="df0aa-126">D3DVS20\_MAX\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="df0aa-127">4</span><span class="sxs-lookup"><span data-stu-id="df0aa-127">4</span></span>              | <span data-ttu-id="df0aa-128">La profundidad máxima del anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="df0aa-128">The maximum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |
| <span data-ttu-id="df0aa-129">D3DVS20 \_ min \_ STATICFLOWCONTROLDEPTH</span><span class="sxs-lookup"><span data-stu-id="df0aa-129">D3DVS20\_MIN\_STATICFLOWCONTROLDEPTH</span></span>  | <span data-ttu-id="df0aa-130">1</span><span class="sxs-lookup"><span data-stu-id="df0aa-130">1</span></span>              | <span data-ttu-id="df0aa-131">La profundidad mínima de anidamiento de las instrucciones [Loop-vs](../direct3dhlsl/loop---vs.md) / [REP-vs](../direct3dhlsl/rep---vs.md) y [Call-vs](../direct3dhlsl/call---vs.md) / [callnz bool-vs](../direct3dhlsl/callnz-bool---vs.md) .</span><span class="sxs-lookup"><span data-stu-id="df0aa-131">The minimum depth of nesting of the [loop - vs](../direct3dhlsl/loop---vs.md)/[rep - vs](../direct3dhlsl/rep---vs.md) and [call - vs](../direct3dhlsl/call---vs.md)/[callnz bool - vs](../direct3dhlsl/callnz-bool---vs.md) instructions.</span></span>                                                                                           |



 

## <a name="constant-information"></a><span data-ttu-id="df0aa-132">Información constante</span><span class="sxs-lookup"><span data-stu-id="df0aa-132">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="df0aa-133">Encabezado</span><span class="sxs-lookup"><span data-stu-id="df0aa-133">Header</span></span>                   | <span data-ttu-id="df0aa-134">d3d9caps. h</span><span class="sxs-lookup"><span data-stu-id="df0aa-134">d3d9caps.h</span></span> |
| <span data-ttu-id="df0aa-135">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="df0aa-135">Minimum operating system</span></span> | <span data-ttu-id="df0aa-136">Windows 98</span><span class="sxs-lookup"><span data-stu-id="df0aa-136">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="df0aa-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="df0aa-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="df0aa-138">Constantes de Direct3D</span><span class="sxs-lookup"><span data-stu-id="df0aa-138">Direct3D Constants</span></span>](dx9-graphics-reference-d3d-constants.md)
</dt> <dt>

[<span data-ttu-id="df0aa-139">**D3DVSHADERCAPS2 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="df0aa-139">**D3DVSHADERCAPS2\_0**</span></span>](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dvshadercaps2_0)
</dt> </dl>

 

 
