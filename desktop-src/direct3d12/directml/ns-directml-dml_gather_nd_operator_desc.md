---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a todos los subbloqueos de la entrada. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802895"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="17507-104">DML_GATHER_ND_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="17507-104">DML_GATHER_ND_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="17507-105">Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a todos los subbloqueos de la entrada.</span><span class="sxs-lookup"><span data-stu-id="17507-105">Gathers elements from the input tensor, using the indices tensor to remap indices to entire subblocks of the input.</span></span> <span data-ttu-id="17507-106">Este operador realiza el pseudocódigo siguiente, donde "..." representa una serie de coordenadas, con el comportamiento exacto dependiente del recuento de dimensiones de entrada e índices.</span><span class="sxs-lookup"><span data-stu-id="17507-106">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior dependent on the input and indices dimension count.</span></span>

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> <span data-ttu-id="17507-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="17507-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="17507-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="17507-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="17507-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17507-109">Syntax</span></span>
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="17507-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="17507-110">Members</span></span>

`InputTensor`

<span data-ttu-id="17507-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="17507-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="17507-112">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="17507-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="17507-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="17507-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="17507-114">Tensor que contiene los índices.</span><span class="sxs-lookup"><span data-stu-id="17507-114">The tensor containing the indices.</span></span> <span data-ttu-id="17507-115">DimensionCount *de* este tensor debe coincidir *con InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="17507-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="17507-116">La última dimensión de *IndicesTensor* es realmente el número de coordenadas por tupla de índice y no puede superar *InputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="17507-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it cannot exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="17507-117">Por ejemplo, un tensor de índices de *tamaños* con ÍndicesDimensionCount = 3 significa una matriz 4x5 de tuplas de dos coordenadas que se indexan en `{1,4,5,2}`  *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="17507-117">For example, an indices tensor of *Sizes* `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="17507-118">A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor.</span><span class="sxs-lookup"><span data-stu-id="17507-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="17507-119">Los índices negativos se interpretan como relativos al final de la dimensión correspondiente.</span><span class="sxs-lookup"><span data-stu-id="17507-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="17507-120">Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="17507-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="17507-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="17507-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="17507-122">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="17507-122">The tensor to write the results to.</span></span> <span data-ttu-id="17507-123">DimensionCount *y* *DataType de* este tensor deben coincidir *con InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="17507-123">The *DimensionCount* and *DataType* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="17507-124">Los *outputTensor.Sizes esperados* son la concatenación de los segmentos iniciales *IndicesTensor.Sizes* y el segmento final *InputTensor.Sizes* para producir:</span><span class="sxs-lookup"><span data-stu-id="17507-124">The expected *OutputTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield:</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

<span data-ttu-id="17507-125">Las dimensiones de salida están alineadas a la derecha, con 1 valor inicial anteponer si es necesario para satisfacer hasta *OutputTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="17507-125">The output dimensions are right-aligned, with leading 1 values prepended if needed to satisfy up to *OutputTensor.DimensionCount*.</span></span>

<span data-ttu-id="17507-126">Aquí tiene un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="17507-126">Here's an example.</span></span>

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

