---
title: iadd (SM4-ASM)
description: Suma de enteros.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b593484aa7c1ef376bb5febf141b144ddef338e0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419967"
---
# <a name="iadd-sm4---asm"></a><span data-ttu-id="fac26-103">iadd (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fac26-103">iadd (sm4 - asm)</span></span>

<span data-ttu-id="fac26-104">Suma de enteros.</span><span class="sxs-lookup"><span data-stu-id="fac26-104">Integer addition.</span></span>



| <span data-ttu-id="fac26-105">iadd dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fac26-105">iadd dest\[.mask\], \[-\]src0\[.swizzle\], \[-\]src1\[.swizzle\]</span></span> |
|------------------------------------------------------------------|



 



| <span data-ttu-id="fac26-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="fac26-106">Item</span></span>                                                            | <span data-ttu-id="fac26-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fac26-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fac26-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fac26-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fac26-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fac26-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fac26-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fac26-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fac26-111">\[en \] el número que se va a agregar a *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="fac26-111">\[in\] The number to be added to *src1*.</span></span><br/>           |
| <span data-ttu-id="fac26-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="fac26-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fac26-113">\[en \] el número que se va a agregar a *src0*.</span><span class="sxs-lookup"><span data-stu-id="fac26-113">\[in\] The number to be added to *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="fac26-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fac26-114">Remarks</span></span>

<span data-ttu-id="fac26-115">Adición de componentes de operandos de 32 bits *src0* y *SRC1*, donde se coloca el resultado de 32 bits correcto en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="fac26-115">Component-wise add of 32-bit operands *src0* and *src1*, placing the correct 32-bit result in *dest*.</span></span> <span data-ttu-id="fac26-116">No se realiza ningún transporte o préstamo más allá de los valores de 32 bits de cada componente, por lo que esta instrucción no es sensible a la firma de sus operandos.</span><span class="sxs-lookup"><span data-stu-id="fac26-116">No carry or borrow beyond the 32-bit values of each component is performed, so this instruction is not sensitive to the signed-ness of its operands.</span></span>

<span data-ttu-id="fac26-117">El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="fac26-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="fac26-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fac26-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fac26-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fac26-119">Vertex Shader</span></span> | <span data-ttu-id="fac26-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fac26-120">Geometry Shader</span></span> | <span data-ttu-id="fac26-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fac26-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fac26-122">x</span><span class="sxs-lookup"><span data-stu-id="fac26-122">x</span></span>             | <span data-ttu-id="fac26-123">x</span><span class="sxs-lookup"><span data-stu-id="fac26-123">x</span></span>               | <span data-ttu-id="fac26-124">x</span><span class="sxs-lookup"><span data-stu-id="fac26-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fac26-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fac26-125">Minimum Shader Model</span></span>

<span data-ttu-id="fac26-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fac26-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fac26-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fac26-127">Shader Model</span></span>                                              | <span data-ttu-id="fac26-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="fac26-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fac26-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fac26-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fac26-130">sí</span><span class="sxs-lookup"><span data-stu-id="fac26-130">yes</span></span>       |
| [<span data-ttu-id="fac26-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fac26-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fac26-132">sí</span><span class="sxs-lookup"><span data-stu-id="fac26-132">yes</span></span>       |
| [<span data-ttu-id="fac26-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fac26-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fac26-134">sí</span><span class="sxs-lookup"><span data-stu-id="fac26-134">yes</span></span>       |
| [<span data-ttu-id="fac26-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fac26-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fac26-136">no</span><span class="sxs-lookup"><span data-stu-id="fac26-136">no</span></span>        |
| [<span data-ttu-id="fac26-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fac26-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fac26-138">no</span><span class="sxs-lookup"><span data-stu-id="fac26-138">no</span></span>        |
| [<span data-ttu-id="fac26-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fac26-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fac26-140">no</span><span class="sxs-lookup"><span data-stu-id="fac26-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fac26-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fac26-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac26-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fac26-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





