---
title: imul (SM4-ASM)
description: Multiplicación de entero con signo.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997f62fc389ad1e0fb6b23dd6c419ff8b3933b41
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784960"
---
# <a name="imul-sm4---asm"></a><span data-ttu-id="435bf-103">imul (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="435bf-103">imul (sm4 - asm)</span></span>

<span data-ttu-id="435bf-104">Multiplicación de entero con signo.</span><span class="sxs-lookup"><span data-stu-id="435bf-104">Signed integer multiply.</span></span>



| <span data-ttu-id="435bf-105">imul destHI \[ . Mask \] , destLO \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="435bf-105">imul destHI\[.mask\], destLO\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------------------|



 



| <span data-ttu-id="435bf-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="435bf-106">Item</span></span>                                                                                           | <span data-ttu-id="435bf-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="435bf-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="435bf-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="435bf-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="435bf-109">\[en \] la dirección de los bits 32 altos del resultado.</span><span class="sxs-lookup"><span data-stu-id="435bf-109">\[in\] The address of the high 32 bits of the result.</span></span><br/> |
| <span data-ttu-id="435bf-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="435bf-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="435bf-111">\[en \] la dirección de los bits 32 inferiores del resultado.</span><span class="sxs-lookup"><span data-stu-id="435bf-111">\[in\] The address of the low 32 bits of the result.</span></span><br/>  |
| <span data-ttu-id="435bf-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="435bf-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="435bf-113">\[en \] el valor que se va a multiplicar por *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="435bf-113">\[in\] The value to multiply with *src1*.</span></span><br/>             |
| <span data-ttu-id="435bf-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="435bf-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="435bf-115">\[en \] el valor que se va a multiplicar por *src0*.</span><span class="sxs-lookup"><span data-stu-id="435bf-115">\[in\] The value to multiply with *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="435bf-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="435bf-116">Remarks</span></span>

<span data-ttu-id="435bf-117">La multiplicación por componentes de operandos de 32 bits *src0* y *SRC1* (ambas están firmadas), lo que produce el resultado de 64 bits completo correcto (por componente).</span><span class="sxs-lookup"><span data-stu-id="435bf-117">Component-wise multiply of 32-bit operands *src0* and *src1* (both are signed), producing the correct full 64-bit (per component) result.</span></span> <span data-ttu-id="435bf-118">Los bits 32 bajos (por componente) se colocan en *destLO*.</span><span class="sxs-lookup"><span data-stu-id="435bf-118">The low 32 bits (per component) are placed in *destLO*.</span></span> <span data-ttu-id="435bf-119">Los bits 32 altos (por componente) se colocan en *destHI*.</span><span class="sxs-lookup"><span data-stu-id="435bf-119">The high 32 bits (per component) are placed in *destHI*.</span></span>

<span data-ttu-id="435bf-120">*DestHI* o *destLO* se pueden especificar como null en lugar de especificar un registro, si no se necesitan los bits superiores o inferiores 32 del resultado de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="435bf-120">Either *destHI* or *destLO* may be specified as NULL instead of specifying a register, if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="435bf-121">El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación aritmética.</span><span class="sxs-lookup"><span data-stu-id="435bf-121">Optional negate modifier on source operands takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="435bf-122">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="435bf-122">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="435bf-123">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="435bf-123">Vertex Shader</span></span> | <span data-ttu-id="435bf-124">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="435bf-124">Geometry Shader</span></span> | <span data-ttu-id="435bf-125">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="435bf-125">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="435bf-126">x</span><span class="sxs-lookup"><span data-stu-id="435bf-126">x</span></span>             | <span data-ttu-id="435bf-127">x</span><span class="sxs-lookup"><span data-stu-id="435bf-127">x</span></span>               | <span data-ttu-id="435bf-128">x</span><span class="sxs-lookup"><span data-stu-id="435bf-128">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="435bf-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="435bf-129">Minimum Shader Model</span></span>

<span data-ttu-id="435bf-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="435bf-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="435bf-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="435bf-131">Shader Model</span></span>                                              | <span data-ttu-id="435bf-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="435bf-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="435bf-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="435bf-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="435bf-134">sí</span><span class="sxs-lookup"><span data-stu-id="435bf-134">yes</span></span>       |
| [<span data-ttu-id="435bf-135">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="435bf-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="435bf-136">sí</span><span class="sxs-lookup"><span data-stu-id="435bf-136">yes</span></span>       |
| [<span data-ttu-id="435bf-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="435bf-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="435bf-138">sí</span><span class="sxs-lookup"><span data-stu-id="435bf-138">yes</span></span>       |
| [<span data-ttu-id="435bf-139">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="435bf-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="435bf-140">no</span><span class="sxs-lookup"><span data-stu-id="435bf-140">no</span></span>        |
| [<span data-ttu-id="435bf-141">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="435bf-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="435bf-142">no</span><span class="sxs-lookup"><span data-stu-id="435bf-142">no</span></span>        |
| [<span data-ttu-id="435bf-143">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="435bf-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="435bf-144">no</span><span class="sxs-lookup"><span data-stu-id="435bf-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="435bf-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="435bf-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="435bf-146">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="435bf-146">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





