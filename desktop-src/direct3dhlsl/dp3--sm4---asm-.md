---
title: DP3 (SM4-ASM)
description: 'Vector de tres dimensiones: producto de componentes RGB, POS-swizzle.'
ms.assetid: 8E6EA6CD-B5BB-4D64-8846-F7B9F7135582
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2598053abed93675107f15af762e0844d4938fbf
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904280"
---
# <a name="dp3-sm4---asm"></a><span data-ttu-id="3064c-103">DP3 (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3064c-103">dp3 (sm4 - asm)</span></span>

<span data-ttu-id="3064c-104">Vector de tres dimensiones: producto de componentes RGB, POS-swizzle.</span><span class="sxs-lookup"><span data-stu-id="3064c-104">3-dimensional vector dot-product of components rgb, POS-swizzle.</span></span>



| <span data-ttu-id="3064c-105">DP3 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="3064c-105">dp3\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],</span></span> |
|---------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="3064c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="3064c-106">Item</span></span>                                                            | <span data-ttu-id="3064c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="3064c-107">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3064c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3064c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3064c-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3064c-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="3064c-110">*dest*  =  *src0. r* \* *SRC1. r*  +  *src0. g* \* *SRC1. g*  +  *src0. b* \* *SRC1* . b</span><span class="sxs-lookup"><span data-stu-id="3064c-110">*dest* = *src0.r* \* *src1.r* + *src0.g* \* *src1.g* + *src0.b* \* *src1.b*</span></span><br/> |
| <span data-ttu-id="3064c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3064c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3064c-112">\[en \] los componentes de operación.</span><span class="sxs-lookup"><span data-stu-id="3064c-112">\[in\] The components in the opertation.</span></span><br/>                                                                                   |
| <span data-ttu-id="3064c-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="3064c-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="3064c-114">\[en \] los componentes de operación.</span><span class="sxs-lookup"><span data-stu-id="3064c-114">\[in\] The components in the opertation.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="3064c-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3064c-115">Remarks</span></span>

<span data-ttu-id="3064c-116">Resultado escalar replicado en los componentes de la máscara de escritura.</span><span class="sxs-lookup"><span data-stu-id="3064c-116">Scalar result replicated to components in write mask.</span></span>

<span data-ttu-id="3064c-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="3064c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3064c-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3064c-118">Vertex Shader</span></span> | <span data-ttu-id="3064c-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="3064c-119">Geometry Shader</span></span> | <span data-ttu-id="3064c-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3064c-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3064c-121">x</span><span class="sxs-lookup"><span data-stu-id="3064c-121">x</span></span>             | <span data-ttu-id="3064c-122">x</span><span class="sxs-lookup"><span data-stu-id="3064c-122">x</span></span>               | <span data-ttu-id="3064c-123">x</span><span class="sxs-lookup"><span data-stu-id="3064c-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3064c-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3064c-124">Minimum Shader Model</span></span>

<span data-ttu-id="3064c-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3064c-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3064c-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3064c-126">Shader Model</span></span>                                              | <span data-ttu-id="3064c-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="3064c-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3064c-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3064c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3064c-129">sí</span><span class="sxs-lookup"><span data-stu-id="3064c-129">yes</span></span>       |
| [<span data-ttu-id="3064c-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3064c-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3064c-131">sí</span><span class="sxs-lookup"><span data-stu-id="3064c-131">yes</span></span>       |
| [<span data-ttu-id="3064c-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3064c-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3064c-133">sí</span><span class="sxs-lookup"><span data-stu-id="3064c-133">yes</span></span>       |
| [<span data-ttu-id="3064c-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3064c-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3064c-135">no</span><span class="sxs-lookup"><span data-stu-id="3064c-135">no</span></span>        |
| [<span data-ttu-id="3064c-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3064c-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3064c-137">no</span><span class="sxs-lookup"><span data-stu-id="3064c-137">no</span></span>        |
| [<span data-ttu-id="3064c-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3064c-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3064c-139">no</span><span class="sxs-lookup"><span data-stu-id="3064c-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3064c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3064c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3064c-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3064c-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





