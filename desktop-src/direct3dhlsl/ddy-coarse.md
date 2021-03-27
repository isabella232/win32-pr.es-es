---
title: ddy_coarse función)
description: Calcula un derivado parcial de precisión baja con respecto a la coordenada y del espacio de pantalla.
ms.assetid: f6103cd3-f7ee-41c2-b3cf-9e72ca84b25e
keywords:
- ddy_coarse de la función HLSL
topic_type:
- apiref
api_name:
- ddy_coarse
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b6fef330e919a31e39306742bb03280454d47626
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076882"
---
# <a name="ddy_coarse-function"></a><span data-ttu-id="d3db7-104">DDY \_ función gruesa</span><span class="sxs-lookup"><span data-stu-id="d3db7-104">ddy\_coarse function</span></span>

<span data-ttu-id="d3db7-105">Calcula un derivado parcial de precisión baja con respecto a la coordenada y del espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="d3db7-105">Computes a low precision partial derivative with respect to the screen-space y-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3db7-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d3db7-106">Syntax</span></span>

``` syntax
float ddy_coarse(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="d3db7-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d3db7-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3db7-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="d3db7-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3db7-109">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d3db7-109">Type: **float**</span></span>

<span data-ttu-id="d3db7-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="d3db7-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3db7-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d3db7-111">Return value</span></span>

<span data-ttu-id="d3db7-112">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="d3db7-112">Type: **float**</span></span>

<span data-ttu-id="d3db7-113">Derivado parcial de precisión baja de *Value*.</span><span class="sxs-lookup"><span data-stu-id="d3db7-113">The low precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3db7-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d3db7-114">Remarks</span></span>

<span data-ttu-id="d3db7-115">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="d3db7-115">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_coarse(float2 value);
float3 ddy_coarse(float3 value);
float4 ddy_coarse(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="d3db7-116">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="d3db7-116">Minimum Shader Model</span></span>

<span data-ttu-id="d3db7-117">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="d3db7-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="d3db7-118">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="d3db7-118">Shader Model</span></span>                                                                | <span data-ttu-id="d3db7-119">Compatible</span><span class="sxs-lookup"><span data-stu-id="d3db7-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="d3db7-120">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="d3db7-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="d3db7-121">sí</span><span class="sxs-lookup"><span data-stu-id="d3db7-121">yes</span></span>       |



 

<span data-ttu-id="d3db7-122">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="d3db7-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="d3db7-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="d3db7-123">Vertex</span></span> | <span data-ttu-id="d3db7-124">Casco</span><span class="sxs-lookup"><span data-stu-id="d3db7-124">Hull</span></span> | <span data-ttu-id="d3db7-125">Dominio</span><span class="sxs-lookup"><span data-stu-id="d3db7-125">Domain</span></span> | <span data-ttu-id="d3db7-126">Geometría</span><span class="sxs-lookup"><span data-stu-id="d3db7-126">Geometry</span></span> | <span data-ttu-id="d3db7-127">Píxel</span><span class="sxs-lookup"><span data-stu-id="d3db7-127">Pixel</span></span> | <span data-ttu-id="d3db7-128">Compute</span><span class="sxs-lookup"><span data-stu-id="d3db7-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="d3db7-129">x</span><span class="sxs-lookup"><span data-stu-id="d3db7-129">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="d3db7-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="d3db7-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3db7-131">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="d3db7-131">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="d3db7-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="d3db7-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




