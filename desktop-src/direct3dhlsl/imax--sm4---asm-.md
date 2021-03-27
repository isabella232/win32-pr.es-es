---
title: IMAX (SM4-ASM)
description: Entero de tipo de componente máximo.
ms.assetid: 005468AA-577E-441F-ACD5-37A691E62CDD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc1bc6311573b1e7b39fbeaa93904203e7aae2ae
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104148985"
---
# <a name="imax-sm4---asm"></a><span data-ttu-id="d7a0c-103">IMAX (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-103">imax (sm4 - asm)</span></span>

<span data-ttu-id="d7a0c-104">Entero de tipo de componente máximo.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-104">Component-wise integer maximum.</span></span>



| <span data-ttu-id="d7a0c-105">IMAX dest \[ . Mask \] , \[  - \] src0 \[ . swizzle \] , \[ - \] SRC1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="d7a0c-105">imax dest\[.mask\], \[ -\]src0\[.swizzle\], \[-\]src1\[.swizzle\],</span></span> |
|--------------------------------------------------------------------|



 



| <span data-ttu-id="d7a0c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7a0c-106">Item</span></span>                                                            | <span data-ttu-id="d7a0c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7a0c-107">Description</span></span>                                                                                             |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7a0c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d7a0c-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="d7a0c-110">*dest*  =  *src0*  >  *SRC1* ?</span><span class="sxs-lookup"><span data-stu-id="d7a0c-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="d7a0c-111">*src0* : *SRC1*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="d7a0c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d7a0c-113">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                       |
| <span data-ttu-id="d7a0c-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d7a0c-115">\[en \] el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="d7a0c-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7a0c-116">Remarks</span></span>

<span data-ttu-id="d7a0c-117">El modificador opcional Negate en los operandos de origen toma el complemento de 2 antes de realizar la operación.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-117">Optional negate modifier on source operands takes 2's complement before performing operation.</span></span>

<span data-ttu-id="d7a0c-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d7a0c-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d7a0c-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d7a0c-119">Vertex Shader</span></span> | <span data-ttu-id="d7a0c-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="d7a0c-120">Geometry Shader</span></span> | <span data-ttu-id="d7a0c-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d7a0c-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d7a0c-122">x</span><span class="sxs-lookup"><span data-stu-id="d7a0c-122">x</span></span>             | <span data-ttu-id="d7a0c-123">x</span><span class="sxs-lookup"><span data-stu-id="d7a0c-123">x</span></span>               | <span data-ttu-id="d7a0c-124">x</span><span class="sxs-lookup"><span data-stu-id="d7a0c-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7a0c-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d7a0c-125">Minimum Shader Model</span></span>

<span data-ttu-id="d7a0c-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d7a0c-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d7a0c-127">Shader Model</span></span>                                              | <span data-ttu-id="d7a0c-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="d7a0c-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d7a0c-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d7a0c-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d7a0c-130">sí</span><span class="sxs-lookup"><span data-stu-id="d7a0c-130">yes</span></span>       |
| [<span data-ttu-id="d7a0c-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d7a0c-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d7a0c-132">sí</span><span class="sxs-lookup"><span data-stu-id="d7a0c-132">yes</span></span>       |
| [<span data-ttu-id="d7a0c-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d7a0c-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d7a0c-134">sí</span><span class="sxs-lookup"><span data-stu-id="d7a0c-134">yes</span></span>       |
| [<span data-ttu-id="d7a0c-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d7a0c-136">no</span><span class="sxs-lookup"><span data-stu-id="d7a0c-136">no</span></span>        |
| [<span data-ttu-id="d7a0c-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d7a0c-138">no</span><span class="sxs-lookup"><span data-stu-id="d7a0c-138">no</span></span>        |
| [<span data-ttu-id="d7a0c-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d7a0c-140">no</span><span class="sxs-lookup"><span data-stu-id="d7a0c-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d7a0c-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7a0c-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7a0c-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





