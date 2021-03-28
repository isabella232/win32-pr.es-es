---
title: ishl (sm5 - asm)
description: Desplazar a la izquierda. | ishl (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362224"
---
# <a name="ishl-sm5---asm"></a><span data-ttu-id="98ef0-104">ishl (sm5 - asm)</span><span class="sxs-lookup"><span data-stu-id="98ef0-104">ishl (sm5 - asm)</span></span>

<span data-ttu-id="98ef0-105">Desplazar a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="98ef0-105">Shift left.</span></span>



| <span data-ttu-id="98ef0-106">ishl dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="98ef0-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="98ef0-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="98ef0-107">Item</span></span>                                                            | <span data-ttu-id="98ef0-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="98ef0-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="98ef0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="98ef0-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="98ef0-110">\[en \] contiene los resultados del desplazamiento.</span><span class="sxs-lookup"><span data-stu-id="98ef0-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="98ef0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="98ef0-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="98ef0-112">\[en \] los valores de 32 bits que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="98ef0-112">\[in\] The 32-bit values to shift.</span></span><br/>       |
| <span data-ttu-id="98ef0-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="98ef0-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="98ef0-114">\[en \] el número de bits que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="98ef0-114">\[in\] The number of bits to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="98ef0-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98ef0-115">Remarks</span></span>

<span data-ttu-id="98ef0-116">Esta instrucción realiza un desplazamiento por componentes de cada valor de 32 bits de *src0* a la izquierda por un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) en *SRC1*, insertando 0.</span><span class="sxs-lookup"><span data-stu-id="98ef0-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="98ef0-117">Los resultados de 32 bits por componente se colocan en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="98ef0-117">The 32-bit per component results are placed in *dest*.</span></span>

<span data-ttu-id="98ef0-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="98ef0-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="98ef0-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="98ef0-119">Vertex</span></span> | <span data-ttu-id="98ef0-120">Casco</span><span class="sxs-lookup"><span data-stu-id="98ef0-120">Hull</span></span> | <span data-ttu-id="98ef0-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="98ef0-121">Domain</span></span> | <span data-ttu-id="98ef0-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="98ef0-122">Geometry</span></span> | <span data-ttu-id="98ef0-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="98ef0-123">Pixel</span></span> | <span data-ttu-id="98ef0-124">Compute</span><span class="sxs-lookup"><span data-stu-id="98ef0-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="98ef0-125">X</span><span class="sxs-lookup"><span data-stu-id="98ef0-125">X</span></span>      | <span data-ttu-id="98ef0-126">X</span><span class="sxs-lookup"><span data-stu-id="98ef0-126">X</span></span>    | <span data-ttu-id="98ef0-127">X</span><span class="sxs-lookup"><span data-stu-id="98ef0-127">X</span></span>      | <span data-ttu-id="98ef0-128">X</span><span class="sxs-lookup"><span data-stu-id="98ef0-128">X</span></span>        | <span data-ttu-id="98ef0-129">X</span><span class="sxs-lookup"><span data-stu-id="98ef0-129">X</span></span>     | <span data-ttu-id="98ef0-130">X</span><span class="sxs-lookup"><span data-stu-id="98ef0-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="98ef0-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="98ef0-131">Minimum Shader Model</span></span>

<span data-ttu-id="98ef0-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="98ef0-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="98ef0-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="98ef0-133">Shader Model</span></span>                                              | <span data-ttu-id="98ef0-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="98ef0-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="98ef0-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="98ef0-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="98ef0-136">sí</span><span class="sxs-lookup"><span data-stu-id="98ef0-136">yes</span></span>       |
| [<span data-ttu-id="98ef0-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="98ef0-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="98ef0-138">no</span><span class="sxs-lookup"><span data-stu-id="98ef0-138">no</span></span>        |
| [<span data-ttu-id="98ef0-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="98ef0-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="98ef0-140">no</span><span class="sxs-lookup"><span data-stu-id="98ef0-140">no</span></span>        |
| [<span data-ttu-id="98ef0-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ef0-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="98ef0-142">no</span><span class="sxs-lookup"><span data-stu-id="98ef0-142">no</span></span>        |
| [<span data-ttu-id="98ef0-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ef0-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="98ef0-144">no</span><span class="sxs-lookup"><span data-stu-id="98ef0-144">no</span></span>        |
| [<span data-ttu-id="98ef0-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ef0-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="98ef0-146">no</span><span class="sxs-lookup"><span data-stu-id="98ef0-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="98ef0-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="98ef0-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="98ef0-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="98ef0-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





