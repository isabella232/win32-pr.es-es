---
UID: NS:directml.DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC
description: Realiza una circunvolución del *FilterTensor* con *InputTensor*. Este operador realiza la circunvolución hacia delante en los datos cuantificados. Este operador es matemáticamente equivalente a descuantificar las entradas, Convolving y, a continuación, cuantificando la salida.
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
ms.openlocfilehash: 01193b19744f413690a3cb5ecccbb8fa60626cb0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721269"
---
# <a name="dml_quantized_linear_convolution_operator_desc-structure-directmlh"></a><span data-ttu-id="5b296-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="5b296-105">DML_QUANTIZED_LINEAR_CONVOLUTION_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="5b296-106">Realiza una circunvolución del *FilterTensor* con *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="5b296-106">Performs a convolution of the *FilterTensor* with the *InputTensor*.</span></span> <span data-ttu-id="5b296-107">Este operador realiza la circunvolución hacia delante en los datos cuantificados.</span><span class="sxs-lookup"><span data-stu-id="5b296-107">This operator performs forward convolution on quantized data.</span></span> <span data-ttu-id="5b296-108">Este operador es matemáticamente equivalente a descuantificar las entradas, Convolving y, a continuación, cuantificando la salida.</span><span class="sxs-lookup"><span data-stu-id="5b296-108">This operator is mathematically equivalent to dequantizing the inputs, convolving, and then quantizing the output.</span></span> 

<span data-ttu-id="5b296-109">Las funciones de cuantificación lineal utilizadas por este operador son las funciones de cuantificación lineal</span><span class="sxs-lookup"><span data-stu-id="5b296-109">The quantize linear functions used by this operator are the linear quantization functions</span></span>

### <a name="dequantize-function"></a><span data-ttu-id="5b296-110">Descuantificar función</span><span class="sxs-lookup"><span data-stu-id="5b296-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="5b296-111">Función cuantificate</span><span class="sxs-lookup"><span data-stu-id="5b296-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="5b296-112">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="5b296-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="5b296-113">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="5b296-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b296-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5b296-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="5b296-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="5b296-115">Members</span></span>

`InputTensor`

<span data-ttu-id="5b296-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-117">Tensores que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-117">A tensor containing the input data.</span></span> <span data-ttu-id="5b296-118">Las dimensiones esperadas de *InputTensor* son `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-118">The expected dimensions of the *InputTensor* are `{ InputBatchCount, InputChannelCount, InputHeight, InputWidth }`.</span></span>


`InputScaleTensor`

<span data-ttu-id="5b296-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-120">Tensores que contiene los datos de la escala de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-120">A tensor containing the input scale data.</span></span> <span data-ttu-id="5b296-121">Las dimensiones esperadas de `InputScaleTensor` son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-121">The expected dimensions of the `InputScaleTensor` are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5b296-122">Este valor de escala se usa para descuantificar los valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-122">This scale value is used for dequantizing the input values.</span></span>


`InputZeroPointTensor`

<span data-ttu-id="5b296-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-124">Un tensores opcional que contiene los datos de punto cero de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-124">An optional tensor containing the input zero point data.</span></span> <span data-ttu-id="5b296-125">Las dimensiones esperadas de *InputZeroPointTensor* son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-125">The expected dimensions of the *InputZeroPointTensor* are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5b296-126">Este valor de punto cero se usa para descuantificar los valores de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-126">This zero point value is used for dequantizing the input values.</span></span>


`FilterTensor`

<span data-ttu-id="5b296-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-128">Tensores que contiene los datos del filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-128">A tensor containing the filter data.</span></span> <span data-ttu-id="5b296-129">Las dimensiones esperadas de *FilterTensor* son `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-129">The expected dimensions of the *FilterTensor* are `{ FilterBatchCount, FilterChannelCount, FilterHeight, FilterWidth }`.</span></span>


`FilterScaleTensor`

<span data-ttu-id="5b296-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-131">Tensores que contiene los datos de la escala del filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-131">A tensor containing the filter scale data.</span></span> <span data-ttu-id="5b296-132">Las dimensiones esperadas de `FilterScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, OutputChannelCount, 1, 1 }` si se requiere la cuantificación por canal.</span><span class="sxs-lookup"><span data-stu-id="5b296-132">The expected dimensions of the `FilterScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="5b296-133">Este valor de escala se usa para descuantificar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-133">This scale value is used for dequantizing the filter values.</span></span>


