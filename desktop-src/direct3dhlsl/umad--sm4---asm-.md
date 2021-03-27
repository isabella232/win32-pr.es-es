---
title: Umad (SM4-ASM)
description: Entero sin signo de multiplicación y suma.
ms.assetid: C0BE31CA-E01D-42C0-A660-E63727CE344F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce52925622cb2f6f7cf53dec0e3f6f65d3fdcb58
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784930"
---
# <a name="umad-sm4---asm"></a><span data-ttu-id="db7a2-103">Umad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="db7a2-103">umad (sm4 - asm)</span></span>

<span data-ttu-id="db7a2-104">Entero sin signo de multiplicación y suma.</span><span class="sxs-lookup"><span data-stu-id="db7a2-104">Unsigned integer multiply and add.</span></span>



| <span data-ttu-id="db7a2-105">Umad dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] , src2 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="db7a2-105">umad dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\], src2\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------|



 



| <span data-ttu-id="db7a2-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="db7a2-106">Item</span></span>                                                            | <span data-ttu-id="db7a2-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="db7a2-107">Description</span></span>                                                             |
|-----------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="db7a2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="db7a2-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="db7a2-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="db7a2-109">\[in\] The address of the result of the operation.</span></span><br/>           |
| <span data-ttu-id="db7a2-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="db7a2-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="db7a2-111">\[en \] el valor que se va a multiplicar por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="db7a2-111">\[in\] The value to multiply with *src1*.</span></span><br/>                    |
| <span data-ttu-id="db7a2-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="db7a2-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="db7a2-113">\[en \] el valor que se va a multiplicar por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="db7a2-113">\[in\] The value to multiply with *src1*.</span></span><br/>                     |
| <span data-ttu-id="db7a2-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="db7a2-114"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="db7a2-115">\[en \] el valor que se va a agregar al producto de *src0* y *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="db7a2-115">\[in\] The value to add to the product of *src0* and *src1*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db7a2-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="db7a2-116">Remarks</span></span>

<span data-ttu-id="db7a2-117">[UMUL](umul--sm4---asm-.md) de componentes de los operandos de 32 bits *src0* y *SRC1* sin signo, manteniendo los 32 bits inferiores, por componente, del resultado.</span><span class="sxs-lookup"><span data-stu-id="db7a2-117">Component-wise [umul](umul--sm4---asm-.md) of 32-bit operands *src0* and *src1* unsigned, keeping the low 32-bits, per component, of the result.</span></span> <span data-ttu-id="db7a2-118">A continuación, esta instrucción realiza una [iadd](iadd--sm4---asm-.md) de *src2*, lo que genera el resultado correcto de 32 bits (por componente).</span><span class="sxs-lookup"><span data-stu-id="db7a2-118">This instruction then performs an [iadd](iadd--sm4---asm-.md) of *src2*, producing the correct low 32-bit (per component) result.</span></span> <span data-ttu-id="db7a2-119">Los resultados de 32 bits se colocan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="db7a2-119">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="db7a2-120">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="db7a2-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="db7a2-121">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="db7a2-121">Vertex Shader</span></span> | <span data-ttu-id="db7a2-122">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="db7a2-122">Geometry Shader</span></span> | <span data-ttu-id="db7a2-123">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="db7a2-123">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="db7a2-124">x</span><span class="sxs-lookup"><span data-stu-id="db7a2-124">x</span></span>             | <span data-ttu-id="db7a2-125">x</span><span class="sxs-lookup"><span data-stu-id="db7a2-125">x</span></span>               | <span data-ttu-id="db7a2-126">x</span><span class="sxs-lookup"><span data-stu-id="db7a2-126">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="db7a2-127">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="db7a2-127">Minimum Shader Model</span></span>

<span data-ttu-id="db7a2-128">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="db7a2-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="db7a2-129">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="db7a2-129">Shader Model</span></span>                                              | <span data-ttu-id="db7a2-130">Compatible</span><span class="sxs-lookup"><span data-stu-id="db7a2-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="db7a2-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="db7a2-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="db7a2-132">sí</span><span class="sxs-lookup"><span data-stu-id="db7a2-132">yes</span></span>       |
| [<span data-ttu-id="db7a2-133">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="db7a2-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="db7a2-134">sí</span><span class="sxs-lookup"><span data-stu-id="db7a2-134">yes</span></span>       |
| [<span data-ttu-id="db7a2-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="db7a2-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="db7a2-136">sí</span><span class="sxs-lookup"><span data-stu-id="db7a2-136">yes</span></span>       |
| [<span data-ttu-id="db7a2-137">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db7a2-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="db7a2-138">no</span><span class="sxs-lookup"><span data-stu-id="db7a2-138">no</span></span>        |
| [<span data-ttu-id="db7a2-139">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db7a2-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="db7a2-140">no</span><span class="sxs-lookup"><span data-stu-id="db7a2-140">no</span></span>        |
| [<span data-ttu-id="db7a2-141">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db7a2-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="db7a2-142">no</span><span class="sxs-lookup"><span data-stu-id="db7a2-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="db7a2-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="db7a2-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db7a2-144">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="db7a2-144">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





