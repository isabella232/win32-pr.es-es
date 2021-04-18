---
title: endswitch (SM4-ASM)
description: Finaliza una instrucción switch.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104419877"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="17bed-103">endswitch (SM4-ASM)</span><span class="sxs-lookup"><span data-stu-id="17bed-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="17bed-104">Finaliza una instrucción [Switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="17bed-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="17bed-105">endswitch</span><span class="sxs-lookup"><span data-stu-id="17bed-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="17bed-106">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17bed-106">Remarks</span></span>

<span data-ttu-id="17bed-107">El formato de token contiene el desplazamiento de la instrucción switch correspondiente en el sombreador como una comodidad.</span><span class="sxs-lookup"><span data-stu-id="17bed-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="17bed-108">Esta instrucción se aplica a las siguientes fases del sombreador:</span><span class="sxs-lookup"><span data-stu-id="17bed-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="17bed-109">Sombreador de vértices</span><span class="sxs-lookup"><span data-stu-id="17bed-109">Vertex Shader</span></span> | <span data-ttu-id="17bed-110">Sombreador de geometría</span><span class="sxs-lookup"><span data-stu-id="17bed-110">Geometry Shader</span></span> | <span data-ttu-id="17bed-111">Sombreador de píxeles</span><span class="sxs-lookup"><span data-stu-id="17bed-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="17bed-112">x</span><span class="sxs-lookup"><span data-stu-id="17bed-112">x</span></span>             | <span data-ttu-id="17bed-113">x</span><span class="sxs-lookup"><span data-stu-id="17bed-113">x</span></span>               | <span data-ttu-id="17bed-114">x</span><span class="sxs-lookup"><span data-stu-id="17bed-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="17bed-115">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="17bed-115">Minimum Shader Model</span></span>

<span data-ttu-id="17bed-116">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="17bed-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="17bed-117">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="17bed-117">Shader Model</span></span>                                              | <span data-ttu-id="17bed-118">Compatible</span><span class="sxs-lookup"><span data-stu-id="17bed-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="17bed-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="17bed-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="17bed-120">sí</span><span class="sxs-lookup"><span data-stu-id="17bed-120">yes</span></span>       |
| [<span data-ttu-id="17bed-121">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="17bed-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="17bed-122">sí</span><span class="sxs-lookup"><span data-stu-id="17bed-122">yes</span></span>       |
| [<span data-ttu-id="17bed-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="17bed-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="17bed-124">sí</span><span class="sxs-lookup"><span data-stu-id="17bed-124">yes</span></span>       |
| [<span data-ttu-id="17bed-125">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17bed-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="17bed-126">no</span><span class="sxs-lookup"><span data-stu-id="17bed-126">no</span></span>        |
| [<span data-ttu-id="17bed-127">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17bed-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="17bed-128">no</span><span class="sxs-lookup"><span data-stu-id="17bed-128">no</span></span>        |
| [<span data-ttu-id="17bed-129">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17bed-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="17bed-130">no</span><span class="sxs-lookup"><span data-stu-id="17bed-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="17bed-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17bed-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17bed-132">Ensamblado modelo de sombreador 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="17bed-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




