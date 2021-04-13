---
title: NE (SM4-ASM)
description: Comparación de punto flotante de vector de modo de componente no equivalente.
ms.assetid: 5BED97D3-8FF6-4F1C-819B-DC8B4A4F2CCA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e53ff726047bd1870e6c836f4508bdf87001b3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419933"
---
# <a name="ne-sm4---asm"></a><span data-ttu-id="2d05e-103">NE (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2d05e-103">ne (sm4 - asm)</span></span>

<span data-ttu-id="2d05e-104">Comparación de punto flotante de vector de modo de componente no equivalente.</span><span class="sxs-lookup"><span data-stu-id="2d05e-104">Component-wise vector floating point not-equal comparison.</span></span>



| <span data-ttu-id="2d05e-105">NE dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] SRC1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="2d05e-105">ne dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="2d05e-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="2d05e-106">Item</span></span>                                                            | <span data-ttu-id="2d05e-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="2d05e-107">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="2d05e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="2d05e-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="2d05e-109">\[en \] el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="2d05e-109">\[in\] The result of the operation.</span></span><br/>         |
| <span data-ttu-id="2d05e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="2d05e-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="2d05e-111">\[en \] los componentes que se van a comparar con *SRC1*.</span><span class="sxs-lookup"><span data-stu-id="2d05e-111">\[in\] The components to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="2d05e-112"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="2d05e-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="2d05e-113">\[en \] los componentes que se van a comparar con *src0*.</span><span class="sxs-lookup"><span data-stu-id="2d05e-113">\[in\] The components to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2d05e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2d05e-114">Remarks</span></span>

<span data-ttu-id="2d05e-115">Esta instrucción realiza la comparación Float (*src0* ! = *SRC1*) de cada componente y escribe el resultado en *dest*.</span><span class="sxs-lookup"><span data-stu-id="2d05e-115">This instruction performs the float comparison (*src0* != *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="2d05e-116">Si la comparación es true, se devuelve 0xFFFFFFFF para ese componente.</span><span class="sxs-lookup"><span data-stu-id="2d05e-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="2d05e-117">De lo contrario, se devuelve 0x0000000.</span><span class="sxs-lookup"><span data-stu-id="2d05e-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="2d05e-118">Las desnormaciones se vacían antes de la comparación con los registros de origen originales intactos.</span><span class="sxs-lookup"><span data-stu-id="2d05e-118">Denorms are flushed before comparison with original source registers untouched.</span></span>

<span data-ttu-id="2d05e-119">+ 0 es igual a-0.</span><span class="sxs-lookup"><span data-stu-id="2d05e-119">+0 equals -0.</span></span>

<span data-ttu-id="2d05e-120">La comparación con NaN devuelve true.</span><span class="sxs-lookup"><span data-stu-id="2d05e-120">Comparison with NaN returns true.</span></span>

<span data-ttu-id="2d05e-121">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2d05e-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2d05e-122">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2d05e-122">Vertex Shader</span></span> | <span data-ttu-id="2d05e-123">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="2d05e-123">Geometry Shader</span></span> | <span data-ttu-id="2d05e-124">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2d05e-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2d05e-125">x</span><span class="sxs-lookup"><span data-stu-id="2d05e-125">x</span></span>             | <span data-ttu-id="2d05e-126">x</span><span class="sxs-lookup"><span data-stu-id="2d05e-126">x</span></span>               | <span data-ttu-id="2d05e-127">x</span><span class="sxs-lookup"><span data-stu-id="2d05e-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2d05e-128">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2d05e-128">Minimum Shader Model</span></span>

<span data-ttu-id="2d05e-129">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2d05e-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2d05e-130">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2d05e-130">Shader Model</span></span>                                              | <span data-ttu-id="2d05e-131">Compatible</span><span class="sxs-lookup"><span data-stu-id="2d05e-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2d05e-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2d05e-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2d05e-133">sí</span><span class="sxs-lookup"><span data-stu-id="2d05e-133">yes</span></span>       |
| [<span data-ttu-id="2d05e-134">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2d05e-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2d05e-135">sí</span><span class="sxs-lookup"><span data-stu-id="2d05e-135">yes</span></span>       |
| [<span data-ttu-id="2d05e-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2d05e-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2d05e-137">sí</span><span class="sxs-lookup"><span data-stu-id="2d05e-137">yes</span></span>       |
| [<span data-ttu-id="2d05e-138">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d05e-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2d05e-139">no</span><span class="sxs-lookup"><span data-stu-id="2d05e-139">no</span></span>        |
| [<span data-ttu-id="2d05e-140">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d05e-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2d05e-141">no</span><span class="sxs-lookup"><span data-stu-id="2d05e-141">no</span></span>        |
| [<span data-ttu-id="2d05e-142">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d05e-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2d05e-143">no</span><span class="sxs-lookup"><span data-stu-id="2d05e-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2d05e-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2d05e-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d05e-145">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2d05e-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





