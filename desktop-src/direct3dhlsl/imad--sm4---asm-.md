---
title: Imad (SM4-ASM)
description: Entero con signo que se multiplica y agrega.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90db4cb0a36b0d3951e8b0490bb3ca08db8d5354
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996860"
---
# <a name="imad-sm4---asm"></a><span data-ttu-id="de68b-103">Imad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="de68b-103">imad (sm4 - asm)</span></span>

<span data-ttu-id="de68b-104">Entero con signo que se multiplica y agrega.</span><span class="sxs-lookup"><span data-stu-id="de68b-104">Signed integer multiply and add.</span></span>



| <span data-ttu-id="de68b-105">Imad dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle \] , \[ - \] src2 \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="de68b-105">imad dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\], \[-\]src2\[.swizzle</span></span> |
|---------------------------------------------------------------------------------------|



 



| <span data-ttu-id="de68b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="de68b-106">Item</span></span>                                                            | <span data-ttu-id="de68b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="de68b-107">Description</span></span>                                                         |
|-----------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="de68b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="de68b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="de68b-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="de68b-109">\[in\] The result of the operation.</span></span><br/>                      |
| <span data-ttu-id="de68b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="de68b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="de68b-111">\[en el \] valor que se va a multiplicar por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="de68b-111">\[in\] Value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="de68b-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="de68b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="de68b-113">\[en el \] valor que se va a multiplicar por *src0*.</span><span class="sxs-lookup"><span data-stu-id="de68b-113">\[in\] Value to multiply with *src0*.</span></span><br/>                    |
| <span data-ttu-id="de68b-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="de68b-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="de68b-115">\[en \] valor para agregar al producto de *src0* y *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="de68b-115">\[in\] Value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de68b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="de68b-116">Remarks</span></span>

<span data-ttu-id="de68b-117">[Imul](imul--sm4---asm-.md) de componentes de los operandos de 32 bits *src0* y *SRC1* (signed), manteniendo un mínimo de 32 bits (por componente) del resultado, seguido de un [iadd](iadd--sm4---asm-.md) de *src2*, que genera el resultado correcto de 32 bits (por componente) correcto.</span><span class="sxs-lookup"><span data-stu-id="de68b-117">Component-wise [imul](imul--sm4---asm-.md) of 32-bit operands *src0* and *src1* (signed), keeping low 32-bits (per component) of the result, followed by an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="de68b-118">Los resultados de 32 bits se colocan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="de68b-118">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="de68b-119">El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación aritmética.</span><span class="sxs-lookup"><span data-stu-id="de68b-119">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="de68b-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="de68b-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="de68b-121">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="de68b-121">Vertex Shader</span></span> | <span data-ttu-id="de68b-122">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="de68b-122">Geometry Shader</span></span> | <span data-ttu-id="de68b-123">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="de68b-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="de68b-124">x</span><span class="sxs-lookup"><span data-stu-id="de68b-124">x</span></span>             | <span data-ttu-id="de68b-125">x</span><span class="sxs-lookup"><span data-stu-id="de68b-125">x</span></span>               | <span data-ttu-id="de68b-126">x</span><span class="sxs-lookup"><span data-stu-id="de68b-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="de68b-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="de68b-127">Minimum Shader Model</span></span>

<span data-ttu-id="de68b-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="de68b-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="de68b-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="de68b-129">Shader Model</span></span>                                              | <span data-ttu-id="de68b-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="de68b-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="de68b-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="de68b-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="de68b-132">sí</span><span class="sxs-lookup"><span data-stu-id="de68b-132">yes</span></span>       |
| [<span data-ttu-id="de68b-133">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="de68b-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="de68b-134">sí</span><span class="sxs-lookup"><span data-stu-id="de68b-134">yes</span></span>       |
| [<span data-ttu-id="de68b-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="de68b-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="de68b-136">sí</span><span class="sxs-lookup"><span data-stu-id="de68b-136">yes</span></span>       |
| [<span data-ttu-id="de68b-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de68b-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="de68b-138">no</span><span class="sxs-lookup"><span data-stu-id="de68b-138">no</span></span>        |
| [<span data-ttu-id="de68b-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de68b-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="de68b-140">no</span><span class="sxs-lookup"><span data-stu-id="de68b-140">no</span></span>        |
| [<span data-ttu-id="de68b-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de68b-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="de68b-142">no</span><span class="sxs-lookup"><span data-stu-id="de68b-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="de68b-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="de68b-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de68b-144">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="de68b-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





