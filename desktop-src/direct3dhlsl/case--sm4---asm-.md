---
title: caso (SM4-ASM)
description: Una etiqueta en una instrucción switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983846"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="ff095-103">caso (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="ff095-103">case (sm4 - asm)</span></span>

<span data-ttu-id="ff095-104">Una etiqueta en una instrucción switch.</span><span class="sxs-lookup"><span data-stu-id="ff095-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="ff095-105">caso \[ 32: bit inmediato\]</span><span class="sxs-lookup"><span data-stu-id="ff095-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="ff095-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ff095-106">Remarks</span></span>

<span data-ttu-id="ff095-107">Dado que el uso de **casos** es válido solo si no se agrega ningún código, varios **casos** (incluido el [predeterminado](default--sm4---asm-.md)) pueden compartir el mismo bloque de código.</span><span class="sxs-lookup"><span data-stu-id="ff095-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="ff095-108">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="ff095-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ff095-109">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="ff095-109">Vertex Shader</span></span> | <span data-ttu-id="ff095-110">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="ff095-110">Geometry Shader</span></span> | <span data-ttu-id="ff095-111">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="ff095-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="ff095-112">x</span><span class="sxs-lookup"><span data-stu-id="ff095-112">x</span></span>             | <span data-ttu-id="ff095-113">x</span><span class="sxs-lookup"><span data-stu-id="ff095-113">x</span></span>               | <span data-ttu-id="ff095-114">x</span><span class="sxs-lookup"><span data-stu-id="ff095-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ff095-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="ff095-115">Minimum Shader Model</span></span>

<span data-ttu-id="ff095-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="ff095-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="ff095-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="ff095-117">Shader Model</span></span>                                              | <span data-ttu-id="ff095-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="ff095-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ff095-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ff095-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ff095-120">sí</span><span class="sxs-lookup"><span data-stu-id="ff095-120">yes</span></span>       |
| [<span data-ttu-id="ff095-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ff095-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ff095-122">sí</span><span class="sxs-lookup"><span data-stu-id="ff095-122">yes</span></span>       |
| [<span data-ttu-id="ff095-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ff095-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ff095-124">sí</span><span class="sxs-lookup"><span data-stu-id="ff095-124">yes</span></span>       |
| [<span data-ttu-id="ff095-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff095-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ff095-126">no</span><span class="sxs-lookup"><span data-stu-id="ff095-126">no</span></span>        |
| [<span data-ttu-id="ff095-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff095-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ff095-128">no</span><span class="sxs-lookup"><span data-stu-id="ff095-128">no</span></span>        |
| [<span data-ttu-id="ff095-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff095-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ff095-130">no</span><span class="sxs-lookup"><span data-stu-id="ff095-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ff095-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ff095-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff095-132">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ff095-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




