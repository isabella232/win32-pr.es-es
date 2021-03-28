---
title: WaveActiveAllEqual función)
description: Devuelve true si la expresión es la misma para cada carril activo de la ola actual (y, por tanto, uniforme en ella).
ms.assetid: E0A051A8-0ADD-4EC7-8D9A-8820CED9DA9D
keywords:
- WaveActiveAllEqual de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllEqual
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 34745e428fcd4453ce7274fc2a5accc6185f5b10
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "103797248"
---
# <a name="waveactiveallequal-function"></a><span data-ttu-id="00e39-104">WaveActiveAllEqual función)</span><span class="sxs-lookup"><span data-stu-id="00e39-104">WaveActiveAllEqual function</span></span>

<span data-ttu-id="00e39-105">Devuelve true si la expresión es la misma para cada carril activo de la ola actual (y, por tanto, uniforme en ella).</span><span class="sxs-lookup"><span data-stu-id="00e39-105">Returns true if the expression is the same for every active lane in the current wave (and thus uniform across it).</span></span>

## <a name="syntax"></a><span data-ttu-id="00e39-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="00e39-106">Syntax</span></span>


``` syntax
bool WaveActiveAllEqual(
   <type> expr
);
```



## <a name="parameters"></a><span data-ttu-id="00e39-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="00e39-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00e39-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="00e39-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="00e39-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="00e39-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00e39-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="00e39-110">Return value</span></span>

<span data-ttu-id="00e39-111">True si la expresión es la misma para cada carril activo de la ola actual.</span><span class="sxs-lookup"><span data-stu-id="00e39-111">True if the expression is the same for every active lane in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="00e39-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="00e39-112">Remarks</span></span>

<span data-ttu-id="00e39-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="00e39-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="00e39-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="00e39-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00e39-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="00e39-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="00e39-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="00e39-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




