---
title: lt (SM4-ASM)
description: Comparación de punto flotante de vector de modo de componente.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67a727987e4eaee017137d62dbe12f8581540876
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358485"
---
# <a name="lt-sm4---asm"></a><span data-ttu-id="ee510-103">lt (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ee510-103">lt (sm4 - asm)</span></span>

<span data-ttu-id="ee510-104">Comparación de punto flotante de vector de modo de componente.</span><span class="sxs-lookup"><span data-stu-id="ee510-104">Component-wise vector floating point less-than comparison.</span></span>



| <span data-ttu-id="ee510-105">lt dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ee510-105">lt dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="ee510-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="ee510-106">Item</span></span>                                                            | <span data-ttu-id="ee510-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="ee510-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="ee510-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ee510-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ee510-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="ee510-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="ee510-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ee510-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ee510-111">\[en \] el valor que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="ee510-111">\[in\] The value to compare to *src1*.</span></span><br/>             |
| <span data-ttu-id="ee510-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="ee510-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ee510-113">\[en \] el valor que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="ee510-113">\[in\] The value to compare to *src0*.</span></span><br/>             |



 

## <a name="remarks"></a><span data-ttu-id="ee510-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ee510-114">Remarks</span></span>

<span data-ttu-id="ee510-115">Esta instrucción realiza la comparación Float (*src0*  <  *SRC1*) de cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="ee510-115">This instruction performs the float comparison (*src0* < *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="ee510-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="ee510-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="ee510-117">De lo contrario, se devuelve 0x0000000</span><span class="sxs-lookup"><span data-stu-id="ee510-117">Otherwise 0x0000000 is returned</span></span>

<span data-ttu-id="ee510-118">Las desnormaciones se vacían antes de la comparación; los registros de origen originales no se tocan.</span><span class="sxs-lookup"><span data-stu-id="ee510-118">Denorms are flushed before comparison; original source registers are untouched.</span></span>

<span data-ttu-id="ee510-119">+ 0 es igual a-0.</span><span class="sxs-lookup"><span data-stu-id="ee510-119">+0 equals -0.</span></span>

<span data-ttu-id="ee510-120">La comparación con NaN devuelve false.</span><span class="sxs-lookup"><span data-stu-id="ee510-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="ee510-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ee510-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ee510-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ee510-122">Vertex Shader</span></span> | <span data-ttu-id="ee510-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ee510-123">Geometry Shader</span></span> | <span data-ttu-id="ee510-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ee510-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ee510-125">x</span><span class="sxs-lookup"><span data-stu-id="ee510-125">x</span></span>             | <span data-ttu-id="ee510-126">x</span><span class="sxs-lookup"><span data-stu-id="ee510-126">x</span></span>               | <span data-ttu-id="ee510-127">x</span><span class="sxs-lookup"><span data-stu-id="ee510-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ee510-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ee510-128">Minimum Shader Model</span></span>

<span data-ttu-id="ee510-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ee510-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ee510-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ee510-130">Shader Model</span></span>                                              | <span data-ttu-id="ee510-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="ee510-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ee510-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ee510-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ee510-133">sí</span><span class="sxs-lookup"><span data-stu-id="ee510-133">yes</span></span>       |
| [<span data-ttu-id="ee510-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ee510-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ee510-135">sí</span><span class="sxs-lookup"><span data-stu-id="ee510-135">yes</span></span>       |
| [<span data-ttu-id="ee510-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ee510-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ee510-137">sí</span><span class="sxs-lookup"><span data-stu-id="ee510-137">yes</span></span>       |
| [<span data-ttu-id="ee510-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee510-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ee510-139">no</span><span class="sxs-lookup"><span data-stu-id="ee510-139">no</span></span>        |
| [<span data-ttu-id="ee510-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee510-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ee510-141">no</span><span class="sxs-lookup"><span data-stu-id="ee510-141">no</span></span>        |
| [<span data-ttu-id="ee510-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee510-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ee510-143">no</span><span class="sxs-lookup"><span data-stu-id="ee510-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ee510-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee510-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee510-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ee510-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





