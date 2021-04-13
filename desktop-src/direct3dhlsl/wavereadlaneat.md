---
title: WaveReadLaneAt función)
description: Devuelve el valor de la expresión para el índice de la calle especificado dentro de la onda especificada.
ms.assetid: CA9467D9-8885-4A5D-87F3-5BA40AE78993
keywords:
- WaveReadLaneAt de función HLSL
topic_type:
- apiref
api_name:
- WaveReadLaneAt
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e40940f2df6685a3096da6886ad3bcb6d9ca99af
ms.sourcegitcommit: 4423a9d48f1c90d2ec2eca68e9cae30df1787f25
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/25/2020
ms.locfileid: "104420500"
---
# <a name="wavereadlaneat-function"></a><span data-ttu-id="06715-104">WaveReadLaneAt función)</span><span class="sxs-lookup"><span data-stu-id="06715-104">WaveReadLaneAt function</span></span>

<span data-ttu-id="06715-105">Devuelve el valor de la expresión para el índice de la calle especificado dentro de la onda especificada.</span><span class="sxs-lookup"><span data-stu-id="06715-105">Returns the value of the expression for the given lane index within the specified wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="06715-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06715-106">Syntax</span></span>

``` syntax
<type> WaveReadLaneAt(
   <type> expr,
   uint laneIndex
);
```

## <a name="parameters"></a><span data-ttu-id="06715-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="06715-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06715-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="06715-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="06715-109">La expresión que se va a evaluar.</span><span class="sxs-lookup"><span data-stu-id="06715-109">The expression to evaluate.</span></span>

</dd> <dt>

<span data-ttu-id="06715-110">*laneIndex*</span><span class="sxs-lookup"><span data-stu-id="06715-110">*laneIndex*</span></span> 
</dt> <dd>

<span data-ttu-id="06715-111">Índice de la calle para la que se devolverá el resultado de *expr* .</span><span class="sxs-lookup"><span data-stu-id="06715-111">The index of the lane for which the *expr* result will be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06715-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="06715-112">Return value</span></span>

<span data-ttu-id="06715-113">El valor resultante es el resultado de *expr*.</span><span class="sxs-lookup"><span data-stu-id="06715-113">The resulting value is the result of *expr*.</span></span> <span data-ttu-id="06715-114">Será uniforme si *laneIndex* es uniforme.</span><span class="sxs-lookup"><span data-stu-id="06715-114">It will be uniform if *laneIndex* is uniform.</span></span>

## <a name="remarks"></a><span data-ttu-id="06715-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06715-115">Remarks</span></span>

<span data-ttu-id="06715-116">Esta función es realmente una difusión del valor de laneIndex'th Lane.</span><span class="sxs-lookup"><span data-stu-id="06715-116">This function is effectively a broadcast of the value in the laneIndex’th lane.</span></span>

<span data-ttu-id="06715-117">Esta función se admite desde el modelo de sombreador 6,0, en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="06715-117">This function is supported from shader model 6.0, in the following types of shaders:</span></span>



| <span data-ttu-id="06715-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="06715-118">Vertex</span></span> | <span data-ttu-id="06715-119">Casco</span><span class="sxs-lookup"><span data-stu-id="06715-119">Hull</span></span> | <span data-ttu-id="06715-120">Dominio</span><span class="sxs-lookup"><span data-stu-id="06715-120">Domain</span></span> | <span data-ttu-id="06715-121">Geometría</span><span class="sxs-lookup"><span data-stu-id="06715-121">Geometry</span></span> | <span data-ttu-id="06715-122">Píxel</span><span class="sxs-lookup"><span data-stu-id="06715-122">Pixel</span></span> | <span data-ttu-id="06715-123">Compute</span><span class="sxs-lookup"><span data-stu-id="06715-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="06715-124">x</span><span class="sxs-lookup"><span data-stu-id="06715-124">x</span></span>     | <span data-ttu-id="06715-125">x</span><span class="sxs-lookup"><span data-stu-id="06715-125">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="06715-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="06715-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06715-127">Información general sobre el modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="06715-127">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="06715-128">Modelo de sombreador 6</span><span class="sxs-lookup"><span data-stu-id="06715-128">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




