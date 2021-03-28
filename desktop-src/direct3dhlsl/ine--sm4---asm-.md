---
title: Nea (SM4-ASM)
description: Comparación de tipo entero de vector de modo de componente no equivalente.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b74a68cf4b1b3c7473f8264e8b83910f4cb0677
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996952"
---
# <a name="ine-sm4---asm"></a><span data-ttu-id="6532a-103">Nea (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6532a-103">ine (sm4 - asm)</span></span>

<span data-ttu-id="6532a-104">Comparación de tipo entero de vector de modo de componente no equivalente.</span><span class="sxs-lookup"><span data-stu-id="6532a-104">Component-wise vector integer not-equal comparison.</span></span>



| <span data-ttu-id="6532a-105">Nea dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="6532a-105">ine dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="6532a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="6532a-106">Item</span></span>                                                            | <span data-ttu-id="6532a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="6532a-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="6532a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="6532a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="6532a-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="6532a-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="6532a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="6532a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="6532a-111">\[en \] contiene el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="6532a-111">\[in\] Contains the value to compare to *src1*.</span></span><br/>    |
| <span data-ttu-id="6532a-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="6532a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="6532a-113">\[en \] contiene el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="6532a-113">\[in\] Contains the value to compare to *src0*.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="6532a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6532a-114">Remarks</span></span>

<span data-ttu-id="6532a-115">Realiza la comparación de enteros (*src0* ! = *SRC1*) de cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="6532a-115">Performs the integer comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="6532a-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="6532a-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="6532a-117">De lo contrario, se devuelve 0x0000000</span><span class="sxs-lookup"><span data-stu-id="6532a-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="6532a-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="6532a-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6532a-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="6532a-119">Vertex Shader</span></span> | <span data-ttu-id="6532a-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="6532a-120">Geometry Shader</span></span> | <span data-ttu-id="6532a-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="6532a-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6532a-122">x</span><span class="sxs-lookup"><span data-stu-id="6532a-122">x</span></span>             | <span data-ttu-id="6532a-123">x</span><span class="sxs-lookup"><span data-stu-id="6532a-123">x</span></span>               | <span data-ttu-id="6532a-124">x</span><span class="sxs-lookup"><span data-stu-id="6532a-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6532a-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="6532a-125">Minimum Shader Model</span></span>

<span data-ttu-id="6532a-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6532a-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6532a-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="6532a-127">Shader Model</span></span>                                              | <span data-ttu-id="6532a-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="6532a-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6532a-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6532a-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6532a-130">sí</span><span class="sxs-lookup"><span data-stu-id="6532a-130">yes</span></span>       |
| [<span data-ttu-id="6532a-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6532a-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6532a-132">sí</span><span class="sxs-lookup"><span data-stu-id="6532a-132">yes</span></span>       |
| [<span data-ttu-id="6532a-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6532a-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6532a-134">sí</span><span class="sxs-lookup"><span data-stu-id="6532a-134">yes</span></span>       |
| [<span data-ttu-id="6532a-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6532a-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6532a-136">no</span><span class="sxs-lookup"><span data-stu-id="6532a-136">no</span></span>        |
| [<span data-ttu-id="6532a-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6532a-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6532a-138">no</span><span class="sxs-lookup"><span data-stu-id="6532a-138">no</span></span>        |
| [<span data-ttu-id="6532a-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6532a-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6532a-140">no</span><span class="sxs-lookup"><span data-stu-id="6532a-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6532a-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6532a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6532a-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6532a-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





