---
title: QuadReadLaneAt función)
description: Devuelve el valor de origen especificado de la calle identificada por el ID. de calle dentro del cuádruple actual.
ms.assetid: 5CD7EE4C-E64E-46A3-ABDC-1BF65D0F96BE
keywords:
- QuadReadLaneAt de función HLSL
topic_type:
- apiref
api_name:
- QuadReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ddc772c2dca66873891483431eab14ad504da77e
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104488536"
---
# <a name="quadreadlaneat-function"></a><span data-ttu-id="b901e-104">QuadReadLaneAt función)</span><span class="sxs-lookup"><span data-stu-id="b901e-104">QuadReadLaneAt function</span></span>

<span data-ttu-id="b901e-105">Devuelve el valor de origen especificado de la calle identificada por el ID. de calle dentro del cuádruple actual.</span><span class="sxs-lookup"><span data-stu-id="b901e-105">Returns the specified source value from the lane identified by the lane ID within the current quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="b901e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b901e-106">Syntax</span></span>


``` syntax
<type> QuadReadLaneAt(
   <type> sourceValue,
   uint   quadLaneID  
);
```



## <a name="parameters"></a><span data-ttu-id="b901e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b901e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b901e-108">*Valor*</span><span class="sxs-lookup"><span data-stu-id="b901e-108">*sourceValue*</span></span> 
</dt> <dd>

<span data-ttu-id="b901e-109">El tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="b901e-109">The requested type.</span></span>

</dd> <dt>

<span data-ttu-id="b901e-110">*quadLaneID*</span><span class="sxs-lookup"><span data-stu-id="b901e-110">*quadLaneID*</span></span> 
</dt> <dd>

<span data-ttu-id="b901e-111">El identificador de la calle; Este será un valor de 0 a 3.</span><span class="sxs-lookup"><span data-stu-id="b901e-111">The lane ID; this will be a value from 0 to 3.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b901e-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b901e-112">Return value</span></span>

<span data-ttu-id="b901e-113">Valor de origen especificado.</span><span class="sxs-lookup"><span data-stu-id="b901e-113">The specified source value.</span></span> <span data-ttu-id="b901e-114">El resultado de esta función es uniforme en todo el cuádruple.</span><span class="sxs-lookup"><span data-stu-id="b901e-114">The result of this function is uniform across the quad.</span></span> <span data-ttu-id="b901e-115">Si la calle de origen está inactiva, los resultados son indefinidos.</span><span class="sxs-lookup"><span data-stu-id="b901e-115">If the source lane is inactive, the results are undefined.</span></span>

## <a name="remarks"></a><span data-ttu-id="b901e-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b901e-116">Remarks</span></span>

<span data-ttu-id="b901e-117">Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="b901e-117">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="b901e-118">Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.</span><span class="sxs-lookup"><span data-stu-id="b901e-118">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="b901e-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="b901e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b901e-120">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="b901e-120">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




