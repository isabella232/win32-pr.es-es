---
title: deriv_rty_fine (SM5-ASM)
description: Calcula la tasa de cambio de los componentes. | deriv_rty_fine (SM5-ASM)
ms.assetid: 7C5769A6-443C-4208-BD09-3DF3C5902624
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f0274fd04ae88ee412c95947691628754ba197
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998112"
---
# <a name="deriv_rty_fine-sm5---asm"></a><span data-ttu-id="35226-104">derive \_ propiedad \_ Fine (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="35226-104">deriv\_rty\_fine (sm5 - asm)</span></span>

<span data-ttu-id="35226-105">Calcula la tasa de cambio de los componentes.</span><span class="sxs-lookup"><span data-stu-id="35226-105">Computes the rate of change of components.</span></span>



| <span data-ttu-id="35226-106">derive \_ propiedad \_ Fine \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="35226-106">deriv\_rty\_fine\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\],</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="35226-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="35226-107">Item</span></span>                                                            | <span data-ttu-id="35226-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="35226-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="35226-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="35226-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="35226-110">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="35226-110">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="35226-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="35226-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="35226-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="35226-112">\[in\] The components in the operation.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="35226-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35226-113">Remarks</span></span>

<span data-ttu-id="35226-114">Para obtener más información, vea [derivar \_ RTX \_ Fine.](deriv-rtx-fine--sm5---asm-.md)</span><span class="sxs-lookup"><span data-stu-id="35226-114">For more information, see [deriv\_rtx\_fine.](deriv-rtx-fine--sm5---asm-.md)</span></span>

<span data-ttu-id="35226-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="35226-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="35226-116">Vértice</span><span class="sxs-lookup"><span data-stu-id="35226-116">Vertex</span></span> | <span data-ttu-id="35226-117">Casco</span><span class="sxs-lookup"><span data-stu-id="35226-117">Hull</span></span> | <span data-ttu-id="35226-118">Dominio</span><span class="sxs-lookup"><span data-stu-id="35226-118">Domain</span></span> | <span data-ttu-id="35226-119">Geometría</span><span class="sxs-lookup"><span data-stu-id="35226-119">Geometry</span></span> | <span data-ttu-id="35226-120">Píxel</span><span class="sxs-lookup"><span data-stu-id="35226-120">Pixel</span></span> | <span data-ttu-id="35226-121">Compute</span><span class="sxs-lookup"><span data-stu-id="35226-121">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="35226-122">X</span><span class="sxs-lookup"><span data-stu-id="35226-122">X</span></span>     |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="35226-123">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="35226-123">Minimum Shader Model</span></span>

<span data-ttu-id="35226-124">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="35226-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="35226-125">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="35226-125">Shader Model</span></span>                                              | <span data-ttu-id="35226-126">Compatible</span><span class="sxs-lookup"><span data-stu-id="35226-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="35226-127">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="35226-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="35226-128">sí</span><span class="sxs-lookup"><span data-stu-id="35226-128">yes</span></span>       |
| [<span data-ttu-id="35226-129">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="35226-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="35226-130">no</span><span class="sxs-lookup"><span data-stu-id="35226-130">no</span></span>        |
| [<span data-ttu-id="35226-131">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="35226-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="35226-132">no</span><span class="sxs-lookup"><span data-stu-id="35226-132">no</span></span>        |
| [<span data-ttu-id="35226-133">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35226-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="35226-134">no</span><span class="sxs-lookup"><span data-stu-id="35226-134">no</span></span>        |
| [<span data-ttu-id="35226-135">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35226-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="35226-136">no</span><span class="sxs-lookup"><span data-stu-id="35226-136">no</span></span>        |
| [<span data-ttu-id="35226-137">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35226-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="35226-138">no</span><span class="sxs-lookup"><span data-stu-id="35226-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="35226-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="35226-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="35226-140">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="35226-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





