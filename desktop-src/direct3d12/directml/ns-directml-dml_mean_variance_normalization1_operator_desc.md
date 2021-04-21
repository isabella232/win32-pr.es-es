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
ms.openlocfilehash: 759bf25d4b6a97e70c6de7708a5c9fd0bccae439
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803403"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="0d0d5-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="0d0d5-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="0d0d5-105">Realiza una función de normalización de varianza media en el tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="0d0d5-106">Este operador calculará la media y la varianza del tensor de entrada para realizar la normalización.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="0d0d5-107">Este operador realiza el cálculo siguiente.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="0d0d5-108">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="0d0d5-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="0d0d5-109">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="0d0d5-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0d5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d0d5-110">Syntax</span></span>
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
## <a name="members"></a><span data-ttu-id="0d0d5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d0d5-111">Members</span></span>

`InputTensor`

<span data-ttu-id="0d0d5-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d0d5-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0d0d5-113">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-113">A tensor containing the Input data.</span></span> <span data-ttu-id="0d0d5-114">Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="0d0d5-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`ScaleTensor`

<span data-ttu-id="0d0d5-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d0d5-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0d0d5-116">Tensor opcional que contiene los datos de escala.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-116">An optional tensor containing the Scale data.</span></span>

<span data-ttu-id="0d0d5-117">Si **DML_FEATURE_LEVEL** es menor que **DML_FEATURE_LEVEL_4_0**, las dimensiones de este tensor deben ser `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }` .</span><span class="sxs-lookup"><span data-stu-id="0d0d5-117">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ ScaleBatchCount, ChannelCount, ScaleHeight, ScaleWidth }`.</span></span> <span data-ttu-id="0d0d5-118">Las dimensiones ScaleBatchCount, ScaleHeight y ScaleWidth deben coincidir con *InputTensor* o establecerse en 1 para difundir automáticamente esas dimensiones a través de la entrada.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-118">The dimensions ScaleBatchCount, ScaleHeight, and ScaleWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="0d0d5-119">Si **DML_FEATURE_LEVEL** es mayor o igual que **DML_FEATURE_LEVEL_4_0**, cualquier dimensión se puede establecer en 1 y se difunde automáticamente para que coincida con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-119">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="0d0d5-120">Este tensor es necesario si *se usa BiasTensor.*</span><span class="sxs-lookup"><span data-stu-id="0d0d5-120">This tensor is required if the *BiasTensor* is used.</span></span>

`BiasTensor`

<span data-ttu-id="0d0d5-121">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d0d5-121">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>


<span data-ttu-id="0d0d5-122">Tensor opcional que contiene los datos de Bias.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-122">An optional tensor containing the Bias data.</span></span>

<span data-ttu-id="0d0d5-123">Si **DML_FEATURE_LEVEL** es menor que **DML_FEATURE_LEVEL_4_0**, las dimensiones de este tensor deben ser `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }` .</span><span class="sxs-lookup"><span data-stu-id="0d0d5-123">If **DML_FEATURE_LEVEL** is less than **DML_FEATURE_LEVEL_4_0**, then this tensor's dimensions should be `{ BiasBatchCount, ChannelCount, BiasHeight, BiasWidth }`.</span></span> <span data-ttu-id="0d0d5-124">Las dimensiones BiasBatchCount, BiasHeight y BiasWidth deben coincidir con *InputTensor* o establecerse en 1 para difundir automáticamente esas dimensiones a través de la entrada.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-124">The dimensions BiasBatchCount, BiasHeight, and BiasWidth should either match *InputTensor*, or be set to 1 to automatically broadcast those dimensions across the input.</span></span>

<span data-ttu-id="0d0d5-125">Si **DML_FEATURE_LEVEL** es mayor o igual que **DML_FEATURE_LEVEL_4_0**, cualquier dimensión se puede establecer en 1 y se difunde automáticamente para que coincida con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-125">If **DML_FEATURE_LEVEL** is greater than or equal to **DML_FEATURE_LEVEL_4_0**, then any dimension can be set to 1, and be automatically broadcast to match *InputTensor*.</span></span>

<span data-ttu-id="0d0d5-126">Este tensor es necesario si se usa *ScaleTensor.*</span><span class="sxs-lookup"><span data-stu-id="0d0d5-126">This tensor is required if the *ScaleTensor* is used.</span></span>

`OutputTensor`

<span data-ttu-id="0d0d5-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d0d5-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="0d0d5-128">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-128">A tensor to write the results to.</span></span> <span data-ttu-id="0d0d5-129">Las dimensiones de este tensor son `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="0d0d5-129">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>

