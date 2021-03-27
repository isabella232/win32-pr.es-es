---
title: WaveActiveAnyTrue función)
description: Devuelve true si la expresión es verdadera en cualquiera de las calles activas de la onda actual.
ms.assetid: 203E2E1D-0AA2-4E4A-80F7-D1FE7579A742
keywords:
- WaveActiveAnyTrue de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveAnyTrue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 16801c4329f5bc0bf325d8bb67e8c0bb94887678
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997173"
---
# <a name="waveactiveanytrue-function"></a><span data-ttu-id="44fb1-104">WaveActiveAnyTrue función)</span><span class="sxs-lookup"><span data-stu-id="44fb1-104">WaveActiveAnyTrue function</span></span>

<span data-ttu-id="44fb1-105">Devuelve true si la expresión es verdadera en cualquiera de las calles activas de la onda actual.</span><span class="sxs-lookup"><span data-stu-id="44fb1-105">Returns true if the expression is true in any of the active lanes in the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="44fb1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="44fb1-106">Syntax</span></span>

``` syntax
bool WaveActiveAnyTrue(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="44fb1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="44fb1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44fb1-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="44fb1-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="44fb1-109">Expresión booleana que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="44fb1-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44fb1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="44fb1-110">Return value</span></span>

<span data-ttu-id="44fb1-111">True si la expresión es verdadera en cualquier calle.</span><span class="sxs-lookup"><span data-stu-id="44fb1-111">True if the expression is true in any lane.</span></span>

## <a name="remarks"></a><span data-ttu-id="44fb1-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="44fb1-112">Remarks</span></span>

<span data-ttu-id="44fb1-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="44fb1-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="44fb1-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="44fb1-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44fb1-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="44fb1-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="44fb1-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="44fb1-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




