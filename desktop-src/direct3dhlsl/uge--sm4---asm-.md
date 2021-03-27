---
title: UGE (SM4-ASM)
description: Comparación de entero sin signo de vector de modo de componente con comparación mayor o igual que.
ms.assetid: CA8E19EC-619F-4C19-B6FD-91650B5DAF9F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4aecd9e39aa94c69acefff0f6a0fdf843cec5d8
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904284"
---
# <a name="uge-sm4---asm"></a><span data-ttu-id="6ae95-103">UGE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6ae95-103">uge (sm4 - asm)</span></span>

<span data-ttu-id="6ae95-104">Comparación de entero sin signo de vector de modo de componente con comparación mayor o igual que.</span><span class="sxs-lookup"><span data-stu-id="6ae95-104">Component-wise vector unsigned integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="6ae95-105">UGE dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6ae95-105">uge dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="6ae95-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6ae95-106">Item</span></span>                                                            | <span data-ttu-id="6ae95-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae95-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6ae95-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6ae95-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6ae95-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6ae95-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="6ae95-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6ae95-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6ae95-111">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="6ae95-111">\[in\] The components to compare to *src1*.</span></span><br/>        |
| <span data-ttu-id="6ae95-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="6ae95-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6ae95-113">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="6ae95-113">\[in\] The components to compare to *src0*.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="6ae95-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ae95-114">Remarks</span></span>

<span data-ttu-id="6ae95-115">Esta instrucción realiza la comparación de enteros sin signo (*src0*  >=  *SRC1*) para cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="6ae95-115">This instruction performs the unsigned integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="6ae95-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="6ae95-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="6ae95-117">De lo contrario, se devuelve 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="6ae95-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="6ae95-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="6ae95-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6ae95-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="6ae95-119">Vertex Shader</span></span> | <span data-ttu-id="6ae95-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="6ae95-120">Geometry Shader</span></span> | <span data-ttu-id="6ae95-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="6ae95-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6ae95-122">x</span><span class="sxs-lookup"><span data-stu-id="6ae95-122">x</span></span>             | <span data-ttu-id="6ae95-123">x</span><span class="sxs-lookup"><span data-stu-id="6ae95-123">x</span></span>               | <span data-ttu-id="6ae95-124">x</span><span class="sxs-lookup"><span data-stu-id="6ae95-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6ae95-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6ae95-125">Minimum Shader Model</span></span>

<span data-ttu-id="6ae95-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6ae95-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6ae95-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6ae95-127">Shader Model</span></span>                                              | <span data-ttu-id="6ae95-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="6ae95-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6ae95-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6ae95-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6ae95-130">sí</span><span class="sxs-lookup"><span data-stu-id="6ae95-130">yes</span></span>       |
| [<span data-ttu-id="6ae95-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6ae95-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6ae95-132">sí</span><span class="sxs-lookup"><span data-stu-id="6ae95-132">yes</span></span>       |
| [<span data-ttu-id="6ae95-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6ae95-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6ae95-134">sí</span><span class="sxs-lookup"><span data-stu-id="6ae95-134">yes</span></span>       |
| [<span data-ttu-id="6ae95-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae95-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6ae95-136">no</span><span class="sxs-lookup"><span data-stu-id="6ae95-136">no</span></span>        |
| [<span data-ttu-id="6ae95-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae95-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6ae95-138">no</span><span class="sxs-lookup"><span data-stu-id="6ae95-138">no</span></span>        |
| [<span data-ttu-id="6ae95-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae95-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6ae95-140">no</span><span class="sxs-lookup"><span data-stu-id="6ae95-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6ae95-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6ae95-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ae95-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6ae95-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





