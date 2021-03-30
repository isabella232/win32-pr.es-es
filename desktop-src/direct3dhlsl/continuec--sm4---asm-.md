---
title: continuec (SM4-ASM)
description: Continúa la ejecución condicionalmente al principio del bucle actual.
ms.assetid: 1A5B1951-CE1E-479C-AE0F-FC5FB93E0DE9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d480d8828f8f68af1f6a2ff4f52224041d5241df
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983843"
---
# <a name="continuec-sm4---asm"></a><span data-ttu-id="e5dc7-103">continuec (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="e5dc7-103">continuec (sm4 - asm)</span></span>

<span data-ttu-id="e5dc7-104">Continúa la ejecución condicionalmente al principio del bucle actual.</span><span class="sxs-lookup"><span data-stu-id="e5dc7-104">Conditionally continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="e5dc7-105">continuec { \_ z </span><span class="sxs-lookup"><span data-stu-id="e5dc7-105">continuec{\_z</span></span>\|<span data-ttu-id="e5dc7-106">\_NZ} src0. Select ( \_ componente)</span><span class="sxs-lookup"><span data-stu-id="e5dc7-106">\_nz} src0.select\_component</span></span> |
|---------------------------------------------|



 



| <span data-ttu-id="e5dc7-107">Término</span><span class="sxs-lookup"><span data-stu-id="e5dc7-107">Term</span></span>                                                            | <span data-ttu-id="e5dc7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="e5dc7-108">Description</span></span>                                                          |
|-----------------------------------------------------------------|----------------------------------------------------------------------|
| <span data-ttu-id="e5dc7-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="e5dc7-109"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="e5dc7-110">\[en \] el componente en el que se va a probar la condición.</span><span class="sxs-lookup"><span data-stu-id="e5dc7-110">\[in\] The component against which to test the condition.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e5dc7-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e5dc7-111">Remarks</span></span>

<span data-ttu-id="e5dc7-112">**continuec** solo se puede usar dentro de un [bucle](loop--sm4---asm-.md) o [ENDLOOP](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="e5dc7-112">**continuec** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="e5dc7-113">En el ejemplo siguiente se muestra cómo usar la instrucción **continuec** .</span><span class="sxs-lookup"><span data-stu-id="e5dc7-113">The following example shows how to use the **continuec** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    continuec_z r1.x  // if all bits of r1.x are zero then
                                      // continue at beginning of loop.
                    ...
                    continuec_nz r3.y // if any bit in r3.y is set then
                                      // continue at beginning of loop.

                    ...
                endloop

```



<span data-ttu-id="e5dc7-114">El formato de token contiene el desplazamiento de la instrucción de bucle correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="e5dc7-114">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="e5dc7-115">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="e5dc7-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e5dc7-116">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="e5dc7-116">Vertex Shader</span></span> | <span data-ttu-id="e5dc7-117">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="e5dc7-117">Geometry Shader</span></span> | <span data-ttu-id="e5dc7-118">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="e5dc7-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="e5dc7-119">x</span><span class="sxs-lookup"><span data-stu-id="e5dc7-119">x</span></span>             | <span data-ttu-id="e5dc7-120">x</span><span class="sxs-lookup"><span data-stu-id="e5dc7-120">x</span></span>               | <span data-ttu-id="e5dc7-121">x</span><span class="sxs-lookup"><span data-stu-id="e5dc7-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e5dc7-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e5dc7-122">Minimum Shader Model</span></span>

<span data-ttu-id="e5dc7-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e5dc7-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e5dc7-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e5dc7-124">Shader Model</span></span>                                              | <span data-ttu-id="e5dc7-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="e5dc7-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e5dc7-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e5dc7-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e5dc7-127">sí</span><span class="sxs-lookup"><span data-stu-id="e5dc7-127">yes</span></span>       |
| [<span data-ttu-id="e5dc7-128">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e5dc7-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e5dc7-129">sí</span><span class="sxs-lookup"><span data-stu-id="e5dc7-129">yes</span></span>       |
| [<span data-ttu-id="e5dc7-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e5dc7-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e5dc7-131">sí</span><span class="sxs-lookup"><span data-stu-id="e5dc7-131">yes</span></span>       |
| [<span data-ttu-id="e5dc7-132">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5dc7-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e5dc7-133">no</span><span class="sxs-lookup"><span data-stu-id="e5dc7-133">no</span></span>        |
| [<span data-ttu-id="e5dc7-134">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5dc7-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e5dc7-135">no</span><span class="sxs-lookup"><span data-stu-id="e5dc7-135">no</span></span>        |
| [<span data-ttu-id="e5dc7-136">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5dc7-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e5dc7-137">no</span><span class="sxs-lookup"><span data-stu-id="e5dc7-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e5dc7-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e5dc7-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5dc7-139">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e5dc7-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





