---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Realiza una función de multiplicación de matriz en datos cuantificados. Este operador es matemáticamente equivalente a descuantizar las entradas, después realizar la multiplicación de la matriz y, a continuación, cuantificar la salida.
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
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418051"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a><span data-ttu-id="fd743-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="fd743-104">DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="fd743-105">Realiza una función de multiplicación de matriz en datos cuantificados.</span><span class="sxs-lookup"><span data-stu-id="fd743-105">Performs a matrix multiplication function on quantized data.</span></span> <span data-ttu-id="fd743-106">Este operador es matemáticamente equivalente a descuantizar las entradas, después realizar la multiplicación de la matriz y, a continuación, cuantificar la salida.</span><span class="sxs-lookup"><span data-stu-id="fd743-106">This operator is mathematically equivalent to dequantizing the inputs, then performing matrix multiply, and then quantizing the output.</span></span>

<span data-ttu-id="fd743-107">Este operador requiere que la matriz multiplique los tensores de entrada sea 4D, cuyo formato es `{ BatchCount, ChannelCount, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="fd743-107">This operator requires the matrix multiply input tensors to be 4D which are formatted as `{ BatchCount, ChannelCount, Height, Width }`.</span></span> <span data-ttu-id="fd743-108">El operador de multiplicación de matriz realizará batchcount \* channelcount número de multiplicaciones de matrices independientes.</span><span class="sxs-lookup"><span data-stu-id="fd743-108">The matrix multiply operator will perform BatchCount \* ChannelCount number of independent matrix multiplications.</span></span> 

<span data-ttu-id="fd743-109">Por ejemplo, si *ATensor* tiene tamaños de y  BTensor tiene tamaños de y OutputTensor tiene tamaños de , el operador de multiplicación de matriz realizará multiplicaciones de matrices independientes de BatchCount \* ChannelCount de dimensiones `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.</span><span class="sxs-lookup"><span data-stu-id="fd743-109">For example, if *ATensor* has *Sizes* of `{ BatchCount, ChannelCount, M, K }`, and *BTensor* has *Sizes* of `{ BatchCount, ChannelCount, K, N }`, and *OutputTensor* has *Sizes* of `{ BatchCount, ChannelCount, M, N }`, then the matrix multiply operator will perform BatchCount \* ChannelCount independent matrix multiplications of dimensions {M,K} x {K,N} = {M,N}.</span></span> 

### <a name="dequantize-function"></a><span data-ttu-id="fd743-110">Función Dequantize</span><span class="sxs-lookup"><span data-stu-id="fd743-110">Dequantize function</span></span>

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a><span data-ttu-id="fd743-111">Función Quantize</span><span class="sxs-lookup"><span data-stu-id="fd743-111">Quantize function</span></span>

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> <span data-ttu-id="fd743-112">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="fd743-112">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="fd743-113">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="fd743-113">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="fd743-114">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="fd743-114">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="fd743-115">Miembros</span><span class="sxs-lookup"><span data-stu-id="fd743-115">Members</span></span>

`ATensor`

<span data-ttu-id="fd743-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-117">Tensor que contiene los datos A.</span><span class="sxs-lookup"><span data-stu-id="fd743-117">A tensor containing the A data.</span></span> <span data-ttu-id="fd743-118">Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, M, K }` .</span><span class="sxs-lookup"><span data-stu-id="fd743-118">This tensor's dimensions should be `{ BatchCount, ChannelCount, M, K }`.</span></span>


`AScaleTensor`

<span data-ttu-id="fd743-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-120">Tensor que contiene los datos de escala de ATensor.</span><span class="sxs-lookup"><span data-stu-id="fd743-120">A tensor containing the ATensor scale data.</span></span> <span data-ttu-id="fd743-121">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `AScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, M, 1 }` cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="fd743-121">The expected dimensions of the `AScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="fd743-122">Estos valores de escala se usan para descuantizar los valores A.</span><span class="sxs-lookup"><span data-stu-id="fd743-122">These scale values are used for dequantizing the A values.</span></span>


`AZeroPointTensor`

<span data-ttu-id="fd743-123">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-123">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-124">Tensor opcional que contiene los datos de punto cero de *ATensor.*</span><span class="sxs-lookup"><span data-stu-id="fd743-124">An optional tensor containing the *ATensor* zero point data.</span></span> <span data-ttu-id="fd743-125">Las dimensiones esperadas de AZeroPointTensor son si se requiere una cuantificación por tensor o si se requiere una `{ 1, 1, 1, 1 }` `{ 1, 1, M, 1 }` cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="fd743-125">The expected dimensions of the AZeroPointTensor are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="fd743-126">Estos valores de punto cero se usan para descuantizar los valores de ATensor.</span><span class="sxs-lookup"><span data-stu-id="fd743-126">These zero point values are used for dequantizing the ATensor values.</span></span>


