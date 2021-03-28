---
title: itof (SM4-ASM)
description: Entero con signo a conversión de punto flotante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103904292"
---
# <a name="itof-sm4---asm"></a><span data-ttu-id="85419-103">itof (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="85419-103">itof (sm4 - asm)</span></span>

<span data-ttu-id="85419-104">Entero con signo a conversión de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="85419-104">Signed integer to floating point conversion.</span></span>



| <span data-ttu-id="85419-105">itof dest \[ . Mask \] , \[ - \] src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="85419-105">itof dest\[.mask\], \[-\]src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="85419-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="85419-106">Item</span></span>                                                            | <span data-ttu-id="85419-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="85419-107">Description</span></span>                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="85419-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="85419-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="85419-109">\[en \] contiene el resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="85419-109">\[in\] Contains the result of the operation.</span></span><br/> |
| <span data-ttu-id="85419-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="85419-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="85419-111">\[en \] contiene el valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="85419-111">\[in\] Contains the value to convert.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="85419-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85419-112">Remarks</span></span>

<span data-ttu-id="85419-113">En esta instrucción de conversión de entero a flotante con signo se supone que *src0* contiene un entero de 4-tupla con signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="85419-113">This signed integer-to-float conversion instruction assumes that *src0* contains a signed 32-bit integer 4-tuple.</span></span> <span data-ttu-id="85419-114">Una vez ejecutada la instrucción, *dest* contendrá una tupla de 4 puntos flotantes.</span><span class="sxs-lookup"><span data-stu-id="85419-114">After the instruction executes, *dest* will contain a floating-point 4-tuple.</span></span>

<span data-ttu-id="85419-115">La conversión se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="85419-115">The conversion is performed per-component.</span></span>

<span data-ttu-id="85419-116">Cuando un valor de entrada de tipo entero es demasiado grande para representarse exactamente en el formato de punto flotante, se recomienda encarecidamente usar el redondeo al modo par más cercano, pero no es necesario.</span><span class="sxs-lookup"><span data-stu-id="85419-116">When an integer input value is too large in magnitude to be represented exactly in the floating point format, rounding to nearest even mode is strongly recommended but not required.</span></span>

<span data-ttu-id="85419-117">El modificador opcional Negate en el operando de origen toma el complemento de 2 antes de realizar la operación aritmética.</span><span class="sxs-lookup"><span data-stu-id="85419-117">The optional negate modifier on source operand takes 2's complement before performing arithmetic operation.</span></span>

<span data-ttu-id="85419-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="85419-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="85419-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="85419-119">Vertex Shader</span></span> | <span data-ttu-id="85419-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="85419-120">Geometry Shader</span></span> | <span data-ttu-id="85419-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="85419-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="85419-122">x</span><span class="sxs-lookup"><span data-stu-id="85419-122">x</span></span>             | <span data-ttu-id="85419-123">x</span><span class="sxs-lookup"><span data-stu-id="85419-123">x</span></span>               | <span data-ttu-id="85419-124">x</span><span class="sxs-lookup"><span data-stu-id="85419-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="85419-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="85419-125">Minimum Shader Model</span></span>

<span data-ttu-id="85419-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="85419-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="85419-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="85419-127">Shader Model</span></span>                                              | <span data-ttu-id="85419-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="85419-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="85419-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="85419-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="85419-130">sí</span><span class="sxs-lookup"><span data-stu-id="85419-130">yes</span></span>       |
| [<span data-ttu-id="85419-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="85419-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="85419-132">sí</span><span class="sxs-lookup"><span data-stu-id="85419-132">yes</span></span>       |
| [<span data-ttu-id="85419-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="85419-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="85419-134">sí</span><span class="sxs-lookup"><span data-stu-id="85419-134">yes</span></span>       |
| [<span data-ttu-id="85419-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85419-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="85419-136">no</span><span class="sxs-lookup"><span data-stu-id="85419-136">no</span></span>        |
| [<span data-ttu-id="85419-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85419-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="85419-138">no</span><span class="sxs-lookup"><span data-stu-id="85419-138">no</span></span>        |
| [<span data-ttu-id="85419-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85419-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="85419-140">no</span><span class="sxs-lookup"><span data-stu-id="85419-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="85419-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="85419-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85419-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="85419-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





