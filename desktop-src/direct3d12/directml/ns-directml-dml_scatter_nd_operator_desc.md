---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia todo el tensores de entrada en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes de la tensores de actualizaciones.
ms.topic: reference
tech.root: directml
ms.date: 11/04/2020
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721297"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="b95b4-103">DML_SCATTER_ND_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="b95b4-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="b95b4-104">Copia todo el tensores de entrada en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes de la tensores de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="b95b4-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="b95b4-105">Este operador realiza el siguiente pseudocódigo, donde "..." representa una serie de coordenadas, con el comportamiento exacto determinado por el tamaño del eje y de los índices.</span><span class="sxs-lookup"><span data-stu-id="b95b4-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="b95b4-106">Si dos índices de elementos de salida se superponen (que no son válidos), no hay ninguna garantía de la última escritura que gana.</span><span class="sxs-lookup"><span data-stu-id="b95b4-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b95b4-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="b95b4-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="b95b4-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="b95b4-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b95b4-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b95b4-109">Syntax</span></span>
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a><span data-ttu-id="b95b4-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="b95b4-110">Members</span></span>

`InputTensor`

<span data-ttu-id="b95b4-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b95b4-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b95b4-112">Tensores del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="b95b4-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="b95b4-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b95b4-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b95b4-114">Tensores que contiene los índices.</span><span class="sxs-lookup"><span data-stu-id="b95b4-114">A tensor containing the indices.</span></span> <span data-ttu-id="b95b4-115">El *DimensionCount* de este tensores debe coincidir con *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="b95b4-116">La última dimensión de *IndicesTensor* es en realidad el número de coordenadas por tupla de índice y no debe supera *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="b95b4-117">Por ejemplo, un tensores de índices de tamaño `{1,4,5,2}` con *IndicesDimensionCount* = 3 significa una matriz 4x5 de tuplas de coordenadas de dos valores que indexan en *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="b95b4-118">A partir de `DML_FEATURE_LEVEL_3_0` , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensores.</span><span class="sxs-lookup"><span data-stu-id="b95b4-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="b95b4-119">Los índices negativos se interpretan como en relación con el final de la dimensión respectiva.</span><span class="sxs-lookup"><span data-stu-id="b95b4-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="b95b4-120">Por ejemplo, un índice de-1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="b95b4-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="b95b4-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b95b4-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b95b4-122">Tensores que contiene los nuevos valores para reemplazar los valores de entrada existentes en los índices correspondientes.</span><span class="sxs-lookup"><span data-stu-id="b95b4-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="b95b4-123">El *DimensionCount* de este tensores debe coincidir con *InputTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="b95b4-124">El *UpdatesTensor esperado. los tamaños* son la concatenación de los segmentos iniciales *IndicesTensor. Sizes* y *InputTensor. Sizes* final para producir lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="b95b4-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="b95b4-125">Las dimensiones están alineadas a la derecha, con un valor inicial de 1 delante, si es necesario, para satisfacer *UpdatesTensor. DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="b95b4-126">Aquí tiene un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="b95b4-126">Here's an example.</span></span>

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