`BTensor`

<span data-ttu-id="fd743-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-128">Tensor que contiene los datos B.</span><span class="sxs-lookup"><span data-stu-id="fd743-128">A tensor containing the B data.</span></span> <span data-ttu-id="fd743-129">Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, K, N }` .</span><span class="sxs-lookup"><span data-stu-id="fd743-129">This tensor's dimensions should be `{ BatchCount, ChannelCount, K, N }`.</span></span>


`BScaleTensor`

<span data-ttu-id="fd743-130">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-130">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-131">Tensor que contiene los datos de escala *de BTensor.*</span><span class="sxs-lookup"><span data-stu-id="fd743-131">A tensor containing the *BTensor* scale data.</span></span> <span data-ttu-id="fd743-132">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `BScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, 1, N }` cuantificación por columna.</span><span class="sxs-lookup"><span data-stu-id="fd743-132">The expected dimensions of the `BScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="fd743-133">Estos valores de escala se usan para descuantizar los *valores de BTensor.*</span><span class="sxs-lookup"><span data-stu-id="fd743-133">These scale values are used for dequantizing the *BTensor* values.</span></span>


`BZeroPointTensor`

<span data-ttu-id="fd743-134">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-134">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-135">Tensor opcional que contiene los datos de punto cero de *BTensor.*</span><span class="sxs-lookup"><span data-stu-id="fd743-135">An optional tensor containing the *BTensor* zero point data.</span></span> <span data-ttu-id="fd743-136">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `BZeroPointTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, 1, N }` cuantificación por columna.</span><span class="sxs-lookup"><span data-stu-id="fd743-136">The expected dimensions of the `BZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, 1, N }` if per column quantization is required.</span></span> <span data-ttu-id="fd743-137">Estos valores de punto cero se usan para descuantizar los *valores de BTensor.*</span><span class="sxs-lookup"><span data-stu-id="fd743-137">These zero point values are used for dequantizing the *BTensor* values.</span></span>


`OutputScaleTensor`

