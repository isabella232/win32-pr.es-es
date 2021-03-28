---
title: Umax (SM4-ASM)
description: Entero sin signo de modo de componente máximo.
ms.assetid: 86BCF7A7-99CA-481B-82B4-E0BA30963344
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ceb1fda620facce31132f56ed888d18022ca27ec
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419928"
---
# <a name="umax-sm4---asm"></a><span data-ttu-id="95305-103">Umax (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="95305-103">umax (sm4 - asm)</span></span>

<span data-ttu-id="95305-104">Entero sin signo de modo de componente máximo.</span><span class="sxs-lookup"><span data-stu-id="95305-104">Component-wise unsigned integer maximum.</span></span>



| <span data-ttu-id="95305-105">Umax dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle \] ,</span><span class="sxs-lookup"><span data-stu-id="95305-105">umax dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\],</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="95305-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="95305-106">Item</span></span>                                                            | <span data-ttu-id="95305-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="95305-107">Description</span></span>                                                                                                            |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="95305-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="95305-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="95305-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="95305-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="95305-110">*dest*  =  *src0*  >  *SRC1* ?</span><span class="sxs-lookup"><span data-stu-id="95305-110">*dest* = *src0* > *src1* ?</span></span> <span data-ttu-id="95305-111">*src0* : *SRC1*</span><span class="sxs-lookup"><span data-stu-id="95305-111">*src0* : *src1*</span></span><br/> |
| <span data-ttu-id="95305-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="95305-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="95305-113">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="95305-113">\[in\] The value to compare to *src1*.</span></span><br/>                                                                      |
| <span data-ttu-id="95305-114"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="95305-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="95305-115">\[en \] el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="95305-115">\[in\] The value to compare to *src0*.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="95305-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95305-116">Remarks</span></span>

<span data-ttu-id="95305-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="95305-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="95305-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="95305-118">Vertex Shader</span></span> | <span data-ttu-id="95305-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="95305-119">Geometry Shader</span></span> | <span data-ttu-id="95305-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="95305-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="95305-121">x</span><span class="sxs-lookup"><span data-stu-id="95305-121">x</span></span>             | <span data-ttu-id="95305-122">x</span><span class="sxs-lookup"><span data-stu-id="95305-122">x</span></span>               | <span data-ttu-id="95305-123">x</span><span class="sxs-lookup"><span data-stu-id="95305-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="95305-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="95305-124">Minimum Shader Model</span></span>

<span data-ttu-id="95305-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="95305-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="95305-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="95305-126">Shader Model</span></span>                                              | <span data-ttu-id="95305-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="95305-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="95305-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="95305-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="95305-129">sí</span><span class="sxs-lookup"><span data-stu-id="95305-129">yes</span></span>       |
| [<span data-ttu-id="95305-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="95305-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="95305-131">sí</span><span class="sxs-lookup"><span data-stu-id="95305-131">yes</span></span>       |
| [<span data-ttu-id="95305-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="95305-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="95305-133">sí</span><span class="sxs-lookup"><span data-stu-id="95305-133">yes</span></span>       |
| [<span data-ttu-id="95305-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95305-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="95305-135">no</span><span class="sxs-lookup"><span data-stu-id="95305-135">no</span></span>        |
| [<span data-ttu-id="95305-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95305-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="95305-137">no</span><span class="sxs-lookup"><span data-stu-id="95305-137">no</span></span>        |
| [<span data-ttu-id="95305-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95305-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="95305-139">no</span><span class="sxs-lookup"><span data-stu-id="95305-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="95305-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="95305-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="95305-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="95305-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





