---
title: QuadReadAcrossY función)
description: Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección Y.
ms.assetid: 6C03D1E6-433F-4CCA-A5EA-C3F34BB2B93B
keywords:
- QuadReadAcrossY de función HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72b5ede0df733e60ba4b1bcc01a04f1daaedc708
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104984099"
---
# <a name="quadreadacrossy-function"></a><span data-ttu-id="6f6d1-104">QuadReadAcrossY función)</span><span class="sxs-lookup"><span data-stu-id="6f6d1-104">QuadReadAcrossY function</span></span>

<span data-ttu-id="6f6d1-105">Devuelve el valor de origen especificado leído de la otra calle de este cuádruple en la dirección Y.</span><span class="sxs-lookup"><span data-stu-id="6f6d1-105">Returns the specified source value read from the other lane in this quad in the Y direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f6d1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6f6d1-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossY(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="6f6d1-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="6f6d1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f6d1-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="6f6d1-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="6f6d1-109">El tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="6f6d1-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f6d1-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6f6d1-110">Return value</span></span>

<span data-ttu-id="6f6d1-111">Valor de origen especificado.</span><span class="sxs-lookup"><span data-stu-id="6f6d1-111">The specified source value.</span></span> <span data-ttu-id="6f6d1-112">Si la calle de origen está inactiva, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="6f6d1-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f6d1-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6f6d1-113">Remarks</span></span>

<span data-ttu-id="6f6d1-114">Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="6f6d1-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="6f6d1-115">Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.</span><span class="sxs-lookup"><span data-stu-id="6f6d1-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="6f6d1-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="6f6d1-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f6d1-117">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="6f6d1-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




