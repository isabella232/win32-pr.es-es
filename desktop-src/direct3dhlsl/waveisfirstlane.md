---
title: WaveIsFirstLane función)
description: Devuelve true solo para el carril activo en la ola actual con el índice más pequeño.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- WaveIsFirstLane de función HLSL
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104359521"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="7d5fd-104">WaveIsFirstLane función)</span><span class="sxs-lookup"><span data-stu-id="7d5fd-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="7d5fd-105">Devuelve true solo para el carril activo en la ola actual con el índice más pequeño.</span><span class="sxs-lookup"><span data-stu-id="7d5fd-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d5fd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7d5fd-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="7d5fd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7d5fd-107">Parameters</span></span>

<span data-ttu-id="7d5fd-108">Esta función no tiene parámetros.</span><span class="sxs-lookup"><span data-stu-id="7d5fd-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7d5fd-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7d5fd-109">Return value</span></span>

<span data-ttu-id="7d5fd-110">True solo para el carril activo en la ola actual con el índice más pequeño.</span><span class="sxs-lookup"><span data-stu-id="7d5fd-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="7d5fd-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d5fd-111">Remarks</span></span>

<span data-ttu-id="7d5fd-112">Esta función se puede utilizar para identificar las operaciones que se van a ejecutar solo una vez por cada onda.</span><span class="sxs-lookup"><span data-stu-id="7d5fd-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="7d5fd-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="7d5fd-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="7d5fd-114">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7d5fd-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="7d5fd-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="7d5fd-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5fd-116">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="7d5fd-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="7d5fd-117">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="7d5fd-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




