---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Invierte los elementos de una o varias *subsecuencias* de un tensor. El conjunto de subsecuencias que se va a invertir se elige en función de las longitudes de eje y secuencia proporcionadas.
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
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804000"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a><span data-ttu-id="56b93-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="56b93-104">DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="56b93-105">Invierte los elementos de una o varias *subsecuencias* de un tensor.</span><span class="sxs-lookup"><span data-stu-id="56b93-105">Reverses the elements of one or more *subsequences* of a tensor.</span></span> <span data-ttu-id="56b93-106">El conjunto de subsecuencias que se va a invertir se elige en función de las longitudes de eje y secuencia proporcionadas.</span><span class="sxs-lookup"><span data-stu-id="56b93-106">The set of subsequences to be reversed is chosen based on the provided axis and sequence lengths.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="56b93-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="56b93-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="56b93-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="56b93-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="56b93-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="56b93-109">Syntax</span></span>
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="56b93-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="56b93-110">Members</span></span>

`InputTensor`

<span data-ttu-id="56b93-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="56b93-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="56b93-112">Tensor de entrada que contiene los elementos que se invertirán.</span><span class="sxs-lookup"><span data-stu-id="56b93-112">The input tensor containing elements to be reversed.</span></span>


`SequenceLengthsTensor`

<span data-ttu-id="56b93-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="56b93-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="56b93-114">Un tensor que contiene un valor para cada subsecuencia que se va a invertir, que indica la longitud de los elementos de esa subsecuencia.</span><span class="sxs-lookup"><span data-stu-id="56b93-114">A tensor containing a value for each subsequence to be reversed, denoting the length in elements of that subsequence.</span></span> <span data-ttu-id="56b93-115">Solo se invierten los elementos dentro de la longitud de la subsecuencia; Los elementos restantes a lo largo de ese eje se copian en la salida sin cambios.</span><span class="sxs-lookup"><span data-stu-id="56b93-115">Only the elements within the length of the subsequence are reversed; the remaining elements along that axis are copied to the output unchanged.</span></span>

<span data-ttu-id="56b93-116">Este tensor debe tener un recuento de dimensiones  y tamaños iguales a *InputTensor,* excepto para la dimensión especificada por el *parámetro Axis.*</span><span class="sxs-lookup"><span data-stu-id="56b93-116">This tensor must have dimension count and sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter.</span></span> <span data-ttu-id="56b93-117">El tamaño de la *dimensión Eje* debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="56b93-117">The size of the *Axis* dimension must be 1.</span></span> <span data-ttu-id="56b93-118">Por ejemplo, si *InputTensor* tiene tamaños de y Eje es 1, los tamaños de `{2,3,4,5}` *SequenceLengthsTensor* deben ser  `{2,1,4,5}` .</span><span class="sxs-lookup"><span data-stu-id="56b93-118">For example if the *InputTensor* has sizes of `{2,3,4,5}`, and *Axis* is 1, then the sizes of the *SequenceLengthsTensor* must be `{2,1,4,5}`.</span></span>

<span data-ttu-id="56b93-119">Si la longitud de una subsecuencia supera el número máximo de elementos a lo largo de ese eje, este operador se comporta como si el valor se fijara al máximo.</span><span class="sxs-lookup"><span data-stu-id="56b93-119">If the length of a subsequence exceeds the maximum number of elements along that axis, then this operator behaves as if the value were clamped to the maximum.</span></span>


`OutputTensor`

<span data-ttu-id="56b93-120">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="56b93-120">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="56b93-121">Tensor de salida en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="56b93-121">The output tensor to write the results to.</span></span> <span data-ttu-id="56b93-122">Este tensor debe tener los mismos tamaños y tipo de datos que *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="56b93-122">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>


`Axis`

<span data-ttu-id="56b93-123">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="56b93-123">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="56b93-124">Índice de la dimensión sobre la que se invertirán los elementos.</span><span class="sxs-lookup"><span data-stu-id="56b93-124">The index of the dimension to reverse elements over.</span></span> <span data-ttu-id="56b93-125">Este valor debe ser menor que dimensionCount de *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="56b93-125">This value must be less than the DimensionCount of the *InputTensor*.</span></span>

## <a name="examples"></a><span data-ttu-id="56b93-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="56b93-126">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="56b93-127">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="56b93-127">Example 1</span></span>

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

### <a name="example-2-reversing-along-a-different-axis"></a><span data-ttu-id="56b93-128">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="56b93-128">Example 2.</span></span> <span data-ttu-id="56b93-129">Invertir a lo largo de un eje diferente</span><span class="sxs-lookup"><span data-stu-id="56b93-129">Reversing along a different axis</span></span>

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

