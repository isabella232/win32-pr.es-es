---
UID: NS:directml.DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
title: DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC
description: Realiza una función de normalización de varianza media en la tensores de entrada. Este operador calculará la media y la varianza de la tensores de entrada para realizar la normalización.
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
ms.openlocfilehash: f3302f8081ed4bf64fa858ac3e303519089d01fb
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721276"
---
# <a name="dml_mean_variance_normalization1_operator_desc-structure-directmlh"></a><span data-ttu-id="f9be5-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="f9be5-104">DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="f9be5-105">Realiza una función de normalización de varianza media en la tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="f9be5-105">Performs a mean variance normalization function on the input tensor.</span></span> <span data-ttu-id="f9be5-106">Este operador calculará la media y la varianza de la tensores de entrada para realizar la normalización.</span><span class="sxs-lookup"><span data-stu-id="f9be5-106">This operator will calculate the mean and variance of the input tensor to perform normalization.</span></span> <span data-ttu-id="f9be5-107">Este operador realiza el siguiente cálculo.</span><span class="sxs-lookup"><span data-stu-id="f9be5-107">This operator performs the following computation.</span></span>

```
Output = FusedActivation(Scale * ((Input - Mean) / sqrt(Variance + Epsilon)) + Bias).
```

> [!IMPORTANT]
> <span data-ttu-id="f9be5-108">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="f9be5-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="f9be5-109">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="f9be5-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f9be5-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f9be5-110">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="f9be5-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f9be5-111">Members</span></span>

`InputTensor`

<span data-ttu-id="f9be5-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f9be5-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f9be5-113">Tensores que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="f9be5-113">A tensor containing the Input data.</span></span> <span data-ttu-id="f9be5-114">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="f9be5-114">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`ScaleTensor`

<span data-ttu-id="f9be5-115">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f9be5-115">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f9be5-116">Un tensores opcional que contiene los datos de la escala.</span><span class="sxs-lookup"><span data-stu-id="f9be5-116">An optional tensor containing the Scale data.</span></span> <span data-ttu-id="f9be5-117">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="f9be5-117">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="f9be5-118">Cualquier dimensión se puede reemplazar por 1 para difundirla en esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="f9be5-118">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="f9be5-119">Este tensores es obligatorio si se usa *BiasTensor* .</span><span class="sxs-lookup"><span data-stu-id="f9be5-119">This tensor is required if the *BiasTensor* is used.</span></span>


`BiasTensor`

<span data-ttu-id="f9be5-120">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f9be5-120">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f9be5-121">Un tensores opcional que contiene los datos de la diferencia.</span><span class="sxs-lookup"><span data-stu-id="f9be5-121">An optional tensor containing the bias data.</span></span> <span data-ttu-id="f9be5-122">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="f9be5-122">This tensor's dimensions should be `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="f9be5-123">Cualquier dimensión se puede reemplazar por 1 para difundirla en esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="f9be5-123">Any dimension can be replaced with 1 to broadcast in that dimension.</span></span> <span data-ttu-id="f9be5-124">Este tensores es obligatorio si se usa *ScaleTensor* .</span><span class="sxs-lookup"><span data-stu-id="f9be5-124">This tensor is required if the *ScaleTensor* is used.</span></span>


`OutputTensor`

