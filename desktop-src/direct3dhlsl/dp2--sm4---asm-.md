---
title: DP2 (SM4-ASM)
description: 'Vector de 2D de 2 dimensiones: producto de componentes RG, POS-swizzle.'
ms.assetid: E35F6A8B-6D8E-4660-B0F3-95B76BC19229
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4073def6cb315dc0268d1ce8e3f28039b9b2a69
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419904"
---
# <a name="dp2-sm4---asm"></a><span data-ttu-id="f2b4c-103">DP2 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-103">dp2 (sm4 - asm)</span></span>

<span data-ttu-id="f2b4c-104">Vector de 2D de 2 dimensiones: producto de componentes RG, POS-swizzle.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-104">2-dimensional vector dot-product of components rg, POS-swizzle.</span></span>



| <span data-ttu-id="f2b4c-105">DP2 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f2b4c-105">dp2\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|--------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="f2b4c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="f2b4c-106">Item</span></span>                                                            | <span data-ttu-id="f2b4c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f2b4c-107">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2b4c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f2b4c-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-109">\[in\] The address of the result of the operation.</span></span> <br/> <span data-ttu-id="f2b4c-110">*dest*  =  *src0. r* \* *SRC1. r*  +  *src0. g* \* *SRC1. g*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g*</span></span><br/> |
| <span data-ttu-id="f2b4c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f2b4c-112">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-112">\[in\] The components in the operation.</span></span><br/>                                                                             |
| <span data-ttu-id="f2b4c-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="f2b4c-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="f2b4c-114">\[en \] los componentes de la operación.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-114">\[in\] The components in the operation.</span></span><br/>                                                                             |



 

## <a name="remarks"></a><span data-ttu-id="f2b4c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f2b4c-115">Remarks</span></span>

<span data-ttu-id="f2b4c-116">Resultado escalar replicado en los componentes de la máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="f2b4c-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="f2b4c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f2b4c-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="f2b4c-118">Vertex Shader</span></span> | <span data-ttu-id="f2b4c-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="f2b4c-119">Geometry Shader</span></span> | <span data-ttu-id="f2b4c-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="f2b4c-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="f2b4c-121">x</span><span class="sxs-lookup"><span data-stu-id="f2b4c-121">x</span></span>             | <span data-ttu-id="f2b4c-122">x</span><span class="sxs-lookup"><span data-stu-id="f2b4c-122">x</span></span>               | <span data-ttu-id="f2b4c-123">x</span><span class="sxs-lookup"><span data-stu-id="f2b4c-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f2b4c-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="f2b4c-124">Minimum Shader Model</span></span>

<span data-ttu-id="f2b4c-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f2b4c-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f2b4c-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="f2b4c-126">Shader Model</span></span>                                              | <span data-ttu-id="f2b4c-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="f2b4c-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f2b4c-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f2b4c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f2b4c-129">sí</span><span class="sxs-lookup"><span data-stu-id="f2b4c-129">yes</span></span>       |
| [<span data-ttu-id="f2b4c-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f2b4c-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f2b4c-131">sí</span><span class="sxs-lookup"><span data-stu-id="f2b4c-131">yes</span></span>       |
| [<span data-ttu-id="f2b4c-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f2b4c-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f2b4c-133">sí</span><span class="sxs-lookup"><span data-stu-id="f2b4c-133">yes</span></span>       |
| [<span data-ttu-id="f2b4c-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f2b4c-135">no</span><span class="sxs-lookup"><span data-stu-id="f2b4c-135">no</span></span>        |
| [<span data-ttu-id="f2b4c-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f2b4c-137">no</span><span class="sxs-lookup"><span data-stu-id="f2b4c-137">no</span></span>        |
| [<span data-ttu-id="f2b4c-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f2b4c-139">no</span><span class="sxs-lookup"><span data-stu-id="f2b4c-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f2b4c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f2b4c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f2b4c-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f2b4c-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





