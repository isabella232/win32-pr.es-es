---
title: Valor absoluto
description: Toma el valor absoluto de un operando de origen utilizado en una operación aritmética.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104358507"
---
# <a name="absolute-value"></a><span data-ttu-id="a8af7-103">Valor absoluto</span><span class="sxs-lookup"><span data-stu-id="a8af7-103">Absolute Value</span></span>

<span data-ttu-id="a8af7-104">Toma el valor absoluto de un operando de origen utilizado en una operación aritmética.</span><span class="sxs-lookup"><span data-stu-id="a8af7-104">Take the absolute value of a source operand used in an arithmetic operation.</span></span>



| <span data-ttu-id="a8af7-105">\_ABS</span><span class="sxs-lookup"><span data-stu-id="a8af7-105">\_abs</span></span> |
|-------|



 

<span data-ttu-id="a8af7-106">Este modificador se usa solo para las instrucciones y el punto flotante de precisión sencilla y doble.</span><span class="sxs-lookup"><span data-stu-id="a8af7-106">This modifier is used for single and double precision floating point and instructions only.</span></span> <span data-ttu-id="a8af7-107">El modificador **\_ ABS** fuerza el signo de los números en el operando de origen Positive, incluidos los valores INF.</span><span class="sxs-lookup"><span data-stu-id="a8af7-107">The **\_abs** modifier forces the sign of the number(s) on the source operand positive, including on INF values.</span></span>

<span data-ttu-id="a8af7-108">Al aplicar **\_ ABS** en Nan, se conservan Nan, aunque el patrón de bits Nan determinado que Results no está definido.</span><span class="sxs-lookup"><span data-stu-id="a8af7-108">Applying **\_abs** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="a8af7-109">Cuando \_ se combina ABS con el modificador [Negate](negate.md) , la combinación obliga al signo a ser negativo, como si se aplicara primero el modificador **\_ ABS** y luego el valor **negado**.</span><span class="sxs-lookup"><span data-stu-id="a8af7-109">When \_abs is combined with the [negate](negate.md) modifier, the combination forces the sign to be negative, as if the **\_abs** modifier is applied first, then the **negate**.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="a8af7-110">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="a8af7-110">Minimum Shader Model</span></span>

<span data-ttu-id="a8af7-111">Este modificador es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="a8af7-111">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="a8af7-112">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="a8af7-112">Shader Model</span></span>                                              | <span data-ttu-id="a8af7-113">Compatible</span><span class="sxs-lookup"><span data-stu-id="a8af7-113">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="a8af7-114">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="a8af7-114">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="a8af7-115">sí</span><span class="sxs-lookup"><span data-stu-id="a8af7-115">yes</span></span>       |
| [<span data-ttu-id="a8af7-116">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="a8af7-116">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="a8af7-117">sí</span><span class="sxs-lookup"><span data-stu-id="a8af7-117">yes</span></span>       |
| [<span data-ttu-id="a8af7-118">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="a8af7-118">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="a8af7-119">sí</span><span class="sxs-lookup"><span data-stu-id="a8af7-119">yes</span></span>       |
| [<span data-ttu-id="a8af7-120">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8af7-120">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="a8af7-121">no</span><span class="sxs-lookup"><span data-stu-id="a8af7-121">no</span></span>        |
| [<span data-ttu-id="a8af7-122">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8af7-122">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="a8af7-123">no</span><span class="sxs-lookup"><span data-stu-id="a8af7-123">no</span></span>        |
| [<span data-ttu-id="a8af7-124">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="a8af7-124">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="a8af7-125">no</span><span class="sxs-lookup"><span data-stu-id="a8af7-125">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="a8af7-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a8af7-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a8af7-127">Modificadores de instrucciones</span><span class="sxs-lookup"><span data-stu-id="a8af7-127">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