<span data-ttu-id="f9be5-125">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f9be5-125">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f9be5-126">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="f9be5-126">A tensor to write the results to.</span></span> <span data-ttu-id="f9be5-127">Las dimensiones de este tensores son `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="f9be5-127">This tensor's dimensions are `{ BatchCount, ChannelCount, Height, Width }`.</span></span>


`AxisCount`

<span data-ttu-id="f9be5-128">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">uint</a></b></span><span class="sxs-lookup"><span data-stu-id="f9be5-128">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b></span></span>

<span data-ttu-id="f9be5-129">Número de ejes.</span><span class="sxs-lookup"><span data-stu-id="f9be5-129">The number of axes.</span></span> <span data-ttu-id="f9be5-130">Este campo determina el tamaño de la matriz de *ejes* .</span><span class="sxs-lookup"><span data-stu-id="f9be5-130">This field determines the size of the *Axes* array.</span></span>


`Axes`

<span data-ttu-id="f9be5-131">Tipo: \_ tamaño de campo \_ \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="f9be5-131">Type: \_Field\_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span> 

<span data-ttu-id="f9be5-132">Ejes en los que se va a calcular la media y la varianza.</span><span class="sxs-lookup"><span data-stu-id="f9be5-132">The axes along which to calculate the Mean and Variance.</span></span>


`NormalizeVariance`

<span data-ttu-id="f9be5-133">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">bool</a></b></span><span class="sxs-lookup"><span data-stu-id="f9be5-133">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="f9be5-134">**True** si la capa de normalización incluye la varianza en el cálculo de la normalización.</span><span class="sxs-lookup"><span data-stu-id="f9be5-134">**TRUE** if the Normalization layer includes Variance in the normalization calculation.</span></span> <span data-ttu-id="f9be5-135">En caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f9be5-135">Otherwise, **FALSE**.</span></span> <span data-ttu-id="f9be5-136">Si es **false**, la ecuación de normalización es `Output = FusedActivation(Scale * (Input - Mean) + Bias)` .</span><span class="sxs-lookup"><span data-stu-id="f9be5-136">If **FALSE**, then normalization equation is `Output = FusedActivation(Scale * (Input - Mean) + Bias)`.</span></span>


`Epsilon`

<span data-ttu-id="f9be5-137">Tipo: <b> <a href="/windows/desktop/WinProg/windows-data-types">float</a></b></span><span class="sxs-lookup"><span data-stu-id="f9be5-137">Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b></span></span>

<span data-ttu-id="f9be5-138">Valor de épsilon que se va a usar para evitar la división por cero.</span><span class="sxs-lookup"><span data-stu-id="f9be5-138">The epsilon value to use to avoid division by zero.</span></span> <span data-ttu-id="f9be5-139">Se recomienda un valor de 0,00001 como predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f9be5-139">A value of 0.00001 is recommended as default.</span></span>


`FusedActivation`

<span data-ttu-id="f9be5-140">Tipo: \_ Maybenull \_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f9be5-140">Type: \_Maybenull\_ **const [DML_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_operator_desc)\***</span></span>

<span data-ttu-id="f9be5-141">Capa de activación con fusible opcional que se va a aplicar después de la normalización.</span><span class="sxs-lookup"><span data-stu-id="f9be5-141">An optional fused activation layer to apply after the normalization.</span></span>


## <a name="remarks"></a><span data-ttu-id="f9be5-142">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f9be5-142">Remarks</span></span>
<span data-ttu-id="f9be5-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** es un superconjunto de la funcionalidad de [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="f9be5-143">**DML_MEAN_VARIANCE_NORMALIZATION1_OPERATOR_DESC** is a superset of functionality of [DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_mean_variance_normalization_operator_desc).</span></span> <span data-ttu-id="f9be5-144">Aquí, el establecimiento de la matriz de **ejes** en `{ 0, 2, 3 }` es el equivalente de establecer *CrossChannel* en **false** en **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; al establecer la matriz de **ejes** en `{ 1, 2, 3 }` es equivalente a establecer *Crosschannel* en **true**.</span><span class="sxs-lookup"><span data-stu-id="f9be5-144">Here, setting the **Axes** array to `{ 0, 2, 3 }` is the equivalent of setting *CrossChannel* to **FALSE** in **DML_MEAN_VARIANCE_NORMALIZATION_OPERATOR_DESC**; while setting the **Axes** array to `{ 1, 2, 3 }` is equivalent of setting *CrossChannel* to **TRUE**.</span></span>

## <a name="availability"></a><span data-ttu-id="f9be5-145">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="f9be5-145">Availability</span></span>
<span data-ttu-id="f9be5-146">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="f9be5-146">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f9be5-147">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="f9be5-147">Tensor constraints</span></span>
* <span data-ttu-id="f9be5-148">*InputTensor* y *OutputTensor* deben tener el mismo *tamaño*.</span><span class="sxs-lookup"><span data-stu-id="f9be5-148">*InputTensor* and *OutputTensor* must have the same *Sizes*.</span></span>
* <span data-ttu-id="f9be5-149">*BiasTensor*, *InputTensor*, *OutputTensor* y *ScaleTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="f9be5-149">*BiasTensor*, *InputTensor*, *OutputTensor*, and *ScaleTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f9be5-150">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="f9be5-150">Tensor support</span></span>
| <span data-ttu-id="f9be5-151">Tensores</span><span class="sxs-lookup"><span data-stu-id="f9be5-151">Tensor</span></span> | <span data-ttu-id="f9be5-152">Clase</span><span class="sxs-lookup"><span data-stu-id="f9be5-152">Kind</span></span> | <span data-ttu-id="f9be5-153">Dimensions</span><span class="sxs-lookup"><span data-stu-id="f9be5-153">Dimensions</span></span> | <span data-ttu-id="f9be5-154">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="f9be5-154">Supported dimension counts</span></span> | <span data-ttu-id="f9be5-155">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="f9be5-155">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="f9be5-156">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f9be5-156">InputTensor</span></span> | <span data-ttu-id="f9be5-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="f9be5-157">Input</span></span> | <span data-ttu-id="f9be5-158">{BatchCount, ChannelCount, height, width}</span><span class="sxs-lookup"><span data-stu-id="f9be5-158">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="f9be5-159">4</span><span class="sxs-lookup"><span data-stu-id="f9be5-159">4</span></span> | <span data-ttu-id="f9be5-160">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f9be5-160">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f9be5-161">ScaleTensor</span><span class="sxs-lookup"><span data-stu-id="f9be5-161">ScaleTensor</span></span> | <span data-ttu-id="f9be5-162">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="f9be5-162">Optional input</span></span> | <span data-ttu-id="f9be5-163">{ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth}</span><span class="sxs-lookup"><span data-stu-id="f9be5-163">{ ScaleBatchCount, ScaleChannelCount, ScaleHeight, ScaleWidth }</span></span> | <span data-ttu-id="f9be5-164">4</span><span class="sxs-lookup"><span data-stu-id="f9be5-164">4</span></span> | <span data-ttu-id="f9be5-165">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f9be5-165">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f9be5-166">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="f9be5-166">BiasTensor</span></span> | <span data-ttu-id="f9be5-167">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="f9be5-167">Optional input</span></span> | <span data-ttu-id="f9be5-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span><span class="sxs-lookup"><span data-stu-id="f9be5-168">{ BiasBatchCount, BiasChannelCount, BiasHeight, BiasWidth }</span></span> | <span data-ttu-id="f9be5-169">4</span><span class="sxs-lookup"><span data-stu-id="f9be5-169">4</span></span> | <span data-ttu-id="f9be5-170">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f9be5-170">FLOAT32, FLOAT16</span></span> |
| <span data-ttu-id="f9be5-171">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f9be5-171">OutputTensor</span></span> | <span data-ttu-id="f9be5-172">Output</span><span class="sxs-lookup"><span data-stu-id="f9be5-172">Output</span></span> | <span data-ttu-id="f9be5-173">{BatchCount, ChannelCount, height, width}</span><span class="sxs-lookup"><span data-stu-id="f9be5-173">{ BatchCount, ChannelCount, Height, Width }</span></span> | <span data-ttu-id="f9be5-174">4</span><span class="sxs-lookup"><span data-stu-id="f9be5-174">4</span></span> | <span data-ttu-id="f9be5-175">FLOAT32, FLOAT16</span><span class="sxs-lookup"><span data-stu-id="f9be5-175">FLOAT32, FLOAT16</span></span> |


## <a name="requirements"></a><span data-ttu-id="f9be5-176">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f9be5-176">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f9be5-177">**Header**</span><span class="sxs-lookup"><span data-stu-id="f9be5-177">**Header**</span></span> | <span data-ttu-id="f9be5-178">directml. h</span><span class="sxs-lookup"><span data-stu-id="f9be5-178">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="f9be5-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="f9be5-179">See also</span></span>

[<span data-ttu-id="f9be5-180">Usar operadores combinados para mejorar el rendimiento</span><span class="sxs-lookup"><span data-stu-id="f9be5-180">Using fused operators for improved performance</span></span>](../dml-fused-activations.md)