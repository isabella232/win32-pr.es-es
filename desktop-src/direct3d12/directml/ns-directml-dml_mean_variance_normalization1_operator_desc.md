---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Realiza una función de normalización de varianza media en el tensor de entrada. Este operador calculará la media y la varianza del tensor de entrada para realizar la normalización.
helpviewer_keywords:
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure
- direct3d12.dml_mean_variance_normalization1_operator_desc
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
- directml/DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
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
- DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
ms.openlocfilehash: ae22b004f1e879eb020ddcfe39a5f26481a508b0
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549789"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="5cc4e-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="5cc4e-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="5cc4e-105">Realiza una función de normalización de varianza media en el tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="5cc4e-106">Este operador calculará la media y la varianza del tensor de entrada para realizar la normalización.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="5cc4e-107">Este operador realiza el cálculo siguiente.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="5cc4e-108">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="5cc4e-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="5cc4e-109">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="5cc4e-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5cc4e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5cc4e-110">Syntax</span></span>
```cpp
struct DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC {
  const DML_TENSOR_DESC   *InputTensor;
  const DML_TENSOR_DESC   *ScaleTensor;
  const DML_TENSOR_DESC   *BiasTensor;
  const DML_TENSOR_DESC   *OutputTensor;
  UINT                    AxisCount;
  const UINT              *Axes;
  BOOL                    NormalizeVariance;
  FLOAT                   Epsilon;
  const DML_OPERATOR_DESC *FusedActivation;
};
```
## <a name="members"></a><span data-ttu-id="5cc4e-111">Members</span><span class="sxs-lookup"><span data-stu-id="5cc4e-111">Members</span></span>

`InputTensor`

<span data-ttu-id="5cc4e-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cc4e-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5cc4e-113">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-113">A tensor containing the Input data.</span></span> <span data-ttu-id="5cc4e-114">Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="5cc4e-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="5cc4e-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cc4e-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5cc4e-116">Tensor opcional que contiene los datos de escala.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="5cc4e-117">Si **DML_FEATURE_LEVEL** es menor que **DML_FEATURE_LEVEL_4_0**, las dimensiones de este tensor deben ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5cc4e-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="5cc4e-118">Las dimensiones ScaleBatchCount, ScaleHeight y ScaleWidth deben coincidir con *InputTensor* o establecerse en 1 para difundir automáticamente esas dimensiones a través de la entrada.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="5cc4e-119">Si **DML_FEATURE_LEVEL** es mayor o igual **que DML_FEATURE_LEVEL_4_0**, cualquier dimensión se puede establecer en 1 y se difunde automáticamente para que coincida con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="5cc4e-120">Este tensor es necesario si se *usa BiasTensor.*</span><span class="sxs-lookup"><span data-stu-id="5cc4e-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="5cc4e-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cc4e-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="5cc4e-122">Tensor opcional que contiene los datos de Bias.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="5cc4e-123">Si **DML_FEATURE_LEVEL** es menor que **DML_FEATURE_LEVEL_4_0**, las dimensiones de este tensor deben ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5cc4e-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="5cc4e-124">Las dimensiones BiasBatchCount, BiasHeight y BiasWidth deben coincidir con *InputTensor* o establecerse en 1 para difundir automáticamente esas dimensiones a través de la entrada.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="5cc4e-125">Si **DML_FEATURE_LEVEL** es mayor o igual **que DML_FEATURE_LEVEL_4_0**, cualquier dimensión se puede establecer en 1 y difundirse automáticamente para que coincida con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="5cc4e-126">Este tensor es necesario si se *usa ScaleTensor.*</span><span class="sxs-lookup"><span data-stu-id="5cc4e-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="5cc4e-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cc4e-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5cc4e-128">Tensor en el que escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-128">A tensor to write the results to.</span></span> <span data-ttu-id="5cc4e-129">Las dimensiones de este tensor son `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="5cc4e-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="5cc4e-130">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="5cc4e-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="5cc4e-131">Número de ejes.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-131">The number of axes.</span></span> <span data-ttu-id="5cc4e-132">Este campo determina el tamaño de la matriz *Axes.*</span><span class="sxs-lookup"><span data-stu-id="5cc4e-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="5cc4e-133">Tipo: \_ Tamaño de campo \_ \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5cc4e-133">Type: \_Field\_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span> 

<span data-ttu-id="5cc4e-134">Ejes a lo largo del cual se calculan la media y la varianza.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="5cc4e-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="5cc4e-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="5cc4e-136">**TRUE** si la capa de normalización incluye Varianza en el cálculo de normalización.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="5cc4e-137">De lo contrario, **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="5cc4e-138">Si **es FALSE,** la ecuación de normalización es `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="5cc4e-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="5cc4e-139">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="5cc4e-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="5cc4e-140">Valor de epsilon que se usará para evitar la división por cero.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="5cc4e-141">Se recomienda un valor de 0,00001 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="5cc4e-142">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5cc4e-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="5cc4e-143">Una capa de activación fusionada opcional que se aplicará después de la normalización.</span><span class="sxs-lookup"><span data-stu-id="5cc4e-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="5cc4e-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5cc4e-144">Remarks</span></span>
<span data-ttu-id="5cc4e-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** es un superconjunto de funcionalidad de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="5cc4e-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="5cc4e-146">Aquí, establecer la matriz **Axes** en es equivalente a establecer CrossChannel en FALSE en DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC ; mientras que establecer la matriz `{ 0, 2, 3 }` **Axes**   en es equivalente a establecer  `{ 1, 2, 3 }` *CrossChannel* en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="5cc4e-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="5cc4e-147">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="5cc4e-147">Availability</span></span>
<span data-ttu-id="5cc4e-148">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="5cc4e-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5cc4e-149">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-149">Tensor constraints</span></span>

