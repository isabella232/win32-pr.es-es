---
title: GE (SM4-ASM)
description: Comparación mayor o igual de punto flotante de vector de modo de componente.
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419913"
---
# <a name="ge-sm4---asm"></a><span data-ttu-id="d686f-103">GE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="d686f-103">ge (sm4 - asm)</span></span>

<span data-ttu-id="d686f-104">Comparación mayor o igual de punto flotante de vector de modo de componente.</span><span class="sxs-lookup"><span data-stu-id="d686f-104">Component-wise vector floating point greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="d686f-105">GE dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="d686f-105">ge dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="d686f-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="d686f-106">Item</span></span>                                                            | <span data-ttu-id="d686f-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="d686f-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="d686f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="d686f-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="d686f-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="d686f-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="d686f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="d686f-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="d686f-111">\[en \] el componente que se va a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="d686f-111">\[in\] The component to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="d686f-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="d686f-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="d686f-113">\[en \] el componente que se va a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="d686f-113">\[in\] The component to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d686f-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d686f-114">Remarks</span></span>

<span data-ttu-id="d686f-115">Realiza la comparación de punto flotante (*src0*  >=  *SRC1*) de cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="d686f-115">Performs the float comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="d686f-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="d686f-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="d686f-117">De lo contrario, se devuelve 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="d686f-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="d686f-118">Las desnormaciones se vacían antes de la comparación y los registros de origen originales no se tocan.</span><span class="sxs-lookup"><span data-stu-id="d686f-118">Denorms are flushed before comparison, and original source registers are untouched.</span></span> <span data-ttu-id="d686f-119">+ 0 es igual a-0.</span><span class="sxs-lookup"><span data-stu-id="d686f-119">+0 equals -0.</span></span> <span data-ttu-id="d686f-120">La comparación con NaN devuelve false.</span><span class="sxs-lookup"><span data-stu-id="d686f-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="d686f-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="d686f-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="d686f-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="d686f-122">Vertex Shader</span></span> | <span data-ttu-id="d686f-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="d686f-123">Geometry Shader</span></span> | <span data-ttu-id="d686f-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="d686f-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="d686f-125">x</span><span class="sxs-lookup"><span data-stu-id="d686f-125">x</span></span>             | <span data-ttu-id="d686f-126">x</span><span class="sxs-lookup"><span data-stu-id="d686f-126">x</span></span>               | <span data-ttu-id="d686f-127">x</span><span class="sxs-lookup"><span data-stu-id="d686f-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="d686f-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d686f-128">Minimum Shader Model</span></span>

<span data-ttu-id="d686f-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d686f-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d686f-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d686f-130">Shader Model</span></span>                                              | <span data-ttu-id="d686f-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="d686f-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="d686f-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d686f-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="d686f-133">sí</span><span class="sxs-lookup"><span data-stu-id="d686f-133">yes</span></span>       |
| [<span data-ttu-id="d686f-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="d686f-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="d686f-135">sí</span><span class="sxs-lookup"><span data-stu-id="d686f-135">yes</span></span>       |
| [<span data-ttu-id="d686f-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="d686f-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="d686f-137">sí</span><span class="sxs-lookup"><span data-stu-id="d686f-137">yes</span></span>       |
| [<span data-ttu-id="d686f-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d686f-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="d686f-139">no</span><span class="sxs-lookup"><span data-stu-id="d686f-139">no</span></span>        |
| [<span data-ttu-id="d686f-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d686f-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="d686f-141">no</span><span class="sxs-lookup"><span data-stu-id="d686f-141">no</span></span>        |
| [<span data-ttu-id="d686f-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d686f-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="d686f-143">no</span><span class="sxs-lookup"><span data-stu-id="d686f-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="d686f-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d686f-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d686f-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="d686f-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





