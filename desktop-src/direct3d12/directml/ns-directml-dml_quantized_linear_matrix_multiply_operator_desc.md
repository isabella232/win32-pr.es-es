---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Realiza una función de multiplicación de matrices en datos cuantificados. Este operador es matemáticamente equivalente a descuantificar las entradas y, a continuación, realizar la multiplicación de la matriz y cuantificar la salida.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721301"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="6e4fc-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="6e4fc-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="6e4fc-105">Realiza una función de multiplicación de matrices en datos cuantificados.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="6e4fc-106">Este operador es matemáticamente equivalente a descuantificar las entradas y, a continuación, realizar la multiplicación de la matriz y cuantificar la salida.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="6e4fc-107">Este operador requiere que la matriz multiplique los idiomas de entrada a 4D, cuyo formato es `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="6e4fc-108">El operador de multiplicación de la matriz realizará el BatchCount \* ChannelCount número de multiplicaciones de matriz independiente.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="6e4fc-109">Por ejemplo, si *ATensor* tiene  los tamaños `{ BatchCount, ChannelCount, M, K }` , y *BTensor* tiene *tamaños* `{ BatchCount, ChannelCount, K, N }` , y *OutputTensor* tiene *tamaños* `{ BatchCount, ChannelCount, M, N }` , el operador de multiplicación de la matriz realizará la multiplicación de las dimensiones de la matriz independiente BatchCount \* ChannelCount {m, K} x {k, n} = {m, n}.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="6e4fc-110">Descuantificar función</span><span class="sxs-lookup"><span data-stu-id="6e4fc-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="6e4fc-111">Función cuantificate</span><span class="sxs-lookup"><span data-stu-id="6e4fc-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="6e4fc-112">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="6e4fc-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="6e4fc-113">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="6e4fc-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4fc-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6e4fc-114">Syntax</span></span>
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a><span data-ttu-id="6e4fc-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="6e4fc-115">Members</span></span>

`ATensor`

