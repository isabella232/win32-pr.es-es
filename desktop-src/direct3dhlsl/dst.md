---
title: DST (función)
description: Calcula un vector de distancia. | DST (función)
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- DST de la función HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "103914342"
---
# <a name="dst-function"></a><span data-ttu-id="ac4ca-105">DST (función)</span><span class="sxs-lookup"><span data-stu-id="ac4ca-105">dst function</span></span>

<span data-ttu-id="ac4ca-106">Calcula un vector de distancia.</span><span class="sxs-lookup"><span data-stu-id="ac4ca-106">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac4ca-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ac4ca-107">Syntax</span></span>

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a><span data-ttu-id="ac4ca-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ac4ca-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac4ca-109">*src0* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac4ca-109">*src0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4ca-110">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="ac4ca-110">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="ac4ca-111">Primer vector.</span><span class="sxs-lookup"><span data-stu-id="ac4ca-111">The first vector.</span></span>

</dd> <dt>

<span data-ttu-id="ac4ca-112">*SRC1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ac4ca-112">*src1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac4ca-113">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="ac4ca-113">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="ac4ca-114">Segundo vector.</span><span class="sxs-lookup"><span data-stu-id="ac4ca-114">The second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac4ca-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac4ca-115">Return value</span></span>

<span data-ttu-id="ac4ca-116">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="ac4ca-116">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="ac4ca-117">Vector de distancia calculado.</span><span class="sxs-lookup"><span data-stu-id="ac4ca-117">The computed distance vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="ac4ca-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ac4ca-118">Remarks</span></span>

<span data-ttu-id="ac4ca-119">Esta función intrínseca proporciona la misma funcionalidad que la instrucción [DST](dst---vs.md)del sombreador de vértices.</span><span class="sxs-lookup"><span data-stu-id="ac4ca-119">This intrinsic function provides the same functionality as the Vertex Shader instruction [dst](dst---vs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="ac4ca-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="ac4ca-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac4ca-121">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="ac4ca-121">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




