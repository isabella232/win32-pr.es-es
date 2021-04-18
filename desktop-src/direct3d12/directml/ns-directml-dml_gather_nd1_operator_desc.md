---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Recopila elementos de la tensores de entrada, mediante los índices tensores para reasignar los índices a subbloqueos completos de la entrada. | DML_GATHER_ND1_OPERATOR_DESC
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
ms.openlocfilehash: dc7f33f50fa6a0c1cd2850b8e02aad30d75afeb1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105721418"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a><span data-ttu-id="a3273-104">DML_GATHER_ND1_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="a3273-104">DML_GATHER_ND1_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="a3273-105">Recopila elementos de la tensores de entrada, mediante los índices tensores para reasignar los índices a subbloqueos completos de la entrada.</span><span class="sxs-lookup"><span data-stu-id="a3273-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="a3273-106">Este operador realiza el siguiente pseudocódigo, donde "..." representa una serie de coordenadas, con el comportamiento exacto que depende del número de dimensiones del lote, de entrada y de índices.</span><span class="sxs-lookup"><span data-stu-id="a3273-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the batch, input, and indices dimension count.</span></span>

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> <span data-ttu-id="a3273-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="a3273-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="a3273-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="a3273-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="a3273-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a3273-109">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a3273-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="a3273-110">Members</span></span>

`InputTensor`

<span data-ttu-id="a3273-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a3273-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a3273-112">Tensores del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="a3273-112">The tensor to read from.</span></span>

`IndicesTensor`

<span data-ttu-id="a3273-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a3273-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a3273-114">Tensores que contiene los índices.</span><span class="sxs-lookup"><span data-stu-id="a3273-114">The tensor containing the indices.</span></span> <span data-ttu-id="a3273-115">El *DimensionCount* de este tensores debe coincidir con *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a3273-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="a3273-116">La última dimensión de *IndicesTensor* es en realidad el número de coordenadas por tupla de índice y no puede superar *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a3273-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="a3273-117">Por ejemplo, un índice tensores de *tamaños* `{1,4,5,2}` con *IndicesDimensionCount* = 3 significa una matriz 4x5 de tuplas de 2 coordenadas que indexan en *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="a3273-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="a3273-118">A partir de `DML_FEATURE_LEVEL_3_0` , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensores.</span><span class="sxs-lookup"><span data-stu-id="a3273-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="a3273-119">Los índices negativos se interpretan como en relación con el final de la dimensión respectiva.</span><span class="sxs-lookup"><span data-stu-id="a3273-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="a3273-120">Por ejemplo, un índice de-1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="a3273-120">For example, an index of -1 refers to the last element along that dimension.</span></span>

`OutputTensor`

<span data-ttu-id="a3273-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="a3273-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="a3273-122">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="a3273-122">The tensor to write the results to.</span></span> <span data-ttu-id="a3273-123">*DimensionCount* y *DataType* de este tensores deben coincidir con *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a3273-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="a3273-124">El *OutputTensor esperado. los tamaños* son la concatenación de los segmentos de *IndicesTensor. Sizes* iniciales y *InputTensor. Sizes* final, que produce lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="a3273-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment, which yields the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="a3273-125">Las dimensiones están alineadas a la derecha, con un valor inicial de 1 delante, si es necesario, para satisfacer *OutputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a3273-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="a3273-126">Aquí tiene un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="a3273-126">Here's an example.</span></span>

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

<span data-ttu-id="a3273-127">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a3273-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a3273-128">El número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las principales que no son relevantes, que van `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="a3273-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="a3273-129">Por ejemplo, dado *InputTensor. Sizes*  =  `{1,1,4,6}` y `InputDimensionCount` = 3, los índices significativos reales son `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="a3273-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`IndicesDimensionCount`

<span data-ttu-id="a3273-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a3273-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a3273-131">El número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las principales que no sean importantes, que abarcan [1, *IndicesTensor. DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="a3273-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="a3273-132">Por ejemplo, dado *IndicesTensor. Sizes*  =  `{1,1,4,6}` y *IndicesDimensionCount* = 3, los índices significativos reales son `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="a3273-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

`BatchDimensionCount`

