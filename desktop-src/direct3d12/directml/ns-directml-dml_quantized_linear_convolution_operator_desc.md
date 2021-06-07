---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Realiza una convolución del *filterTensor* con *inputTensor*. Este operador realiza la convolución hacia delante en datos cuantificados. Este operador es matemáticamente equivalente a descuantizar las entradas, implicar y, a continuación, cuantificar la salida.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_convolution_operator_desc
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
ms.openlocfilehash: 5b98e1f57268cab70c2fb672991bce3d67419db8
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417963"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="ccaa7-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="ccaa7-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="ccaa7-106">Realiza una convolución del *filterTensor* con *inputTensor*.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="ccaa7-107">Este operador realiza la convolución hacia delante en datos cuantificados.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="ccaa7-108">Este operador es matemáticamente equivalente a descuantizar las entradas, implicar y, a continuación, cuantificar la salida.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="ccaa7-109">Las funciones lineales de cuantificación usadas por este operador son las funciones de cuantificación lineales.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="ccaa7-110">Función Dequantize</span><span class="sxs-lookup"><span data-stu-id="ccaa7-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="ccaa7-111">Función Quantize</span><span class="sxs-lookup"><span data-stu-id="ccaa7-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="ccaa7-112">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="ccaa7-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="ccaa7-113">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="ccaa7-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ccaa7-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ccaa7-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *InputScaleTensor;
  const DML_TENSOR_DESC *InputZeroPointTensor;
  const DML_TENSOR_DESC *FilterTensor;
  const DML_TENSOR_DESC *FilterScaleTensor;
  const DML_TENSOR_DESC *FilterZeroPointTensor;
  const DML_TENSOR_DESC *BiasTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  DimensionCount;
  const UINT            *Strides;
  const UINT            *Dilations;
  const UINT            *StartPadding;
  const UINT            *EndPadding;
  UINT                  GroupCount;
};
```



## <a name="members"></a><span data-ttu-id="ccaa7-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="ccaa7-115">Members</span></span>

`InputTensor`

<span data-ttu-id="ccaa7-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-117">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-117">A tensor containing the input data.</span></span> <span data-ttu-id="ccaa7-118">Las dimensiones esperadas de *InputTensor* son `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="ccaa7-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-120">Tensor que contiene los datos de escala de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="ccaa7-121">Las dimensiones esperadas de son `InputScaleTensor` `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ccaa7-122">Este valor de escala se usa para descuantizar los valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="ccaa7-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-124">Tensor opcional que contiene los datos de punto cero de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="ccaa7-125">Las dimensiones esperadas de *InputZeroPointTensor* son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ccaa7-126">Este valor de punto cero se usa para descuantizar los valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="ccaa7-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-128">Tensor que contiene los datos de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-128">A tensor containing the filter data.</span></span> <span data-ttu-id="ccaa7-129">Las dimensiones esperadas del *filterTensor* son `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="ccaa7-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-131">Tensor que contiene los datos de escala de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="ccaa7-132">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `FilterScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, OutputChannelCount, 1, 1 }` cuantificación por canal.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="ccaa7-133">Este valor de escala se usa para descuantizar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="ccaa7-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-135">Tensor opcional que contiene los datos de punto cero de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="ccaa7-136">Las dimensiones esperadas de *FilterZeroPointTensor* son si se requiere una cuantificación por tensor o si se requiere una cuantificación por `{ 1, 1, 1, 1 }` `{ 1, OutputChannelCount, 1, 1 }` canal.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="ccaa7-137">Este valor de punto cero se usa para descuantizar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="ccaa7-138">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-139">Tensor que contiene los datos de sesgo.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-139">A tensor containing the bias data.</span></span> <span data-ttu-id="ccaa7-140">El tensor de sesgo es un tensor que contiene datos que se difunden a través del tensor de salida al final de la convolución que se agrega al resultado.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="ccaa7-141">Las dimensiones esperadas de BiasTensor son `{ 1, OutputChannelCount, 1, 1 }` para 4D.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="ccaa7-142">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-143">Tensor que contiene los datos de escala de salida.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="ccaa7-144">Las dimensiones esperadas de OutputScaleTensor son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ccaa7-145">Este valor de escala de entrada se usa para cuantificar los valores de salida de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="ccaa7-146">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-147">Tensor opcional que contiene los datos de punto cero de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="ccaa7-148">Las dimensiones esperadas de OutputZeroPointTensor son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="ccaa7-149">Este valor de punto cero de entrada se usa para cuantificar la convolución de los valores de salida.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="ccaa7-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="ccaa7-151">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-151">A tensor to write the results to.</span></span> <span data-ttu-id="ccaa7-152">Las dimensiones esperadas de OutputTensor son `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="ccaa7-153">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ccaa7-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ccaa7-154">Número de dimensiones espaciales para la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="ccaa7-155">Las dimensiones espaciales son las dimensiones inferiores del tensor *FilterTensor* del filtro de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="ccaa7-156">Este valor también determina el tamaño de las matrices *Strides*, *Posición,* *StartPadding* y *EndPadding.*</span><span class="sxs-lookup"><span data-stu-id="ccaa7-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="ccaa7-157">Solo se admite un valor de 2.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="ccaa7-158">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-158">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccaa7-159">Los avances de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-159">The strides of the convolution operation.</span></span> <span data-ttu-id="ccaa7-160">Estos strides se aplican al filtro de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="ccaa7-161">Son independientes de los avances de tensor incluidos [en DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="ccaa7-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="ccaa7-162">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-162">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccaa7-163">Las convoluciones de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="ccaa7-164">Las reparaciones son avances que se aplican a los elementos del kernel de filtro.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="ccaa7-165">Esto tiene el efecto de simular un kernel de filtro mayor mediante el relleno de los elementos internos del kernel de filtro con ceros.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="ccaa7-166">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-166">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccaa7-167">Valores de relleno que se aplicarán al principio de cada dimensión espacial del filtro y del tensor de entrada de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="ccaa7-168">Tipo: \_ Field_size \_ (DimensionCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="ccaa7-168">Type: \_Field_size\_(DimensionCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ccaa7-169">Valores de relleno que se aplicarán al final de cada dimensión espacial del filtro y del tensor de entrada de la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="ccaa7-170">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="ccaa7-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="ccaa7-171">Número de grupos en los que se va a dividir la operación de convolución.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="ccaa7-172">*GroupCount* se puede usar para lograr la convolución por profundidad estableciendo *GroupCount* en el número de canales de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="ccaa7-173">Esto divide la convolución en una convolución independiente por canal de entrada.</span><span class="sxs-lookup"><span data-stu-id="ccaa7-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="ccaa7-174">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="ccaa7-174">Availability</span></span>
<span data-ttu-id="ccaa7-175">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="ccaa7-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="ccaa7-176">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-176">Tensor constraints</span></span>
* <span data-ttu-id="ccaa7-177">*FilterTensor* y *FilterZeroPointTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="ccaa7-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="ccaa7-178">*InputTensor* y *InputZeroPointTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="ccaa7-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="ccaa7-179">*OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="ccaa7-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="ccaa7-180">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-180">Tensor support</span></span>
| <span data-ttu-id="ccaa7-181">Tensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-181">Tensor</span></span> | <span data-ttu-id="ccaa7-182">Tipo</span><span class="sxs-lookup"><span data-stu-id="ccaa7-182">Kind</span></span> | <span data-ttu-id="ccaa7-183">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="ccaa7-183">Supported dimension counts</span></span> | <span data-ttu-id="ccaa7-184">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="ccaa7-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="ccaa7-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-185">InputTensor</span></span> | <span data-ttu-id="ccaa7-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccaa7-186">Input</span></span> | <span data-ttu-id="ccaa7-187">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-187">4</span></span> | <span data-ttu-id="ccaa7-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ccaa7-188">INT8, UINT8</span></span> |
| <span data-ttu-id="ccaa7-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-189">InputScaleTensor</span></span> | <span data-ttu-id="ccaa7-190">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccaa7-190">Input</span></span> | <span data-ttu-id="ccaa7-191">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-191">4</span></span> | <span data-ttu-id="ccaa7-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ccaa7-192">FLOAT32</span></span> |
| <span data-ttu-id="ccaa7-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-193">InputZeroPointTensor</span></span> | <span data-ttu-id="ccaa7-194">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="ccaa7-194">Optional input</span></span> | <span data-ttu-id="ccaa7-195">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-195">4</span></span> | <span data-ttu-id="ccaa7-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ccaa7-196">INT8, UINT8</span></span> |
| <span data-ttu-id="ccaa7-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-197">FilterTensor</span></span> | <span data-ttu-id="ccaa7-198">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccaa7-198">Input</span></span> | <span data-ttu-id="ccaa7-199">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-199">4</span></span> | <span data-ttu-id="ccaa7-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ccaa7-200">INT8, UINT8</span></span> |
| <span data-ttu-id="ccaa7-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-201">FilterScaleTensor</span></span> | <span data-ttu-id="ccaa7-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccaa7-202">Input</span></span> | <span data-ttu-id="ccaa7-203">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-203">4</span></span> | <span data-ttu-id="ccaa7-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ccaa7-204">FLOAT32</span></span> |
| <span data-ttu-id="ccaa7-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="ccaa7-206">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="ccaa7-206">Optional input</span></span> | <span data-ttu-id="ccaa7-207">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-207">4</span></span> | <span data-ttu-id="ccaa7-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ccaa7-208">INT8, UINT8</span></span> |
| <span data-ttu-id="ccaa7-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-209">BiasTensor</span></span> | <span data-ttu-id="ccaa7-210">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="ccaa7-210">Optional input</span></span> | <span data-ttu-id="ccaa7-211">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-211">4</span></span> | <span data-ttu-id="ccaa7-212">INT32</span><span class="sxs-lookup"><span data-stu-id="ccaa7-212">INT32</span></span> |
| <span data-ttu-id="ccaa7-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-213">OutputScaleTensor</span></span> | <span data-ttu-id="ccaa7-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="ccaa7-214">Input</span></span> | <span data-ttu-id="ccaa7-215">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-215">4</span></span> | <span data-ttu-id="ccaa7-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="ccaa7-216">FLOAT32</span></span> |
| <span data-ttu-id="ccaa7-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="ccaa7-218">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="ccaa7-218">Optional input</span></span> | <span data-ttu-id="ccaa7-219">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-219">4</span></span> | <span data-ttu-id="ccaa7-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ccaa7-220">INT8, UINT8</span></span> |
| <span data-ttu-id="ccaa7-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="ccaa7-221">OutputTensor</span></span> | <span data-ttu-id="ccaa7-222">Resultados</span><span class="sxs-lookup"><span data-stu-id="ccaa7-222">Output</span></span> | <span data-ttu-id="ccaa7-223">4</span><span class="sxs-lookup"><span data-stu-id="ccaa7-223">4</span></span> | <span data-ttu-id="ccaa7-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="ccaa7-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="ccaa7-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ccaa7-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ccaa7-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="ccaa7-226">**Header**</span></span> | <span data-ttu-id="ccaa7-227">directml.h</span><span class="sxs-lookup"><span data-stu-id="ccaa7-227">directml.h</span></span> |