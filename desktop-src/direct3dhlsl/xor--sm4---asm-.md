---
title: XOR (SM4-ASM)
description: XOR bit a bit.
ms.assetid: 6B949653-6DDA-402B-8ABE-B93858B68470
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7a998bd1e95793f463d7f234b464a542bed4fc0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419887"
---
# <a name="xor-sm4---asm"></a><span data-ttu-id="eaa1b-103">XOR (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="eaa1b-103">xor (sm4 - asm)</span></span>

<span data-ttu-id="eaa1b-104">XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-104">Bitwise xor.</span></span>



| <span data-ttu-id="eaa1b-105">XOR dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="eaa1b-105">xor dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="eaa1b-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="eaa1b-106">Item</span></span>                                                            | <span data-ttu-id="eaa1b-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="eaa1b-107">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eaa1b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="eaa1b-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="eaa1b-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-109">\[in\] The result of the operation.</span></span><br/>       |
| <span data-ttu-id="eaa1b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="eaa1b-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="eaa1b-111">\[en \] los componentes de a XOR con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-111">\[in\] The components to XOR with *src1*.</span></span><br/> |
| <span data-ttu-id="eaa1b-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="eaa1b-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="eaa1b-113">\[en \] los componentes de a XOR con *src0*.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-113">\[in\] The components to XOR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="eaa1b-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="eaa1b-114">Remarks</span></span>

<span data-ttu-id="eaa1b-115">Esta instrucción realiza una XOR lógica lógica de componentes de cada par de valores de 32 bits de *src0* y *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-115">This instruction performs a component-wise logical XOR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="eaa1b-116">los resultados de 32 bits se colocan en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-116">32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="eaa1b-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="eaa1b-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="eaa1b-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="eaa1b-118">Vertex Shader</span></span> | <span data-ttu-id="eaa1b-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="eaa1b-119">Geometry Shader</span></span> | <span data-ttu-id="eaa1b-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="eaa1b-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="eaa1b-121">x</span><span class="sxs-lookup"><span data-stu-id="eaa1b-121">x</span></span>             | <span data-ttu-id="eaa1b-122">x</span><span class="sxs-lookup"><span data-stu-id="eaa1b-122">x</span></span>               | <span data-ttu-id="eaa1b-123">x</span><span class="sxs-lookup"><span data-stu-id="eaa1b-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="eaa1b-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="eaa1b-124">Minimum Shader Model</span></span>

<span data-ttu-id="eaa1b-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="eaa1b-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="eaa1b-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="eaa1b-126">Shader Model</span></span>                                              | <span data-ttu-id="eaa1b-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="eaa1b-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="eaa1b-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="eaa1b-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="eaa1b-129">sí</span><span class="sxs-lookup"><span data-stu-id="eaa1b-129">yes</span></span>       |
| [<span data-ttu-id="eaa1b-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="eaa1b-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="eaa1b-131">sí</span><span class="sxs-lookup"><span data-stu-id="eaa1b-131">yes</span></span>       |
| [<span data-ttu-id="eaa1b-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="eaa1b-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="eaa1b-133">sí</span><span class="sxs-lookup"><span data-stu-id="eaa1b-133">yes</span></span>       |
| [<span data-ttu-id="eaa1b-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eaa1b-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="eaa1b-135">no</span><span class="sxs-lookup"><span data-stu-id="eaa1b-135">no</span></span>        |
| [<span data-ttu-id="eaa1b-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eaa1b-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="eaa1b-137">no</span><span class="sxs-lookup"><span data-stu-id="eaa1b-137">no</span></span>        |
| [<span data-ttu-id="eaa1b-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eaa1b-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="eaa1b-139">no</span><span class="sxs-lookup"><span data-stu-id="eaa1b-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="eaa1b-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eaa1b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa1b-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="eaa1b-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