<span data-ttu-id="fd743-138">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-138">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-139">Tensor que contiene los datos de escala de filtro.</span><span class="sxs-lookup"><span data-stu-id="fd743-139">A tensor containing the filter scale data.</span></span> <span data-ttu-id="fd743-140">Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `OutputScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, M, 1 }` cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="fd743-140">The expected dimensions of the `OutputScaleTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required, or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="fd743-141">Este valor de escala se usa para descuantizar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="fd743-141">This scale value is used for dequantizing the filter values.</span></span>


`OutputZeroPointTensor`

<span data-ttu-id="fd743-142">Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-142">Type: _Maybenull\_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-143">Tensor opcional que contiene los datos de punto cero de filtro.</span><span class="sxs-lookup"><span data-stu-id="fd743-143">An optional tensor containing the filter zero point data.</span></span> <span data-ttu-id="fd743-144">Las dimensiones esperadas de son si se requiere una cuantificación por `OutputZeroPointTensor` `{ 1, 1, 1, 1 }` tensor o si se requiere una `{ 1, 1, M, 1 }` cuantificación por fila.</span><span class="sxs-lookup"><span data-stu-id="fd743-144">The expected dimensions of the `OutputZeroPointTensor` are `{ 1, 1, 1, 1 }` if per tensor quantization is required or `{ 1, 1, M, 1 }` if per row quantization is required.</span></span> <span data-ttu-id="fd743-145">Este valor de punto cero se usa para descuantizar los valores de filtro.</span><span class="sxs-lookup"><span data-stu-id="fd743-145">This zero point value is used for dequantizing the filter values.</span></span>


`OutputTensor`

<span data-ttu-id="fd743-146">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="fd743-146">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="fd743-147">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="fd743-147">A tensor to write the results to.</span></span> <span data-ttu-id="fd743-148">Las dimensiones de este tensor son `{ BatchCount, ChannelCount, M, N }` .</span><span class="sxs-lookup"><span data-stu-id="fd743-148">This tensor's dimensions are `{ BatchCount, ChannelCount, M, N }`.</span></span>

## <a name="availability"></a><span data-ttu-id="fd743-149">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="fd743-149">Availability</span></span>
<span data-ttu-id="fd743-150">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="fd743-150">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="fd743-151">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="fd743-151">Tensor constraints</span></span>
* <span data-ttu-id="fd743-152">*ATensor* y `AZeroPointTensor` deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="fd743-152">*ATensor* and `AZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="fd743-153">*BTensor* y `BZeroPointTensor` deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="fd743-153">*BTensor* and `BZeroPointTensor` must have the same *DataType*.</span></span>
* <span data-ttu-id="fd743-154">*OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="fd743-154">*OutputTensor* and `OutputZeroPointTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="fd743-155">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="fd743-155">Tensor support</span></span>
| <span data-ttu-id="fd743-156">Tensor</span><span class="sxs-lookup"><span data-stu-id="fd743-156">Tensor</span></span> | <span data-ttu-id="fd743-157">Tipo</span><span class="sxs-lookup"><span data-stu-id="fd743-157">Kind</span></span> | <span data-ttu-id="fd743-158">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="fd743-158">Supported dimension counts</span></span> | <span data-ttu-id="fd743-159">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="fd743-159">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="fd743-160">ATensor</span><span class="sxs-lookup"><span data-stu-id="fd743-160">ATensor</span></span> | <span data-ttu-id="fd743-161">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd743-161">Input</span></span> | <span data-ttu-id="fd743-162">4</span><span class="sxs-lookup"><span data-stu-id="fd743-162">4</span></span> | <span data-ttu-id="fd743-163">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="fd743-163">INT8, UINT8</span></span> |
| <span data-ttu-id="fd743-164">AScaleTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-164">AScaleTensor</span></span> | <span data-ttu-id="fd743-165">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd743-165">Input</span></span> | <span data-ttu-id="fd743-166">4</span><span class="sxs-lookup"><span data-stu-id="fd743-166">4</span></span> | <span data-ttu-id="fd743-167">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="fd743-167">FLOAT32</span></span> |
| <span data-ttu-id="fd743-168">AZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-168">AZeroPointTensor</span></span> | <span data-ttu-id="fd743-169">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="fd743-169">Optional input</span></span> | <span data-ttu-id="fd743-170">4</span><span class="sxs-lookup"><span data-stu-id="fd743-170">4</span></span> | <span data-ttu-id="fd743-171">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="fd743-171">INT8, UINT8</span></span> |
| <span data-ttu-id="fd743-172">BTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-172">BTensor</span></span> | <span data-ttu-id="fd743-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd743-173">Input</span></span> | <span data-ttu-id="fd743-174">4</span><span class="sxs-lookup"><span data-stu-id="fd743-174">4</span></span> | <span data-ttu-id="fd743-175">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="fd743-175">INT8, UINT8</span></span> |
| <span data-ttu-id="fd743-176">BScaleTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-176">BScaleTensor</span></span> | <span data-ttu-id="fd743-177">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd743-177">Input</span></span> | <span data-ttu-id="fd743-178">4</span><span class="sxs-lookup"><span data-stu-id="fd743-178">4</span></span> | <span data-ttu-id="fd743-179">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="fd743-179">FLOAT32</span></span> |
| <span data-ttu-id="fd743-180">BZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-180">BZeroPointTensor</span></span> | <span data-ttu-id="fd743-181">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="fd743-181">Optional input</span></span> | <span data-ttu-id="fd743-182">4</span><span class="sxs-lookup"><span data-stu-id="fd743-182">4</span></span> | <span data-ttu-id="fd743-183">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="fd743-183">INT8, UINT8</span></span> |
| <span data-ttu-id="fd743-184">OutputScaleTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-184">OutputScaleTensor</span></span> | <span data-ttu-id="fd743-185">Entrada</span><span class="sxs-lookup"><span data-stu-id="fd743-185">Input</span></span> | <span data-ttu-id="fd743-186">4</span><span class="sxs-lookup"><span data-stu-id="fd743-186">4</span></span> | <span data-ttu-id="fd743-187">FLOAT32</span><span class="sxs-lookup"><span data-stu-id="fd743-187">FLOAT32</span></span> |
| <span data-ttu-id="fd743-188">OutputZeroPointTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-188">OutputZeroPointTensor</span></span> | <span data-ttu-id="fd743-189">Entrada opcional</span><span class="sxs-lookup"><span data-stu-id="fd743-189">Optional input</span></span> | <span data-ttu-id="fd743-190">4</span><span class="sxs-lookup"><span data-stu-id="fd743-190">4</span></span> | <span data-ttu-id="fd743-191">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="fd743-191">INT8, UINT8</span></span> |
| <span data-ttu-id="fd743-192">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="fd743-192">OutputTensor</span></span> | <span data-ttu-id="fd743-193">Resultados</span><span class="sxs-lookup"><span data-stu-id="fd743-193">Output</span></span> | <span data-ttu-id="fd743-194">4</span><span class="sxs-lookup"><span data-stu-id="fd743-194">4</span></span> | <span data-ttu-id="fd743-195">INT8, UINT8</span><span class="sxs-lookup"><span data-stu-id="fd743-195">INT8, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="fd743-196">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fd743-196">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="fd743-197">**Header**</span><span class="sxs-lookup"><span data-stu-id="fd743-197">**Header**</span></span> | <span data-ttu-id="fd743-198">directml.h</span><span class="sxs-lookup"><span data-stu-id="fd743-198">directml.h</span></span> |