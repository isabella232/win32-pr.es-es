---
title: ULT (SM4-ASM)
description: Comparación de entero sin signo de vector de modo de componente y menor que.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 624c09d182e9ecfd4d1b603f6fd2c34b83d768ed
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996884"
---
# <a name="ult-sm4---asm"></a><span data-ttu-id="144e1-103">ULT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="144e1-103">ult (sm4 - asm)</span></span>

<span data-ttu-id="144e1-104">Comparación de entero sin signo de vector de modo de componente y menor que.</span><span class="sxs-lookup"><span data-stu-id="144e1-104">Component-wise vector unsigned integer less-than comparison.</span></span>



| <span data-ttu-id="144e1-105">ULT dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="144e1-105">ult dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="144e1-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="144e1-106">Item</span></span>                                                            | <span data-ttu-id="144e1-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="144e1-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="144e1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="144e1-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="144e1-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="144e1-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="144e1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="144e1-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="144e1-111">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="144e1-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="144e1-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="144e1-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="144e1-113">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="144e1-113">\[in\] The value to compare to *src1*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="144e1-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="144e1-114">Remarks</span></span>

<span data-ttu-id="144e1-115">Realiza la comparación de enteros sin signo (*src0*  <  *SRC1*) para cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="144e1-115">Performs the unsigned integer comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="144e1-116">Si la comparación es true, esta instrucción devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="144e1-116">If the comparison is true, this instruction returns 0xFFFFFFFF for that component.</span></span> <span data-ttu-id="144e1-117">De lo contrario, devuelve 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="144e1-117">Otherwise it returns 0x0000000.</span></span>

<span data-ttu-id="144e1-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="144e1-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="144e1-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="144e1-119">Vertex Shader</span></span> | <span data-ttu-id="144e1-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="144e1-120">Geometry Shader</span></span> | <span data-ttu-id="144e1-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="144e1-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="144e1-122">x</span><span class="sxs-lookup"><span data-stu-id="144e1-122">x</span></span>             | <span data-ttu-id="144e1-123">x</span><span class="sxs-lookup"><span data-stu-id="144e1-123">x</span></span>               | <span data-ttu-id="144e1-124">x</span><span class="sxs-lookup"><span data-stu-id="144e1-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="144e1-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="144e1-125">Minimum Shader Model</span></span>

<span data-ttu-id="144e1-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="144e1-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="144e1-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="144e1-127">Shader Model</span></span>                                              | <span data-ttu-id="144e1-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="144e1-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="144e1-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="144e1-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="144e1-130">sí</span><span class="sxs-lookup"><span data-stu-id="144e1-130">yes</span></span>       |
| [<span data-ttu-id="144e1-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="144e1-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="144e1-132">sí</span><span class="sxs-lookup"><span data-stu-id="144e1-132">yes</span></span>       |
| [<span data-ttu-id="144e1-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="144e1-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="144e1-134">sí</span><span class="sxs-lookup"><span data-stu-id="144e1-134">yes</span></span>       |
| [<span data-ttu-id="144e1-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="144e1-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="144e1-136">no</span><span class="sxs-lookup"><span data-stu-id="144e1-136">no</span></span>        |
| [<span data-ttu-id="144e1-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="144e1-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="144e1-138">no</span><span class="sxs-lookup"><span data-stu-id="144e1-138">no</span></span>        |
| [<span data-ttu-id="144e1-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="144e1-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="144e1-140">no</span><span class="sxs-lookup"><span data-stu-id="144e1-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="144e1-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="144e1-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="144e1-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="144e1-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





