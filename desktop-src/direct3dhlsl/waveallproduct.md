---
title: WaveActiveProduct función)
description: Multiplica los valores de la expresión en todas las calles activas de la ola actual y los replica de nuevo en todas las calles activas.
ms.assetid: B259244D-C993-4F4A-AF09-F077D99AD025
keywords:
- WaveActiveProduct de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveProduct
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8e1d400541a2654657c1a462c38494d20af13e6
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103904900"
---
# <a name="waveactiveproduct-function"></a><span data-ttu-id="45815-104">WaveActiveProduct función)</span><span class="sxs-lookup"><span data-stu-id="45815-104">WaveActiveProduct function</span></span>

<span data-ttu-id="45815-105">Multiplica los valores de la expresión en todas las calles activas de la ola actual y los replica de nuevo en todas las calles activas.</span><span class="sxs-lookup"><span data-stu-id="45815-105">Multiplies the values of the expression together across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="45815-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="45815-106">Syntax</span></span>

``` syntax
<type> WaveActiveProduct(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="45815-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="45815-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45815-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="45815-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="45815-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="45815-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45815-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="45815-110">Return value</span></span>

<span data-ttu-id="45815-111">Valor del producto.</span><span class="sxs-lookup"><span data-stu-id="45815-111">The product value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45815-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="45815-112">Remarks</span></span>

<span data-ttu-id="45815-113">El orden de las operaciones es indefinido.</span><span class="sxs-lookup"><span data-stu-id="45815-113">The order of operations is undefined.</span></span>

<span data-ttu-id="45815-114">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="45815-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="45815-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="45815-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45815-116">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="45815-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="45815-117">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="45815-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




