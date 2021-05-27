---
UID: NS:directml.DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
title: DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
description: Calcula los degradados de repropagación para la [normalización por lotes.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)
helpviewer_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC structure
- direct3d12.dml_batch_normalization_grad_operator_desc
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
req.header: directml.h
req.include-header: ''
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
- directml/DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- DirectML.h
api_name:
- DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
ms.openlocfilehash: 2b94ac1dcf389d424aaf74d615f36cdf7acc804c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550440"
---
# <a name="dml_batch_normalization_grad_operator_desc-directmlh"></a><span data-ttu-id="a06a7-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="a06a7-103">DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="a06a7-104">Calcula los degradados de repropagación para la [normalización por lotes.](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc)</span><span class="sxs-lookup"><span data-stu-id="a06a7-104">Computes backpropagation gradients for [batch normalization](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc).</span></span> <span data-ttu-id="a06a7-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** realiza varios cálculos, que se detallan en las descripciones de salida independientes.</span><span class="sxs-lookup"><span data-stu-id="a06a7-105">**DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC** performs multiple computations, which are detailed in the separate output descriptions.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a06a7-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="a06a7-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="a06a7-107">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="a06a7-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a06a7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a06a7-108">Syntax</span></span>
```cpp
struct DML_BATCH_NORMALIZATION_GRAD_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* InputGradientTensor;
    const DML_TENSOR_DESC* MeanTensor;
    const DML_TENSOR_DESC* VarianceTensor;
    const DML_TENSOR_DESC* ScaleTensor;

    const DML_TENSOR_DESC* OutputGradientTensor;
    const DML_TENSOR_DESC* OutputScaleGradientTensor;
    const DML_TENSOR_DESC* OutputBiasGradientTensor;

    FLOAT Epsilon;
};
```

## <a name="members"></a><span data-ttu-id="a06a7-109">Members</span><span class="sxs-lookup"><span data-stu-id="a06a7-109">Members</span></span>

`InputTensor`

<span data-ttu-id="a06a7-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-111">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="a06a7-111">A tensor containing the input data.</span></span> <span data-ttu-id="a06a7-112">Suele ser el mismo tensor que se proporcionó que *inputTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso de reenvío.</span><span class="sxs-lookup"><span data-stu-id="a06a7-112">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

`InputGradientTensor`

<span data-ttu-id="a06a7-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-114">Tensor de degradado entrante.</span><span class="sxs-lookup"><span data-stu-id="a06a7-114">The incoming gradient tensor.</span></span> <span data-ttu-id="a06a7-115">Normalmente, esto se obtiene a partir de la salida de la repropagación de una capa anterior.</span><span class="sxs-lookup"><span data-stu-id="a06a7-115">This is typically obtained from the output of backpropagation of a preceding layer.</span></span> <span data-ttu-id="a06a7-116">Este tensor debe tener los mismos tamaños de dimensión que *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="a06a7-116">This tensor must have the same dimension sizes as *InputTensor*.</span></span>

`MeanTensor`

<span data-ttu-id="a06a7-117">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-117">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-118">Tensor que contiene los datos medio.</span><span class="sxs-lookup"><span data-stu-id="a06a7-118">A tensor containing the mean data.</span></span> <span data-ttu-id="a06a7-119">Suele ser el mismo tensor que se proporcionó que *meanTensor* [**para DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="a06a7-119">This is typically the same tensor that was provided as the *MeanTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="a06a7-120">Las dimensiones que no tengan el mismo tamaño que la dimensión correspondiente de *InputTensor* deben tener un tamaño de 1 para que se puedan difundir para que coincidan con la entrada.</span><span class="sxs-lookup"><span data-stu-id="a06a7-120">Any dimensions that don't have the same size as the corresponding dimension of *InputTensor* must have a size of 1 so that they can be broadcast to match the input.</span></span>

<span data-ttu-id="a06a7-121">Por ejemplo, los tamaños siguientes son aceptables.</span><span class="sxs-lookup"><span data-stu-id="a06a7-121">For example, the following sizes are acceptable.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 4, 1, 1] or [3, 4, 1, 1] or [3, 4, 5, 1] or [3, 4, 5, 6] or [1, 1, 1, 1]
```

<span data-ttu-id="a06a7-122">El siguiente es un error, ya que, para que sea compatible con la difusión, las dimensiones que no coincidan deben tener el tamaño 1.</span><span class="sxs-lookup"><span data-stu-id="a06a7-122">The following is an error since, in order to be broadcast compatible, any dimensions that don't match must be size 1.</span></span>

```
InputTensor: [3, 4, 5, 6]  
MeanTensor : [1, 2, 1, 1]  // 2 causes an error.
```

`VarianceTensor`

<span data-ttu-id="a06a7-123">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-123">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-124">Tensor que contiene los datos de varianza.</span><span class="sxs-lookup"><span data-stu-id="a06a7-124">A tensor containing the variance data.</span></span> <span data-ttu-id="a06a7-125">Suele ser el mismo tensor que se proporcionó que *varianceTensor* [**para DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="a06a7-125">This is typically the same tensor that was provided as the *VarianceTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="a06a7-126">Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor.*</span><span class="sxs-lookup"><span data-stu-id="a06a7-126">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`ScaleTensor`

<span data-ttu-id="a06a7-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-128">Tensor que contiene los datos de escala.</span><span class="sxs-lookup"><span data-stu-id="a06a7-128">A tensor containing the scale data.</span></span> <span data-ttu-id="a06a7-129">Suele ser el mismo tensor que se proporcionó que *ScaleTensor* [**para DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el pase hacia delante.</span><span class="sxs-lookup"><span data-stu-id="a06a7-129">This is typically the same tensor that was provided as the *ScaleTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span> <span data-ttu-id="a06a7-130">Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor.*</span><span class="sxs-lookup"><span data-stu-id="a06a7-130">This tensor must have the same dimension sizes as *MeanTensor*.</span></span>

`OutputGradientTensor`

<span data-ttu-id="a06a7-131">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-131">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-132">Para cada valor correspondiente de las entradas, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))` .</span><span class="sxs-lookup"><span data-stu-id="a06a7-132">For every corresponding value in the inputs, `OutputGradient = InputGradient * (Scale / sqrt(Variance + Epsilon))`.</span></span>

