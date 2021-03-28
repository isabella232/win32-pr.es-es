---
title: WaveActiveBitXor función)
description: Devuelve el XOR bit a bit de todos los valores de la expresión en todas las calles activas de la onda actual y lo replica de nuevo en todas las calles activas.
ms.assetid: A6807D17-1E6E-4997-AB52-32FAB5857219
keywords:
- WaveActiveBitXor de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e55ce8a43311f4f4c428e97bff1e107ab5c7038
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078601"
---
# <a name="waveactivebitxor-function"></a><span data-ttu-id="633a8-104">WaveActiveBitXor función)</span><span class="sxs-lookup"><span data-stu-id="633a8-104">WaveActiveBitXor function</span></span>

<span data-ttu-id="633a8-105">Devuelve el XOR bit a bit de todos los valores de la expresión en todas las calles activas de la onda actual y lo replica de nuevo en todas las calles activas.</span><span class="sxs-lookup"><span data-stu-id="633a8-105">Returns the bitwise XOR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="633a8-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="633a8-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitXor(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="633a8-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="633a8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="633a8-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="633a8-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="633a8-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="633a8-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="633a8-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="633a8-110">Return value</span></span>

<span data-ttu-id="633a8-111">Valor XOR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="633a8-111">The bitwise XOR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="633a8-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="633a8-112">Remarks</span></span>

<span data-ttu-id="633a8-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="633a8-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="633a8-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="633a8-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="633a8-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="633a8-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="633a8-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="633a8-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




