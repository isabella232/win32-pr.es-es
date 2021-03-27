---
title: WaveActiveSum función)
description: Suma el valor de la expresión en todas las calles activas de la ola actual y lo replica en todas las calles de la ola actual.
ms.assetid: 94CEF4AA-D6DE-4B00-9743-F491F255FE3D
keywords:
- WaveActiveSum de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveSum
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b98ecf2521841b9da73e1b917d44f1d91b7876d2
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103995734"
---
# <a name="waveactivesum-function"></a><span data-ttu-id="6883d-104">WaveActiveSum función)</span><span class="sxs-lookup"><span data-stu-id="6883d-104">WaveActiveSum function</span></span>

<span data-ttu-id="6883d-105">Suma el valor de la expresión en todas las calles activas de la ola actual y lo replica en todas las calles de la ola actual.</span><span class="sxs-lookup"><span data-stu-id="6883d-105">Sums up the value of the expression across all active lanes in the current wave and replicates it to all lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="6883d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6883d-106">Syntax</span></span>

``` syntax
<type> WaveActiveSum(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="6883d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6883d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6883d-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="6883d-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="6883d-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="6883d-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6883d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6883d-110">Return value</span></span>

<span data-ttu-id="6883d-111">Valor de suma.</span><span class="sxs-lookup"><span data-stu-id="6883d-111">The sum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6883d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6883d-112">Remarks</span></span>

<span data-ttu-id="6883d-113">El orden de las operaciones es indefinido.</span><span class="sxs-lookup"><span data-stu-id="6883d-113">The order of operations is undefined.</span></span>

<span data-ttu-id="6883d-114">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="6883d-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="6883d-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="6883d-115">Examples</span></span>

``` syntax
float3 total = WaveActiveSum( position ); // sum positions in wave
float3 center = total/count;           // compute average of these positions
```

## <a name="see-also"></a><span data-ttu-id="6883d-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="6883d-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6883d-117">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="6883d-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="6883d-118">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="6883d-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