<span data-ttu-id="6e4fc-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-117">Tensores que contiene los datos.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-117">A tensor containing the A data.</span></span> <span data-ttu-id="6e4fc-118">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="6e4fc-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-120">Tensores que contiene los datos de la escala ATensor.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="6e4fc-121">Las dimensiones esperadas de `AScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="6e4fc-122">Estos valores de escala se usan para descuantificar los valores de un.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="6e4fc-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-124">Un tensores opcional que contiene los datos de cero puntos de *ATensor* .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="6e4fc-125">Las dimensiones esperadas de AZeroPointTensor son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="6e4fc-126">Estos valores de punto cero se usan para descuantificar los valores de ATensor.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="6e4fc-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-128">Tensores que contiene los datos de B.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-128">A tensor containing the B data.</span></span> <span data-ttu-id="6e4fc-129">Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="6e4fc-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-131">Tensores que contiene los datos de la escala *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="6e4fc-132">Las dimensiones esperadas de `BScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, 1, N }` si se requiere la cuantificación por columna.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="6e4fc-133">Estos valores de escala se usan para descuantificar los valores de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="6e4fc-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-135">Un tensores opcional que contiene los datos de cero puntos de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="6e4fc-136">Las dimensiones esperadas de `BZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, 1, N }` si se requiere la cuantificación por columna.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="6e4fc-137">Estos valores de punto cero se usan para descuantificar los valores de *BTensor* .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="6e4fc-138">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-139">Tensores que contiene los datos de la escala del filtro.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="6e4fc-140">Las dimensiones esperadas de `OutputScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="6e4fc-141">Este valor de escala se usa para descuantificar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="6e4fc-142">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-143">Un tensores opcional que contiene los datos del punto cero del filtro.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="6e4fc-144">Las dimensiones esperadas de `OutputZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="6e4fc-145">Este valor de punto cero se usa para descuantificar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="6e4fc-146">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="6e4fc-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="6e4fc-147">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-147">A tensor to write the results to.</span></span> <span data-ttu-id="6e4fc-148">Las dimensiones de este tensores son `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="6e4fc-149">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="6e4fc-149">Availability</span></span>
<span data-ttu-id="6e4fc-150">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="6e4fc-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="6e4fc-151">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="6e4fc-151">Tensor constraints</span></span>
* <span data-ttu-id="6e4fc-152">*ATensor* y `AZeroPointTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="6e4fc-153">*BTensor* y `BZeroPointTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="6e4fc-154">*OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="6e4fc-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="6e4fc-155">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="6e4fc-155">Tensor support</span></span>
| <span data-ttu-id="6e4fc-156">Tensores</span><span class="sxs-lookup"><span data-stu-id="6e4fc-156">Tensor</span></span> | <span data-ttu-id="6e4fc-157">Clase</span><span class="sxs-lookup"><span data-stu-id="6e4fc-157">Kind</span></span> | <span data-ttu-id="6e4fc-158">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="6e4fc-158">Supported dimension counts</span></span> | <span data-ttu-id="6e4fc-159">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="6e4fc-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="6e4fc-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-160">ATensor</span></span> | <span data-ttu-id="6e4fc-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e4fc-161">Input</span></span> | <span data-ttu-id="6e4fc-162">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-162">4</span></span> | <span data-ttu-id="6e4fc-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="6e4fc-163">INT8, UINT8</span></span> |
| <span data-ttu-id="6e4fc-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-164">AScaleTensor</span></span> | <span data-ttu-id="6e4fc-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e4fc-165">Input</span></span> | <span data-ttu-id="6e4fc-166">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-166">4</span></span> | <span data-ttu-id="6e4fc-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="6e4fc-167">FLOAT32</span></span> |
| <span data-ttu-id="6e4fc-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-168">AZeroPointTensor</span></span> | <span data-ttu-id="6e4fc-169">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="6e4fc-169">Optional input</span></span> | <span data-ttu-id="6e4fc-170">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-170">4</span></span> | <span data-ttu-id="6e4fc-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="6e4fc-171">INT8, UINT8</span></span> |
| <span data-ttu-id="6e4fc-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-172">BTensor</span></span> | <span data-ttu-id="6e4fc-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e4fc-173">Input</span></span> | <span data-ttu-id="6e4fc-174">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-174">4</span></span> | <span data-ttu-id="6e4fc-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="6e4fc-175">INT8, UINT8</span></span> |
| <span data-ttu-id="6e4fc-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-176">BScaleTensor</span></span> | <span data-ttu-id="6e4fc-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e4fc-177">Input</span></span> | <span data-ttu-id="6e4fc-178">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-178">4</span></span> | <span data-ttu-id="6e4fc-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="6e4fc-179">FLOAT32</span></span> |
| <span data-ttu-id="6e4fc-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-180">BZeroPointTensor</span></span> | <span data-ttu-id="6e4fc-181">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="6e4fc-181">Optional input</span></span> | <span data-ttu-id="6e4fc-182">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-182">4</span></span> | <span data-ttu-id="6e4fc-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="6e4fc-183">INT8, UINT8</span></span> |
| <span data-ttu-id="6e4fc-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-184">OutputScaleTensor</span></span> | <span data-ttu-id="6e4fc-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="6e4fc-185">Input</span></span> | <span data-ttu-id="6e4fc-186">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-186">4</span></span> | <span data-ttu-id="6e4fc-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="6e4fc-187">FLOAT32</span></span> |
| <span data-ttu-id="6e4fc-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="6e4fc-189">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="6e4fc-189">Optional input</span></span> | <span data-ttu-id="6e4fc-190">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-190">4</span></span> | <span data-ttu-id="6e4fc-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="6e4fc-191">INT8, UINT8</span></span> |
| <span data-ttu-id="6e4fc-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="6e4fc-192">OutputTensor</span></span> | <span data-ttu-id="6e4fc-193">Output</span><span class="sxs-lookup"><span data-stu-id="6e4fc-193">Output</span></span> | <span data-ttu-id="6e4fc-194">4</span><span class="sxs-lookup"><span data-stu-id="6e4fc-194">4</span></span> | <span data-ttu-id="6e4fc-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="6e4fc-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="6e4fc-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6e4fc-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="6e4fc-197">**Header**</span><span class="sxs-lookup"><span data-stu-id="6e4fc-197">**Header**</span></span> | <span data-ttu-id="6e4fc-198">directml. h</span><span class="sxs-lookup"><span data-stu-id="6e4fc-198">directml.h</span></span> |