---
title: WaveReadLaneFirst función)
description: Devuelve el valor de la expresión para el carril activo de la onda actual con el índice más pequeño.
ms.assetid: 89CA4FD5-4573-42ED-88D3-01C79C69FF6F
keywords:
- WaveReadLaneFirst de función HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneFirst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 04d10e5439b8cd653f7c0a37d3a951167561f964
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984103"
---
# <a name="wavereadlanefirst-function"></a><span data-ttu-id="f19f1-104">WaveReadLaneFirst función)</span><span class="sxs-lookup"><span data-stu-id="f19f1-104">WaveReadLaneFirst function</span></span>

<span data-ttu-id="f19f1-105">Devuelve el valor de la expresión para el carril activo de la onda actual con el índice más pequeño.</span><span class="sxs-lookup"><span data-stu-id="f19f1-105">Returns the value of the expression for the active lane of the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="f19f1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f19f1-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneFirst(
   <type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="f19f1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f19f1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f19f1-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="f19f1-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="f19f1-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="f19f1-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f19f1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f19f1-110">Return value</span></span>

<span data-ttu-id="f19f1-111">El valor resultante es uniforme en toda la onda.</span><span class="sxs-lookup"><span data-stu-id="f19f1-111">The resulting value is uniform across the wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="f19f1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f19f1-112">Remarks</span></span>

<span data-ttu-id="f19f1-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="f19f1-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="f19f1-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="f19f1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f19f1-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="f19f1-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="f19f1-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="f19f1-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




