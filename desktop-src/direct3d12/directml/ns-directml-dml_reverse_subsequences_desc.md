---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Invierte los elementos de una o más *subsecuencias* de un tensores. El conjunto de subsecuencias que se va a invertir se elige en función del eje y las longitudes de secuencia proporcionadas.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 5baf16c5acd1ce5c5f44e68420e93aabaa276ea7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721298"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="63aaf-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="63aaf-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="63aaf-105">Invierte los elementos de una o más *subsecuencias* de un tensores.</span><span class="sxs-lookup"><span data-stu-id="63aaf-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="63aaf-106">El conjunto de subsecuencias que se va a invertir se elige en función del eje y las longitudes de secuencia proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="63aaf-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63aaf-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="63aaf-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="63aaf-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="63aaf-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="63aaf-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63aaf-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="63aaf-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="63aaf-110">Members</span></span>

`InputTensor`

<span data-ttu-id="63aaf-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63aaf-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63aaf-112">Tensores de entrada que contiene los elementos que se van a invertir.</span><span class="sxs-lookup"><span data-stu-id="63aaf-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="63aaf-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63aaf-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63aaf-114">Un tensores que contiene un valor para cada subsecuencia que se va a invertir, que denota la longitud en elementos de esa subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="63aaf-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="63aaf-115">Solo se invierten los elementos de la longitud de la subsecuencia; los elementos restantes a lo largo del eje se copian en la salida sin cambios.</span><span class="sxs-lookup"><span data-stu-id="63aaf-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="63aaf-116">Este tensores debe tener un número de dimensiones y tamaños igual a *InputTensor*, *excepto* la dimensión especificada por el parámetro de *eje* .</span><span class="sxs-lookup"><span data-stu-id="63aaf-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="63aaf-117">El tamaño de la dimensión del *eje* debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="63aaf-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="63aaf-118">Por ejemplo, si *InputTensor* tiene tamaños de `{2,3,4,5}` y *AXIS* es 1, los tamaños de *SequenceLengthsTensor* deben ser `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="63aaf-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="63aaf-119">Si la longitud de una subsecuencia supera el número máximo de elementos a lo largo de ese eje, este operador se comporta como si el valor estuviera fijado al máximo.</span><span class="sxs-lookup"><span data-stu-id="63aaf-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="63aaf-120">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="63aaf-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="63aaf-121">Tensores de salida en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="63aaf-121">The output tensor to write the results to.</span></span> <span data-ttu-id="63aaf-122">Este tensores debe tener los mismos tamaños y tipo de datos que *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="63aaf-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="63aaf-123">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="63aaf-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="63aaf-124">Índice de la dimensión en la que se van a invertir los elementos.</span><span class="sxs-lookup"><span data-stu-id="63aaf-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="63aaf-125">Este valor debe ser menor que el valor de DimensionCount de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="63aaf-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="63aaf-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="63aaf-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="63aaf-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="63aaf-127">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="63aaf-128">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="63aaf-128">Example 2.</span></span> <span data-ttu-id="63aaf-129">Invertir a lo largo de un eje diferente</span><span class="sxs-lookup"><span data-stu-id="63aaf-129">Reversing along a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a><span data-ttu-id="63aaf-130">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="63aaf-130">Availability</span></span>
<span data-ttu-id="63aaf-131">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="63aaf-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="63aaf-132">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="63aaf-132">Tensor constraints</span></span>
* <span data-ttu-id="63aaf-133">*InputTensor*, *OutputTensor* y *SequenceLengthsTensor* deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="63aaf-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="63aaf-134">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="63aaf-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="63aaf-135">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="63aaf-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="63aaf-136">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="63aaf-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="63aaf-137">Tensores</span><span class="sxs-lookup"><span data-stu-id="63aaf-137">Tensor</span></span> | <span data-ttu-id="63aaf-138">Clase</span><span class="sxs-lookup"><span data-stu-id="63aaf-138">Kind</span></span> | <span data-ttu-id="63aaf-139">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="63aaf-139">Supported dimension counts</span></span> | <span data-ttu-id="63aaf-140">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="63aaf-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="63aaf-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="63aaf-141">InputTensor</span></span> | <span data-ttu-id="63aaf-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="63aaf-142">Input</span></span> | <span data-ttu-id="63aaf-143">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="63aaf-143">4 to 5</span></span> | <span data-ttu-id="63aaf-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="63aaf-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="63aaf-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="63aaf-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="63aaf-146">Entrada</span><span class="sxs-lookup"><span data-stu-id="63aaf-146">Input</span></span> | <span data-ttu-id="63aaf-147">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="63aaf-147">4 to 5</span></span> | <span data-ttu-id="63aaf-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="63aaf-148">UINT32</span></span> |
| <span data-ttu-id="63aaf-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="63aaf-149">OutputTensor</span></span> | <span data-ttu-id="63aaf-150">Output</span><span class="sxs-lookup"><span data-stu-id="63aaf-150">Output</span></span> | <span data-ttu-id="63aaf-151">de 4 a 5</span><span class="sxs-lookup"><span data-stu-id="63aaf-151">4 to 5</span></span> | <span data-ttu-id="63aaf-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="63aaf-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="63aaf-153">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="63aaf-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="63aaf-154">Tensores</span><span class="sxs-lookup"><span data-stu-id="63aaf-154">Tensor</span></span> | <span data-ttu-id="63aaf-155">Clase</span><span class="sxs-lookup"><span data-stu-id="63aaf-155">Kind</span></span> | <span data-ttu-id="63aaf-156">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="63aaf-156">Supported dimension counts</span></span> | <span data-ttu-id="63aaf-157">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="63aaf-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="63aaf-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="63aaf-158">InputTensor</span></span> | <span data-ttu-id="63aaf-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="63aaf-159">Input</span></span> | <span data-ttu-id="63aaf-160">4</span><span class="sxs-lookup"><span data-stu-id="63aaf-160">4</span></span> | <span data-ttu-id="63aaf-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="63aaf-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="63aaf-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="63aaf-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="63aaf-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="63aaf-163">Input</span></span> | <span data-ttu-id="63aaf-164">4</span><span class="sxs-lookup"><span data-stu-id="63aaf-164">4</span></span> | <span data-ttu-id="63aaf-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="63aaf-165">UINT32</span></span> |
| <span data-ttu-id="63aaf-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="63aaf-166">OutputTensor</span></span> | <span data-ttu-id="63aaf-167">Output</span><span class="sxs-lookup"><span data-stu-id="63aaf-167">Output</span></span> | <span data-ttu-id="63aaf-168">4</span><span class="sxs-lookup"><span data-stu-id="63aaf-168">4</span></span> | <span data-ttu-id="63aaf-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="63aaf-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="63aaf-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63aaf-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="63aaf-171">**Header**</span><span class="sxs-lookup"><span data-stu-id="63aaf-171">**Header**</span></span> | <span data-ttu-id="63aaf-172">directml. h</span><span class="sxs-lookup"><span data-stu-id="63aaf-172">directml.h</span></span> |