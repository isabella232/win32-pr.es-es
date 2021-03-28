---
title: y (SM4-ASM)
description: AND bit a bit.
ms.assetid: 403DA289-E2CF-4736-8882-4131F884F777
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ec9474322aafda2706502898902d01d0e13143
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784979"
---
# <a name="and-sm4---asm"></a><span data-ttu-id="fa403-103">y (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fa403-103">and (sm4 - asm)</span></span>

<span data-ttu-id="fa403-104">And bit **a** bit.</span><span class="sxs-lookup"><span data-stu-id="fa403-104">Bitwise **AND**.</span></span>



| <span data-ttu-id="fa403-105">y dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="fa403-105">and dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="fa403-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="fa403-106">Item</span></span>                                                            | <span data-ttu-id="fa403-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="fa403-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fa403-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fa403-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fa403-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fa403-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fa403-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fa403-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fa403-111">\[en \] el valor de 32 bits en **y** con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="fa403-111">\[in\] The 32-bit value to **AND** with *src1*.</span></span><br/>    |
| <span data-ttu-id="fa403-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="fa403-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fa403-113">\[en \] el valor de 32 bits en **y** con *src0*.</span><span class="sxs-lookup"><span data-stu-id="fa403-113">\[in\] The 32-bit value to **AND** with *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="fa403-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fa403-114">Remarks</span></span>

<span data-ttu-id="fa403-115">Lógica de componentes **y** de cada par de valores de 32 bits de *src0* y *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="fa403-115">Component-wise logical **AND** of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="fa403-116">Los resultados de 32 bits se colocan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="fa403-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="fa403-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fa403-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fa403-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fa403-118">Vertex Shader</span></span> | <span data-ttu-id="fa403-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fa403-119">Geometry Shader</span></span> | <span data-ttu-id="fa403-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fa403-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fa403-121">x</span><span class="sxs-lookup"><span data-stu-id="fa403-121">x</span></span>             | <span data-ttu-id="fa403-122">x</span><span class="sxs-lookup"><span data-stu-id="fa403-122">x</span></span>               | <span data-ttu-id="fa403-123">x</span><span class="sxs-lookup"><span data-stu-id="fa403-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fa403-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fa403-124">Minimum Shader Model</span></span>

<span data-ttu-id="fa403-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fa403-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fa403-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fa403-126">Shader Model</span></span>                                              | <span data-ttu-id="fa403-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="fa403-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fa403-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fa403-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fa403-129">sí</span><span class="sxs-lookup"><span data-stu-id="fa403-129">yes</span></span>       |
| [<span data-ttu-id="fa403-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fa403-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fa403-131">sí</span><span class="sxs-lookup"><span data-stu-id="fa403-131">yes</span></span>       |
| [<span data-ttu-id="fa403-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fa403-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fa403-133">sí</span><span class="sxs-lookup"><span data-stu-id="fa403-133">yes</span></span>       |
| [<span data-ttu-id="fa403-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa403-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fa403-135">no</span><span class="sxs-lookup"><span data-stu-id="fa403-135">no</span></span>        |
| [<span data-ttu-id="fa403-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa403-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fa403-137">no</span><span class="sxs-lookup"><span data-stu-id="fa403-137">no</span></span>        |
| [<span data-ttu-id="fa403-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa403-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fa403-139">no</span><span class="sxs-lookup"><span data-stu-id="fa403-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fa403-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fa403-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa403-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa403-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





