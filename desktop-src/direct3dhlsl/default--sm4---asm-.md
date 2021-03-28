---
title: predeterminado (SM4-ASM)
description: Una etiqueta opcional en una instrucción switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983830"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="2bdb2-103">predeterminado (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="2bdb2-103">default (sm4 - asm)</span></span>

<span data-ttu-id="2bdb2-104">Una etiqueta opcional en una instrucción [Switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="2bdb2-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="2bdb2-105">default</span><span class="sxs-lookup"><span data-stu-id="2bdb2-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="2bdb2-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2bdb2-106">Remarks</span></span>

<span data-ttu-id="2bdb2-107">Esta instrucción funciona igual que el **valor predeterminado** en C. pasar a través solo es válido si no hay ningún código agregado, por lo que varios casos (incluido el **predeterminado**) pueden compartir el mismo bloque de código.</span><span class="sxs-lookup"><span data-stu-id="2bdb2-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="2bdb2-108">Solo se permite una instrucción **default** en una construcción **Switch** .</span><span class="sxs-lookup"><span data-stu-id="2bdb2-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="2bdb2-109">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="2bdb2-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="2bdb2-110">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="2bdb2-110">Vertex Shader</span></span> | <span data-ttu-id="2bdb2-111">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="2bdb2-111">Geometry Shader</span></span> | <span data-ttu-id="2bdb2-112">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="2bdb2-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="2bdb2-113">x</span><span class="sxs-lookup"><span data-stu-id="2bdb2-113">x</span></span>             | <span data-ttu-id="2bdb2-114">x</span><span class="sxs-lookup"><span data-stu-id="2bdb2-114">x</span></span>               | <span data-ttu-id="2bdb2-115">x</span><span class="sxs-lookup"><span data-stu-id="2bdb2-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="2bdb2-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="2bdb2-116">Minimum Shader Model</span></span>

<span data-ttu-id="2bdb2-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2bdb2-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2bdb2-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="2bdb2-118">Shader Model</span></span>                                              | <span data-ttu-id="2bdb2-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="2bdb2-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="2bdb2-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2bdb2-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="2bdb2-121">sí</span><span class="sxs-lookup"><span data-stu-id="2bdb2-121">yes</span></span>       |
| [<span data-ttu-id="2bdb2-122">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="2bdb2-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="2bdb2-123">sí</span><span class="sxs-lookup"><span data-stu-id="2bdb2-123">yes</span></span>       |
| [<span data-ttu-id="2bdb2-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="2bdb2-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="2bdb2-125">sí</span><span class="sxs-lookup"><span data-stu-id="2bdb2-125">yes</span></span>       |
| [<span data-ttu-id="2bdb2-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bdb2-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="2bdb2-127">no</span><span class="sxs-lookup"><span data-stu-id="2bdb2-127">no</span></span>        |
| [<span data-ttu-id="2bdb2-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bdb2-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="2bdb2-129">no</span><span class="sxs-lookup"><span data-stu-id="2bdb2-129">no</span></span>        |
| [<span data-ttu-id="2bdb2-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bdb2-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="2bdb2-131">no</span><span class="sxs-lookup"><span data-stu-id="2bdb2-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="2bdb2-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2bdb2-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2bdb2-133">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="2bdb2-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




