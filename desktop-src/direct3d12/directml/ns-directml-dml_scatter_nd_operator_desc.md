---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia el tensor de entrada completo en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes del tensor de actualizaciones.
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
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803983"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a><span data-ttu-id="d59c7-103">DML_SCATTER_ND_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d59c7-103">DML_SCATTER_ND_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="d59c7-104">Copia el tensor de entrada completo en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes del tensor de actualizaciones.</span><span class="sxs-lookup"><span data-stu-id="d59c7-104">Copies the whole input tensor to the output, then overwrites selected indices with corresponding values from the updates tensor.</span></span> <span data-ttu-id="d59c7-105">Este operador realiza el pseudocódigo siguiente, donde "..." representa una serie de coordenadas, con el comportamiento exacto determinado por el tamaño del eje y los índices.</span><span class="sxs-lookup"><span data-stu-id="d59c7-105">This operator performs the following pseudocode, where "..." represents a series of coordinates, with the exact behavior determined by the axis and indices size.</span></span>

```
output = input
output[indices[...]] = updates[...]
```

<span data-ttu-id="d59c7-106">Si dos índices de elementos de salida se superponen (lo que no es válido), no hay ninguna garantía de cuál gana la última escritura.</span><span class="sxs-lookup"><span data-stu-id="d59c7-106">If two output element indices overlap (which is invalid), there is no guarantee of which last write wins.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d59c7-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="d59c7-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d59c7-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d59c7-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d59c7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d59c7-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="d59c7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d59c7-110">Members</span></span>

`InputTensor`

<span data-ttu-id="d59c7-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d59c7-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d59c7-112">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="d59c7-112">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="d59c7-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d59c7-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d59c7-114">Tensor que contiene los índices.</span><span class="sxs-lookup"><span data-stu-id="d59c7-114">A tensor containing the indices.</span></span> <span data-ttu-id="d59c7-115">DimensionCount *de* este tensor debe coincidir *con InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="d59c7-115">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d59c7-116">La última dimensión de *IndicesTensor* es realmente el número de coordenadas por tupla de índice y no debe superar *InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="d59c7-116">The last dimension of the *IndicesTensor* is actually the number of coordinates per index tuple, and it mustn't exceed *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d59c7-117">Por ejemplo, un tensor de índices de tamaño `{1,4,5,2}` *con IndicesDimensionCount* = 3 significa una matriz 4x5 de tuplas de coordenadas de 2 valores que se indexan en *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="d59c7-117">For example, an indices tensor of size `{1,4,5,2}` with *IndicesDimensionCount* = 3 means a 4x5 array of 2-value coordinate tuples that index into *InputTensor*.</span></span>

<span data-ttu-id="d59c7-118">A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor.</span><span class="sxs-lookup"><span data-stu-id="d59c7-118">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="d59c7-119">Los índices negativos se interpretan como relativos al final de la dimensión respectiva.</span><span class="sxs-lookup"><span data-stu-id="d59c7-119">Negative indices are interpreted as being relative to the end of the respective dimension.</span></span> <span data-ttu-id="d59c7-120">Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="d59c7-120">For example, an index of -1 refers to the last element along that dimension.</span></span>


`UpdatesTensor`

<span data-ttu-id="d59c7-121">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d59c7-121">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d59c7-122">Tensor que contiene los nuevos valores para reemplazar los valores de entrada existentes en los índices correspondientes.</span><span class="sxs-lookup"><span data-stu-id="d59c7-122">A tensor containing the new values to replace the existing input values at the corresponding indices.</span></span> <span data-ttu-id="d59c7-123">DimensionCount *de* este tensor debe coincidir *con InputTensor.DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="d59c7-123">The *DimensionCount* of this tensor must match *InputTensor.DimensionCount*.</span></span> <span data-ttu-id="d59c7-124">Los valores *esperados de UpdatesTensor.Sizes* son la concatenación de los segmentos iniciales *IndicesTensor.Sizes* y *inputTensor.Sizes* para producir lo siguiente.</span><span class="sxs-lookup"><span data-stu-id="d59c7-124">The expected *UpdatesTensor.Sizes* are the concatenation of the *IndicesTensor.Sizes* leading segments and *InputTensor.Sizes* trailing segment to yield the following.</span></span>

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

<span data-ttu-id="d59c7-125">Las dimensiones están alineadas a la derecha, con 1 valor inicial anteponer si es necesario para satisfacer *UpdatesTensor.DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="d59c7-125">The dimensions are right-aligned, with leading 1 values prepended if needed to satisfy *UpdatesTensor.DimensionCount*.</span></span>

<span data-ttu-id="d59c7-126">Aquí tiene un ejemplo.</span><span class="sxs-lookup"><span data-stu-id="d59c7-126">Here's an example.</span></span>

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

<span data-ttu-id="d59c7-127">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d59c7-127">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d59c7-128">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="d59c7-128">The tensor to write the results to.</span></span> <span data-ttu-id="d59c7-129">Los *tamaños* y *datatype* de este tensor deben coincidir *con InputTensor.Sizes.*</span><span class="sxs-lookup"><span data-stu-id="d59c7-129">The *Sizes* and *DataType* of this tensor must match *InputTensor.Sizes*.</span></span>


`InputDimensionCount`

