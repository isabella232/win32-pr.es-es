---
title: iEQ (SM4-ASM)
description: Comparación de igualdad de entero de vector de modo de componente.
ms.assetid: AD010554-80DC-4D2D-B04C-2638276DDC34
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 579a47ffe38b8322b748f6ba64ce9bbbc26a5bd9
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996953"
---
# <a name="ieq-sm4---asm"></a><span data-ttu-id="60a55-103">iEQ (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="60a55-103">ieq (sm4 - asm)</span></span>

<span data-ttu-id="60a55-104">Comparación de igualdad de entero de vector de modo de componente.</span><span class="sxs-lookup"><span data-stu-id="60a55-104">Component-wise vector integer equality comparison.</span></span>



| <span data-ttu-id="60a55-105">dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="60a55-105">dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|---------------------------------------------------|



 



| <span data-ttu-id="60a55-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="60a55-106">Item</span></span>                                                            | <span data-ttu-id="60a55-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="60a55-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="60a55-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="60a55-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="60a55-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="60a55-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="60a55-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="60a55-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="60a55-111">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="60a55-111">\[in\] The value to compare with *src1*.</span></span><br/>           |
| <span data-ttu-id="60a55-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="60a55-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="60a55-113">\[en \] el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="60a55-113">\[in\] The value to compare with *src0*.</span></span><br/>           |



 

## <a name="remarks"></a><span data-ttu-id="60a55-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="60a55-114">Remarks</span></span>

<span data-ttu-id="60a55-115">Esta instrucción realiza la comparación de enteros (*src0*  ==  *SRC1*) para cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="60a55-115">This instruction performs the integer comparison (*src0* == *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="60a55-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="60a55-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="60a55-117">De lo contrario, se devuelve 0x0000000</span><span class="sxs-lookup"><span data-stu-id="60a55-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="60a55-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="60a55-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="60a55-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="60a55-119">Vertex Shader</span></span> | <span data-ttu-id="60a55-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="60a55-120">Geometry Shader</span></span> | <span data-ttu-id="60a55-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="60a55-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="60a55-122">x</span><span class="sxs-lookup"><span data-stu-id="60a55-122">x</span></span>             | <span data-ttu-id="60a55-123">x</span><span class="sxs-lookup"><span data-stu-id="60a55-123">x</span></span>               | <span data-ttu-id="60a55-124">x</span><span class="sxs-lookup"><span data-stu-id="60a55-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="60a55-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="60a55-125">Minimum Shader Model</span></span>

<span data-ttu-id="60a55-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="60a55-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="60a55-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="60a55-127">Shader Model</span></span>                                              | <span data-ttu-id="60a55-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="60a55-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="60a55-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="60a55-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="60a55-130">sí</span><span class="sxs-lookup"><span data-stu-id="60a55-130">yes</span></span>       |
| [<span data-ttu-id="60a55-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="60a55-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="60a55-132">sí</span><span class="sxs-lookup"><span data-stu-id="60a55-132">yes</span></span>       |
| [<span data-ttu-id="60a55-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="60a55-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="60a55-134">sí</span><span class="sxs-lookup"><span data-stu-id="60a55-134">yes</span></span>       |
| [<span data-ttu-id="60a55-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60a55-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="60a55-136">no</span><span class="sxs-lookup"><span data-stu-id="60a55-136">no</span></span>        |
| [<span data-ttu-id="60a55-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60a55-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="60a55-138">no</span><span class="sxs-lookup"><span data-stu-id="60a55-138">no</span></span>        |
| [<span data-ttu-id="60a55-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60a55-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="60a55-140">no</span><span class="sxs-lookup"><span data-stu-id="60a55-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="60a55-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="60a55-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60a55-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="60a55-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