`AxisCount`

<span data-ttu-id="0d0d5-130">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span><span class="sxs-lookup"><span data-stu-id="0d0d5-130">Type: <b><a href="/windows/win32/winprog/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="0d0d5-131">Número de ejes.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-131">The number of axes.</span></span> <span data-ttu-id="0d0d5-132">Este campo determina el tamaño de la matriz *Axes.*</span><span class="sxs-lookup"><span data-stu-id="0d0d5-132">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="0d0d5-133">Tipo: \_ Tamaño de campo \_ \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="0d0d5-133">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span> 

<span data-ttu-id="0d0d5-134">Ejes a lo largo de los que se calculan la media y la varianza.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-134">The axes along which to calculate the Mean and Variance.</span></span>

`NormalizeVariance`

<span data-ttu-id="0d0d5-135">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="0d0d5-135">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="0d0d5-136">**TRUE** si la capa normalización incluye Varianza en el cálculo de normalización.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-136">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="0d0d5-137">De lo contrario, **FALSE**.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-137">Otherwise, **FALSE**.</span></span> <span data-ttu-id="0d0d5-138">Si **es FALSE**, la ecuación de normalización es `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="0d0d5-138">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>

`Epsilon`

<span data-ttu-id="0d0d5-139">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span><span class="sxs-lookup"><span data-stu-id="0d0d5-139">Type: <b><a href="/windows/win32/winprog/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="0d0d5-140">Valor de epsilon que se usará para evitar la división por cero.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-140">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="0d0d5-141">Se recomienda un valor de 0,00001 como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-141">A value of 0.00001 is recommended as default.</span></span>

`FusedActivation`

<span data-ttu-id="0d0d5-142">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="0d0d5-142">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="0d0d5-143">Una capa de activación fusionada opcional que se aplicará después de la normalización.</span><span class="sxs-lookup"><span data-stu-id="0d0d5-143">An optional fused activation layer to apply after the normalization.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d0d5-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0d0d5-144">Remarks</span></span>
<span data-ttu-id="0d0d5-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** es un superconjunto de funcionalidad de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="0d0d5-145">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="0d0d5-146">Aquí, establecer la matriz **Axes** en equivale a establecer CrossChannel en FALSE en `{ 0, 2, 3 }` **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC;**  mientras que establecer la matriz **Axes** en es equivalente a establecer  `{ 1, 2, 3 }` *CrossChannel* en **TRUE.**</span><span class="sxs-lookup"><span data-stu-id="0d0d5-146">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="0d0d5-147">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="0d0d5-147">Availability</span></span>
<span data-ttu-id="0d0d5-148">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="0d0d5-148">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="0d0d5-149">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-149">Tensor constraints</span></span>

<span data-ttu-id="0d0d5-150">*BiasTensor,* *InputTensor,* *OutputTensor* y *ScaleTensor* deben tener los mismos *DataType* y *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="0d0d5-150">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType* and *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="0d0d5-151">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="0d0d5-152">DML_FEATURE_LEVEL_3_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="0d0d5-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="0d0d5-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-153">Tensor</span></span> | <span data-ttu-id="0d0d5-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d0d5-154">Kind</span></span> | <span data-ttu-id="0d0d5-155">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="0d0d5-155">Supported dimension counts</span></span> | <span data-ttu-id="0d0d5-156">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="0d0d5-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0d0d5-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-157">InputTensor</span></span> | <span data-ttu-id="0d0d5-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d0d5-158">Input</span></span> | <span data-ttu-id="0d0d5-159">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="0d0d5-159">1 to 8</span></span> | <span data-ttu-id="0d0d5-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0d0d5-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-161">ScaleTensor</span></span> | <span data-ttu-id="0d0d5-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="0d0d5-162">Optional input</span></span> | <span data-ttu-id="0d0d5-163">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="0d0d5-163">1 to 8</span></span> | <span data-ttu-id="0d0d5-164">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-164">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0d0d5-165">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-165">BiasTensor</span></span> | <span data-ttu-id="0d0d5-166">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="0d0d5-166">Optional input</span></span> | <span data-ttu-id="0d0d5-167">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="0d0d5-167">1 to 8</span></span> | <span data-ttu-id="0d0d5-168">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-168">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0d0d5-169">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-169">OutputTensor</span></span> | <span data-ttu-id="0d0d5-170">Resultados</span><span class="sxs-lookup"><span data-stu-id="0d0d5-170">Output</span></span> | <span data-ttu-id="0d0d5-171">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="0d0d5-171">1 to 8</span></span> | <span data-ttu-id="0d0d5-172">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-172">FLOAT32, FLOAT16</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="0d0d5-173">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="0d0d5-173">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="0d0d5-174">Tensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-174">Tensor</span></span> | <span data-ttu-id="0d0d5-175">Tipo</span><span class="sxs-lookup"><span data-stu-id="0d0d5-175">Kind</span></span> | <span data-ttu-id="0d0d5-176">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="0d0d5-176">Supported dimension counts</span></span> | <span data-ttu-id="0d0d5-177">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="0d0d5-177">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="0d0d5-178">InputTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-178">InputTensor</span></span> | <span data-ttu-id="0d0d5-179">Entrada</span><span class="sxs-lookup"><span data-stu-id="0d0d5-179">Input</span></span> | <span data-ttu-id="0d0d5-180">4</span><span class="sxs-lookup"><span data-stu-id="0d0d5-180">4</span></span> | <span data-ttu-id="0d0d5-181">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-181">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0d0d5-182">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-182">ScaleTensor</span></span> | <span data-ttu-id="0d0d5-183">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="0d0d5-183">Optional input</span></span> | <span data-ttu-id="0d0d5-184">4</span><span class="sxs-lookup"><span data-stu-id="0d0d5-184">4</span></span> | <span data-ttu-id="0d0d5-185">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-185">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0d0d5-186">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-186">BiasTensor</span></span> | <span data-ttu-id="0d0d5-187">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="0d0d5-187">Optional input</span></span> | <span data-ttu-id="0d0d5-188">4</span><span class="sxs-lookup"><span data-stu-id="0d0d5-188">4</span></span> | <span data-ttu-id="0d0d5-189">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-189">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="0d0d5-190">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="0d0d5-190">OutputTensor</span></span> | <span data-ttu-id="0d0d5-191">Resultados</span><span class="sxs-lookup"><span data-stu-id="0d0d5-191">Output</span></span> | <span data-ttu-id="0d0d5-192">4</span><span class="sxs-lookup"><span data-stu-id="0d0d5-192">4</span></span> | <span data-ttu-id="0d0d5-193">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="0d0d5-193">FLOAT32, FLOAT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="0d0d5-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d0d5-194">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="0d0d5-195">**Header**</span><span class="sxs-lookup"><span data-stu-id="0d0d5-195">**Header**</span></span> | <span data-ttu-id="0d0d5-196">directml.h</span><span class="sxs-lookup"><span data-stu-id="0d0d5-196">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="0d0d5-197">Consulta también</span><span class="sxs-lookup"><span data-stu-id="0d0d5-197">See also</span></span>

[<span data-ttu-id="0d0d5-198">Uso de operadores fusionados para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="0d0d5-198">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)
