---
title: WaveGetLaneCount función)
description: Devuelve el número de calles de una onda en esta arquitectura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- WaveGetLaneCount de función HLSL
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104421624"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="f6d69-104">WaveGetLaneCount función)</span><span class="sxs-lookup"><span data-stu-id="f6d69-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="f6d69-105">Devuelve el número de calles de una onda en esta arquitectura.</span><span class="sxs-lookup"><span data-stu-id="f6d69-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6d69-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6d69-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="f6d69-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f6d69-107">Parameters</span></span>

<span data-ttu-id="f6d69-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="f6d69-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f6d69-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f6d69-109">Return value</span></span>

<span data-ttu-id="f6d69-110">El resultado estará entre 4 y 128, e incluye todas las ondas: las calles activas, inactivas y/o auxiliares.</span><span class="sxs-lookup"><span data-stu-id="f6d69-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="f6d69-111">El resultado devuelto por esta función puede variar significativamente según la implementación del controlador.</span><span class="sxs-lookup"><span data-stu-id="f6d69-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6d69-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6d69-112">Remarks</span></span>

<span data-ttu-id="f6d69-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="f6d69-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="f6d69-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f6d69-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="f6d69-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6d69-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6d69-116">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="f6d69-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="f6d69-117">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="f6d69-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




