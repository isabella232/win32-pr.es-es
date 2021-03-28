---
title: ddy_fine función)
description: Calcula un derivado parcial de precisión alta con respecto a la coordenada x del espacio de pantalla. | ddy_fine función)
ms.assetid: 29fcdbc9-470b-4b5b-b18c-f75dd2c87920
keywords:
- ddy_fine de la función HLSL
topic_type:
- apiref
api_name:
- ddy_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2a4cb297180a4988cb049ccebfa4f82571c4655c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104998287"
---
# <a name="ddy_fine-function"></a><span data-ttu-id="95d06-105">\_función DDY Fine</span><span class="sxs-lookup"><span data-stu-id="95d06-105">ddy\_fine function</span></span>

<span data-ttu-id="95d06-106">Calcula un derivado parcial de precisión alta con respecto a la coordenada x del espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="95d06-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="95d06-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="95d06-107">Syntax</span></span>

``` syntax
float ddy_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="95d06-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="95d06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95d06-109">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="95d06-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95d06-110">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="95d06-110">Type: **float**</span></span>

<span data-ttu-id="95d06-111">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="95d06-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95d06-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="95d06-112">Return value</span></span>

<span data-ttu-id="95d06-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="95d06-113">Type: **float**</span></span>

<span data-ttu-id="95d06-114">El derivado parcial de precisión alta de *Value*.</span><span class="sxs-lookup"><span data-stu-id="95d06-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="95d06-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="95d06-115">Remarks</span></span>

<span data-ttu-id="95d06-116">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="95d06-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddy_fine(float2 value);
float3 ddy_fine(float3 value);
float4 ddy_fine(float4 value);  
```

### <a name="minimum-shader-model"></a><span data-ttu-id="95d06-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="95d06-117">Minimum Shader Model</span></span>

<span data-ttu-id="95d06-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="95d06-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="95d06-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="95d06-119">Shader Model</span></span>                                                                | <span data-ttu-id="95d06-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="95d06-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="95d06-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="95d06-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="95d06-122">sí</span><span class="sxs-lookup"><span data-stu-id="95d06-122">yes</span></span>       |



 

<span data-ttu-id="95d06-123">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="95d06-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="95d06-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="95d06-124">Vertex</span></span> | <span data-ttu-id="95d06-125">Casco</span><span class="sxs-lookup"><span data-stu-id="95d06-125">Hull</span></span> | <span data-ttu-id="95d06-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="95d06-126">Domain</span></span> | <span data-ttu-id="95d06-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="95d06-127">Geometry</span></span> | <span data-ttu-id="95d06-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="95d06-128">Pixel</span></span> | <span data-ttu-id="95d06-129">Compute</span><span class="sxs-lookup"><span data-stu-id="95d06-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="95d06-130">x</span><span class="sxs-lookup"><span data-stu-id="95d06-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="95d06-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="95d06-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95d06-132">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="95d06-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="95d06-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="95d06-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




