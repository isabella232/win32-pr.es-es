---
title: MOV (SM4-ASM)
description: Movimiento de componentes. | MOV (SM4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279943"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="dfe83-104">MOV (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="dfe83-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="dfe83-105">Movimiento de componentes.</span><span class="sxs-lookup"><span data-stu-id="dfe83-105">Component-wise move.</span></span>



| <span data-ttu-id="dfe83-106">Instrucción: MOV \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="dfe83-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="dfe83-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="dfe83-107">Item</span></span>                                                            | <span data-ttu-id="dfe83-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="dfe83-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dfe83-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="dfe83-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="dfe83-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="dfe83-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="dfe83-111">*dest*  =  *src0*</span><span class="sxs-lookup"><span data-stu-id="dfe83-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="dfe83-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="dfe83-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="dfe83-113">\[en \] los componentes que se van a trasladar.</span><span class="sxs-lookup"><span data-stu-id="dfe83-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="dfe83-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dfe83-114">Remarks</span></span>

<span data-ttu-id="dfe83-115">Los modificadores, a excepción de swizzle, suponen que los datos son de punto flotante.</span><span class="sxs-lookup"><span data-stu-id="dfe83-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="dfe83-116">La ausencia de modificadores solo mueve los datos sin modificar los bits.</span><span class="sxs-lookup"><span data-stu-id="dfe83-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="dfe83-117">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="dfe83-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="dfe83-118">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="dfe83-118">Vertex Shader</span></span> | <span data-ttu-id="dfe83-119">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="dfe83-119">Geometry Shader</span></span> | <span data-ttu-id="dfe83-120">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="dfe83-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="dfe83-121">x</span><span class="sxs-lookup"><span data-stu-id="dfe83-121">x</span></span>             | <span data-ttu-id="dfe83-122">x</span><span class="sxs-lookup"><span data-stu-id="dfe83-122">x</span></span>               | <span data-ttu-id="dfe83-123">x</span><span class="sxs-lookup"><span data-stu-id="dfe83-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="dfe83-124">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="dfe83-124">Minimum Shader Model</span></span>

<span data-ttu-id="dfe83-125">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dfe83-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="dfe83-126">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="dfe83-126">Shader Model</span></span>                                              | <span data-ttu-id="dfe83-127">Compatible</span><span class="sxs-lookup"><span data-stu-id="dfe83-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="dfe83-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="dfe83-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="dfe83-129">sí</span><span class="sxs-lookup"><span data-stu-id="dfe83-129">yes</span></span>       |
| [<span data-ttu-id="dfe83-130">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="dfe83-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="dfe83-131">sí</span><span class="sxs-lookup"><span data-stu-id="dfe83-131">yes</span></span>       |
| [<span data-ttu-id="dfe83-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="dfe83-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="dfe83-133">sí</span><span class="sxs-lookup"><span data-stu-id="dfe83-133">yes</span></span>       |
| [<span data-ttu-id="dfe83-134">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfe83-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="dfe83-135">no</span><span class="sxs-lookup"><span data-stu-id="dfe83-135">no</span></span>        |
| [<span data-ttu-id="dfe83-136">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfe83-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="dfe83-137">no</span><span class="sxs-lookup"><span data-stu-id="dfe83-137">no</span></span>        |
| [<span data-ttu-id="dfe83-138">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfe83-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="dfe83-139">no</span><span class="sxs-lookup"><span data-stu-id="dfe83-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="dfe83-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dfe83-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dfe83-141">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="dfe83-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





