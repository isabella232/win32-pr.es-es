---
title: no (SM4-ASM)
description: Not bit a bit.
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983886"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="fb5e3-103">no (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fb5e3-103">not (sm4 - asm)</span></span>

<span data-ttu-id="fb5e3-104">Not bit a bit.</span><span class="sxs-lookup"><span data-stu-id="fb5e3-104">Bitwise not.</span></span>



| <span data-ttu-id="fb5e3-105">no dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fb5e3-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="fb5e3-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="fb5e3-106">Item</span></span>                                                            | <span data-ttu-id="fb5e3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fb5e3-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fb5e3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fb5e3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fb5e3-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fb5e3-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fb5e3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fb5e3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fb5e3-111">\[en \] los componentes originales.</span><span class="sxs-lookup"><span data-stu-id="fb5e3-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="fb5e3-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fb5e3-112">Remarks</span></span>

<span data-ttu-id="fb5e3-113">Esta instrucción realiza un complemento de uno de los componentes de cada valor de 32 bits de *src0*.</span><span class="sxs-lookup"><span data-stu-id="fb5e3-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="fb5e3-114">Los resultados de 32 bits se almacenan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="fb5e3-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="fb5e3-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fb5e3-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fb5e3-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fb5e3-116">Vertex Shader</span></span> | <span data-ttu-id="fb5e3-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fb5e3-117">Geometry Shader</span></span> | <span data-ttu-id="fb5e3-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fb5e3-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fb5e3-119">x</span><span class="sxs-lookup"><span data-stu-id="fb5e3-119">x</span></span>             | <span data-ttu-id="fb5e3-120">x</span><span class="sxs-lookup"><span data-stu-id="fb5e3-120">x</span></span>               | <span data-ttu-id="fb5e3-121">x</span><span class="sxs-lookup"><span data-stu-id="fb5e3-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fb5e3-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fb5e3-122">Minimum Shader Model</span></span>

<span data-ttu-id="fb5e3-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fb5e3-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fb5e3-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fb5e3-124">Shader Model</span></span>                                              | <span data-ttu-id="fb5e3-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="fb5e3-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fb5e3-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fb5e3-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fb5e3-127">sí</span><span class="sxs-lookup"><span data-stu-id="fb5e3-127">yes</span></span>       |
| [<span data-ttu-id="fb5e3-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fb5e3-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fb5e3-129">sí</span><span class="sxs-lookup"><span data-stu-id="fb5e3-129">yes</span></span>       |
| [<span data-ttu-id="fb5e3-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fb5e3-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fb5e3-131">sí</span><span class="sxs-lookup"><span data-stu-id="fb5e3-131">yes</span></span>       |
| [<span data-ttu-id="fb5e3-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb5e3-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fb5e3-133">no</span><span class="sxs-lookup"><span data-stu-id="fb5e3-133">no</span></span>        |
| [<span data-ttu-id="fb5e3-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb5e3-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fb5e3-135">no</span><span class="sxs-lookup"><span data-stu-id="fb5e3-135">no</span></span>        |
| [<span data-ttu-id="fb5e3-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb5e3-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fb5e3-137">no</span><span class="sxs-lookup"><span data-stu-id="fb5e3-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fb5e3-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fb5e3-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb5e3-139">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fb5e3-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





