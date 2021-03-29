---
title: mad (función)
description: Realiza una operación aritmética de multiplicación/suma con tres valores.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- HLSL de la función de Mad
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104487166"
---
# <a name="mad-function"></a><span data-ttu-id="e122e-104">mad (función)</span><span class="sxs-lookup"><span data-stu-id="e122e-104">mad function</span></span>

<span data-ttu-id="e122e-105">Realiza una operación aritmética de multiplicación/suma con tres valores.</span><span class="sxs-lookup"><span data-stu-id="e122e-105">Performs an arithmetic multiply/add operation on three values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e122e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e122e-106">Syntax</span></span>

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a><span data-ttu-id="e122e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="e122e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e122e-108">*mvalue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e122e-108">*mvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e122e-109">Tipo: **Numeric**</span><span class="sxs-lookup"><span data-stu-id="e122e-109">Type: **numeric**</span></span>

<span data-ttu-id="e122e-110">Valor de multiplicación.</span><span class="sxs-lookup"><span data-stu-id="e122e-110">The multiplication value.</span></span>

</dd> <dt>

<span data-ttu-id="e122e-111">*un valorque* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e122e-111">*avalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e122e-112">Tipo: **Numeric**</span><span class="sxs-lookup"><span data-stu-id="e122e-112">Type: **numeric**</span></span>

<span data-ttu-id="e122e-113">Primer valor de suma.</span><span class="sxs-lookup"><span data-stu-id="e122e-113">The first addition value.</span></span>

</dd> <dt>

<span data-ttu-id="e122e-114">*bValue* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="e122e-114">*bvalue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e122e-115">Tipo: **Numeric**</span><span class="sxs-lookup"><span data-stu-id="e122e-115">Type: **numeric**</span></span>

<span data-ttu-id="e122e-116">Segundo valor de suma.</span><span class="sxs-lookup"><span data-stu-id="e122e-116">The second addition value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e122e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e122e-117">Return value</span></span>

<span data-ttu-id="e122e-118">Tipo: **Numeric**</span><span class="sxs-lookup"><span data-stu-id="e122e-118">Type: **numeric**</span></span>

<span data-ttu-id="e122e-119">Resultado de *mvalue* \* *un valorque*  +  *bValue*.</span><span class="sxs-lookup"><span data-stu-id="e122e-119">The result of *mvalue* \* *avalue* + *bvalue*.</span></span>

## <a name="remarks"></a><span data-ttu-id="e122e-120">Observaciones</span><span class="sxs-lookup"><span data-stu-id="e122e-120">Remarks</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="e122e-121">Modelo de sombreador mínimo</span><span class="sxs-lookup"><span data-stu-id="e122e-121">Minimum Shader Model</span></span>

<span data-ttu-id="e122e-122">Esta función se admite en los siguientes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="e122e-122">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="e122e-123">Modelo de sombreador</span><span class="sxs-lookup"><span data-stu-id="e122e-123">Shader Model</span></span>                                                                | <span data-ttu-id="e122e-124">Compatible</span><span class="sxs-lookup"><span data-stu-id="e122e-124">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="e122e-125">Modelos de sombreador [modelo 5](d3d11-graphics-reference-sm5.md) y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="e122e-125">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="e122e-126">sí</span><span class="sxs-lookup"><span data-stu-id="e122e-126">yes</span></span>       |



 

<span data-ttu-id="e122e-127">Esta función se admite en los siguientes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="e122e-127">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="e122e-128">Vértice</span><span class="sxs-lookup"><span data-stu-id="e122e-128">Vertex</span></span> | <span data-ttu-id="e122e-129">Casco</span><span class="sxs-lookup"><span data-stu-id="e122e-129">Hull</span></span> | <span data-ttu-id="e122e-130">Dominio</span><span class="sxs-lookup"><span data-stu-id="e122e-130">Domain</span></span> | <span data-ttu-id="e122e-131">Geometría</span><span class="sxs-lookup"><span data-stu-id="e122e-131">Geometry</span></span> | <span data-ttu-id="e122e-132">Píxel</span><span class="sxs-lookup"><span data-stu-id="e122e-132">Pixel</span></span> | <span data-ttu-id="e122e-133">Compute</span><span class="sxs-lookup"><span data-stu-id="e122e-133">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="e122e-134">x</span><span class="sxs-lookup"><span data-stu-id="e122e-134">x</span></span>      | <span data-ttu-id="e122e-135">x</span><span class="sxs-lookup"><span data-stu-id="e122e-135">x</span></span>    | <span data-ttu-id="e122e-136">x</span><span class="sxs-lookup"><span data-stu-id="e122e-136">x</span></span>      | <span data-ttu-id="e122e-137">x</span><span class="sxs-lookup"><span data-stu-id="e122e-137">x</span></span>        | <span data-ttu-id="e122e-138">x</span><span class="sxs-lookup"><span data-stu-id="e122e-138">x</span></span>     | <span data-ttu-id="e122e-139">x</span><span class="sxs-lookup"><span data-stu-id="e122e-139">x</span></span>       |



 

