---
title: WaveGetLaneIndex función)
description: Devuelve el índice de la calle actual dentro de la onda actual.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- WaveGetLaneIndex de función HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997176"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="33431-104">WaveGetLaneIndex función)</span><span class="sxs-lookup"><span data-stu-id="33431-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="33431-105">Devuelve el índice de la calle actual dentro de la onda actual.</span><span class="sxs-lookup"><span data-stu-id="33431-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="33431-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="33431-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="33431-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="33431-107">Parameters</span></span>

<span data-ttu-id="33431-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="33431-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33431-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="33431-109">Return value</span></span>

<span data-ttu-id="33431-110">Índice de la calle actual.</span><span class="sxs-lookup"><span data-stu-id="33431-110">The current lane index.</span></span> <span data-ttu-id="33431-111">El resultado estará entre 0 y el resultado devuelto por [**WaveGetLaneCount**](wavegetlanecount.md).</span><span class="sxs-lookup"><span data-stu-id="33431-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="33431-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="33431-112">Remarks</span></span>

<span data-ttu-id="33431-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="33431-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="33431-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="33431-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33431-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="33431-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="33431-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="33431-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




