---
title: WaveActiveAllTrue función)
description: Devuelve true si la expresión es verdadera en todas las calles activas de la ola actual.
ms.assetid: C4EC5A02-6070-4FF4-B855-F597FFFE66F0
keywords:
- WaveActiveAllTrue de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveAllTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a26e0ce757257d6fdd8296239dcf086bff5f1666
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488530"
---
# <a name="waveactivealltrue-function"></a><span data-ttu-id="4abfe-104">WaveActiveAllTrue función)</span><span class="sxs-lookup"><span data-stu-id="4abfe-104">WaveActiveAllTrue function</span></span>

<span data-ttu-id="4abfe-105">Devuelve true si la expresión es verdadera en todas las calles activas de la ola actual.</span><span class="sxs-lookup"><span data-stu-id="4abfe-105">Returns true if the expression is true in all active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="4abfe-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4abfe-106">Syntax</span></span>

``` syntax
bool WaveActiveAllTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="4abfe-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4abfe-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4abfe-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="4abfe-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="4abfe-109">Expresión booleana que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="4abfe-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4abfe-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4abfe-110">Return value</span></span>

<span data-ttu-id="4abfe-111">True si la expresión es verdadera en todas las calles.</span><span class="sxs-lookup"><span data-stu-id="4abfe-111">True if the expression is true in all lanes.</span></span>

## <a name="remarks"></a><span data-ttu-id="4abfe-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4abfe-112">Remarks</span></span>

<span data-ttu-id="4abfe-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="4abfe-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="4abfe-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="4abfe-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abfe-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="4abfe-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="4abfe-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="4abfe-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