<span data-ttu-id="e122e-140">Los autores del sombreador pueden usar el intrínsecas de **Mad** para dirigirse explícitamente a la instrucción de hardware de **Mad** en el resultado del sombreador compilado, lo que es especialmente útil con los sombreadores que marcan los resultados con la palabra clave [precisa](dx-graphics-hlsl-appendix-keywords.md) .</span><span class="sxs-lookup"><span data-stu-id="e122e-140">Shader authors can use the **mad** instrinsic to explicitly target the **mad** hardware instruction in the compiled shader output, which is particularly useful with shaders that mark results with the [precise](dx-graphics-hlsl-appendix-keywords.md) keyword.</span></span> <span data-ttu-id="e122e-141">La instrucción de **Mad** se puede implementar en hardware como "fusionada", que ofrece mayor precisión que la implementación de una instrucción **mul** seguida de una instrucción **Add** o como un tipo **mul**  +  **Add**.</span><span class="sxs-lookup"><span data-stu-id="e122e-141">The **mad** instruction can be implemented in hardware as either "fused," which offers higher precision than implementing a **mul** instruction followed by an **add** instruction, or as a **mul** + **add**.</span></span>

<span data-ttu-id="e122e-142">Si los autores del sombreador usan el intrínsecas de **Mad** para calcular un resultado que el sombreador marcó como preciso, indican al hardware que use cualquier implementación válida de la instrucción de **Mad** (fusionada o no), siempre que la implementación sea coherente para todos los usos de la función intrínseca de **Mad** en cualquier sombreador de ese hardware.</span><span class="sxs-lookup"><span data-stu-id="e122e-142">If shader authors use the **mad** instrinsic to calculate a result that the shader marked as precise, they indicate to the hardware to use any valid implementation of the **mad** instruction (fused or not) as long as the implementation is consistent for all uses of that **mad** intrinsic in any shader on that hardware.</span></span> <span data-ttu-id="e122e-143">Los sombreadores pueden aprovechar mejor las posibles mejoras de rendimiento mediante el uso de una instrucción nativa de **Mad** (frente a la   +  **adición** de Mul) en algún hardware.</span><span class="sxs-lookup"><span data-stu-id="e122e-143">Shaders can then take advantage of potential performance improvements by using a native **mad** instruction (versus **mul** + **add**) on some hardware.</span></span> <span data-ttu-id="e122e-144">El resultado de realizar una instrucción de hardware de **Mad** nativa puede ser o no diferente de la realización de un **mul** seguido de una **adición**.</span><span class="sxs-lookup"><span data-stu-id="e122e-144">The result of performing a native **mad** hardware instruction might or might not be different than performing a **mul** followed by an **add**.</span></span> <span data-ttu-id="e122e-145">Sin embargo, en cualquier caso, el resultado debe ser coherente para que se produzca la misma operación en varios sombreadores o en partes diferentes de un sombreador.</span><span class="sxs-lookup"><span data-stu-id="e122e-145">However, whatever the result is, the result must be consistent for the same operation to occur in multiple shaders or different parts of a shader.</span></span>

## <a name="see-also"></a><span data-ttu-id="e122e-146">Vea también</span><span class="sxs-lookup"><span data-stu-id="e122e-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e122e-147">Funciones intrínsecas</span><span class="sxs-lookup"><span data-stu-id="e122e-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="e122e-148">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e122e-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




