---
title: Negate
description: Voltea el signo del valor de un operando de origen utilizado en una operación aritmética.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cc2637a76b52b28eefcfb3637cc8b2d406c02c06
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/20/2019
ms.locfileid: "104077080"
---
# <a name="negate"></a><span data-ttu-id="bf7f8-103">Negate</span><span class="sxs-lookup"><span data-stu-id="bf7f8-103">Negate</span></span>

<span data-ttu-id="bf7f8-104">Voltea el signo del valor de un operando de origen utilizado en una operación aritmética.</span><span class="sxs-lookup"><span data-stu-id="bf7f8-104">Flips the sign of the value of a source operand used in an arithmetic operation.</span></span>



| \-  |
|-----|



 

<span data-ttu-id="bf7f8-105">En el caso de las instrucciones y el punto flotante de precisión sencilla y doble, el modificador Nega el signo de los números del operando de origen, incluidos los valores INF.</span><span class="sxs-lookup"><span data-stu-id="bf7f8-105">For single and double precision floating point and instructions, the negate modifier flips the sign of the number(s) in the source operand, including on INF values.</span></span> <span data-ttu-id="bf7f8-106">Al aplicar **niega** en Nan, se conservan Nan, aunque el patrón de bits Nan determinado que Results no está definido.</span><span class="sxs-lookup"><span data-stu-id="bf7f8-106">Applying **negate** on NaN preserves NaN, although the particular NaN bit pattern that results is not defined.</span></span>

<span data-ttu-id="bf7f8-107">En el caso de las instrucciones de entero, el modificador **Negate** toma el complemento de 2 de los números en el operando de origen.</span><span class="sxs-lookup"><span data-stu-id="bf7f8-107">For integer instructions, the **negate** modifier takes the 2's complement of the number(s) in the source operand.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="bf7f8-108">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="bf7f8-108">Minimum Shader Model</span></span>

<span data-ttu-id="bf7f8-109">Este modificador es compatible con los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf7f8-109">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="bf7f8-110">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="bf7f8-110">Shader Model</span></span>                                              | <span data-ttu-id="bf7f8-111">Compatible</span><span class="sxs-lookup"><span data-stu-id="bf7f8-111">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="bf7f8-112">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="bf7f8-112">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="bf7f8-113">sí</span><span class="sxs-lookup"><span data-stu-id="bf7f8-113">yes</span></span>       |
| [<span data-ttu-id="bf7f8-114">Modelo de sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="bf7f8-114">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="bf7f8-115">sí</span><span class="sxs-lookup"><span data-stu-id="bf7f8-115">yes</span></span>       |
| [<span data-ttu-id="bf7f8-116">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="bf7f8-116">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="bf7f8-117">sí</span><span class="sxs-lookup"><span data-stu-id="bf7f8-117">yes</span></span>       |
| [<span data-ttu-id="bf7f8-118">Shader Model 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf7f8-118">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="bf7f8-119">no</span><span class="sxs-lookup"><span data-stu-id="bf7f8-119">no</span></span>        |
| [<span data-ttu-id="bf7f8-120">Shader Model 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf7f8-120">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="bf7f8-121">no</span><span class="sxs-lookup"><span data-stu-id="bf7f8-121">no</span></span>        |
| [<span data-ttu-id="bf7f8-122">Shader Model 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="bf7f8-122">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="bf7f8-123">no</span><span class="sxs-lookup"><span data-stu-id="bf7f8-123">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="bf7f8-124">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="bf7f8-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7f8-125">Modificadores de instrucciones</span><span class="sxs-lookup"><span data-stu-id="bf7f8-125">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




