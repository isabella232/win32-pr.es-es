---
title: Imin (SM4-ASM)
description: Entero de tipo de componente mínimo.
ms.assetid: 8EDD5503-76D5-4078-BFBA-1DA9260C6E68
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 942384e7a988e4919a483e09c75e476d5a6917ba
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419962"
---
# <a name="imin-sm4---asm"></a><span data-ttu-id="b1a45-103">Imin (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b1a45-103">imin (sm4 - asm)</span></span>

<span data-ttu-id="b1a45-104">Entero de tipo de componente mínimo.</span><span class="sxs-lookup"><span data-stu-id="b1a45-104">Component-wise integer minimum.</span></span>



| <span data-ttu-id="b1a45-105">Imin dest \[ . Mask \] , \[  - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="b1a45-105">imin dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="b1a45-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="b1a45-106">Item</span></span>                                                            | <span data-ttu-id="b1a45-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1a45-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1a45-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b1a45-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b1a45-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="b1a45-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="b1a45-110">*dest*  =  *src0*  <  *SRC1* ?</span><span class="sxs-lookup"><span data-stu-id="b1a45-110">*dest* = *src0* < *src1* ?</span></span> <span data-ttu-id="b1a45-111">*src0* : *SRC1*</span><span class="sxs-lookup"><span data-stu-id="b1a45-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="b1a45-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b1a45-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b1a45-113">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="b1a45-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="b1a45-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="b1a45-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b1a45-115">\[en \] el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="b1a45-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="b1a45-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1a45-116">Remarks</span></span>

<span data-ttu-id="b1a45-117">El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="b1a45-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="b1a45-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="b1a45-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b1a45-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="b1a45-119">Vertex Shader</span></span> | <span data-ttu-id="b1a45-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="b1a45-120">Geometry Shader</span></span> | <span data-ttu-id="b1a45-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="b1a45-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b1a45-122">x</span><span class="sxs-lookup"><span data-stu-id="b1a45-122">x</span></span>             | <span data-ttu-id="b1a45-123">x</span><span class="sxs-lookup"><span data-stu-id="b1a45-123">x</span></span>               | <span data-ttu-id="b1a45-124">x</span><span class="sxs-lookup"><span data-stu-id="b1a45-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b1a45-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="b1a45-125">Minimum Shader Model</span></span>

<span data-ttu-id="b1a45-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b1a45-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b1a45-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="b1a45-127">Shader Model</span></span>                                              | <span data-ttu-id="b1a45-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="b1a45-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b1a45-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b1a45-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b1a45-130">sí</span><span class="sxs-lookup"><span data-stu-id="b1a45-130">yes</span></span>       |
| [<span data-ttu-id="b1a45-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b1a45-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b1a45-132">sí</span><span class="sxs-lookup"><span data-stu-id="b1a45-132">yes</span></span>       |
| [<span data-ttu-id="b1a45-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b1a45-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b1a45-134">sí</span><span class="sxs-lookup"><span data-stu-id="b1a45-134">yes</span></span>       |
| [<span data-ttu-id="b1a45-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1a45-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b1a45-136">no</span><span class="sxs-lookup"><span data-stu-id="b1a45-136">no</span></span>        |
| [<span data-ttu-id="b1a45-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1a45-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b1a45-138">no</span><span class="sxs-lookup"><span data-stu-id="b1a45-138">no</span></span>        |
| [<span data-ttu-id="b1a45-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1a45-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b1a45-140">no</span><span class="sxs-lookup"><span data-stu-id="b1a45-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b1a45-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1a45-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1a45-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b1a45-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





