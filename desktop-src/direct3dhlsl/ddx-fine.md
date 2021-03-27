---
title: ddx_fine función)
description: Calcula un derivado parcial de precisión alta con respecto a la coordenada x del espacio de pantalla. | ddx_fine función)
ms.assetid: 41062d6f-2b7f-4594-a6de-da37ded5d444
keywords:
- ddx_fine de la función HLSL
topic_type:
- apiref
api_name:
- ddx_fine
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c1a579ba5899cf4d3ac3f25ef5a40337f6291977
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104986755"
---
# <a name="ddx_fine-function"></a><span data-ttu-id="85412-105">\_función DDX Fine</span><span class="sxs-lookup"><span data-stu-id="85412-105">ddx\_fine function</span></span>

<span data-ttu-id="85412-106">Calcula un derivado parcial de precisión alta con respecto a la coordenada x del espacio de pantalla.</span><span class="sxs-lookup"><span data-stu-id="85412-106">Computes a high precision partial derivative with respect to the screen-space x-coordinate.</span></span>

## <a name="syntax"></a><span data-ttu-id="85412-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="85412-107">Syntax</span></span>

``` syntax
float ddx_fine(
  in float value
);
```

## <a name="parameters"></a><span data-ttu-id="85412-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="85412-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85412-109">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="85412-109">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="85412-110">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="85412-110">Type: **float**</span></span>

<span data-ttu-id="85412-111">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="85412-111">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85412-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="85412-112">Return value</span></span>

<span data-ttu-id="85412-113">Tipo: **float**</span><span class="sxs-lookup"><span data-stu-id="85412-113">Type: **float**</span></span>

<span data-ttu-id="85412-114">El derivado parcial de precisión alta de *Value*.</span><span class="sxs-lookup"><span data-stu-id="85412-114">The high precision partial derivative of *value*.</span></span>

## <a name="remarks"></a><span data-ttu-id="85412-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="85412-115">Remarks</span></span>

<span data-ttu-id="85412-116">También están disponibles las siguientes versiones sobrecargadas:</span><span class="sxs-lookup"><span data-stu-id="85412-116">The following overloaded versions are also available:</span></span>

``` syntax
float2 ddx_fine(float2 value);
float3 ddx_fine(float3 value);
float4 ddx_fine(float4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="85412-117">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="85412-117">Minimum Shader Model</span></span>

<span data-ttu-id="85412-118">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="85412-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="85412-119">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="85412-119">Shader Model</span></span>                                                                | <span data-ttu-id="85412-120">Compatible</span><span class="sxs-lookup"><span data-stu-id="85412-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="85412-121">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="85412-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="85412-122">sí</span><span class="sxs-lookup"><span data-stu-id="85412-122">yes</span></span>       |



 

<span data-ttu-id="85412-123">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="85412-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="85412-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="85412-124">Vertex</span></span> | <span data-ttu-id="85412-125">Casco</span><span class="sxs-lookup"><span data-stu-id="85412-125">Hull</span></span> | <span data-ttu-id="85412-126">Dominio</span><span class="sxs-lookup"><span data-stu-id="85412-126">Domain</span></span> | <span data-ttu-id="85412-127">Geometría</span><span class="sxs-lookup"><span data-stu-id="85412-127">Geometry</span></span> | <span data-ttu-id="85412-128">Píxel</span><span class="sxs-lookup"><span data-stu-id="85412-128">Pixel</span></span> | <span data-ttu-id="85412-129">Compute</span><span class="sxs-lookup"><span data-stu-id="85412-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | <span data-ttu-id="85412-130">x</span><span class="sxs-lookup"><span data-stu-id="85412-130">x</span></span>     |         |



 

## <a name="see-also"></a><span data-ttu-id="85412-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="85412-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85412-132">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="85412-132">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="85412-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="85412-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




