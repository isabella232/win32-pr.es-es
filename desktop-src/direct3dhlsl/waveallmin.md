---
title: WaveActiveMin función)
description: Devuelve el valor mínimo de la expresión en todas las calles activas de la onda actual lo replica de nuevo en todas las calles activas.
ms.assetid: BA762C02-894C-4AF9-A226-C1E3AAC286FF
keywords:
- WaveActiveMin de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveMin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91555df354ab2b7ffc447a9422c4811ae23e6e0c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078602"
---
# <a name="waveactivemin-function"></a><span data-ttu-id="19f64-104">WaveActiveMin función)</span><span class="sxs-lookup"><span data-stu-id="19f64-104">WaveActiveMin function</span></span>

<span data-ttu-id="19f64-105">Devuelve el valor mínimo de la expresión en todas las calles activas de la onda actual lo replica de nuevo en todas las calles activas.</span><span class="sxs-lookup"><span data-stu-id="19f64-105">Returns the minimum value of the expression across all active lanes in the current wave replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="19f64-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="19f64-106">Syntax</span></span>

``` syntax
<type> WaveActiveMin(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="19f64-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19f64-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19f64-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="19f64-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="19f64-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="19f64-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19f64-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19f64-110">Return value</span></span>

<span data-ttu-id="19f64-111">Valor mínimo.</span><span class="sxs-lookup"><span data-stu-id="19f64-111">The minimum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19f64-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="19f64-112">Remarks</span></span>

<span data-ttu-id="19f64-113">El orden de las operaciones es indefinido.</span><span class="sxs-lookup"><span data-stu-id="19f64-113">The order of operations is undefined.</span></span>

<span data-ttu-id="19f64-114">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="19f64-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="19f64-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="19f64-115">Examples</span></span>

``` syntax
 float3 minPos = WaveActiveMin( myPoint.position );
    BoundingBox.min = min( minPos, BoundingBox.min );
```

## <a name="see-also"></a><span data-ttu-id="19f64-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="19f64-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19f64-117">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="19f64-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="19f64-118">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="19f64-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