<span data-ttu-id="a06a7-133">Este tensor debe tener los mismos tamaños de dimensión *que InputTensor* / *InputGradientTensor*.</span><span class="sxs-lookup"><span data-stu-id="a06a7-133">This tensor must have the same dimension sizes as *InputTensor*/*InputGradientTensor*.</span></span>

`OutputScaleGradientTensor`

<span data-ttu-id="a06a7-134">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-134">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-135">Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor* / *VarianceTensor* / *ScaleTensor'.*</span><span class="sxs-lookup"><span data-stu-id="a06a7-135">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="a06a7-136">El siguiente cálculo se realiza o cada valor correspondiente en las entradas.</span><span class="sxs-lookup"><span data-stu-id="a06a7-136">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputScaleGradient = sum(InputGradient * (Input - Mean) / sqrt(Variance + Epsilon))`

<span data-ttu-id="a06a7-137">se `sum` calcula en todas las dimensiones que deben difundirse.</span><span class="sxs-lookup"><span data-stu-id="a06a7-137">The `sum` is computed across any dimensions that need to be broadcast.</span></span> <span data-ttu-id="a06a7-138">Si no se necesita difusión, no se necesita ninguna suma.</span><span class="sxs-lookup"><span data-stu-id="a06a7-138">If there is no broadcast needed, then no sum is needed.</span></span>

<span data-ttu-id="a06a7-139">Aquí tiene un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a06a7-139">Here's an example.</span></span>

```
InputTensor              : [3, 4, 5, 6]  
MeanTensor               : [1, 4, 1, 1] // dimensions 0, 2, 3 needed broadcasting  
OutputScaleGradientTensor: [1, 4, 1, 1]  
```

<span data-ttu-id="a06a7-140">El elemento [0, **0,** 0, 0] de es la suma de para los `OutputScaleGradientTensor` `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` 90 elementos (3 \* 5 \* 6) [[0,2], **0**, [0,4], [0,5]].</span><span class="sxs-lookup"><span data-stu-id="a06a7-140">Element [0, **0**, 0, 0] of `OutputScaleGradientTensor` is the sum of `(InputGradient * (Input - Mean) / sqrt(variance + Epsilon)` for all 90 (3\*5\*6) elements [[0,2], **0**, [0,4], [0,5]].</span></span>

`OutputBiasGradientTensor`

<span data-ttu-id="a06a7-141">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a06a7-141">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a06a7-142">Este tensor debe tener los mismos tamaños de dimensión *que MeanTensor* / *VarianceTensor* / *ScaleTensor'.*</span><span class="sxs-lookup"><span data-stu-id="a06a7-142">This tensor must have the same dimension sizes as *MeanTensor*/*VarianceTensor*/*ScaleTensor\`*.</span></span>

<span data-ttu-id="a06a7-143">El siguiente cálculo se realiza o cada valor correspondiente en las entradas.</span><span class="sxs-lookup"><span data-stu-id="a06a7-143">The following computation is done or every corresponding value in the inputs.</span></span>

`OutputBiasGradient = sum(InputGradient)`  

<span data-ttu-id="a06a7-144">se calcula en todas las dimensiones que se deben `sum` difundir (vea el ejemplo de *OutputScaleGradientTensor).*</span><span class="sxs-lookup"><span data-stu-id="a06a7-144">The `sum` is computed across any dimensions that need to be broadcast (see the example for *OutputScaleGradientTensor*).</span></span> <span data-ttu-id="a06a7-145">Si no se necesita ninguna difusión, no se necesita ninguna suma.</span><span class="sxs-lookup"><span data-stu-id="a06a7-145">If there is no broadcast needed, then no sum is needed.</span></span>

`Epsilon`

<span data-ttu-id="a06a7-146">Tipo: **[FLOAT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a06a7-146">Type: **[FLOAT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a06a7-147">Valor pequeño que se agrega a la varianza para evitar cero.</span><span class="sxs-lookup"><span data-stu-id="a06a7-147">A small value added to the variance to avoid zero.</span></span>

## <a name="availability"></a><span data-ttu-id="a06a7-148">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="a06a7-148">Availability</span></span>
<span data-ttu-id="a06a7-149">Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="a06a7-149">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a06a7-150">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-150">Tensor constraints</span></span>
<span data-ttu-id="a06a7-151">*InputGradientTensor,* *InputTensor*, *MeanTensor,* *OutputBiasGradientTensor,* *OutputGradientTensor,* *OutputScaleGradientTensor,* *ScaleTensor* y *VarianceTensor* deben tener los mismos *dataType* y *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="a06a7-151">*InputGradientTensor*, *InputTensor*, *MeanTensor*, *OutputBiasGradientTensor*, *OutputGradientTensor*, *OutputScaleGradientTensor*, *ScaleTensor*, and *VarianceTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a06a7-152">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-152">Tensor support</span></span>
| <span data-ttu-id="a06a7-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-153">Tensor</span></span> | <span data-ttu-id="a06a7-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="a06a7-154">Kind</span></span> | <span data-ttu-id="a06a7-155">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="a06a7-155">Supported dimension counts</span></span> | <span data-ttu-id="a06a7-156">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="a06a7-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a06a7-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-157">InputTensor</span></span> | <span data-ttu-id="a06a7-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="a06a7-158">Input</span></span> | <span data-ttu-id="a06a7-159">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-159">1 to 8</span></span> | <span data-ttu-id="a06a7-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-161">InputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-161">InputGradientTensor</span></span> | <span data-ttu-id="a06a7-162">Entrada</span><span class="sxs-lookup"><span data-stu-id="a06a7-162">Input</span></span> | <span data-ttu-id="a06a7-163">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-163">1 to 8</span></span> | <span data-ttu-id="a06a7-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-165">MeanTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-165">MeanTensor</span></span> | <span data-ttu-id="a06a7-166">Entrada</span><span class="sxs-lookup"><span data-stu-id="a06a7-166">Input</span></span> | <span data-ttu-id="a06a7-167">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-167">1 to 8</span></span> | <span data-ttu-id="a06a7-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-169">VarianceTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-169">VarianceTensor</span></span> | <span data-ttu-id="a06a7-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="a06a7-170">Input</span></span> | <span data-ttu-id="a06a7-171">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-171">1 to 8</span></span> | <span data-ttu-id="a06a7-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-172">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-173">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-173">ScaleTensor</span></span> | <span data-ttu-id="a06a7-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="a06a7-174">Input</span></span> | <span data-ttu-id="a06a7-175">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-175">1 to 8</span></span> | <span data-ttu-id="a06a7-176">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-176">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-177">OutputGradientTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-177">OutputGradientTensor</span></span> | <span data-ttu-id="a06a7-178">Resultados</span><span class="sxs-lookup"><span data-stu-id="a06a7-178">Output</span></span> | <span data-ttu-id="a06a7-179">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-179">1 to 8</span></span> | <span data-ttu-id="a06a7-180">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-180">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-181">OutputScaleGradientTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-181">OutputScaleGradientTensor</span></span> | <span data-ttu-id="a06a7-182">Resultados</span><span class="sxs-lookup"><span data-stu-id="a06a7-182">Output</span></span> | <span data-ttu-id="a06a7-183">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-183">1 to 8</span></span> | <span data-ttu-id="a06a7-184">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-184">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="a06a7-185">OutputBiasGradientTensor</span><span class="sxs-lookup"><span data-stu-id="a06a7-185">OutputBiasGradientTensor</span></span> | <span data-ttu-id="a06a7-186">Resultados</span><span class="sxs-lookup"><span data-stu-id="a06a7-186">Output</span></span> | <span data-ttu-id="a06a7-187">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a06a7-187">1 to 8</span></span> | <span data-ttu-id="a06a7-188">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="a06a7-188">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="a06a7-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a06a7-189">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a06a7-190">**Header**</span><span class="sxs-lookup"><span data-stu-id="a06a7-190">**Header**</span></span> | <span data-ttu-id="a06a7-191">directml.h</span><span class="sxs-lookup"><span data-stu-id="a06a7-191">directml.h</span></span> |