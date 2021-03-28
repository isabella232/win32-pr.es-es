---
title: QuadReadAcrossX función)
description: Devuelve el valor local especificado leído de la otra calle de este cuádruple en la dirección X.
ms.assetid: 7A7E0623-30EC-4167-90A5-D79E10A394CC
keywords:
- QuadReadAcrossX de función HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cd41b0bd84861d23153f02ba6328d17b70287866
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104149730"
---
# <a name="quadreadacrossx-function"></a><span data-ttu-id="4981f-104">QuadReadAcrossX función)</span><span class="sxs-lookup"><span data-stu-id="4981f-104">QuadReadAcrossX function</span></span>

<span data-ttu-id="4981f-105">Devuelve el valor local especificado leído de la otra calle de este cuádruple en la dirección X.</span><span class="sxs-lookup"><span data-stu-id="4981f-105">Returns the specified local value read from the other lane in this quad in the X direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="4981f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4981f-106">Syntax</span></span>

``` syntax
<type> QuadReadAcrossX(
   <type> localValue
);
```

## <a name="parameters"></a><span data-ttu-id="4981f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4981f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4981f-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="4981f-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="4981f-109">El tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="4981f-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4981f-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4981f-110">Return value</span></span>

<span data-ttu-id="4981f-111">Valor local especificado.</span><span class="sxs-lookup"><span data-stu-id="4981f-111">The specified local value.</span></span> <span data-ttu-id="4981f-112">Si la calle de origen está inactiva, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="4981f-112">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="4981f-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4981f-113">Remarks</span></span>

<span data-ttu-id="4981f-114">Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="4981f-114">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="4981f-115">Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.</span><span class="sxs-lookup"><span data-stu-id="4981f-115">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="4981f-116">Vea también</span><span class="sxs-lookup"><span data-stu-id="4981f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4981f-117">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="4981f-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




