---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a los subbloques completos de la entrada. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417980"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="f4d7c-104">DML_GATHER_ND1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="f4d7c-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="f4d7c-105">Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a los subbloques completos de la entrada.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="f4d7c-106">Este operador realiza el pseudocódigo siguiente, donde "..." representa una serie de coordenadas, con el comportamiento exacto dependiente del recuento de dimensiones de lote, entrada e índices.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="f4d7c-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="f4d7c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="f4d7c-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="f4d7c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4d7c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f4d7c-109">Syntax</span></span>

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a><span data-ttu-id="f4d7c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="f4d7c-110">Members</span></span>

`InputTensor`

<span data-ttu-id="f4d7c-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4d7c-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4d7c-112">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="f4d7c-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4d7c-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4d7c-114">Tensor que contiene los índices.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-114">The tensor containing the indices.</span></span> <span data-ttu-id="f4d7c-115">DimensionCount de este tensor debe coincidir *con InputTensor.DimensionCount.* </span><span class="sxs-lookup"><span data-stu-id="f4d7c-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f4d7c-116">La última dimensión de *IndicesTensor* es realmente el número de coordenadas por tupla de índice y no puede superar *InputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f4d7c-117">Por ejemplo, un tensor de índices de *tamaños* con ÍndicesDimensionCount = 3 significa una matriz 4x5 de tuplas de dos coordenadas que indexan en `{1,4,5,2}`  *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="f4d7c-118">A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="f4d7c-119">Los índices negativos se interpretan como relativos al final de la dimensión respectiva.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="f4d7c-120">Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="f4d7c-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="f4d7c-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="f4d7c-122">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-122">The tensor to write the results to.</span></span> <span data-ttu-id="f4d7c-123">DimensionCount *y* *DataType de* este tensor deben coincidir *con InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="f4d7c-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="f4d7c-124">Los *outputTensor.Sizes esperados* son la concatenación de los segmentos iniciales *IndicesTensor.Sizes* y el segmento final *InputTensor.Sizes,* que produce lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="f4d7c-125">Las dimensiones están alineadas a la derecha, con 1 valor inicial anteponer si es necesario para satisfacer *OutputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="f4d7c-126">Este es un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-126">Here's an example.</span></span>

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

<span data-ttu-id="f4d7c-127">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f4d7c-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f4d7c-128">Número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las iniciales irrelevantes, que abarcan `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="f4d7c-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="f4d7c-129">Por ejemplo, *dados InputTensor.Sizes*  =  `{1,1,4,6}` y = `InputDimensionCount` 3, los índices significativos reales son `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="f4d7c-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="f4d7c-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f4d7c-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f4d7c-131">Número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las iniciales irrelevantes, que van [1, *IndicesTensor.DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="f4d7c-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="f4d7c-132">Por ejemplo, *dados IndicesTensor.Sizes* e  =  `{1,1,4,6}` *IndicesDimensionCount* = 3, los índices significativos reales son `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="f4d7c-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="f4d7c-133">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="f4d7c-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="f4d7c-134">Número de dimensiones dentro de cada tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) que se consideran lotes independientes, que se encuentran dentro de [0, *InputTensor.DimensionCount*) y [0, *IndicesTensor.DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="f4d7c-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="f4d7c-135">El número de lotes puede ser 0, lo que implica un único lote.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="f4d7c-136">Por ejemplo, *dados indicesTensor.Sizes*  =  `{1,3,4,5,6,7}` e *IndicesDimensionCount* = 5 y = 2, hay lotes e `BatchDimensionCount` índices `{3,4}` significativos `{5,6,7}` .</span><span class="sxs-lookup"><span data-stu-id="f4d7c-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4d7c-137">Comentarios</span><span class="sxs-lookup"><span data-stu-id="f4d7c-137">Remarks</span></span>
<span data-ttu-id="f4d7c-138">**DML_GATHER_ND1_OPERATOR_DESC** *agrega BatchDimensionCount* y es equivalente a [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) cuando *BatchDimensionCount* = 0.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="f4d7c-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="f4d7c-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="f4d7c-140">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-140">Example 1.</span></span> <span data-ttu-id="f4d7c-141">Remapping 1D</span><span class="sxs-lookup"><span data-stu-id="f4d7c-141">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="f4d7c-142">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-142">Example 2.</span></span> <span data-ttu-id="f4d7c-143">2D remapping with batch count (Remapping 2D con recuento de lotes)</span><span class="sxs-lookup"><span data-stu-id="f4d7c-143">2D remapping with batch count</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a><span data-ttu-id="f4d7c-144">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="f4d7c-144">Availability</span></span>
<span data-ttu-id="f4d7c-145">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="f4d7c-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="f4d7c-146">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="f4d7c-146">Tensor constraints</span></span>
* <span data-ttu-id="f4d7c-147">*Los índicesTensor*, *InputTensor* y *OutputTensor* deben tener el mismo *dimensioncount.*</span><span class="sxs-lookup"><span data-stu-id="f4d7c-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="f4d7c-148">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de datos*.</span><span class="sxs-lookup"><span data-stu-id="f4d7c-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="f4d7c-149">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="f4d7c-149">Tensor support</span></span>
| <span data-ttu-id="f4d7c-150">Tensor</span><span class="sxs-lookup"><span data-stu-id="f4d7c-150">Tensor</span></span> | <span data-ttu-id="f4d7c-151">Tipo</span><span class="sxs-lookup"><span data-stu-id="f4d7c-151">Kind</span></span> | <span data-ttu-id="f4d7c-152">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="f4d7c-152">Supported dimension counts</span></span> | <span data-ttu-id="f4d7c-153">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="f4d7c-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="f4d7c-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="f4d7c-154">InputTensor</span></span> | <span data-ttu-id="f4d7c-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4d7c-155">Input</span></span> | <span data-ttu-id="f4d7c-156">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f4d7c-156">1 to 8</span></span> | <span data-ttu-id="f4d7c-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f4d7c-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="f4d7c-158">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="f4d7c-158">IndicesTensor</span></span> | <span data-ttu-id="f4d7c-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="f4d7c-159">Input</span></span> | <span data-ttu-id="f4d7c-160">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f4d7c-160">1 to 8</span></span> | <span data-ttu-id="f4d7c-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="f4d7c-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="f4d7c-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="f4d7c-162">OutputTensor</span></span> | <span data-ttu-id="f4d7c-163">Resultados</span><span class="sxs-lookup"><span data-stu-id="f4d7c-163">Output</span></span> | <span data-ttu-id="f4d7c-164">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="f4d7c-164">1 to 8</span></span> | <span data-ttu-id="f4d7c-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="f4d7c-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="f4d7c-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f4d7c-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="f4d7c-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="f4d7c-167">**Header**</span></span> | <span data-ttu-id="f4d7c-168">directml.h</span><span class="sxs-lookup"><span data-stu-id="f4d7c-168">directml.h</span></span> |
