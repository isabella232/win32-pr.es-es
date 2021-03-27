---
title: ubfe (SM5-ASM)
description: Dado un intervalo de bits en un número, desplace esos bits a LSB y establezca los bits restantes en 0.
ms.assetid: CC6BE378-2726-47A2-8E23-B8151521F72D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ebbe853ec1b53b452f32d79c9c2ec120e826b8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904286"
---
# <a name="ubfe-sm5---asm"></a><span data-ttu-id="63981-103">ubfe (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="63981-103">ubfe (sm5 - asm)</span></span>

<span data-ttu-id="63981-104">Dado un intervalo de bits en un número, desplace esos bits a LSB y establezca los bits restantes en 0.</span><span class="sxs-lookup"><span data-stu-id="63981-104">Given a range of bits in a number, shift those bits to the LSB and set remaining bits to 0.</span></span>



| <span data-ttu-id="63981-105">ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="63981-105">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="63981-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="63981-106">Item</span></span>                                                            | <span data-ttu-id="63981-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="63981-107">Description</span></span>                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="63981-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="63981-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="63981-109">\[en \] contiene los resultados de la instrucción.</span><span class="sxs-lookup"><span data-stu-id="63981-109">\[in\] Contains the results of the instruction.</span></span><br/>                     |
| <span data-ttu-id="63981-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="63981-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="63981-111">\[en \] LSB 5 bits, proporcione el ancho de campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="63981-111">\[in\] The LSB 5 bits provide the bitfield width (0-31).</span></span><br/>            |
| <span data-ttu-id="63981-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="63981-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="63981-113">\[en \] los 5 bits LSB de *SRC1* , proporcione el desplazamiento de campo de bits (0-31).</span><span class="sxs-lookup"><span data-stu-id="63981-113">\[in\] The LSB 5 bits of *src1* provide the bitfield offset (0-31).</span></span><br/> |
| <span data-ttu-id="63981-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="63981-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="63981-115">\[en \] el número que se va a desplazar.</span><span class="sxs-lookup"><span data-stu-id="63981-115">\[in\] The number to shift.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="63981-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63981-116">Remarks</span></span>

``` syntax
 
        Given width, offset:
                if( width == 0 )
                {
                    dest = 0
                }
                else if( width + offset < 32 )
                {
                    shl dest, src2, 32-(width+offset)
                    ushr dest, dest, 32-width
                }
                else
                {
                    ushr dest, src2, offset
                }
```

<span data-ttu-id="63981-117">Use esta instrucción para desempaquetar los enteros o marcas sin signo.</span><span class="sxs-lookup"><span data-stu-id="63981-117">Use this instruction to unpack unsigned integers or flags.</span></span>

<span data-ttu-id="63981-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="63981-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="63981-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="63981-119">Vertex</span></span> | <span data-ttu-id="63981-120">Casco</span><span class="sxs-lookup"><span data-stu-id="63981-120">Hull</span></span> | <span data-ttu-id="63981-121">Dominio</span><span class="sxs-lookup"><span data-stu-id="63981-121">Domain</span></span> | <span data-ttu-id="63981-122">Geometría</span><span class="sxs-lookup"><span data-stu-id="63981-122">Geometry</span></span> | <span data-ttu-id="63981-123">Píxel</span><span class="sxs-lookup"><span data-stu-id="63981-123">Pixel</span></span> | <span data-ttu-id="63981-124">Compute</span><span class="sxs-lookup"><span data-stu-id="63981-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="63981-125">X</span><span class="sxs-lookup"><span data-stu-id="63981-125">X</span></span>      | <span data-ttu-id="63981-126">X</span><span class="sxs-lookup"><span data-stu-id="63981-126">X</span></span>    | <span data-ttu-id="63981-127">X</span><span class="sxs-lookup"><span data-stu-id="63981-127">X</span></span>      | <span data-ttu-id="63981-128">X</span><span class="sxs-lookup"><span data-stu-id="63981-128">X</span></span>        | <span data-ttu-id="63981-129">X</span><span class="sxs-lookup"><span data-stu-id="63981-129">X</span></span>     | <span data-ttu-id="63981-130">X</span><span class="sxs-lookup"><span data-stu-id="63981-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="63981-131">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="63981-131">Minimum Shader Model</span></span>

<span data-ttu-id="63981-132">Esta instrucción es compatible con los siguientes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="63981-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="63981-133">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="63981-133">Shader Model</span></span>                                              | <span data-ttu-id="63981-134">Compatible</span><span class="sxs-lookup"><span data-stu-id="63981-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="63981-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="63981-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="63981-136">sí</span><span class="sxs-lookup"><span data-stu-id="63981-136">yes</span></span>       |
| [<span data-ttu-id="63981-137">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="63981-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="63981-138">no</span><span class="sxs-lookup"><span data-stu-id="63981-138">no</span></span>        |
| [<span data-ttu-id="63981-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="63981-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="63981-140">no</span><span class="sxs-lookup"><span data-stu-id="63981-140">no</span></span>        |
| [<span data-ttu-id="63981-141">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63981-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="63981-142">no</span><span class="sxs-lookup"><span data-stu-id="63981-142">no</span></span>        |
| [<span data-ttu-id="63981-143">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63981-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="63981-144">no</span><span class="sxs-lookup"><span data-stu-id="63981-144">no</span></span>        |
| [<span data-ttu-id="63981-145">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63981-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="63981-146">no</span><span class="sxs-lookup"><span data-stu-id="63981-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="63981-147">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="63981-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="63981-148">Ensamblador modelo de sombreador 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="63981-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