<span data-ttu-id="b95b4-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="b95b4-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="b95b4-128">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="b95b4-128">The tensor to write the results to.</span></span> <span data-ttu-id="b95b4-129">Los *tamaños* y el *tipo* de los tipos de tensores deben coincidir con *InputTensor. Sizes*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="b95b4-130">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b95b4-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b95b4-131">El número de dimensiones de entrada reales dentro de *InputTensor* después de omitir cualquier otro que sea irrelevante, que oscila entre [1, *InputTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="b95b4-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="b95b4-132">Por ejemplo, dado *InputTensor. Sizes* = {1,1,4,6} y *InputDimensionCount* = 3, los índices significativos reales son {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="b95b4-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="b95b4-133">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="b95b4-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="b95b4-134">El número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir cualquier otro que sea irrelevante, que oscila entre [1, *IndicesTensor. DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="b95b4-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="b95b4-135">Por ejemplo, dado *IndicesTensor. Sizes* = {1,1,4,6} y *IndicesDimensionCount* = 3, los índices significativos reales son {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="b95b4-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="b95b4-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="b95b4-136">Examples</span></span>

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a><span data-ttu-id="b95b4-137">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="b95b4-137">Availability</span></span>
<span data-ttu-id="b95b4-138">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="b95b4-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="b95b4-139">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="b95b4-139">Tensor constraints</span></span>
* <span data-ttu-id="b95b4-140">*IndicesTensor*, *InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="b95b4-141">*InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="b95b4-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="b95b4-142">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="b95b4-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="b95b4-143">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b95b4-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="b95b4-144">Tensores</span><span class="sxs-lookup"><span data-stu-id="b95b4-144">Tensor</span></span> | <span data-ttu-id="b95b4-145">Clase</span><span class="sxs-lookup"><span data-stu-id="b95b4-145">Kind</span></span> | <span data-ttu-id="b95b4-146">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="b95b4-146">Supported dimension counts</span></span> | <span data-ttu-id="b95b4-147">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="b95b4-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b95b4-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-148">InputTensor</span></span> | <span data-ttu-id="b95b4-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="b95b4-149">Input</span></span> | <span data-ttu-id="b95b4-150">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b95b4-150">1 to 8</span></span> | <span data-ttu-id="b95b4-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b95b4-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b95b4-152">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-152">IndicesTensor</span></span> | <span data-ttu-id="b95b4-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="b95b4-153">Input</span></span> | <span data-ttu-id="b95b4-154">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b95b4-154">1 to 8</span></span> | <span data-ttu-id="b95b4-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="b95b4-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="b95b4-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-156">UpdatesTensor</span></span> | <span data-ttu-id="b95b4-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="b95b4-157">Input</span></span> | <span data-ttu-id="b95b4-158">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b95b4-158">1 to 8</span></span> | <span data-ttu-id="b95b4-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b95b4-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b95b4-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-160">OutputTensor</span></span> | <span data-ttu-id="b95b4-161">Output</span><span class="sxs-lookup"><span data-stu-id="b95b4-161">Output</span></span> | <span data-ttu-id="b95b4-162">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="b95b4-162">1 to 8</span></span> | <span data-ttu-id="b95b4-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b95b4-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="b95b4-164">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b95b4-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="b95b4-165">Tensores</span><span class="sxs-lookup"><span data-stu-id="b95b4-165">Tensor</span></span> | <span data-ttu-id="b95b4-166">Clase</span><span class="sxs-lookup"><span data-stu-id="b95b4-166">Kind</span></span> | <span data-ttu-id="b95b4-167">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="b95b4-167">Supported dimension counts</span></span> | <span data-ttu-id="b95b4-168">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="b95b4-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="b95b4-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-169">InputTensor</span></span> | <span data-ttu-id="b95b4-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="b95b4-170">Input</span></span> | <span data-ttu-id="b95b4-171">4</span><span class="sxs-lookup"><span data-stu-id="b95b4-171">4</span></span> | <span data-ttu-id="b95b4-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b95b4-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b95b4-173">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-173">IndicesTensor</span></span> | <span data-ttu-id="b95b4-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="b95b4-174">Input</span></span> | <span data-ttu-id="b95b4-175">4</span><span class="sxs-lookup"><span data-stu-id="b95b4-175">4</span></span> | <span data-ttu-id="b95b4-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="b95b4-176">UINT32</span></span> |
| <span data-ttu-id="b95b4-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-177">UpdatesTensor</span></span> | <span data-ttu-id="b95b4-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="b95b4-178">Input</span></span> | <span data-ttu-id="b95b4-179">4</span><span class="sxs-lookup"><span data-stu-id="b95b4-179">4</span></span> | <span data-ttu-id="b95b4-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b95b4-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="b95b4-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="b95b4-181">OutputTensor</span></span> | <span data-ttu-id="b95b4-182">Output</span><span class="sxs-lookup"><span data-stu-id="b95b4-182">Output</span></span> | <span data-ttu-id="b95b4-183">4</span><span class="sxs-lookup"><span data-stu-id="b95b4-183">4</span></span> | <span data-ttu-id="b95b4-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="b95b4-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="b95b4-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b95b4-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="b95b4-186">**Header**</span><span class="sxs-lookup"><span data-stu-id="b95b4-186">**Header**</span></span> | <span data-ttu-id="b95b4-187">directml. h</span><span class="sxs-lookup"><span data-stu-id="b95b4-187">directml.h</span></span> |