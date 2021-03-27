---
title: Break (SM4-ASM)
description: Mueve el punto de ejecución a la instrucción después del siguiente ENDLOOP o endswitch.
ms.assetid: 411FB361-FBD1-4180-8D81-2074BA8972B7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06396d062e9126091052126737e3e05c58dbdb16
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358481"
---
# <a name="break-sm4---asm"></a><span data-ttu-id="0f700-103">Break (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0f700-103">break (sm4 - asm)</span></span>

<span data-ttu-id="0f700-104">Mueve el punto de ejecución a la instrucción después del siguiente [ENDLOOP](endloop--sm4---asm-.md) o [endswitch](endswitch--sm4---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="0f700-104">Moves the point of execution to the instruction after the next [endloop](endloop--sm4---asm-.md) or [endswitch](endswitch--sm4---asm-.md).</span></span>



| <span data-ttu-id="0f700-105">break</span><span class="sxs-lookup"><span data-stu-id="0f700-105">break</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="0f700-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0f700-106">Remarks</span></span>

<span data-ttu-id="0f700-107">El formato de token contiene el desplazamiento de la instrucción **ENDLOOP** o **endswitch** correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="0f700-107">The token format contains the offset of the corresponding **endloop** or **endswitch** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="0f700-108">En el ejemplo siguiente se muestra la instrucción **break** .</span><span class="sxs-lookup"><span data-stu-id="0f700-108">The following example shows the **break** instruction.</span></span>


```
                loop
                    // example of termination condition
                    if_nz r0.x
                        break
                    endif
                    ...
                endloop
```



<span data-ttu-id="0f700-109">Esta instrucción debe aparecer dentro de un **bucle** / **ENDLOOP** o en un **caso** en un **modificador** / **endswitch**.</span><span class="sxs-lookup"><span data-stu-id="0f700-109">This instruction must appear within a **loop**/**endloop** or in a **case** in a **switch**/**endswitch**.</span></span>

<span data-ttu-id="0f700-110">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="0f700-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0f700-111">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="0f700-111">Vertex Shader</span></span> | <span data-ttu-id="0f700-112">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="0f700-112">Geometry Shader</span></span> | <span data-ttu-id="0f700-113">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="0f700-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0f700-114">x</span><span class="sxs-lookup"><span data-stu-id="0f700-114">x</span></span>             | <span data-ttu-id="0f700-115">x</span><span class="sxs-lookup"><span data-stu-id="0f700-115">x</span></span>               | <span data-ttu-id="0f700-116">x</span><span class="sxs-lookup"><span data-stu-id="0f700-116">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0f700-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="0f700-117">Minimum Shader Model</span></span>

<span data-ttu-id="0f700-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0f700-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0f700-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="0f700-119">Shader Model</span></span>                                              | <span data-ttu-id="0f700-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="0f700-120">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0f700-121">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0f700-121">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0f700-122">sí</span><span class="sxs-lookup"><span data-stu-id="0f700-122">yes</span></span>       |
| [<span data-ttu-id="0f700-123">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0f700-123">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0f700-124">sí</span><span class="sxs-lookup"><span data-stu-id="0f700-124">yes</span></span>       |
| [<span data-ttu-id="0f700-125">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0f700-125">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0f700-126">sí</span><span class="sxs-lookup"><span data-stu-id="0f700-126">yes</span></span>       |
| [<span data-ttu-id="0f700-127">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f700-127">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0f700-128">no</span><span class="sxs-lookup"><span data-stu-id="0f700-128">no</span></span>        |
| [<span data-ttu-id="0f700-129">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f700-129">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0f700-130">no</span><span class="sxs-lookup"><span data-stu-id="0f700-130">no</span></span>        |
| [<span data-ttu-id="0f700-131">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f700-131">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0f700-132">no</span><span class="sxs-lookup"><span data-stu-id="0f700-132">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0f700-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0f700-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0f700-134">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0f700-134">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