`FilterZeroPointTensor`

<span data-ttu-id="5b296-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-135">Un tensores opcional que contiene los datos del punto cero del filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-135">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="5b296-136">Las dimensiones esperadas de *FilterZeroPointTensor* son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, OutputChannelCount, 1, 1 }` si se requiere la cuantificación por canal.</span><span class="sxs-lookup"><span data-stu-id="5b296-136">The expected dimensions of the *FilterZeroPointTensor* are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, OutputChannelCount, 1, 1 }` if per channel quantization is required.</span></span> <span data-ttu-id="5b296-137">Este valor de punto cero se usa para descuantificar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-137">This zero point value is used for dequantizing the filter values.</span></span>


`BiasTensor`

<span data-ttu-id="5b296-138">Tipo: \_ Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-138">Type: \_Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-139">Tensores que contiene los datos de sesgo.</span><span class="sxs-lookup"><span data-stu-id="5b296-139">A tensor containing the bias data.</span></span> <span data-ttu-id="5b296-140">Bias tensores es un tensores que contiene datos que se difunden a través de la tensores de salida al final de la circunvolución que se agrega al resultado.</span><span class="sxs-lookup"><span data-stu-id="5b296-140">The bias tensor is a tensor containing data which is broadcasted across the output tensor at the end of the convolution which is added to the result.</span></span> <span data-ttu-id="5b296-141">Las dimensiones esperadas de BiasTensor son `{ 1, OutputChannelCount, 1, 1 }` para 4D.</span><span class="sxs-lookup"><span data-stu-id="5b296-141">The expected dimensions of the BiasTensor are `{ 1, OutputChannelCount, 1, 1 }` for 4D.</span></span>


`OutputScaleTensor`