<span data-ttu-id="5cc4e-150">*BiasTensor,* *InputTensor,* *OutputTensor* y *ScaleTensor* deben tener los mismos *DataType* y *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="5cc4e-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5cc4e-151">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="5cc4e-152">DML_FEATURE_LEVEL_3_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="5cc4e-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="5cc4e-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-153">Tensor</span></span> | <span data-ttu-id="5cc4e-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cc4e-154">Kind</span></span> | <span data-ttu-id="5cc4e-155">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="5cc4e-155">Supported dimension counts</span></span> | <span data-ttu-id="5cc4e-156">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="5cc4e-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5cc4e-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-157">InputTensor</span></span> | <span data-ttu-id="5cc4e-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cc4e-158">Input</span></span> | <span data-ttu-id="5cc4e-159">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5cc4e-159">1 to 8</span></span> | <span data-ttu-id="5cc4e-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5cc4e-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-161">ScaleTensor</span></span> | <span data-ttu-id="5cc4e-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5cc4e-162">Optional input</span></span> | <span data-ttu-id="5cc4e-163">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5cc4e-163">1 to 8</span></span> | <span data-ttu-id="5cc4e-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5cc4e-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-165">BiasTensor</span></span> | <span data-ttu-id="5cc4e-166">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5cc4e-166">Optional input</span></span> | <span data-ttu-id="5cc4e-167">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5cc4e-167">1 to 8</span></span> | <span data-ttu-id="5cc4e-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5cc4e-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-169">OutputTensor</span></span> | <span data-ttu-id="5cc4e-170">Resultados</span><span class="sxs-lookup"><span data-stu-id="5cc4e-170">Output</span></span> | <span data-ttu-id="5cc4e-171">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="5cc4e-171">1 to 8</span></span> | <span data-ttu-id="5cc4e-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="5cc4e-173">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="5cc4e-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="5cc4e-174">Tensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-174">Tensor</span></span> | <span data-ttu-id="5cc4e-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="5cc4e-175">Kind</span></span> | <span data-ttu-id="5cc4e-176">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="5cc4e-176">Supported dimension counts</span></span> | <span data-ttu-id="5cc4e-177">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="5cc4e-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5cc4e-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-178">InputTensor</span></span> | <span data-ttu-id="5cc4e-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="5cc4e-179">Input</span></span> | <span data-ttu-id="5cc4e-180">4</span><span class="sxs-lookup"><span data-stu-id="5cc4e-180">4</span></span> | <span data-ttu-id="5cc4e-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5cc4e-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-182">ScaleTensor</span></span> | <span data-ttu-id="5cc4e-183">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5cc4e-183">Optional input</span></span> | <span data-ttu-id="5cc4e-184">4</span><span class="sxs-lookup"><span data-stu-id="5cc4e-184">4</span></span> | <span data-ttu-id="5cc4e-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5cc4e-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-186">BiasTensor</span></span> | <span data-ttu-id="5cc4e-187">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5cc4e-187">Optional input</span></span> | <span data-ttu-id="5cc4e-188">4</span><span class="sxs-lookup"><span data-stu-id="5cc4e-188">4</span></span> | <span data-ttu-id="5cc4e-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="5cc4e-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5cc4e-190">OutputTensor</span></span> | <span data-ttu-id="5cc4e-191">Resultados</span><span class="sxs-lookup"><span data-stu-id="5cc4e-191">Output</span></span> | <span data-ttu-id="5cc4e-192">4</span><span class="sxs-lookup"><span data-stu-id="5cc4e-192">4</span></span> | <span data-ttu-id="5cc4e-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="5cc4e-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="5cc4e-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5cc4e-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5cc4e-195">**Header**</span><span class="sxs-lookup"><span data-stu-id="5cc4e-195">**Header**</span></span> | <span data-ttu-id="5cc4e-196">directml.h</span><span class="sxs-lookup"><span data-stu-id="5cc4e-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="5cc4e-197">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5cc4e-197">See also</span></span>

[<span data-ttu-id="5cc4e-198">Uso de operadores fusionados para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="5cc4e-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)