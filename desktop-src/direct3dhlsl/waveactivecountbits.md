---
title: WaveActiveCountBits función)
description: Cuenta el número de variables Booleanas que se evalúan como true en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- WaveActiveCountBits de función HLSL
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/07/2020
ms.locfileid: "104359551"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="69aee-104">WaveActiveCountBits función)</span><span class="sxs-lookup"><span data-stu-id="69aee-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="69aee-105">Cuenta el número de variables Booleanas que se evalúan como true en todas las calles activas de la onda actual y replica el resultado en todas las calles de la onda.</span><span class="sxs-lookup"><span data-stu-id="69aee-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="69aee-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69aee-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="69aee-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="69aee-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69aee-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="69aee-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="69aee-109">Variables Booleanas que se van a evaluar.</span><span class="sxs-lookup"><span data-stu-id="69aee-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="69aee-110">Proporcionar un valor booleano true explícito devuelve el número de calles activas.</span><span class="sxs-lookup"><span data-stu-id="69aee-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69aee-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="69aee-111">Return value</span></span>

<span data-ttu-id="69aee-112">El número de que se evalúa como true en todas las calles activas de la ola actual.</span><span class="sxs-lookup"><span data-stu-id="69aee-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="69aee-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69aee-113">Remarks</span></span>

<span data-ttu-id="69aee-114">Esta función se admite desde el modelo de sombreador 6,0 en todas las fases del sombreador.</span><span class="sxs-lookup"><span data-stu-id="69aee-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="69aee-115">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="69aee-115">Examples</span></span>

<span data-ttu-id="69aee-116">Esto se puede implementar de forma más eficaz que un WaveActiveSum completo, tal y como se describe en el ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="69aee-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="69aee-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="69aee-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69aee-118">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="69aee-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="69aee-119">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="69aee-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




