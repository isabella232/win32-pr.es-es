---
title: Else (SM4-ASM)
description: Inicia un bloque else.
ms.assetid: CFF25E78-D986-4EC5-B542-B3396EFF88E1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e283a2621c916ac254daab9f055be0ffe1ba67d
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983890"
---
# <a name="else-sm4---asm"></a><span data-ttu-id="329a6-103">Else (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="329a6-103">else (sm4 - asm)</span></span>

<span data-ttu-id="329a6-104">Inicia un bloque **else** .</span><span class="sxs-lookup"><span data-stu-id="329a6-104">Starts an **else** block.</span></span>



| <span data-ttu-id="329a6-105">else</span><span class="sxs-lookup"><span data-stu-id="329a6-105">else</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="329a6-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="329a6-106">Remarks</span></span>

<span data-ttu-id="329a6-107">El formato de token contiene el desplazamiento de la instrucción de [endif](endif--sm4---asm-.md) correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="329a6-107">The token format contains the offset of the corresponding [endif](endif--sm4---asm-.md) instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="329a6-108">En el ejemplo siguiente se muestra cómo usar la instrucción **else** .</span><span class="sxs-lookup"><span data-stu-id="329a6-108">The following example shows how to use the **else** instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="329a6-109">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="329a6-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="329a6-110">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="329a6-110">Vertex Shader</span></span> | <span data-ttu-id="329a6-111">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="329a6-111">Geometry Shader</span></span> | <span data-ttu-id="329a6-112">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="329a6-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="329a6-113">x</span><span class="sxs-lookup"><span data-stu-id="329a6-113">x</span></span>             | <span data-ttu-id="329a6-114">x</span><span class="sxs-lookup"><span data-stu-id="329a6-114">x</span></span>               | <span data-ttu-id="329a6-115">x</span><span class="sxs-lookup"><span data-stu-id="329a6-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="329a6-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="329a6-116">Minimum Shader Model</span></span>

<span data-ttu-id="329a6-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="329a6-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="329a6-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="329a6-118">Shader Model</span></span>                                              | <span data-ttu-id="329a6-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="329a6-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="329a6-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="329a6-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="329a6-121">sí</span><span class="sxs-lookup"><span data-stu-id="329a6-121">yes</span></span>       |
| [<span data-ttu-id="329a6-122">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="329a6-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="329a6-123">sí</span><span class="sxs-lookup"><span data-stu-id="329a6-123">yes</span></span>       |
| [<span data-ttu-id="329a6-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="329a6-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="329a6-125">sí</span><span class="sxs-lookup"><span data-stu-id="329a6-125">yes</span></span>       |
| [<span data-ttu-id="329a6-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="329a6-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="329a6-127">no</span><span class="sxs-lookup"><span data-stu-id="329a6-127">no</span></span>        |
| [<span data-ttu-id="329a6-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="329a6-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="329a6-129">no</span><span class="sxs-lookup"><span data-stu-id="329a6-129">no</span></span>        |
| [<span data-ttu-id="329a6-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="329a6-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="329a6-131">no</span><span class="sxs-lookup"><span data-stu-id="329a6-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="329a6-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="329a6-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="329a6-133">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="329a6-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




