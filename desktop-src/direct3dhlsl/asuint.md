---
title: asuint (función)
description: Reinterpreta el patrón de bits de un valor de 64 bits como dos enteros de 32 bits sin signo.
ms.assetid: 29671661-4fec-46e5-9b6f-56fba8e1d756
keywords:
- función asuint HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c54ed89e112482df4a54f35e24a04694e88fa490
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076900"
---
# <a name="asuint-function"></a><span data-ttu-id="671a4-104">asuint (función)</span><span class="sxs-lookup"><span data-stu-id="671a4-104">asuint function</span></span>

<span data-ttu-id="671a4-105">Reinterpreta el patrón de bits de un valor de 64 bits como dos enteros de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="671a4-105">Reinterprets the bit pattern of a 64-bit value as two unsigned 32-bit integers.</span></span>

## <a name="syntax"></a><span data-ttu-id="671a4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="671a4-106">Syntax</span></span>

``` syntax
void asuint(
  in  double value,
  out uint lowbits,
  out uint highbits
);
```

## <a name="parameters"></a><span data-ttu-id="671a4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="671a4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="671a4-108">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="671a4-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="671a4-109">Tipo: **Double**</span><span class="sxs-lookup"><span data-stu-id="671a4-109">Type: **double**</span></span>

<span data-ttu-id="671a4-110">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="671a4-110">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="671a4-111">*lowbits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="671a4-111">*lowbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="671a4-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="671a4-112">Type: **uint**</span></span>

<span data-ttu-id="671a4-113">Patrón de *valor* de 32 bits bajo.</span><span class="sxs-lookup"><span data-stu-id="671a4-113">The low 32-bit pattern of *value*.</span></span>

</dd> <dt>

<span data-ttu-id="671a4-114">*highbits* \[ enuncia\]</span><span class="sxs-lookup"><span data-stu-id="671a4-114">*highbits* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="671a4-115">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="671a4-115">Type: **uint**</span></span>

<span data-ttu-id="671a4-116">Modelo de *valor* de 32 bits alto.</span><span class="sxs-lookup"><span data-stu-id="671a4-116">The high 32-bit pattern of *value*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="671a4-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="671a4-117">Return value</span></span>

<span data-ttu-id="671a4-118">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="671a4-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="671a4-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="671a4-119">Remarks</span></span>

<span data-ttu-id="671a4-120">Esta función es una versión alternativa del intrínseco [**asuint**](dx-graphics-hlsl-asuint.md) que está disponible en los modelos de sombreador anteriores y que se incorporó para el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="671a4-120">This function is an alternate version of the [**asuint**](dx-graphics-hlsl-asuint.md) intrinsic that has been available in earlier shader models, and was introduced for Shader Model 5.</span></span> <span data-ttu-id="671a4-121">La función original (reconocida en el compilador de HLSL por su firma diferente) sigue estando disponible para el modelo de sombreador 5.</span><span class="sxs-lookup"><span data-stu-id="671a4-121">The original function (recognized in the HLSL compiler by its different signature) remains available to Shader Model 5.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="671a4-122">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="671a4-122">Minimum Shader Model</span></span>

<span data-ttu-id="671a4-123">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="671a4-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="671a4-124">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="671a4-124">Shader Model</span></span>                                                                | <span data-ttu-id="671a4-125">Compatible</span><span class="sxs-lookup"><span data-stu-id="671a4-125">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="671a4-126">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="671a4-126">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="671a4-127">sí</span><span class="sxs-lookup"><span data-stu-id="671a4-127">yes</span></span>       |



 

<span data-ttu-id="671a4-128">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="671a4-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="671a4-129">Vértice</span><span class="sxs-lookup"><span data-stu-id="671a4-129">Vertex</span></span> | <span data-ttu-id="671a4-130">Casco</span><span class="sxs-lookup"><span data-stu-id="671a4-130">Hull</span></span> | <span data-ttu-id="671a4-131">Dominio</span><span class="sxs-lookup"><span data-stu-id="671a4-131">Domain</span></span> | <span data-ttu-id="671a4-132">Geometría</span><span class="sxs-lookup"><span data-stu-id="671a4-132">Geometry</span></span> | <span data-ttu-id="671a4-133">Píxel</span><span class="sxs-lookup"><span data-stu-id="671a4-133">Pixel</span></span> | <span data-ttu-id="671a4-134">Compute</span><span class="sxs-lookup"><span data-stu-id="671a4-134">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="671a4-135">x</span><span class="sxs-lookup"><span data-stu-id="671a4-135">x</span></span>      | <span data-ttu-id="671a4-136">x</span><span class="sxs-lookup"><span data-stu-id="671a4-136">x</span></span>    | <span data-ttu-id="671a4-137">x</span><span class="sxs-lookup"><span data-stu-id="671a4-137">x</span></span>      | <span data-ttu-id="671a4-138">x</span><span class="sxs-lookup"><span data-stu-id="671a4-138">x</span></span>        | <span data-ttu-id="671a4-139">x</span><span class="sxs-lookup"><span data-stu-id="671a4-139">x</span></span>     | <span data-ttu-id="671a4-140">x</span><span class="sxs-lookup"><span data-stu-id="671a4-140">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="671a4-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="671a4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671a4-142">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="671a4-142">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="671a4-143">**asuint (DirectX HLSL)**</span><span class="sxs-lookup"><span data-stu-id="671a4-143">**asuint (DirectX HLSL)**</span></span>](dx-graphics-hlsl-asuint.md)
</dt> <dt>

[<span data-ttu-id="671a4-144">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="671a4-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




