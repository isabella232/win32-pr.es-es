---
title: WaveActiveMax función)
description: Devuelve el valor máximo de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.
ms.assetid: 19101C56-2618-4F34-8725-DF92198ABDA4
keywords:
- WaveActiveMax de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c0fd10f578d598c326cdfb4cf943d3a35fe78a9
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2020
ms.locfileid: "104421676"
---
# <a name="waveactivemax-function"></a><span data-ttu-id="d0b31-104">WaveActiveMax función)</span><span class="sxs-lookup"><span data-stu-id="d0b31-104">WaveActiveMax function</span></span>

<span data-ttu-id="d0b31-105">Devuelve el valor máximo de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.</span><span class="sxs-lookup"><span data-stu-id="d0b31-105">Returns the maximum value of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b31-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d0b31-106">Syntax</span></span>

``` syntax
<type> WaveActiveMax(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="d0b31-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d0b31-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b31-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="d0b31-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="d0b31-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="d0b31-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b31-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d0b31-110">Return value</span></span>

<span data-ttu-id="d0b31-111">Valor máximo.</span><span class="sxs-lookup"><span data-stu-id="d0b31-111">The maximum value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b31-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d0b31-112">Remarks</span></span>

<span data-ttu-id="d0b31-113">El orden de las operaciones es indefinido.</span><span class="sxs-lookup"><span data-stu-id="d0b31-113">The order of operations is undefined.</span></span>

<span data-ttu-id="d0b31-114">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="d0b31-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="d0b31-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d0b31-115">Examples</span></span>

``` syntax
 float3 maxPos = WaveActiveMax( myPoint.position );
    BoundingBox.max = max( maxPos, BoundingBox.max );
```

## <a name="see-also"></a><span data-ttu-id="d0b31-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0b31-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0b31-117">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="d0b31-117">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="d0b31-118">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="d0b31-118">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