<span data-ttu-id="5b296-142">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-142">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-143">Tensores que contiene los datos de la escala de salida.</span><span class="sxs-lookup"><span data-stu-id="5b296-143">A tensor containing the output scale data.</span></span> <span data-ttu-id="5b296-144">Las dimensiones esperadas de OutputScaleTensor son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-144">The expected dimensions of the OutputScaleTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5b296-145">Este valor de escala de entrada se utiliza para cuantificar los valores de salida de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-145">This input scale value is used for quantizing the convolution output values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="5b296-146">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-146">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-147">Un tensores opcional que contiene los datos del punto cero del filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-147">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="5b296-148">Las dimensiones esperadas de OutputZeroPointTensor son `{ 1, 1, 1, 1 }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-148">The expected dimensions of the OutputZeroPointTensor are `{ 1, 1, 1, 1 }`.</span></span> <span data-ttu-id="5b296-149">Este valor de punto cero de entrada se utiliza para cuantificar la circunvolución de los valores de salida.</span><span class="sxs-lookup"><span data-stu-id="5b296-149">This input zero point value is used for quantizing the convolution the output values.</span></span>


`OutputTensor`

<span data-ttu-id="5b296-150">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-150">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="5b296-151">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="5b296-151">A tensor to write the results to.</span></span> <span data-ttu-id="5b296-152">Las dimensiones esperadas de OutputTensor son `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }` .</span><span class="sxs-lookup"><span data-stu-id="5b296-152">The expected dimensions of the OutputTensor are `{ OutputBatchCount, OutputChannelCount, OutputHeight, OutputWidth }`.</span></span>


`DimensionCount`

<span data-ttu-id="5b296-153">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5b296-153">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5b296-154">El número de dimensiones espaciales para la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-154">The number of spatial dimensions for the convolution operation.</span></span> <span data-ttu-id="5b296-155">Las dimensiones espaciales son las dimensiones inferiores del filtro de circunvolución tensores *FilterTensor*.</span><span class="sxs-lookup"><span data-stu-id="5b296-155">Spatial dimensions are the lower dimensions of the convolution filter tensor *FilterTensor*.</span></span> <span data-ttu-id="5b296-156">Este valor también determina el tamaño de las matrices de los *progresos*, *Dilations*, *StartPadding* y *EndPadding* .</span><span class="sxs-lookup"><span data-stu-id="5b296-156">This value also determines the size of the *Strides*, *Dilations*, *StartPadding*, and *EndPadding* arrays.</span></span> <span data-ttu-id="5b296-157">Solo se admite un valor de 2.</span><span class="sxs-lookup"><span data-stu-id="5b296-157">Only a value of 2 is supported.</span></span>


`Strides`

<span data-ttu-id="5b296-158">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-158">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5b296-159">Los progresos de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-159">The strides of the convolution operation.</span></span> <span data-ttu-id="5b296-160">Estos avances se aplican al filtro de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-160">These strides are applied to the convolution filter.</span></span> <span data-ttu-id="5b296-161">Son independientes de los progresos de tensores incluidos en [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span><span class="sxs-lookup"><span data-stu-id="5b296-161">They are separate from the tensor strides included in [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc).</span></span>


`Dilations`

<span data-ttu-id="5b296-162">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-162">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5b296-163">Dilations de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-163">The Dilations of the convolution operation.</span></span> <span data-ttu-id="5b296-164">Dilations son los progresos aplicados a los elementos del kernel de filtro.</span><span class="sxs-lookup"><span data-stu-id="5b296-164">Dilations are strides applied to the elements of the filter kernel.</span></span> <span data-ttu-id="5b296-165">Esto tiene el efecto de simular un kernel de filtro mayor al rellenar los elementos de kernel del filtro interno con ceros.</span><span class="sxs-lookup"><span data-stu-id="5b296-165">This has the effect of simulating a larger filter kernel by padding the internal filter kernel elements with zeros.</span></span>


`StartPadding`

<span data-ttu-id="5b296-166">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-166">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5b296-167">Valores de relleno que se van a aplicar al principio de cada dimensión espacial del filtro y tensores de entrada de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-167">The padding values to be applied to the beginning of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`EndPadding`

<span data-ttu-id="5b296-168">Tipo: \_ Field_size \_ (DimensionCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="5b296-168">Type: \_Field_size\_(DimensionCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="5b296-169">Valores de relleno que se van a aplicar al final de cada dimensión espacial del filtro y tensores de entrada de la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-169">The padding values to be applied to the end of each spatial dimension of the filter and input tensor of the convolution operation.</span></span>


`GroupCount`

<span data-ttu-id="5b296-170">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="5b296-170">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="5b296-171">Número de grupos en los que se va a dividir la operación de circunvolución.</span><span class="sxs-lookup"><span data-stu-id="5b296-171">The number of groups which to divide the convolution operation into.</span></span> <span data-ttu-id="5b296-172">*GroupCount* se puede usar para lograr una circunvolución de nivel de profundidad estableciendo el valor de *GroupCount* igual al número de canales de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-172">*GroupCount* can be used to achieve depth-wise convolution by setting the *GroupCount* equal to the input channel count.</span></span> <span data-ttu-id="5b296-173">Esto divide la circunvolución en una circunvolución independiente por canal de entrada.</span><span class="sxs-lookup"><span data-stu-id="5b296-173">This divides the convolution up into a separate convolution per input channel.</span></span> 

## <a name="availability"></a><span data-ttu-id="5b296-174">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="5b296-174">Availability</span></span>
<span data-ttu-id="5b296-175">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="5b296-175">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="5b296-176">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="5b296-176">Tensor constraints</span></span>
* <span data-ttu-id="5b296-177">*FilterTensor* y *FilterZeroPointTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="5b296-177">*FilterTensor* and *FilterZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="5b296-178">*InputTensor* y *InputZeroPointTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="5b296-178">*InputTensor* and *InputZeroPointTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="5b296-179">*OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="5b296-179">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="5b296-180">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="5b296-180">Tensor support</span></span>
| <span data-ttu-id="5b296-181">Tensores</span><span class="sxs-lookup"><span data-stu-id="5b296-181">Tensor</span></span> | <span data-ttu-id="5b296-182">Clase</span><span class="sxs-lookup"><span data-stu-id="5b296-182">Kind</span></span> | <span data-ttu-id="5b296-183">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="5b296-183">Supported dimension counts</span></span> | <span data-ttu-id="5b296-184">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="5b296-184">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="5b296-185">InputTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-185">InputTensor</span></span> | <span data-ttu-id="5b296-186">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b296-186">Input</span></span> | <span data-ttu-id="5b296-187">4</span><span class="sxs-lookup"><span data-stu-id="5b296-187">4</span></span> | <span data-ttu-id="5b296-188">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b296-188">INT8, UINT8</span></span> |
| <span data-ttu-id="5b296-189">InputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-189">InputScaleTensor</span></span> | <span data-ttu-id="5b296-190">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b296-190">Input</span></span> | <span data-ttu-id="5b296-191">4</span><span class="sxs-lookup"><span data-stu-id="5b296-191">4</span></span> | <span data-ttu-id="5b296-192">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="5b296-192">FLOAT32</span></span> |
| <span data-ttu-id="5b296-193">InputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-193">InputZeroPointTensor</span></span> | <span data-ttu-id="5b296-194">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5b296-194">Optional input</span></span> | <span data-ttu-id="5b296-195">4</span><span class="sxs-lookup"><span data-stu-id="5b296-195">4</span></span> | <span data-ttu-id="5b296-196">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b296-196">INT8, UINT8</span></span> |
| <span data-ttu-id="5b296-197">FilterTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-197">FilterTensor</span></span> | <span data-ttu-id="5b296-198">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b296-198">Input</span></span> | <span data-ttu-id="5b296-199">4</span><span class="sxs-lookup"><span data-stu-id="5b296-199">4</span></span> | <span data-ttu-id="5b296-200">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b296-200">INT8, UINT8</span></span> |
| <span data-ttu-id="5b296-201">FilterScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-201">FilterScaleTensor</span></span> | <span data-ttu-id="5b296-202">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b296-202">Input</span></span> | <span data-ttu-id="5b296-203">4</span><span class="sxs-lookup"><span data-stu-id="5b296-203">4</span></span> | <span data-ttu-id="5b296-204">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="5b296-204">FLOAT32</span></span> |
| <span data-ttu-id="5b296-205">FilterZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-205">FilterZeroPointTensor</span></span> | <span data-ttu-id="5b296-206">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5b296-206">Optional input</span></span> | <span data-ttu-id="5b296-207">4</span><span class="sxs-lookup"><span data-stu-id="5b296-207">4</span></span> | <span data-ttu-id="5b296-208">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b296-208">INT8, UINT8</span></span> |
| <span data-ttu-id="5b296-209">BiasTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-209">BiasTensor</span></span> | <span data-ttu-id="5b296-210">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5b296-210">Optional input</span></span> | <span data-ttu-id="5b296-211">4</span><span class="sxs-lookup"><span data-stu-id="5b296-211">4</span></span> | <span data-ttu-id="5b296-212">INT32</span><span class="sxs-lookup"><span data-stu-id="5b296-212">INT32</span></span> |
| <span data-ttu-id="5b296-213">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-213">OutputScaleTensor</span></span> | <span data-ttu-id="5b296-214">Entrada</span><span class="sxs-lookup"><span data-stu-id="5b296-214">Input</span></span> | <span data-ttu-id="5b296-215">4</span><span class="sxs-lookup"><span data-stu-id="5b296-215">4</span></span> | <span data-ttu-id="5b296-216">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="5b296-216">FLOAT32</span></span> |
| <span data-ttu-id="5b296-217">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-217">OutputZeroPointTensor</span></span> | <span data-ttu-id="5b296-218">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="5b296-218">Optional input</span></span> | <span data-ttu-id="5b296-219">4</span><span class="sxs-lookup"><span data-stu-id="5b296-219">4</span></span> | <span data-ttu-id="5b296-220">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b296-220">INT8, UINT8</span></span> |
| <span data-ttu-id="5b296-221">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="5b296-221">OutputTensor</span></span> | <span data-ttu-id="5b296-222">Output</span><span class="sxs-lookup"><span data-stu-id="5b296-222">Output</span></span> | <span data-ttu-id="5b296-223">4</span><span class="sxs-lookup"><span data-stu-id="5b296-223">4</span></span> | <span data-ttu-id="5b296-224">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="5b296-224">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="5b296-225">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5b296-225">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="5b296-226">**Header**</span><span class="sxs-lookup"><span data-stu-id="5b296-226">**Header**</span></span> | <span data-ttu-id="5b296-227">directml. h</span><span class="sxs-lookup"><span data-stu-id="5b296-227">directml.h</span></span> |