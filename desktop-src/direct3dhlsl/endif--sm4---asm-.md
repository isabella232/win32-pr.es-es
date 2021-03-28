---
title: endif (SM4-ASM)
description: Finaliza una instrucción if.
ms.assetid: 9F4CF9E0-4D9D-4300-B432-432C560F34BB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d3fa6cf0efd395843212f6bacac478285e496c2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077064"
---
# <a name="endif-sm4---asm"></a><span data-ttu-id="ac735-103">endif (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ac735-103">endif (sm4 - asm)</span></span>

<span data-ttu-id="ac735-104">Finaliza una instrucción [If](if--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="ac735-104">Ends an [if](if--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="ac735-105">endif</span><span class="sxs-lookup"><span data-stu-id="ac735-105">endif</span></span> |
|-------|



 

## <a name="remarks"></a><span data-ttu-id="ac735-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac735-106">Remarks</span></span>

<span data-ttu-id="ac735-107">En el ejemplo siguiente se muestra cómo usar la instrucción endif.</span><span class="sxs-lookup"><span data-stu-id="ac735-107">The following example shows how to use the endif instruction.</span></span>

``` syntax
                if     // any of the various forms of if* statements
                   ...
                else   // (optional)
                   ...
                endif
```

<span data-ttu-id="ac735-108">El formato de token contiene el desplazamiento de la instrucción **If** correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="ac735-108">The token format contains the offset of the corresponding **if** instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="ac735-109">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ac735-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ac735-110">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ac735-110">Vertex Shader</span></span> | <span data-ttu-id="ac735-111">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ac735-111">Geometry Shader</span></span> | <span data-ttu-id="ac735-112">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ac735-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ac735-113">x</span><span class="sxs-lookup"><span data-stu-id="ac735-113">x</span></span>             | <span data-ttu-id="ac735-114">x</span><span class="sxs-lookup"><span data-stu-id="ac735-114">x</span></span>               | <span data-ttu-id="ac735-115">x</span><span class="sxs-lookup"><span data-stu-id="ac735-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ac735-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ac735-116">Minimum Shader Model</span></span>

<span data-ttu-id="ac735-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ac735-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ac735-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ac735-118">Shader Model</span></span>                                              | <span data-ttu-id="ac735-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="ac735-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ac735-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ac735-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ac735-121">sí</span><span class="sxs-lookup"><span data-stu-id="ac735-121">yes</span></span>       |
| [<span data-ttu-id="ac735-122">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ac735-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ac735-123">sí</span><span class="sxs-lookup"><span data-stu-id="ac735-123">yes</span></span>       |
| [<span data-ttu-id="ac735-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ac735-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ac735-125">sí</span><span class="sxs-lookup"><span data-stu-id="ac735-125">yes</span></span>       |
| [<span data-ttu-id="ac735-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac735-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ac735-127">no</span><span class="sxs-lookup"><span data-stu-id="ac735-127">no</span></span>        |
| [<span data-ttu-id="ac735-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac735-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ac735-129">no</span><span class="sxs-lookup"><span data-stu-id="ac735-129">no</span></span>        |
| [<span data-ttu-id="ac735-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac735-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ac735-131">no</span><span class="sxs-lookup"><span data-stu-id="ac735-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ac735-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ac735-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ac735-133">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ac735-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




