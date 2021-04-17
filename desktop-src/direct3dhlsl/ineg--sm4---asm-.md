---
title: INEG (SM4-ASM)
description: el complemento de 2.
ms.assetid: 20C1EEC8-E349-4398-8EE3-EDD01EBCD4B1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec4da3e0cbb08bee7bd732a4da8175705d1e1a0f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419957"
---
# <a name="ineg-sm4---asm"></a><span data-ttu-id="cc6ed-103">INEG (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cc6ed-103">ineg (sm4 - asm)</span></span>

<span data-ttu-id="cc6ed-104">el complemento de 2.</span><span class="sxs-lookup"><span data-stu-id="cc6ed-104">2's complement.</span></span>



| <span data-ttu-id="cc6ed-105">INEG dest \[ . Mask \] , src0 \[ . swizzle</span><span class="sxs-lookup"><span data-stu-id="cc6ed-105">ineg dest\[.mask\], src0\[.swizzle</span></span> |
|------------------------------------|



 



| <span data-ttu-id="cc6ed-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="cc6ed-106">Item</span></span>                                                            | <span data-ttu-id="cc6ed-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="cc6ed-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="cc6ed-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cc6ed-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cc6ed-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="cc6ed-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="cc6ed-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cc6ed-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cc6ed-111">\[en \] contiene los valores de la operación.</span><span class="sxs-lookup"><span data-stu-id="cc6ed-111">\[in\] Contains the values for the operation.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="cc6ed-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="cc6ed-112">Remarks</span></span>

<span data-ttu-id="cc6ed-113">Esta instrucción realiza el complemento del componente 2 de cada valor de 32 bits de *src0*.</span><span class="sxs-lookup"><span data-stu-id="cc6ed-113">This instruction performs component-wise 2's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="cc6ed-114">Los resultados de 32 bits se almacenan en *dest*.</span><span class="sxs-lookup"><span data-stu-id="cc6ed-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="cc6ed-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="cc6ed-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cc6ed-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="cc6ed-116">Vertex Shader</span></span> | <span data-ttu-id="cc6ed-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="cc6ed-117">Geometry Shader</span></span> | <span data-ttu-id="cc6ed-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="cc6ed-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cc6ed-119">x</span><span class="sxs-lookup"><span data-stu-id="cc6ed-119">x</span></span>             | <span data-ttu-id="cc6ed-120">x</span><span class="sxs-lookup"><span data-stu-id="cc6ed-120">x</span></span>               | <span data-ttu-id="cc6ed-121">x</span><span class="sxs-lookup"><span data-stu-id="cc6ed-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cc6ed-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="cc6ed-122">Minimum Shader Model</span></span>

<span data-ttu-id="cc6ed-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cc6ed-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cc6ed-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="cc6ed-124">Shader Model</span></span>                                              | <span data-ttu-id="cc6ed-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="cc6ed-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cc6ed-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cc6ed-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cc6ed-127">sí</span><span class="sxs-lookup"><span data-stu-id="cc6ed-127">yes</span></span>       |
| [<span data-ttu-id="cc6ed-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cc6ed-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cc6ed-129">sí</span><span class="sxs-lookup"><span data-stu-id="cc6ed-129">yes</span></span>       |
| [<span data-ttu-id="cc6ed-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cc6ed-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cc6ed-131">sí</span><span class="sxs-lookup"><span data-stu-id="cc6ed-131">yes</span></span>       |
| [<span data-ttu-id="cc6ed-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc6ed-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cc6ed-133">no</span><span class="sxs-lookup"><span data-stu-id="cc6ed-133">no</span></span>        |
| [<span data-ttu-id="cc6ed-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc6ed-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cc6ed-135">no</span><span class="sxs-lookup"><span data-stu-id="cc6ed-135">no</span></span>        |
| [<span data-ttu-id="cc6ed-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc6ed-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cc6ed-137">no</span><span class="sxs-lookup"><span data-stu-id="cc6ed-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cc6ed-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cc6ed-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc6ed-139">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cc6ed-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





