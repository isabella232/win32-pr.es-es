---
title: WaveActiveBallot función)
description: Devuelve un uint4 que contiene una máscara de máscara de la evaluación de la expresión booleana para todas las calles activas de la ola actual.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- WaveActiveBallot de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104533597"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="1ee65-104">WaveActiveBallot función)</span><span class="sxs-lookup"><span data-stu-id="1ee65-104">WaveActiveBallot function</span></span>

<span data-ttu-id="1ee65-105">Devuelve un uint4 que contiene una máscara de máscara de la evaluación de la expresión booleana para todas las calles activas de la ola actual.</span><span class="sxs-lookup"><span data-stu-id="1ee65-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="1ee65-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1ee65-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="1ee65-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1ee65-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ee65-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="1ee65-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="1ee65-109">Expresión booleana que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="1ee65-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ee65-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1ee65-110">Return value</span></span>

<span data-ttu-id="1ee65-111">Un uint4 que contiene una máscara de máscara de la evaluación de la expresión booleana para todas las calles activas de la ola actual.</span><span class="sxs-lookup"><span data-stu-id="1ee65-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="1ee65-112">El bit menos significativo corresponde a la calle con el índice cero.</span><span class="sxs-lookup"><span data-stu-id="1ee65-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="1ee65-113">Los bits correspondientes a las calles inactivas serán cero.</span><span class="sxs-lookup"><span data-stu-id="1ee65-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="1ee65-114">Los bits que son mayores o iguales que [**WaveGetLaneCount**](wavegetlanecount.md) serán cero.</span><span class="sxs-lookup"><span data-stu-id="1ee65-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ee65-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1ee65-115">Remarks</span></span>

<span data-ttu-id="1ee65-116">Diferentes GPU tienen distintos anchos de procesador SIMD (recuentos de carril).</span><span class="sxs-lookup"><span data-stu-id="1ee65-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="1ee65-117">La mayoría de estas funciones **WaveXXX** pueden funcionar en el nivel de abstracción donde se oculta el ancho de la máquina SIMD.</span><span class="sxs-lookup"><span data-stu-id="1ee65-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="1ee65-118">Para maximizar la portabilidad del código entre GPU, utilice los intrínsecos que no se basan en el ancho de la máquina.</span><span class="sxs-lookup"><span data-stu-id="1ee65-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="1ee65-119">Por ejemplo, use:</span><span class="sxs-lookup"><span data-stu-id="1ee65-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="1ee65-120">En lugar de:</span><span class="sxs-lookup"><span data-stu-id="1ee65-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="1ee65-121">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="1ee65-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="1ee65-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="1ee65-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="1ee65-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="1ee65-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ee65-124">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1ee65-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="1ee65-125">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1ee65-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




