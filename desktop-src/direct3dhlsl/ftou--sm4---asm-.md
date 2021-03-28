---
title: ftou (SM4-ASM)
description: Conversión de punto flotante a entero sin signo.
ms.assetid: 0E3E090B-72C0-4CED-AFA5-2DDCF67D7263
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4a5e65e4bb9d4e71e4a2000f00861cf63e7c181
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358475"
---
# <a name="ftou-sm4---asm"></a><span data-ttu-id="3b290-103">ftou (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="3b290-103">ftou (sm4 - asm)</span></span>

<span data-ttu-id="3b290-104">Conversión de punto flotante a entero sin signo.</span><span class="sxs-lookup"><span data-stu-id="3b290-104">Floating point to unsigned integer conversion.</span></span>



| <span data-ttu-id="3b290-105">ftou dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3b290-105">ftou dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="3b290-106">ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="3b290-106">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------|



 



| <span data-ttu-id="3b290-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="3b290-107">Item</span></span>                                                            | <span data-ttu-id="3b290-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="3b290-108">Description</span></span>                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="3b290-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="3b290-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="3b290-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="3b290-110">\[in\] The address of the result of the operation.</span></span> <br/> |
| <span data-ttu-id="3b290-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="3b290-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="3b290-112">\[en \] el valor que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="3b290-112">\[in\] The value to convert.</span></span><br/>                        |



 

## <a name="remarks"></a><span data-ttu-id="3b290-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="3b290-113">Remarks</span></span>

<span data-ttu-id="3b290-114">La conversión se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="3b290-114">The conversion is performed per-component.</span></span> <span data-ttu-id="3b290-115">El redondeo siempre se realiza hacia cero, siguiendo la Convención de C para las conversiones de Float a int.</span><span class="sxs-lookup"><span data-stu-id="3b290-115">Rounding is always performed towards zero, following the C convention for casts from float to int.</span></span>

<span data-ttu-id="3b290-116">Las aplicaciones que requieren una semántica de redondeo diferente pueden invocar las instrucciones **Round** antes de la conversión a un entero.</span><span class="sxs-lookup"><span data-stu-id="3b290-116">Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="3b290-117">Las entradas se fijan en el intervalo \[ 0.0 f... 4294967295.999 f \] antes de la conversión y los valores Nan de entrada producen un resultado cero.</span><span class="sxs-lookup"><span data-stu-id="3b290-117">Inputs are clamped to the range \[0.0f ... 4294967295.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="3b290-118">Los modificadores de valor absoluto y de negación opcionales se aplican a los valores de origen antes de la conversión.</span><span class="sxs-lookup"><span data-stu-id="3b290-118">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="3b290-119">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="3b290-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="3b290-120">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="3b290-120">Vertex Shader</span></span> | <span data-ttu-id="3b290-121">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="3b290-121">Geometry Shader</span></span> | <span data-ttu-id="3b290-122">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="3b290-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="3b290-123">x</span><span class="sxs-lookup"><span data-stu-id="3b290-123">x</span></span>             | <span data-ttu-id="3b290-124">x</span><span class="sxs-lookup"><span data-stu-id="3b290-124">x</span></span>               | <span data-ttu-id="3b290-125">x</span><span class="sxs-lookup"><span data-stu-id="3b290-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="3b290-126">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="3b290-126">Minimum Shader Model</span></span>

<span data-ttu-id="3b290-127">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3b290-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3b290-128">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="3b290-128">Shader Model</span></span>                                              | <span data-ttu-id="3b290-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="3b290-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="3b290-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3b290-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="3b290-131">sí</span><span class="sxs-lookup"><span data-stu-id="3b290-131">yes</span></span>       |
| [<span data-ttu-id="3b290-132">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="3b290-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="3b290-133">sí</span><span class="sxs-lookup"><span data-stu-id="3b290-133">yes</span></span>       |
| [<span data-ttu-id="3b290-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="3b290-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="3b290-135">sí</span><span class="sxs-lookup"><span data-stu-id="3b290-135">yes</span></span>       |
| [<span data-ttu-id="3b290-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b290-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="3b290-137">no</span><span class="sxs-lookup"><span data-stu-id="3b290-137">no</span></span>        |
| [<span data-ttu-id="3b290-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b290-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="3b290-139">no</span><span class="sxs-lookup"><span data-stu-id="3b290-139">no</span></span>        |
| [<span data-ttu-id="3b290-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b290-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="3b290-141">no</span><span class="sxs-lookup"><span data-stu-id="3b290-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="3b290-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b290-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b290-143">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="3b290-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





