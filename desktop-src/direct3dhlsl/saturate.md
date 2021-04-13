---
title: Saturación (referencia de HLSL)
description: Fija el resultado de una operación aritmética de punto flotante de precisión única o doble a \ 0.0 f... 1.0 f \ intervalo.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420025"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="c23a0-103">Saturación (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="c23a0-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="c23a0-104">Fija el resultado de una operación aritmética de punto flotante de precisión única o doble a \[ 0,0 f... 1.0 intervalo de f \] .</span><span class="sxs-lookup"><span data-stu-id="c23a0-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="c23a0-105">\_sábado</span><span class="sxs-lookup"><span data-stu-id="c23a0-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="c23a0-106">El modificador de resultado de instrucción **saturada** realiza la siguiente operación en los valores de resultado de una operación aritmética de punto flotante que tiene el \_ SAT aplicado:</span><span class="sxs-lookup"><span data-stu-id="c23a0-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="c23a0-107">donde min () y Max () en la expresión anterior se comportan de la manera en que operan [min](min--sm4---asm-.md), [Max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md)o [dmáx](dmax--sm5---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="c23a0-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="c23a0-108">`_sat(NaN)` devuelve 0, según las reglas de min y Max.</span><span class="sxs-lookup"><span data-stu-id="c23a0-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="c23a0-109">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="c23a0-109">Minimum Shader Model</span></span>

<span data-ttu-id="c23a0-110">Este modificador es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="c23a0-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="c23a0-111">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="c23a0-111">Shader Model</span></span>                                              | <span data-ttu-id="c23a0-112">Compatible</span><span class="sxs-lookup"><span data-stu-id="c23a0-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="c23a0-113">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="c23a0-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="c23a0-114">sí</span><span class="sxs-lookup"><span data-stu-id="c23a0-114">yes</span></span>       |
| [<span data-ttu-id="c23a0-115">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="c23a0-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="c23a0-116">sí</span><span class="sxs-lookup"><span data-stu-id="c23a0-116">yes</span></span>       |
| [<span data-ttu-id="c23a0-117">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="c23a0-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="c23a0-118">sí</span><span class="sxs-lookup"><span data-stu-id="c23a0-118">yes</span></span>       |
| [<span data-ttu-id="c23a0-119">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c23a0-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="c23a0-120">no</span><span class="sxs-lookup"><span data-stu-id="c23a0-120">no</span></span>        |
| [<span data-ttu-id="c23a0-121">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c23a0-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="c23a0-122">no</span><span class="sxs-lookup"><span data-stu-id="c23a0-122">no</span></span>        |
| [<span data-ttu-id="c23a0-123">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="c23a0-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="c23a0-124">no</span><span class="sxs-lookup"><span data-stu-id="c23a0-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="c23a0-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c23a0-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c23a0-126">Modificadores de instrucciones</span><span class="sxs-lookup"><span data-stu-id="c23a0-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




