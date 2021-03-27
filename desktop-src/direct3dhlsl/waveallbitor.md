---
title: WaveActiveBitOr función)
description: Devuelve la operación OR bit a bit de todos los valores de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.
ms.assetid: FC8E5987-DAA7-41E6-A1AB-AA0E6A82CFC7
keywords:
- WaveActiveBitOr de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveBitOr
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6870ac8406a581e358b00ef728562dc59118a933
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104078603"
---
# <a name="waveactivebitor-function"></a><span data-ttu-id="08569-104">WaveActiveBitOr función)</span><span class="sxs-lookup"><span data-stu-id="08569-104">WaveActiveBitOr function</span></span>

<span data-ttu-id="08569-105">Devuelve la operación OR bit a bit de todos los valores de la expresión en todas las calles activas de la ola actual y lo replica de nuevo en todas las calles activas.</span><span class="sxs-lookup"><span data-stu-id="08569-105">Returns the bitwise OR of all the values of the expression across all active lanes in the current wave and replicates it back to all active lanes.</span></span>

## <a name="syntax"></a><span data-ttu-id="08569-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="08569-106">Syntax</span></span>

``` syntax
<int_type> WaveActiveBitOr(
   <int_type> expr
);
```

## <a name="parameters"></a><span data-ttu-id="08569-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="08569-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08569-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="08569-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="08569-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="08569-109">The expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08569-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="08569-110">Return value</span></span>

<span data-ttu-id="08569-111">Valor OR bit a bit.</span><span class="sxs-lookup"><span data-stu-id="08569-111">The bitwise OR value.</span></span>

## <a name="remarks"></a><span data-ttu-id="08569-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="08569-112">Remarks</span></span>

<span data-ttu-id="08569-113">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="08569-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="08569-114">Vea también</span><span class="sxs-lookup"><span data-stu-id="08569-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08569-115">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="08569-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="08569-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="08569-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