<span data-ttu-id="d59c7-130">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d59c7-130">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d59c7-131">Número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las iniciales irrelevantes, que abarcan [1, *InputTensor.DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="d59c7-131">The number of actual input dimensions within the *InputTensor* after ignoring any irrelevant leading ones, ranging [1, *InputTensor.DimensionCount*).</span></span> <span data-ttu-id="d59c7-132">Por ejemplo, *dados InputTensor.Sizes* = {1,1,4,6} y *InputDimensionCount* = 3, los índices significativos reales son {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="d59c7-132">For example, given *InputTensor.Sizes* = {1,1,4,6} and *InputDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>


`IndicesDimensionCount`

<span data-ttu-id="d59c7-133">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d59c7-133">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d59c7-134">Número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las iniciales irrelevantes, que abarcan [1, *IndicesTensor.DimensionCount*).</span><span class="sxs-lookup"><span data-stu-id="d59c7-134">The number of actual index dimensions within the *IndicesTensor* after ignoring any irrelevant leading ones, ranging [1, *IndicesTensor.DimensionCount*).</span></span> <span data-ttu-id="d59c7-135">Por ejemplo, *dados IndicesTensor.Sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, los índices significativos reales son {1,4,6} .</span><span class="sxs-lookup"><span data-stu-id="d59c7-135">For example, given *IndicesTensor.Sizes* = {1,1,4,6} and *IndicesDimensionCount* = 3, the actual meaningful indices are {1,4,6}.</span></span>

## <a name="examples"></a><span data-ttu-id="d59c7-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d59c7-136">Examples</span></span>

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

## <a name="availability"></a><span data-ttu-id="d59c7-137">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="d59c7-137">Availability</span></span>
<span data-ttu-id="d59c7-138">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d59c7-138">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d59c7-139">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-139">Tensor constraints</span></span>
* <span data-ttu-id="d59c7-140">*IndicesTensor*, *InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="d59c7-140">*IndicesTensor*, *InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="d59c7-141">*InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="d59c7-141">*InputTensor*, *OutputTensor*, and `UpdatesTensor` must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d59c7-142">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-142">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="d59c7-143">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="d59c7-143">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="d59c7-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-144">Tensor</span></span> | <span data-ttu-id="d59c7-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="d59c7-145">Kind</span></span> | <span data-ttu-id="d59c7-146">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="d59c7-146">Supported dimension counts</span></span> | <span data-ttu-id="d59c7-147">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="d59c7-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d59c7-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-148">InputTensor</span></span> | <span data-ttu-id="d59c7-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="d59c7-149">Input</span></span> | <span data-ttu-id="d59c7-150">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d59c7-150">1 to 8</span></span> | <span data-ttu-id="d59c7-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d59c7-151">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d59c7-152">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-152">IndicesTensor</span></span> | <span data-ttu-id="d59c7-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="d59c7-153">Input</span></span> | <span data-ttu-id="d59c7-154">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d59c7-154">1 to 8</span></span> | <span data-ttu-id="d59c7-155">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="d59c7-155">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="d59c7-156">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-156">UpdatesTensor</span></span> | <span data-ttu-id="d59c7-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="d59c7-157">Input</span></span> | <span data-ttu-id="d59c7-158">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d59c7-158">1 to 8</span></span> | <span data-ttu-id="d59c7-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d59c7-159">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d59c7-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-160">OutputTensor</span></span> | <span data-ttu-id="d59c7-161">Resultados</span><span class="sxs-lookup"><span data-stu-id="d59c7-161">Output</span></span> | <span data-ttu-id="d59c7-162">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d59c7-162">1 to 8</span></span> | <span data-ttu-id="d59c7-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d59c7-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="d59c7-164">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="d59c7-164">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="d59c7-165">Tensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-165">Tensor</span></span> | <span data-ttu-id="d59c7-166">Tipo</span><span class="sxs-lookup"><span data-stu-id="d59c7-166">Kind</span></span> | <span data-ttu-id="d59c7-167">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="d59c7-167">Supported dimension counts</span></span> | <span data-ttu-id="d59c7-168">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="d59c7-168">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d59c7-169">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-169">InputTensor</span></span> | <span data-ttu-id="d59c7-170">Entrada</span><span class="sxs-lookup"><span data-stu-id="d59c7-170">Input</span></span> | <span data-ttu-id="d59c7-171">4</span><span class="sxs-lookup"><span data-stu-id="d59c7-171">4</span></span> | <span data-ttu-id="d59c7-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d59c7-172">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d59c7-173">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-173">IndicesTensor</span></span> | <span data-ttu-id="d59c7-174">Entrada</span><span class="sxs-lookup"><span data-stu-id="d59c7-174">Input</span></span> | <span data-ttu-id="d59c7-175">4</span><span class="sxs-lookup"><span data-stu-id="d59c7-175">4</span></span> | <span data-ttu-id="d59c7-176">UINT32</span><span class="sxs-lookup"><span data-stu-id="d59c7-176">UINT32</span></span> |
| <span data-ttu-id="d59c7-177">UpdatesTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-177">UpdatesTensor</span></span> | <span data-ttu-id="d59c7-178">Entrada</span><span class="sxs-lookup"><span data-stu-id="d59c7-178">Input</span></span> | <span data-ttu-id="d59c7-179">4</span><span class="sxs-lookup"><span data-stu-id="d59c7-179">4</span></span> | <span data-ttu-id="d59c7-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d59c7-180">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d59c7-181">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d59c7-181">OutputTensor</span></span> | <span data-ttu-id="d59c7-182">Resultados</span><span class="sxs-lookup"><span data-stu-id="d59c7-182">Output</span></span> | <span data-ttu-id="d59c7-183">4</span><span class="sxs-lookup"><span data-stu-id="d59c7-183">4</span></span> | <span data-ttu-id="d59c7-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d59c7-184">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="d59c7-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d59c7-185">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d59c7-186">**Header**</span><span class="sxs-lookup"><span data-stu-id="d59c7-186">**Header**</span></span> | <span data-ttu-id="d59c7-187">directml.h</span><span class="sxs-lookup"><span data-stu-id="d59c7-187">directml.h</span></span> |