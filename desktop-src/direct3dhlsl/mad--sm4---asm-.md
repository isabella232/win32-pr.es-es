---
title: Mad (SM4-ASM)
description: Agregar multiplicación por componentes.
ms.assetid: 1C24AF49-AA32-4D3A-8478-C9BAC4FE7D77
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d34823cdb3545f29426117b35903c97c08c5807
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077081"
---
# <a name="mad-sm4---asm"></a><span data-ttu-id="13755-103">Mad (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="13755-103">mad (sm4 - asm)</span></span>

<span data-ttu-id="13755-104">Multiplicar por componentes & agregar.</span><span class="sxs-lookup"><span data-stu-id="13755-104">Component-wise multiply & add.</span></span>



| <span data-ttu-id="13755-105">: Mad \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="13755-105">:mad\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\], \[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="13755-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="13755-106">Item</span></span>                                                            | <span data-ttu-id="13755-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="13755-107">Description</span></span>                                                                                  |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13755-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="13755-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="13755-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="13755-109">\[in\] The result of the operation.</span></span><br/> <span data-ttu-id="13755-110">*dest*  =  *src0* \* *SRC1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="13755-110">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="13755-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="13755-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="13755-112">\[en \] multiplicando.</span><span class="sxs-lookup"><span data-stu-id="13755-112">\[in\] The multiplicand.</span></span><br/>                                                          |
| <span data-ttu-id="13755-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="13755-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="13755-114">\[en \] el multiplicador.</span><span class="sxs-lookup"><span data-stu-id="13755-114">\[in\] The multiplier.</span></span><br/>                                                            |
| <span data-ttu-id="13755-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="13755-115"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="13755-116">\[en \] addend.</span><span class="sxs-lookup"><span data-stu-id="13755-116">\[in\] The addend.</span></span><br/>                                                                |



 

## <a name="remarks"></a><span data-ttu-id="13755-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="13755-117">Remarks</span></span>

<span data-ttu-id="13755-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="13755-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="13755-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="13755-119">Vertex Shader</span></span> | <span data-ttu-id="13755-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="13755-120">Geometry Shader</span></span> | <span data-ttu-id="13755-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="13755-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="13755-122">x</span><span class="sxs-lookup"><span data-stu-id="13755-122">x</span></span>             | <span data-ttu-id="13755-123">x</span><span class="sxs-lookup"><span data-stu-id="13755-123">x</span></span>               | <span data-ttu-id="13755-124">x</span><span class="sxs-lookup"><span data-stu-id="13755-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="13755-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="13755-125">Minimum Shader Model</span></span>

<span data-ttu-id="13755-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="13755-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="13755-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="13755-127">Shader Model</span></span>                                              | <span data-ttu-id="13755-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="13755-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="13755-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="13755-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="13755-130">sí</span><span class="sxs-lookup"><span data-stu-id="13755-130">yes</span></span>       |
| [<span data-ttu-id="13755-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="13755-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="13755-132">sí</span><span class="sxs-lookup"><span data-stu-id="13755-132">yes</span></span>       |
| [<span data-ttu-id="13755-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="13755-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="13755-134">sí</span><span class="sxs-lookup"><span data-stu-id="13755-134">yes</span></span>       |
| [<span data-ttu-id="13755-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13755-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="13755-136">no</span><span class="sxs-lookup"><span data-stu-id="13755-136">no</span></span>        |
| [<span data-ttu-id="13755-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13755-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="13755-138">no</span><span class="sxs-lookup"><span data-stu-id="13755-138">no</span></span>        |
| [<span data-ttu-id="13755-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13755-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="13755-140">no</span><span class="sxs-lookup"><span data-stu-id="13755-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="13755-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="13755-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13755-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="13755-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





