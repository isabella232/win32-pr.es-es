---
title: ILT (SM4-ASM)
description: Comparación de tipo entero de vector de modo de componente.
ms.assetid: 5F06E568-6234-4778-8169-D8352FAB5297
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2c2e5e47272412bb483e4782e9a6c35e971293c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358471"
---
# <a name="ilt-sm4---asm"></a><span data-ttu-id="5a15a-103">ILT (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="5a15a-103">ilt (sm4 - asm)</span></span>

<span data-ttu-id="5a15a-104">Comparación de tipo entero de vector de modo de componente.</span><span class="sxs-lookup"><span data-stu-id="5a15a-104">Component-wise vector integer less-than comparison.</span></span>



| <span data-ttu-id="5a15a-105">ILT dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="5a15a-105">ilt dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="5a15a-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="5a15a-106">Item</span></span>                                                            | <span data-ttu-id="5a15a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="5a15a-107">Description</span></span>                                       |
|-----------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="5a15a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="5a15a-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="5a15a-109">Resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="5a15a-109">The result of the operation.</span></span><br/>           |
| <span data-ttu-id="5a15a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="5a15a-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="5a15a-111">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="5a15a-111">\[in\] The value to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="5a15a-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="5a15a-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="5a15a-113">\[en \] el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="5a15a-113">\[in\] The value to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a15a-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5a15a-114">Remarks</span></span>

<span data-ttu-id="5a15a-115">Realiza la comparación de enteros *(src0*  <  *SRC1*) de cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="5a15a-115">Performs the integer comparison *(src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="5a15a-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="5a15a-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="5a15a-117">De lo contrario, se devuelve 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="5a15a-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="5a15a-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="5a15a-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="5a15a-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="5a15a-119">Vertex Shader</span></span> | <span data-ttu-id="5a15a-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="5a15a-120">Geometry Shader</span></span> | <span data-ttu-id="5a15a-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="5a15a-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="5a15a-122">x</span><span class="sxs-lookup"><span data-stu-id="5a15a-122">x</span></span>             | <span data-ttu-id="5a15a-123">x</span><span class="sxs-lookup"><span data-stu-id="5a15a-123">x</span></span>               | <span data-ttu-id="5a15a-124">x</span><span class="sxs-lookup"><span data-stu-id="5a15a-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="5a15a-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="5a15a-125">Minimum Shader Model</span></span>



| <span data-ttu-id="5a15a-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="5a15a-126">Shader Model</span></span>                                              | <span data-ttu-id="5a15a-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="5a15a-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="5a15a-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="5a15a-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="5a15a-129">sí</span><span class="sxs-lookup"><span data-stu-id="5a15a-129">yes</span></span>       |
| [<span data-ttu-id="5a15a-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="5a15a-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="5a15a-131">sí</span><span class="sxs-lookup"><span data-stu-id="5a15a-131">yes</span></span>       |
| [<span data-ttu-id="5a15a-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="5a15a-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="5a15a-133">sí</span><span class="sxs-lookup"><span data-stu-id="5a15a-133">yes</span></span>       |
| [<span data-ttu-id="5a15a-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a15a-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="5a15a-135">no</span><span class="sxs-lookup"><span data-stu-id="5a15a-135">no</span></span>        |
| [<span data-ttu-id="5a15a-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a15a-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="5a15a-137">no</span><span class="sxs-lookup"><span data-stu-id="5a15a-137">no</span></span>        |
| [<span data-ttu-id="5a15a-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a15a-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="5a15a-139">no</span><span class="sxs-lookup"><span data-stu-id="5a15a-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="5a15a-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5a15a-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a15a-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="5a15a-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





