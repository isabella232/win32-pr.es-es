---
title: asdouble (función)
description: Reinterpreta un valor de conversión (valores de 2 32 bits) en un tipo Double.
ms.assetid: 55e5276d-81e1-4e7e-8cb4-0beb57d2fb7f
keywords:
- función de dos funciones HLSL
topic_type:
- apiref
api_name:
- asdouble
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: caa2c83ee01739a2e2ee9595d0a26e1bdb80fef1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076901"
---
# <a name="asdouble-function"></a><span data-ttu-id="8fb0f-104">asdouble (función)</span><span class="sxs-lookup"><span data-stu-id="8fb0f-104">asdouble function</span></span>

<span data-ttu-id="8fb0f-105">Reinterpreta un valor de conversión (valores de 2 32 bits) en un tipo Double.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-105">Reinterprets a cast value (two 32-bit values) into a double.</span></span>

## <a name="syntax"></a><span data-ttu-id="8fb0f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8fb0f-106">Syntax</span></span>

``` syntax
double asdouble(
  in uint lowbits,
  in uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="8fb0f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8fb0f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fb0f-108">*lowbits* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fb0f-108">*lowbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb0f-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8fb0f-109">Type: **uint**</span></span>

<span data-ttu-id="8fb0f-110">Patrón de 32 bits bajo del valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-110">The low 32-bit pattern of the input value.</span></span>

</dd> <dt>

<span data-ttu-id="8fb0f-111">*highbits* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="8fb0f-111">*highbits* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8fb0f-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="8fb0f-112">Type: **uint**</span></span>

<span data-ttu-id="8fb0f-113">El patrón de 32 bits alto del valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-113">The high 32-bit pattern of the input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8fb0f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8fb0f-114">Return value</span></span>

<span data-ttu-id="8fb0f-115">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="8fb0f-115">Type: **double**</span></span>

<span data-ttu-id="8fb0f-116">La entrada (valores de 2 32 bits) se reconvierte como Double.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-116">The input (two 32-bit values) recast as a double.</span></span>

## <a name="remarks"></a><span data-ttu-id="8fb0f-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8fb0f-117">Remarks</span></span>

<span data-ttu-id="8fb0f-118">También está disponible la siguiente versión sobrecargada:</span><span class="sxs-lookup"><span data-stu-id="8fb0f-118">The following overloaded version is also available:</span></span>

``` syntax
double2 asdouble(uint2 lowbits, uint2 highbits);
```

<span data-ttu-id="8fb0f-119">Si el valor de entrada es un componente de 2 32 bits, el tipo de valor devuelto contendrá un doble.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-119">If the input value is two 32-bit components, the return type will contain one double.</span></span> <span data-ttu-id="8fb0f-120">Si el valor de entrada es un componente de 4 32 bits, el tipo de valor devuelto contendrá dos valores double.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-120">If the input value is four 32-bit components, the return type will contain two doubles.</span></span> <span data-ttu-id="8fb0f-121">Si el valor de entrada es un tipo de 64 bits, el valor devuelto tendrá el mismo número de componentes que el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-121">If the input value is a 64-bit type, the returned value will have the same number of components as the input value.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="8fb0f-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="8fb0f-122">Minimum Shader Model</span></span>

<span data-ttu-id="8fb0f-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8fb0f-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8fb0f-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="8fb0f-124">Shader Model</span></span>                                                                | <span data-ttu-id="8fb0f-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="8fb0f-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="8fb0f-126">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="8fb0f-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="8fb0f-127">sí</span><span class="sxs-lookup"><span data-stu-id="8fb0f-127">yes</span></span>       |



 

<span data-ttu-id="8fb0f-128">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8fb0f-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8fb0f-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="8fb0f-129">Vertex</span></span> | <span data-ttu-id="8fb0f-130">Casco</span><span class="sxs-lookup"><span data-stu-id="8fb0f-130">Hull</span></span> | <span data-ttu-id="8fb0f-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="8fb0f-131">Domain</span></span> | <span data-ttu-id="8fb0f-132">Geometría</span><span class="sxs-lookup"><span data-stu-id="8fb0f-132">Geometry</span></span> | <span data-ttu-id="8fb0f-133">Píxel</span><span class="sxs-lookup"><span data-stu-id="8fb0f-133">Pixel</span></span> | <span data-ttu-id="8fb0f-134">Compute</span><span class="sxs-lookup"><span data-stu-id="8fb0f-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="8fb0f-135">x</span><span class="sxs-lookup"><span data-stu-id="8fb0f-135">x</span></span>      | <span data-ttu-id="8fb0f-136">x</span><span class="sxs-lookup"><span data-stu-id="8fb0f-136">x</span></span>    | <span data-ttu-id="8fb0f-137">x</span><span class="sxs-lookup"><span data-stu-id="8fb0f-137">x</span></span>      | <span data-ttu-id="8fb0f-138">x</span><span class="sxs-lookup"><span data-stu-id="8fb0f-138">x</span></span>        | <span data-ttu-id="8fb0f-139">x</span><span class="sxs-lookup"><span data-stu-id="8fb0f-139">x</span></span>     | <span data-ttu-id="8fb0f-140">x</span><span class="sxs-lookup"><span data-stu-id="8fb0f-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="8fb0f-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="8fb0f-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fb0f-142">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="8fb0f-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="8fb0f-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8fb0f-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




