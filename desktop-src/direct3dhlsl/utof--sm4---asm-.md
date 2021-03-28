---
title: utof (SM4-ASM)
description: Entero sin signo para conversión de punto flotante.
ms.assetid: 5A52C959-7B4C-4FA1-B29C-BCAF448419F8
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9283857df12a85819f0d191d13450e0311fdade
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077126"
---
# <a name="utof-sm4---asm"></a><span data-ttu-id="06073-103">utof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="06073-103">utof (sm4 - asm)</span></span>

<span data-ttu-id="06073-104">Entero sin signo para conversión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="06073-104">Unsigned integer to floating point conversion.</span></span>



| <span data-ttu-id="06073-105">utof dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="06073-105">utof dest\[.mask\], src0\[.swizzle\]</span></span> |
|--------------------------------------|



 



| <span data-ttu-id="06073-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="06073-106">Item</span></span>                                                            | <span data-ttu-id="06073-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="06073-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="06073-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="06073-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="06073-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="06073-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="06073-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="06073-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="06073-111">\[en \] los componentes que se van a convertir.</span><span class="sxs-lookup"><span data-stu-id="06073-111">\[in\] The components to convert.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="06073-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06073-112">Remarks</span></span>

<span data-ttu-id="06073-113">*src0* debe contener un entero de una tupla de 4 bits 32 sin signo.</span><span class="sxs-lookup"><span data-stu-id="06073-113">*src0* must contain an unsigned 32-bit integer 4-tuple.</span></span> <span data-ttu-id="06073-114">Una vez ejecutada la instrucción, *dest* contendrá una tupla de 4 puntos flotantes.</span><span class="sxs-lookup"><span data-stu-id="06073-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span> <span data-ttu-id="06073-115">La conversión se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="06073-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="06073-116">Cuando un valor de entrada de tipo entero es demasiado grande para representarlo exactamente en el formato de punto flotante, se redondea al modo uniforme más cercano.</span><span class="sxs-lookup"><span data-stu-id="06073-116">When an integer input value is too large to be represented exactly in the floating point format, round to nearest even mode.</span></span>

<span data-ttu-id="06073-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="06073-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="06073-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="06073-118">Vertex Shader</span></span> | <span data-ttu-id="06073-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="06073-119">Geometry Shader</span></span> | <span data-ttu-id="06073-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="06073-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="06073-121">x</span><span class="sxs-lookup"><span data-stu-id="06073-121">x</span></span>             | <span data-ttu-id="06073-122">x</span><span class="sxs-lookup"><span data-stu-id="06073-122">x</span></span>               | <span data-ttu-id="06073-123">x</span><span class="sxs-lookup"><span data-stu-id="06073-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="06073-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="06073-124">Minimum Shader Model</span></span>

<span data-ttu-id="06073-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="06073-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="06073-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="06073-126">Shader Model</span></span>                                              | <span data-ttu-id="06073-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="06073-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="06073-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="06073-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="06073-129">sí</span><span class="sxs-lookup"><span data-stu-id="06073-129">yes</span></span>       |
| [<span data-ttu-id="06073-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="06073-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="06073-131">sí</span><span class="sxs-lookup"><span data-stu-id="06073-131">yes</span></span>       |
| [<span data-ttu-id="06073-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="06073-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="06073-133">sí</span><span class="sxs-lookup"><span data-stu-id="06073-133">yes</span></span>       |
| [<span data-ttu-id="06073-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06073-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="06073-135">no</span><span class="sxs-lookup"><span data-stu-id="06073-135">no</span></span>        |
| [<span data-ttu-id="06073-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06073-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="06073-137">no</span><span class="sxs-lookup"><span data-stu-id="06073-137">no</span></span>        |
| [<span data-ttu-id="06073-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06073-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="06073-139">no</span><span class="sxs-lookup"><span data-stu-id="06073-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="06073-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="06073-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06073-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="06073-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