## <a name="availability"></a><span data-ttu-id="56b93-130">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="56b93-130">Availability</span></span>
<span data-ttu-id="56b93-131">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="56b93-131">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="56b93-132">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="56b93-132">Tensor constraints</span></span>
* <span data-ttu-id="56b93-133">*InputTensor*, *OutputTensor* y *SequenceLengthsTensor* deben tener el mismo *dimensioncount*.</span><span class="sxs-lookup"><span data-stu-id="56b93-133">*InputTensor*, *OutputTensor*, and *SequenceLengthsTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="56b93-134">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de datos*.</span><span class="sxs-lookup"><span data-stu-id="56b93-134">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="56b93-135">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="56b93-135">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="56b93-136">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="56b93-136">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="56b93-137">Tensor</span><span class="sxs-lookup"><span data-stu-id="56b93-137">Tensor</span></span> | <span data-ttu-id="56b93-138">Tipo</span><span class="sxs-lookup"><span data-stu-id="56b93-138">Kind</span></span> | <span data-ttu-id="56b93-139">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="56b93-139">Supported dimension counts</span></span> | <span data-ttu-id="56b93-140">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="56b93-140">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="56b93-141">InputTensor</span><span class="sxs-lookup"><span data-stu-id="56b93-141">InputTensor</span></span> | <span data-ttu-id="56b93-142">Entrada</span><span class="sxs-lookup"><span data-stu-id="56b93-142">Input</span></span> | <span data-ttu-id="56b93-143">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="56b93-143">4 to 5</span></span> | <span data-ttu-id="56b93-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="56b93-144">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="56b93-145">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="56b93-145">SequenceLengthsTensor</span></span> | <span data-ttu-id="56b93-146">Entrada</span><span class="sxs-lookup"><span data-stu-id="56b93-146">Input</span></span> | <span data-ttu-id="56b93-147">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="56b93-147">4 to 5</span></span> | <span data-ttu-id="56b93-148">UINT32</span><span class="sxs-lookup"><span data-stu-id="56b93-148">UINT32</span></span> |
| <span data-ttu-id="56b93-149">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="56b93-149">OutputTensor</span></span> | <span data-ttu-id="56b93-150">Resultados</span><span class="sxs-lookup"><span data-stu-id="56b93-150">Output</span></span> | <span data-ttu-id="56b93-151">De 4 a 5</span><span class="sxs-lookup"><span data-stu-id="56b93-151">4 to 5</span></span> | <span data-ttu-id="56b93-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="56b93-152">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="56b93-153">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="56b93-153">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="56b93-154">Tensor</span><span class="sxs-lookup"><span data-stu-id="56b93-154">Tensor</span></span> | <span data-ttu-id="56b93-155">Tipo</span><span class="sxs-lookup"><span data-stu-id="56b93-155">Kind</span></span> | <span data-ttu-id="56b93-156">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="56b93-156">Supported dimension counts</span></span> | <span data-ttu-id="56b93-157">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="56b93-157">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="56b93-158">InputTensor</span><span class="sxs-lookup"><span data-stu-id="56b93-158">InputTensor</span></span> | <span data-ttu-id="56b93-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="56b93-159">Input</span></span> | <span data-ttu-id="56b93-160">4</span><span class="sxs-lookup"><span data-stu-id="56b93-160">4</span></span> | <span data-ttu-id="56b93-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="56b93-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="56b93-162">SequenceLengthsTensor</span><span class="sxs-lookup"><span data-stu-id="56b93-162">SequenceLengthsTensor</span></span> | <span data-ttu-id="56b93-163">Entrada</span><span class="sxs-lookup"><span data-stu-id="56b93-163">Input</span></span> | <span data-ttu-id="56b93-164">4</span><span class="sxs-lookup"><span data-stu-id="56b93-164">4</span></span> | <span data-ttu-id="56b93-165">UINT32</span><span class="sxs-lookup"><span data-stu-id="56b93-165">UINT32</span></span> |
| <span data-ttu-id="56b93-166">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="56b93-166">OutputTensor</span></span> | <span data-ttu-id="56b93-167">Resultados</span><span class="sxs-lookup"><span data-stu-id="56b93-167">Output</span></span> | <span data-ttu-id="56b93-168">4</span><span class="sxs-lookup"><span data-stu-id="56b93-168">4</span></span> | <span data-ttu-id="56b93-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="56b93-169">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="56b93-170">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56b93-170">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="56b93-171">**Header**</span><span class="sxs-lookup"><span data-stu-id="56b93-171">**Header**</span></span> | <span data-ttu-id="56b93-172">directml.h</span><span class="sxs-lookup"><span data-stu-id="56b93-172">directml.h</span></span> |