---
title: o (SM4-ASM)
description: OR bit a bit.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996944"
---
# <a name="or-sm4---asm"></a><span data-ttu-id="d7a0c-103">o (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-103">or (sm4 - asm)</span></span>

<span data-ttu-id="d7a0c-104">OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-104">Bitwise or.</span></span>



| <span data-ttu-id="d7a0c-105">o dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d7a0c-105">or dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------|



 



| <span data-ttu-id="d7a0c-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d7a0c-106">Item</span></span>                                                            | <span data-ttu-id="d7a0c-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d7a0c-107">Description</span></span>                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="d7a0c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d7a0c-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-109">\[in\] The result of the operation.</span></span><br/>      |
| <span data-ttu-id="d7a0c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d7a0c-111">\[en \] los componentes a o con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-111">\[in\] The components to OR with *src1*.</span></span><br/> |
| <span data-ttu-id="d7a0c-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="d7a0c-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d7a0c-113">\[en \] los componentes a o con *src0*.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-113">\[in\] The components to OR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d7a0c-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7a0c-114">Remarks</span></span>

<span data-ttu-id="d7a0c-115">Esta instrucción realiza una operación lógica de componente o de cada par de valores de 32 bits de *src0* y *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-115">This instruction performs a component-wise logical OR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="d7a0c-116">Los resultados de 32 bits se colocan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="d7a0c-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d7a0c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d7a0c-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d7a0c-118">Vertex Shader</span></span> | <span data-ttu-id="d7a0c-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="d7a0c-119">Geometry Shader</span></span> | <span data-ttu-id="d7a0c-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d7a0c-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d7a0c-121">x</span><span class="sxs-lookup"><span data-stu-id="d7a0c-121">x</span></span>             | <span data-ttu-id="d7a0c-122">x</span><span class="sxs-lookup"><span data-stu-id="d7a0c-122">x</span></span>               | <span data-ttu-id="d7a0c-123">x</span><span class="sxs-lookup"><span data-stu-id="d7a0c-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d7a0c-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d7a0c-124">Minimum Shader Model</span></span>

<span data-ttu-id="d7a0c-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d7a0c-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d7a0c-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d7a0c-126">Shader Model</span></span>                                              | <span data-ttu-id="d7a0c-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="d7a0c-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d7a0c-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d7a0c-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d7a0c-129">sí</span><span class="sxs-lookup"><span data-stu-id="d7a0c-129">yes</span></span>       |
| [<span data-ttu-id="d7a0c-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d7a0c-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d7a0c-131">sí</span><span class="sxs-lookup"><span data-stu-id="d7a0c-131">yes</span></span>       |
| [<span data-ttu-id="d7a0c-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d7a0c-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d7a0c-133">sí</span><span class="sxs-lookup"><span data-stu-id="d7a0c-133">yes</span></span>       |
| [<span data-ttu-id="d7a0c-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d7a0c-135">no</span><span class="sxs-lookup"><span data-stu-id="d7a0c-135">no</span></span>        |
| [<span data-ttu-id="d7a0c-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d7a0c-137">no</span><span class="sxs-lookup"><span data-stu-id="d7a0c-137">no</span></span>        |
| [<span data-ttu-id="d7a0c-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d7a0c-139">no</span><span class="sxs-lookup"><span data-stu-id="d7a0c-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d7a0c-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d7a0c-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d7a0c-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d7a0c-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





