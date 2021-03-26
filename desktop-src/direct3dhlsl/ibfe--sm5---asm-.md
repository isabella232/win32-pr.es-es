---
title: ibfe (SM5-ASM)
description: Dado un intervalo de bits en un número, desplace esos bits a LSB y firme para extender el MSB del intervalo.
ms.assetid: 1ED39812-A89F-4325-82A0-DA2CCC55A99A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 805d5c1137e25d8b8fa560588b9e876ccc5c8748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784906"
---
# <a name="ibfe-sm5---asm"></a><span data-ttu-id="551fe-103">ibfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="551fe-103">ibfe (sm5 - asm)</span></span>

<span data-ttu-id="551fe-104">Dado un intervalo de bits en un número, desplace esos bits a LSB y firme para extender el MSB del intervalo.</span><span class="sxs-lookup"><span data-stu-id="551fe-104">Given a range of bits in a number, shift those bits to the LSB and sign extend the MSB of the range.</span></span>



| <span data-ttu-id="551fe-105">ibfe dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="551fe-105">ibfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="551fe-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="551fe-106">Item</span></span>                                                            | <span data-ttu-id="551fe-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="551fe-107">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="551fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="551fe-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="551fe-109">\[en \] la dirección de los resultados de la operación.</span><span class="sxs-lookup"><span data-stu-id="551fe-109">\[in\] The address of the results of the operation.</span></span><br/> |
| <span data-ttu-id="551fe-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="551fe-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="551fe-111">\[en \] el ancho del campo de bits.</span><span class="sxs-lookup"><span data-stu-id="551fe-111">\[in\] The bitfield width.</span></span><br/>                          |
| <span data-ttu-id="551fe-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="551fe-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="551fe-113">\[en \] el desplazamiento de campo de bits.</span><span class="sxs-lookup"><span data-stu-id="551fe-113">\[in\] The bitfield offset.</span></span><br/>                         |
| <span data-ttu-id="551fe-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="551fe-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="551fe-115">\[en \] el valor que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="551fe-115">\[in\] The value to shift.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="551fe-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="551fe-116">Remarks</span></span>

<span data-ttu-id="551fe-117">Los LSB 5 bits de src0 proporcionan el ancho del campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="551fe-117">The LSB 5 bits of src0 provide the bitfield width (0-31).</span></span>

<span data-ttu-id="551fe-118">Los LSB 5 bits de SRC1 proporcionan el desplazamiento de bits de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="551fe-118">The LSB 5 bits of src1 provide the bitfield offset (0-31).</span></span>

<span data-ttu-id="551fe-119">En el ejemplo siguiente se muestra cómo utilizar esta instrucción.</span><span class="sxs-lookup"><span data-stu-id="551fe-119">The following example shows how to use this instruction.</span></span>

``` syntax
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ishr dest, dest, 32-width
                }
                else
                {
                    ishr dest, src2, offset
                }
```

<span data-ttu-id="551fe-120">Use esta instrucción para desempaquetar los enteros o marcas con signo.</span><span class="sxs-lookup"><span data-stu-id="551fe-120">Use this instruction to unpack signed integers or flags.</span></span>

<span data-ttu-id="551fe-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="551fe-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="551fe-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="551fe-122">Vertex</span></span> | <span data-ttu-id="551fe-123">Casco</span><span class="sxs-lookup"><span data-stu-id="551fe-123">Hull</span></span> | <span data-ttu-id="551fe-124">Dominio</span><span class="sxs-lookup"><span data-stu-id="551fe-124">Domain</span></span> | <span data-ttu-id="551fe-125">Geometría</span><span class="sxs-lookup"><span data-stu-id="551fe-125">Geometry</span></span> | <span data-ttu-id="551fe-126">Píxel</span><span class="sxs-lookup"><span data-stu-id="551fe-126">Pixel</span></span> | <span data-ttu-id="551fe-127">Compute</span><span class="sxs-lookup"><span data-stu-id="551fe-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="551fe-128">X</span><span class="sxs-lookup"><span data-stu-id="551fe-128">X</span></span>      | <span data-ttu-id="551fe-129">X</span><span class="sxs-lookup"><span data-stu-id="551fe-129">X</span></span>    | <span data-ttu-id="551fe-130">X</span><span class="sxs-lookup"><span data-stu-id="551fe-130">X</span></span>      | <span data-ttu-id="551fe-131">X</span><span class="sxs-lookup"><span data-stu-id="551fe-131">X</span></span>        | <span data-ttu-id="551fe-132">X</span><span class="sxs-lookup"><span data-stu-id="551fe-132">X</span></span>     | <span data-ttu-id="551fe-133">X</span><span class="sxs-lookup"><span data-stu-id="551fe-133">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="551fe-134">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="551fe-134">Minimum Shader Model</span></span>

<span data-ttu-id="551fe-135">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="551fe-135">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="551fe-136">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="551fe-136">Shader Model</span></span>                                              | <span data-ttu-id="551fe-137">Compatible</span><span class="sxs-lookup"><span data-stu-id="551fe-137">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="551fe-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="551fe-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="551fe-139">sí</span><span class="sxs-lookup"><span data-stu-id="551fe-139">yes</span></span>       |
| [<span data-ttu-id="551fe-140">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="551fe-140">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="551fe-141">no</span><span class="sxs-lookup"><span data-stu-id="551fe-141">no</span></span>        |
| [<span data-ttu-id="551fe-142">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="551fe-142">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="551fe-143">no</span><span class="sxs-lookup"><span data-stu-id="551fe-143">no</span></span>        |
| [<span data-ttu-id="551fe-144">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="551fe-144">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="551fe-145">no</span><span class="sxs-lookup"><span data-stu-id="551fe-145">no</span></span>        |
| [<span data-ttu-id="551fe-146">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="551fe-146">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="551fe-147">no</span><span class="sxs-lookup"><span data-stu-id="551fe-147">no</span></span>        |
| [<span data-ttu-id="551fe-148">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="551fe-148">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="551fe-149">no</span><span class="sxs-lookup"><span data-stu-id="551fe-149">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="551fe-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="551fe-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="551fe-151">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="551fe-151">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





