---
title: Continue (SM4-ASM)
description: Continúa la ejecución al principio del bucle actual.
ms.assetid: 3F0021B2-50D1-407C-9EE4-1CB679E184BF
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc53b023e998fcf131a387fc009cfc8cb133ff6a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996900"
---
# <a name="continue-sm4---asm"></a><span data-ttu-id="bfaf1-103">Continue (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="bfaf1-103">continue (sm4 - asm)</span></span>

<span data-ttu-id="bfaf1-104">Continúa la ejecución al principio del bucle actual.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-104">Continues execution at the beginning of the current loop.</span></span>



| <span data-ttu-id="bfaf1-105">continue</span><span class="sxs-lookup"><span data-stu-id="bfaf1-105">continue</span></span> |
|----------|



 

## <a name="remarks"></a><span data-ttu-id="bfaf1-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bfaf1-106">Remarks</span></span>

<span data-ttu-id="bfaf1-107">**continue** solo se puede usar dentro de un [bucle](loop--sm4---asm-.md) o [ENDLOOP](endloop--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="bfaf1-107">**continue** can be used only inside a [loop](loop--sm4---asm-.md) or [endloop](endloop--sm4---asm-.md).</span></span>

<span data-ttu-id="bfaf1-108">En el ejemplo siguiente se muestra cómo usar la instrucción **continue** .</span><span class="sxs-lookup"><span data-stu-id="bfaf1-108">The following example shows how to use the **continue** instruction.</span></span>


```
                loop
                    if_na r0.x
                        break
                    endif
                    if_z r1.x
                        ...
                        continue
                    endif
                    ...
                endloop
```



<span data-ttu-id="bfaf1-109">El formato de token contiene el desplazamiento de la instrucción de bucle correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-109">The token format contains the offset of the corresponding loop instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="bfaf1-110">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="bfaf1-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="bfaf1-111">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="bfaf1-111">Vertex Shader</span></span> | <span data-ttu-id="bfaf1-112">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="bfaf1-112">Geometry Shader</span></span> | <span data-ttu-id="bfaf1-113">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="bfaf1-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="bfaf1-114">x</span><span class="sxs-lookup"><span data-stu-id="bfaf1-114">x</span></span>             | <span data-ttu-id="bfaf1-115">x</span><span class="sxs-lookup"><span data-stu-id="bfaf1-115">x</span></span>               | <span data-ttu-id="bfaf1-116">x</span><span class="sxs-lookup"><span data-stu-id="bfaf1-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="bfaf1-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="bfaf1-117">Minimum Shader Model</span></span>

<span data-ttu-id="bfaf1-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="bfaf1-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="bfaf1-119">Shader Model</span></span>                                              | <span data-ttu-id="bfaf1-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="bfaf1-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bfaf1-121">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bfaf1-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bfaf1-122">sí</span><span class="sxs-lookup"><span data-stu-id="bfaf1-122">yes</span></span>       |
| [<span data-ttu-id="bfaf1-123">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bfaf1-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bfaf1-124">sí</span><span class="sxs-lookup"><span data-stu-id="bfaf1-124">yes</span></span>       |
| [<span data-ttu-id="bfaf1-125">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bfaf1-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bfaf1-126">sí</span><span class="sxs-lookup"><span data-stu-id="bfaf1-126">yes</span></span>       |
| [<span data-ttu-id="bfaf1-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfaf1-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bfaf1-128">no</span><span class="sxs-lookup"><span data-stu-id="bfaf1-128">no</span></span>        |
| [<span data-ttu-id="bfaf1-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfaf1-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bfaf1-130">no</span><span class="sxs-lookup"><span data-stu-id="bfaf1-130">no</span></span>        |
| [<span data-ttu-id="bfaf1-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfaf1-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bfaf1-132">no</span><span class="sxs-lookup"><span data-stu-id="bfaf1-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bfaf1-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bfaf1-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bfaf1-134">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bfaf1-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