<span data-ttu-id="a3273-133">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="a3273-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="a3273-134">El número de dimensiones dentro de cada tensores (*InputTensor*, *IndicesTensor*, *OutputTensor*) que se consideran lotes independientes, que van dentro de [0, *InputTensor. DimensionCount*) y [0, *IndicesTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="a3273-134">The number of dimensions within each tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) that are considered independent batches, ranging within both [0, *InputTensor.DimensionCount*) and [0, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="a3273-135">El número de lotes puede ser 0, lo que implica un único lote.</span><span class="sxs-lookup"><span data-stu-id="a3273-135">The batch count can be 0, implying a single batch.</span></span> <span data-ttu-id="a3273-136">Por ejemplo, dado *IndicesTensor. Sizes*  =  `{1,3,4,5,6,7}` y *IndicesDimensionCount* = 5 y `BatchDimensionCount` = 2, hay lotes `{3,4}` y índices significativos `{5,6,7}` .</span><span class="sxs-lookup"><span data-stu-id="a3273-136">For example, given *IndicesTensor.Sizes* = `{1,3,4,5,6,7}`, and *IndicesDimensionCount* = 5 and `BatchDimensionCount` = 2, there are batches `{3,4}` and meaningful indices `{5,6,7}`.</span></span>

## <a name="remarks"></a><span data-ttu-id="a3273-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a3273-137">Remarks</span></span>
<span data-ttu-id="a3273-138">**DML_GATHER_ND1_OPERATOR_DESC** agrega *BatchDimensionCount* y es equivalente a [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) cuando *BatchDimensionCount* = 0.</span><span class="sxs-lookup"><span data-stu-id="a3273-138">**DML_GATHER_ND1_OPERATOR_DESC** adds *BatchDimensionCount*, and is equivalent to [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) when *BatchDimensionCount* = 0.</span></span>

## <a name="examples"></a><span data-ttu-id="a3273-139">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="a3273-139">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="a3273-140">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="a3273-140">Example 1.</span></span> <span data-ttu-id="a3273-141">reasignación 1D</span><span class="sxs-lookup"><span data-stu-id="a3273-141">1D remapping</span></span>

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

### <a name="example-2-2d-remapping-with-batch-count"></a><span data-ttu-id="a3273-142">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="a3273-142">Example 2.</span></span> <span data-ttu-id="a3273-143">reasignación de 2D con recuento de lotes</span><span class="sxs-lookup"><span data-stu-id="a3273-143">2D remapping with batch count</span></span>

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

## <a name="availability"></a><span data-ttu-id="a3273-144">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="a3273-144">Availability</span></span>
<span data-ttu-id="a3273-145">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="a3273-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="a3273-146">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="a3273-146">Tensor constraints</span></span>
* <span data-ttu-id="a3273-147">*IndicesTensor*, *InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="a3273-147">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="a3273-148">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="a3273-148">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="a3273-149">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="a3273-149">Tensor support</span></span>
| <span data-ttu-id="a3273-150">Tensores</span><span class="sxs-lookup"><span data-stu-id="a3273-150">Tensor</span></span> | <span data-ttu-id="a3273-151">Clase</span><span class="sxs-lookup"><span data-stu-id="a3273-151">Kind</span></span> | <span data-ttu-id="a3273-152">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="a3273-152">Supported dimension counts</span></span> | <span data-ttu-id="a3273-153">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="a3273-153">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="a3273-154">InputTensor</span><span class="sxs-lookup"><span data-stu-id="a3273-154">InputTensor</span></span> | <span data-ttu-id="a3273-155">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3273-155">Input</span></span> | <span data-ttu-id="a3273-156">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a3273-156">1 to 8</span></span> | <span data-ttu-id="a3273-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a3273-157">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="a3273-158">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="a3273-158">IndicesTensor</span></span> | <span data-ttu-id="a3273-159">Entrada</span><span class="sxs-lookup"><span data-stu-id="a3273-159">Input</span></span> | <span data-ttu-id="a3273-160">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a3273-160">1 to 8</span></span> | <span data-ttu-id="a3273-161">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="a3273-161">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="a3273-162">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="a3273-162">OutputTensor</span></span> | <span data-ttu-id="a3273-163">Output</span><span class="sxs-lookup"><span data-stu-id="a3273-163">Output</span></span> | <span data-ttu-id="a3273-164">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="a3273-164">1 to 8</span></span> | <span data-ttu-id="a3273-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="a3273-165">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

## <a name="requirements"></a><span data-ttu-id="a3273-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a3273-166">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a3273-167">**Header**</span><span class="sxs-lookup"><span data-stu-id="a3273-167">**Header**</span></span> | <span data-ttu-id="a3273-168">directml. h</span><span class="sxs-lookup"><span data-stu-id="a3273-168">directml.h</span></span> |
