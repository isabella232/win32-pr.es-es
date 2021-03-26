---
title: 'ftoi (sm4 - asm) '
description: Punto flotante a conversión de enteros con signo.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/17/2020
ms.locfileid: "104359485"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="e0cbc-103">ftoi (sm4 - asm) </span><span class="sxs-lookup"><span data-stu-id="e0cbc-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="e0cbc-104">Punto flotante a conversión de enteros con signo.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="e0cbc-105">ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="e0cbc-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="e0cbc-106">Elemento</span><span class="sxs-lookup"><span data-stu-id="e0cbc-106">Item</span></span> | <span data-ttu-id="e0cbc-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="e0cbc-107">Description</span></span> |
|-|-|
| <span data-ttu-id="e0cbc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="e0cbc-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="e0cbc-109">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="e0cbc-110">*dest*  =  [Round \_ z](round-z--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="e0cbc-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="e0cbc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e0cbc-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e0cbc-112">\[en \] el componente que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="e0cbc-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e0cbc-113">Remarks</span></span>

<span data-ttu-id="e0cbc-114">La conversión se realiza por componente.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-114">The conversion is performed per component.</span></span> <span data-ttu-id="e0cbc-115">El redondeo siempre se realiza hacia cero, siguiendo la Convención de C para las conversiones de Float a int. Las aplicaciones que requieren una semántica de redondeo diferente pueden invocar las instrucciones **Round** antes de la conversión a un entero.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="e0cbc-116">Las entradas se fijan en el intervalo \[ -2147483648.999 f... 2147483647.999 f \] antes de la conversión y los valores Nan de entrada producen un resultado cero.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="e0cbc-117">Los modificadores de valor absoluto y de negación opcionales se aplican a los valores de origen antes de la conversión.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="e0cbc-118">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e0cbc-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="e0cbc-119">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="e0cbc-119">Vertex Shader</span></span> | <span data-ttu-id="e0cbc-120">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="e0cbc-120">Geometry Shader</span></span> | <span data-ttu-id="e0cbc-121">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e0cbc-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="e0cbc-122">x</span><span class="sxs-lookup"><span data-stu-id="e0cbc-122">x</span></span> | <span data-ttu-id="e0cbc-123">x</span><span class="sxs-lookup"><span data-stu-id="e0cbc-123">x</span></span> | <span data-ttu-id="e0cbc-124">x</span><span class="sxs-lookup"><span data-stu-id="e0cbc-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="e0cbc-125">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e0cbc-125">Minimum Shader Model</span></span>

<span data-ttu-id="e0cbc-126">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e0cbc-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="e0cbc-127">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e0cbc-127">Shader Model</span></span> | <span data-ttu-id="e0cbc-128">Compatible</span><span class="sxs-lookup"><span data-stu-id="e0cbc-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="e0cbc-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e0cbc-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="e0cbc-130">sí</span><span class="sxs-lookup"><span data-stu-id="e0cbc-130">yes</span></span> |
| [<span data-ttu-id="e0cbc-131">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e0cbc-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="e0cbc-132">sí</span><span class="sxs-lookup"><span data-stu-id="e0cbc-132">yes</span></span> |
| [<span data-ttu-id="e0cbc-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e0cbc-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="e0cbc-134">sí</span><span class="sxs-lookup"><span data-stu-id="e0cbc-134">yes</span></span> |
| [<span data-ttu-id="e0cbc-135">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0cbc-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e0cbc-136">no</span><span class="sxs-lookup"><span data-stu-id="e0cbc-136">no</span></span> |
| [<span data-ttu-id="e0cbc-137">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0cbc-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e0cbc-138">no</span><span class="sxs-lookup"><span data-stu-id="e0cbc-138">no</span></span> |
| [<span data-ttu-id="e0cbc-139">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0cbc-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e0cbc-140">no</span><span class="sxs-lookup"><span data-stu-id="e0cbc-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="e0cbc-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e0cbc-141">Related topics</span></span>

[<span data-ttu-id="e0cbc-142">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e0cbc-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
