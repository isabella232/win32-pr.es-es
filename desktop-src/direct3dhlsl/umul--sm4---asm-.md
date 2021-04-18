---
title: UMUL (SM4-ASM)
description: Multiplicación de enteros sin signo.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581696ef5aa7d027c30b4ae866d06401275ef4bc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419927"
---
# <a name="umul-sm4---asm"></a><span data-ttu-id="aa37b-103">UMUL (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="aa37b-103">umul (sm4 - asm)</span></span>

<span data-ttu-id="aa37b-104">Multiplicación de enteros sin signo.</span><span class="sxs-lookup"><span data-stu-id="aa37b-104">Unsigned integer multiply.</span></span>



| <span data-ttu-id="aa37b-105">UMUL destHI \[ . Mask \] , destLO \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="aa37b-105">umul destHI\[.mask\], destLO\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="aa37b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="aa37b-106">Item</span></span>                                                                                           | <span data-ttu-id="aa37b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="aa37b-107">Description</span></span>                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span data-ttu-id="aa37b-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span><span class="sxs-lookup"><span data-stu-id="aa37b-108"><span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*</span></span><br/> | <span data-ttu-id="aa37b-109">\[en \] los bits 32 altos del resultado, por componente.</span><span class="sxs-lookup"><span data-stu-id="aa37b-109">\[in\] The high 32 bits of the result, per component.</span></span><br/> |
| <span data-ttu-id="aa37b-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span><span class="sxs-lookup"><span data-stu-id="aa37b-110"><span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*</span></span><br/> | <span data-ttu-id="aa37b-111">\[en \] los bits 32 inferiores del resultado, por componente.</span><span class="sxs-lookup"><span data-stu-id="aa37b-111">\[in\] The low 32 bits of the result, per component.</span></span><br/>  |
| <span data-ttu-id="aa37b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="aa37b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/>                                | <span data-ttu-id="aa37b-113">\[en \] los componentes por los que se va a multiplicar *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="aa37b-113">\[in\] The components by which to multiply *src1*.</span></span><br/>    |
| <span data-ttu-id="aa37b-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="aa37b-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/>                                | <span data-ttu-id="aa37b-115">\[en \] los componentes por los que se va a multiplicar *src0*.</span><span class="sxs-lookup"><span data-stu-id="aa37b-115">\[in\] The components by which to multiply *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="aa37b-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="aa37b-116">Remarks</span></span>

<span data-ttu-id="aa37b-117">Esta instrucción realiza una multiplicación por componentes de operandos de 32 bits sin signo *src0* y *SRC1*, lo que produce el resultado de 64 bits completo correcto por componente.</span><span class="sxs-lookup"><span data-stu-id="aa37b-117">This instruction performs a component-wise multiply of unsigned 32-bit operands *src0* and *src1*, producing the correct full 64-bit result per component.</span></span> <span data-ttu-id="aa37b-118">Los bits inferiores 32 por componente se colocan en *destLO*.</span><span class="sxs-lookup"><span data-stu-id="aa37b-118">The low 32 bits per component are placed in *destLO*.</span></span> <span data-ttu-id="aa37b-119">Los altos 32 bits por componente se colocan en *destHI*.</span><span class="sxs-lookup"><span data-stu-id="aa37b-119">The high 32 bits per component are placed in *destHI*.</span></span>

<span data-ttu-id="aa37b-120">Puede especificar *destHI* o *destLO* como null en lugar de especificar un registro si no se necesitan los bits superiores o inferiores 32 del resultado de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="aa37b-120">You can specify either *destHI* or *destLO* as NULL instead of specifying a register if the high or low 32 bits of the 64-bit result are not needed.</span></span>

<span data-ttu-id="aa37b-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="aa37b-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="aa37b-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="aa37b-122">Vertex Shader</span></span> | <span data-ttu-id="aa37b-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="aa37b-123">Geometry Shader</span></span> | <span data-ttu-id="aa37b-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="aa37b-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="aa37b-125">x</span><span class="sxs-lookup"><span data-stu-id="aa37b-125">x</span></span>             | <span data-ttu-id="aa37b-126">x</span><span class="sxs-lookup"><span data-stu-id="aa37b-126">x</span></span>               | <span data-ttu-id="aa37b-127">x</span><span class="sxs-lookup"><span data-stu-id="aa37b-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="aa37b-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="aa37b-128">Minimum Shader Model</span></span>

<span data-ttu-id="aa37b-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="aa37b-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="aa37b-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="aa37b-130">Shader Model</span></span>                                              | <span data-ttu-id="aa37b-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="aa37b-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="aa37b-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="aa37b-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="aa37b-133">sí</span><span class="sxs-lookup"><span data-stu-id="aa37b-133">yes</span></span>       |
| [<span data-ttu-id="aa37b-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="aa37b-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="aa37b-135">sí</span><span class="sxs-lookup"><span data-stu-id="aa37b-135">yes</span></span>       |
| [<span data-ttu-id="aa37b-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="aa37b-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="aa37b-137">sí</span><span class="sxs-lookup"><span data-stu-id="aa37b-137">yes</span></span>       |
| [<span data-ttu-id="aa37b-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa37b-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="aa37b-139">no</span><span class="sxs-lookup"><span data-stu-id="aa37b-139">no</span></span>        |
| [<span data-ttu-id="aa37b-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa37b-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="aa37b-141">no</span><span class="sxs-lookup"><span data-stu-id="aa37b-141">no</span></span>        |
| [<span data-ttu-id="aa37b-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa37b-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="aa37b-143">no</span><span class="sxs-lookup"><span data-stu-id="aa37b-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="aa37b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="aa37b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa37b-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="aa37b-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