<span data-ttu-id="17507-127">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="17507-127">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="17507-128">Número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las iniciales irrelevantes, que abarcan `[1, *InputTensor.DimensionCount*]` .</span><span class="sxs-lookup"><span data-stu-id="17507-128">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging `[1, *InputTensor.DimensionCount*]`.</span></span> <span data-ttu-id="17507-129">Por ejemplo, *dados InputTensor.Sizes*  =  `{1,1,4,6}` y = `InputDimensionCount` 3, los índices significativos reales son `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="17507-129">For example, given *InputTensor.Sizes* = `{1,1,4,6}` and `InputDimensionCount` = 3, the actual meaningful indices are `{1,4,6}`.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="17507-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="17507-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="17507-131">Número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las iniciales irrelevantes, que van [1, *IndicesTensor.DimensionCount*].</span><span class="sxs-lookup"><span data-stu-id="17507-131">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*].</span></span> <span data-ttu-id="17507-132">Por ejemplo, *dados IndicesTensor.Sizes* e  =  `{1,1,4,6}` *IndicesDimensionCount* = 3, los índices significativos reales son `{1,4,6}` .</span><span class="sxs-lookup"><span data-stu-id="17507-132">For example, given *IndicesTensor.Sizes* = `{1,1,4,6}`, and *IndicesDimensionCount* = 3, the actual meaningful indices are `{1,4,6}`.</span></span>

## <a name="examples"></a><span data-ttu-id="17507-133">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="17507-133">Examples</span></span>

### <a name="example-1-1d-remapping"></a><span data-ttu-id="17507-134">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="17507-134">Example 1.</span></span> <span data-ttu-id="17507-135">Remapping 1D</span><span class="sxs-lookup"><span data-stu-id="17507-135">1D remapping</span></span>

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a><span data-ttu-id="17507-136">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="17507-136">Example 2.</span></span> <span data-ttu-id="17507-137">Remapping 2D</span><span class="sxs-lookup"><span data-stu-id="17507-137">2D remapping</span></span>

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a><span data-ttu-id="17507-138">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17507-138">Remarks</span></span>
<span data-ttu-id="17507-139">Se introdujo una versión más reciente de este operador, `DML_OPERATOR_GATHER_ND1` , en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="17507-139">A newer version of this operator, `DML_OPERATOR_GATHER_ND1`, was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="availability"></a><span data-ttu-id="17507-140">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="17507-140">Availability</span></span>
<span data-ttu-id="17507-141">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="17507-141">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="17507-142">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="17507-142">Tensor constraints</span></span>
* <span data-ttu-id="17507-143">*Los índicesTensor*, *InputTensor* y *OutputTensor* deben tener el mismo *dimensioncount.*</span><span class="sxs-lookup"><span data-stu-id="17507-143">*IndicesTensor*, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="17507-144">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de datos*.</span><span class="sxs-lookup"><span data-stu-id="17507-144">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="17507-145">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="17507-145">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="17507-146">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="17507-146">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="17507-147">Tensor</span><span class="sxs-lookup"><span data-stu-id="17507-147">Tensor</span></span> | <span data-ttu-id="17507-148">Tipo</span><span class="sxs-lookup"><span data-stu-id="17507-148">Kind</span></span> | <span data-ttu-id="17507-149">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="17507-149">Supported dimension counts</span></span> | <span data-ttu-id="17507-150">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="17507-150">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="17507-151">InputTensor</span><span class="sxs-lookup"><span data-stu-id="17507-151">InputTensor</span></span> | <span data-ttu-id="17507-152">Entrada</span><span class="sxs-lookup"><span data-stu-id="17507-152">Input</span></span> | <span data-ttu-id="17507-153">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="17507-153">1 to 8</span></span> | <span data-ttu-id="17507-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="17507-154">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="17507-155">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="17507-155">IndicesTensor</span></span> | <span data-ttu-id="17507-156">Entrada</span><span class="sxs-lookup"><span data-stu-id="17507-156">Input</span></span> | <span data-ttu-id="17507-157">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="17507-157">1 to 8</span></span> | <span data-ttu-id="17507-158">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="17507-158">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="17507-159">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="17507-159">OutputTensor</span></span> | <span data-ttu-id="17507-160">Resultados</span><span class="sxs-lookup"><span data-stu-id="17507-160">Output</span></span> | <span data-ttu-id="17507-161">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="17507-161">1 to 8</span></span> | <span data-ttu-id="17507-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="17507-162">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="17507-163">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="17507-163">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="17507-164">Tensor</span><span class="sxs-lookup"><span data-stu-id="17507-164">Tensor</span></span> | <span data-ttu-id="17507-165">Tipo</span><span class="sxs-lookup"><span data-stu-id="17507-165">Kind</span></span> | <span data-ttu-id="17507-166">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="17507-166">Supported dimension counts</span></span> | <span data-ttu-id="17507-167">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="17507-167">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="17507-168">InputTensor</span><span class="sxs-lookup"><span data-stu-id="17507-168">InputTensor</span></span> | <span data-ttu-id="17507-169">Entrada</span><span class="sxs-lookup"><span data-stu-id="17507-169">Input</span></span> | <span data-ttu-id="17507-170">4</span><span class="sxs-lookup"><span data-stu-id="17507-170">4</span></span> | <span data-ttu-id="17507-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="17507-171">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="17507-172">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="17507-172">IndicesTensor</span></span> | <span data-ttu-id="17507-173">Entrada</span><span class="sxs-lookup"><span data-stu-id="17507-173">Input</span></span> | <span data-ttu-id="17507-174">4</span><span class="sxs-lookup"><span data-stu-id="17507-174">4</span></span> | <span data-ttu-id="17507-175">UINT32</span><span class="sxs-lookup"><span data-stu-id="17507-175">UINT32</span></span> |
| <span data-ttu-id="17507-176">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="17507-176">OutputTensor</span></span> | <span data-ttu-id="17507-177">Resultados</span><span class="sxs-lookup"><span data-stu-id="17507-177">Output</span></span> | <span data-ttu-id="17507-178">4</span><span class="sxs-lookup"><span data-stu-id="17507-178">4</span></span> | <span data-ttu-id="17507-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="17507-179">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="17507-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17507-180">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="17507-181">**Header**</span><span class="sxs-lookup"><span data-stu-id="17507-181">**Header**</span></span> | <span data-ttu-id="17507-182">directml.h</span><span class="sxs-lookup"><span data-stu-id="17507-182">directml.h</span></span> |
