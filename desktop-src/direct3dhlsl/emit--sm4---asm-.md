---
title: emisión (SM4-ASM)
description: Emita un vértice.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "103784894"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="18b1c-103">emisión (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="18b1c-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="18b1c-104">Emita un vértice.</span><span class="sxs-lookup"><span data-stu-id="18b1c-104">Emit a vertex.</span></span>



| <span data-ttu-id="18b1c-105">reflexión</span><span class="sxs-lookup"><span data-stu-id="18b1c-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="18b1c-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="18b1c-106">Remarks</span></span>

<span data-ttu-id="18b1c-107">**Emit** hace que todos los registros o declarados \# se lean fuera del sombreador de geometría para generar un vértice.</span><span class="sxs-lookup"><span data-stu-id="18b1c-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="18b1c-108">Cuando se emiten varias llamadas a **emisión** , se generan primitivas.</span><span class="sxs-lookup"><span data-stu-id="18b1c-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="18b1c-109">**Emit** puede aparecer cualquier número de veces en un sombreador de geometría, incluido en el control de flujo.</span><span class="sxs-lookup"><span data-stu-id="18b1c-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="18b1c-110">Si se han declarado secuencias, debe usar [Emit \_ Stream](emit-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="18b1c-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="18b1c-111">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="18b1c-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="18b1c-112">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="18b1c-112">Vertex Shader</span></span> | <span data-ttu-id="18b1c-113">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="18b1c-113">Geometry Shader</span></span> | <span data-ttu-id="18b1c-114">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="18b1c-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="18b1c-115">x</span><span class="sxs-lookup"><span data-stu-id="18b1c-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="18b1c-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="18b1c-116">Minimum Shader Model</span></span>

<span data-ttu-id="18b1c-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="18b1c-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="18b1c-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="18b1c-118">Shader Model</span></span>                                              | <span data-ttu-id="18b1c-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="18b1c-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="18b1c-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="18b1c-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="18b1c-121">sí</span><span class="sxs-lookup"><span data-stu-id="18b1c-121">yes</span></span>       |
| [<span data-ttu-id="18b1c-122">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="18b1c-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="18b1c-123">sí</span><span class="sxs-lookup"><span data-stu-id="18b1c-123">yes</span></span>       |
| [<span data-ttu-id="18b1c-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="18b1c-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="18b1c-125">sí</span><span class="sxs-lookup"><span data-stu-id="18b1c-125">yes</span></span>       |
| [<span data-ttu-id="18b1c-126">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18b1c-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="18b1c-127">no</span><span class="sxs-lookup"><span data-stu-id="18b1c-127">no</span></span>        |
| [<span data-ttu-id="18b1c-128">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18b1c-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="18b1c-129">no</span><span class="sxs-lookup"><span data-stu-id="18b1c-129">no</span></span>        |
| [<span data-ttu-id="18b1c-130">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18b1c-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="18b1c-131">no</span><span class="sxs-lookup"><span data-stu-id="18b1c-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="18b1c-132">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18b1c-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18b1c-133">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="18b1c-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




