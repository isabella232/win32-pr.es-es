---
title: ushr (SM4-ASM)
description: Desplazar a la derecha. | ushr (SM4-ASM)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104279978"
---
# <a name="ushr-sm4---asm"></a><span data-ttu-id="fde6f-104">ushr (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="fde6f-104">ushr (sm4 - asm)</span></span>

<span data-ttu-id="fde6f-105">Desplazar a la derecha.</span><span class="sxs-lookup"><span data-stu-id="fde6f-105">Shift right.</span></span>



| <span data-ttu-id="fde6f-106">ushr dest \[ . Mask \] , src0 \[ . swizzle \] , SRC1. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="fde6f-106">ushr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="fde6f-107">Elemento</span><span class="sxs-lookup"><span data-stu-id="fde6f-107">Item</span></span>                                                            | <span data-ttu-id="fde6f-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="fde6f-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="fde6f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="fde6f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="fde6f-110">\[en \] la dirección del resultado de la operación.</span><span class="sxs-lookup"><span data-stu-id="fde6f-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="fde6f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="fde6f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="fde6f-112">\[en \] los componentes que se van a desplazar.</span><span class="sxs-lookup"><span data-stu-id="fde6f-112">\[in\] The components to shift.</span></span><br/>                    |
| <span data-ttu-id="fde6f-113"><span id="src1"></span><span id="SRC1"></span>*SRC1*</span><span class="sxs-lookup"><span data-stu-id="fde6f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="fde6f-114">\[en \] la cantidad que se va a desplazar *src0*.</span><span class="sxs-lookup"><span data-stu-id="fde6f-114">\[in\] The amount to shift *src0*.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="fde6f-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fde6f-115">Remarks</span></span>

<span data-ttu-id="fde6f-116">Esta instrucción realiza un desplazamiento por componentes de cada valor de 32 bits de *src0* a la derecha un recuento de bits sin signo proporcionado por el LSB 5 bits (intervalo 0-31) de *SRC1. Seleccione el \_ componente*, insertando 0.</span><span class="sxs-lookup"><span data-stu-id="fde6f-116">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="fde6f-117">El resultado de 32 bits por componente se coloca en el *destino*.</span><span class="sxs-lookup"><span data-stu-id="fde6f-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="fde6f-118">El recuento es un valor escalar que se aplica a todos los componentes.</span><span class="sxs-lookup"><span data-stu-id="fde6f-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="fde6f-119">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="fde6f-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="fde6f-120">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="fde6f-120">Vertex Shader</span></span> | <span data-ttu-id="fde6f-121">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="fde6f-121">Geometry Shader</span></span> | <span data-ttu-id="fde6f-122">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="fde6f-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="fde6f-123">x</span><span class="sxs-lookup"><span data-stu-id="fde6f-123">x</span></span>             | <span data-ttu-id="fde6f-124">x</span><span class="sxs-lookup"><span data-stu-id="fde6f-124">x</span></span>               | <span data-ttu-id="fde6f-125">x</span><span class="sxs-lookup"><span data-stu-id="fde6f-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="fde6f-126">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="fde6f-126">Minimum Shader Model</span></span>

<span data-ttu-id="fde6f-127">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fde6f-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fde6f-128">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="fde6f-128">Shader Model</span></span>                                              | <span data-ttu-id="fde6f-129">Compatible</span><span class="sxs-lookup"><span data-stu-id="fde6f-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fde6f-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fde6f-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fde6f-131">sí</span><span class="sxs-lookup"><span data-stu-id="fde6f-131">yes</span></span>       |
| [<span data-ttu-id="fde6f-132">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fde6f-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fde6f-133">sí</span><span class="sxs-lookup"><span data-stu-id="fde6f-133">yes</span></span>       |
| [<span data-ttu-id="fde6f-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fde6f-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fde6f-135">sí</span><span class="sxs-lookup"><span data-stu-id="fde6f-135">yes</span></span>       |
| [<span data-ttu-id="fde6f-136">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fde6f-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fde6f-137">no</span><span class="sxs-lookup"><span data-stu-id="fde6f-137">no</span></span>        |
| [<span data-ttu-id="fde6f-138">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fde6f-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fde6f-139">no</span><span class="sxs-lookup"><span data-stu-id="fde6f-139">no</span></span>        |
| [<span data-ttu-id="fde6f-140">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fde6f-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fde6f-141">no</span><span class="sxs-lookup"><span data-stu-id="fde6f-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fde6f-142">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fde6f-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fde6f-143">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fde6f-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





