---
title: QuadReadAcrossDiagonal función)
description: Devuelve el valor local especificado que se lee desde la calle opuesta en diagonal en esta cuádruple.
ms.assetid: 2914F1F9-5CE2-437A-ADDB-4955D2C1490B
keywords:
- QuadReadAcrossDiagonal de función HLSL
topic_type:
- apiref
api_name:
- QuadReadAcrossDiagonal
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0e208a022f339e69ea63120db1f67070fa4dfed7
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/04/2020
ms.locfileid: "104997181"
---
# <a name="quadreadacrossdiagonal-function"></a><span data-ttu-id="feafb-104">QuadReadAcrossDiagonal función)</span><span class="sxs-lookup"><span data-stu-id="feafb-104">QuadReadAcrossDiagonal function</span></span>

<span data-ttu-id="feafb-105">Devuelve el valor local especificado que se lee desde la calle opuesta en diagonal en esta cuádruple.</span><span class="sxs-lookup"><span data-stu-id="feafb-105">Returns the specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="syntax"></a><span data-ttu-id="feafb-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="feafb-106">Syntax</span></span>


``` syntax
<type> QuadReadAcrossDiagonal(
   <type> localValue
);
```



## <a name="parameters"></a><span data-ttu-id="feafb-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="feafb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feafb-108">*localValue*</span><span class="sxs-lookup"><span data-stu-id="feafb-108">*localValue*</span></span> 
</dt> <dd>

<span data-ttu-id="feafb-109">El tipo solicitado.</span><span class="sxs-lookup"><span data-stu-id="feafb-109">The requested type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feafb-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="feafb-110">Return value</span></span>

<span data-ttu-id="feafb-111">Valor local especificado que se lee desde la calle opuesta en diagonal en esta cuádruple.</span><span class="sxs-lookup"><span data-stu-id="feafb-111">The specified local value which is read from the diagonally opposite lane in this quad.</span></span>

## <a name="remarks"></a><span data-ttu-id="feafb-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="feafb-112">Remarks</span></span>

<span data-ttu-id="feafb-113">Para obtener más información sobre las cuádruples, consulte [información general sobre el modelo de sombreador 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span><span class="sxs-lookup"><span data-stu-id="feafb-113">For more information on quads, refer to [Overview of Shader Model 6](hlsl-shader-model-6-0-features-for-direct3d-12.md).</span></span>

<span data-ttu-id="feafb-114">Esta función se admite desde el modelo de sombreador 6,0 solo en los sombreadores de píxeles y de cálculo.</span><span class="sxs-lookup"><span data-stu-id="feafb-114">This function is supported from shader model 6.0 only in pixel and compute shaders.</span></span>



 

## <a name="see-also"></a><span data-ttu-id="feafb-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="feafb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feafb-116">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="feafb-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




