---
title: Función InterlockedCompareStore (referencia de HLSL)
description: Compara de forma atómica el destino con el valor de comparación. Si son idénticos, el destino se sobrescribe con el valor de entrada.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- InterlockedCompareStore de función HLSL
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/06/2020
ms.locfileid: "104420158"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="71e22-105">Función InterlockedCompareStore (referencia de HLSL)</span><span class="sxs-lookup"><span data-stu-id="71e22-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="71e22-106">Compara de forma atómica el destino con el valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="71e22-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="71e22-107">Si son idénticos, el destino se sobrescribe con el valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="71e22-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="71e22-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71e22-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="71e22-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="71e22-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71e22-110">*dest* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="71e22-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e22-111">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="71e22-111">Type: **R**</span></span>

<span data-ttu-id="71e22-112">Dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="71e22-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="71e22-113">*comparar \_ valor* \[ en\]</span><span class="sxs-lookup"><span data-stu-id="71e22-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e22-114">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="71e22-114">Type: **T**</span></span>

<span data-ttu-id="71e22-115">El valor de comparación.</span><span class="sxs-lookup"><span data-stu-id="71e22-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="71e22-116">*valor* \[ de de\]</span><span class="sxs-lookup"><span data-stu-id="71e22-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71e22-117">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="71e22-117">Type: **T**</span></span>

<span data-ttu-id="71e22-118">Valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="71e22-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71e22-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="71e22-119">Return value</span></span>

<span data-ttu-id="71e22-120">Esta función no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="71e22-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71e22-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="71e22-121">Remarks</span></span>

<span data-ttu-id="71e22-122">Compara de forma atómica el valor al que hace referencia el *destino* con el *\_ valor de comparación* y almacena el *valor* en la ubicación a la que hace referencia *dest* si los valores coinciden.</span><span class="sxs-lookup"><span data-stu-id="71e22-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="71e22-123">Esta operación solo se puede realizar en recursos con tipo **int** o **uint** y variables de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="71e22-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="71e22-124">Hay dos usos posibles para esta función.</span><span class="sxs-lookup"><span data-stu-id="71e22-124">There are two possible uses for this function.</span></span> <span data-ttu-id="71e22-125">El primero es cuando R es un tipo de variable de memoria compartida.</span><span class="sxs-lookup"><span data-stu-id="71e22-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="71e22-126">En este caso, la función realiza la operación en el registro de memoria compartida al que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="71e22-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="71e22-127">El segundo escenario es cuando R es un tipo de variable de recurso.</span><span class="sxs-lookup"><span data-stu-id="71e22-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="71e22-128">En este escenario, la función realiza la operación en la ubicación del recurso a la que hace referencia *dest*.</span><span class="sxs-lookup"><span data-stu-id="71e22-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="71e22-129">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="71e22-129">Minimum Shader Model</span></span>

<span data-ttu-id="71e22-130">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="71e22-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="71e22-131">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="71e22-131">Shader Model</span></span>                                                                | <span data-ttu-id="71e22-132">Compatible</span><span class="sxs-lookup"><span data-stu-id="71e22-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="71e22-133">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="71e22-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="71e22-134">sí</span><span class="sxs-lookup"><span data-stu-id="71e22-134">yes</span></span>       |



 

<span data-ttu-id="71e22-135">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="71e22-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="71e22-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="71e22-136">Vertex</span></span> | <span data-ttu-id="71e22-137">Casco</span><span class="sxs-lookup"><span data-stu-id="71e22-137">Hull</span></span> | <span data-ttu-id="71e22-138">Dominio</span><span class="sxs-lookup"><span data-stu-id="71e22-138">Domain</span></span> | <span data-ttu-id="71e22-139">Geometría</span><span class="sxs-lookup"><span data-stu-id="71e22-139">Geometry</span></span> | <span data-ttu-id="71e22-140">Píxel</span><span class="sxs-lookup"><span data-stu-id="71e22-140">Pixel</span></span> | <span data-ttu-id="71e22-141">Compute</span><span class="sxs-lookup"><span data-stu-id="71e22-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="71e22-142">x</span><span class="sxs-lookup"><span data-stu-id="71e22-142">x</span></span>     | <span data-ttu-id="71e22-143">x</span><span class="sxs-lookup"><span data-stu-id="71e22-143">x</span></span>    |  <span data-ttu-id="71e22-144">x</span><span class="sxs-lookup"><span data-stu-id="71e22-144">x</span></span>     |  <span data-ttu-id="71e22-145">x</span><span class="sxs-lookup"><span data-stu-id="71e22-145">x</span></span>       | <span data-ttu-id="71e22-146">x</span><span class="sxs-lookup"><span data-stu-id="71e22-146">x</span></span>     | <span data-ttu-id="71e22-147">x</span><span class="sxs-lookup"><span data-stu-id="71e22-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="71e22-148">Vea también</span><span class="sxs-lookup"><span data-stu-id="71e22-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71e22-149">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="71e22-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="71e22-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="71e22-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




