---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Selecciona los elementos *K* más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
f1_keywords:
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417985"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="2290c-103">DML_TOP_K1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="2290c-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="2290c-104">Selecciona los elementos *K* más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="2290c-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="2290c-105">Una *secuencia* hace referencia a uno de los conjuntos de elementos que existen a lo largo de la dimensión *Eje* de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="2290c-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="2290c-106">La elección de si se seleccionan los elementos K más grandes o los elementos K más pequeños se pueden controlar mediante *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="2290c-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2290c-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="2290c-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="2290c-108">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="2290c-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2290c-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2290c-109">Syntax</span></span>
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="2290c-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="2290c-110">Members</span></span>

`InputTensor`

<span data-ttu-id="2290c-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2290c-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2290c-112">Tensor de entrada que contiene los elementos que se deben seleccionar.</span><span class="sxs-lookup"><span data-stu-id="2290c-112">The input tensor containing elements to select.</span></span>

`OutputValueTensor`

<span data-ttu-id="2290c-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2290c-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2290c-114">Tensor de salida en el que se escriben los valores de los *elementos K* principales.</span><span class="sxs-lookup"><span data-stu-id="2290c-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="2290c-115">Los elementos *K* principales se seleccionan en función de si son los más grandes o más pequeños, dependiendo del valor *de AxisDirection.*</span><span class="sxs-lookup"><span data-stu-id="2290c-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="2290c-116">Este tensor debe tener tamaños iguales a *InputTensor* *,* excepto para la dimensión especificada por el parámetro *Axis,* que debe tener un tamaño igual a *K*.</span><span class="sxs-lookup"><span data-stu-id="2290c-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="2290c-117">Se *garantiza que* los valores K seleccionados de cada secuencia de entrada se ordenan de manera descendente (de mayor a [menor)](./ne-directml-dml_axis_direction.md)si *AxisDirection* DML_AXIS_DIRECTION_DECREASING .</span><span class="sxs-lookup"><span data-stu-id="2290c-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="2290c-118">De lo contrario, lo contrario es true y se garantiza que los valores seleccionados se ordenan de forma ascendente (menor a mayor).</span><span class="sxs-lookup"><span data-stu-id="2290c-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>

`OutputIndexTensor`

<span data-ttu-id="2290c-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="2290c-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="2290c-120">Tensor de salida en el que se escriben los índices de los *elementos K* superiores.</span><span class="sxs-lookup"><span data-stu-id="2290c-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="2290c-121">Este tensor debe tener tamaños iguales a *InputTensor* *,* excepto para la dimensión especificada por el parámetro *Axis,* que debe tener un tamaño igual a *K*.</span><span class="sxs-lookup"><span data-stu-id="2290c-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="2290c-122">Los índices devueltos en este tensor se miden con respecto al principio de su secuencia (en lugar del principio del tensor).</span><span class="sxs-lookup"><span data-stu-id="2290c-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="2290c-123">Por ejemplo, un índice de 0 siempre hace referencia al primer elemento de todas las secuencias de un eje.</span><span class="sxs-lookup"><span data-stu-id="2290c-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="2290c-124">En los casos en los que dos o más elementos de la K superior tienen el mismo valor (es decir, cuando hay una vinculación), se incluyen los índices de ambos elementos y se garantiza que se ordenan por índice de elemento ascendente.</span><span class="sxs-lookup"><span data-stu-id="2290c-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="2290c-125">Tenga en cuenta que esto es cierto independientemente del valor de *AxisDirection.*</span><span class="sxs-lookup"><span data-stu-id="2290c-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>

`Axis`

<span data-ttu-id="2290c-126">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2290c-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2290c-127">Índice de la dimensión en la que se seleccionan los elementos.</span><span class="sxs-lookup"><span data-stu-id="2290c-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="2290c-128">Este valor debe ser menor que *dimensionCount* de *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="2290c-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`K`

<span data-ttu-id="2290c-129">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="2290c-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="2290c-130">Número de elementos que se seleccionarán.</span><span class="sxs-lookup"><span data-stu-id="2290c-130">The number of elements to select.</span></span> <span data-ttu-id="2290c-131">*K* debe ser mayor que 0, pero menor que el número de elementos de *InputTensor* a lo largo de la dimensión especificada por *Eje*.</span><span class="sxs-lookup"><span data-stu-id="2290c-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>

`AxisDirection`

<span data-ttu-id="2290c-132">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="2290c-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="2290c-133">Valor de la [enumeración DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) datos.</span><span class="sxs-lookup"><span data-stu-id="2290c-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="2290c-134">Si se establece **en DML_AXIS_DIRECTION_INCREASING**, este operador devuelve *los* *elementos K* más pequeños en orden de aumento del valor.</span><span class="sxs-lookup"><span data-stu-id="2290c-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="2290c-135">De lo contrario, devuelve *los elementos* *K más grandes* en orden decreciente.</span><span class="sxs-lookup"><span data-stu-id="2290c-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="2290c-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="2290c-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="2290c-137">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="2290c-137">Example 1</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="2290c-138">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="2290c-138">Example 2.</span></span> <span data-ttu-id="2290c-139">Uso de un eje diferente</span><span class="sxs-lookup"><span data-stu-id="2290c-139">Using a different axis</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a><span data-ttu-id="2290c-140">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="2290c-140">Example 3.</span></span> <span data-ttu-id="2290c-141">Valores vinculados</span><span class="sxs-lookup"><span data-stu-id="2290c-141">Tied values</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="2290c-142">Ejemplo 4.</span><span class="sxs-lookup"><span data-stu-id="2290c-142">Example 4.</span></span> <span data-ttu-id="2290c-143">Aumentar la dirección del eje</span><span class="sxs-lookup"><span data-stu-id="2290c-143">Increasing axis direction</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a><span data-ttu-id="2290c-144">Comentarios</span><span class="sxs-lookup"><span data-stu-id="2290c-144">Remarks</span></span>
<span data-ttu-id="2290c-145">Cuando *AxisDirection* se establece [en DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), este operador es equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="2290c-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="2290c-146">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="2290c-146">Availability</span></span>
<span data-ttu-id="2290c-147">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="2290c-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="2290c-148">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="2290c-148">Tensor constraints</span></span>

* <span data-ttu-id="2290c-149">*InputTensor,* *OutputIndexTensor y* *OutputValueTensor* deben tener el mismo *dimensioncount*.</span><span class="sxs-lookup"><span data-stu-id="2290c-149">*InputTensor*, *OutputIndexTensor*, and *OutputValueTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="2290c-150">*InputTensor* y *OutputValueTensor* deben tener el mismo *datatype*.</span><span class="sxs-lookup"><span data-stu-id="2290c-150">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="2290c-151">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="2290c-151">Tensor support</span></span>

### <a name="dml_feature_level_3_1-and-above"></a><span data-ttu-id="2290c-152">DML_FEATURE_LEVEL_3_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="2290c-152">DML_FEATURE_LEVEL_3_1 and above</span></span>

| <span data-ttu-id="2290c-153">Tensor</span><span class="sxs-lookup"><span data-stu-id="2290c-153">Tensor</span></span> | <span data-ttu-id="2290c-154">Tipo</span><span class="sxs-lookup"><span data-stu-id="2290c-154">Kind</span></span> | <span data-ttu-id="2290c-155">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="2290c-155">Supported dimension counts</span></span> | <span data-ttu-id="2290c-156">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="2290c-156">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2290c-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2290c-157">InputTensor</span></span> | <span data-ttu-id="2290c-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="2290c-158">Input</span></span> | <span data-ttu-id="2290c-159">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2290c-159">1 to 8</span></span> | <span data-ttu-id="2290c-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2290c-160">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2290c-161">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="2290c-161">OutputValueTensor</span></span> | <span data-ttu-id="2290c-162">Resultados</span><span class="sxs-lookup"><span data-stu-id="2290c-162">Output</span></span> | <span data-ttu-id="2290c-163">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2290c-163">1 to 8</span></span> | <span data-ttu-id="2290c-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2290c-164">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2290c-165">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="2290c-165">OutputIndexTensor</span></span> | <span data-ttu-id="2290c-166">Resultados</span><span class="sxs-lookup"><span data-stu-id="2290c-166">Output</span></span> | <span data-ttu-id="2290c-167">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="2290c-167">1 to 8</span></span> | <span data-ttu-id="2290c-168">UINT32</span><span class="sxs-lookup"><span data-stu-id="2290c-168">UINT32</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="2290c-169">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="2290c-169">DML_FEATURE_LEVEL_2_1 and above</span></span>

| <span data-ttu-id="2290c-170">Tensor</span><span class="sxs-lookup"><span data-stu-id="2290c-170">Tensor</span></span> | <span data-ttu-id="2290c-171">Tipo</span><span class="sxs-lookup"><span data-stu-id="2290c-171">Kind</span></span> | <span data-ttu-id="2290c-172">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="2290c-172">Supported dimension counts</span></span> | <span data-ttu-id="2290c-173">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="2290c-173">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="2290c-174">InputTensor</span><span class="sxs-lookup"><span data-stu-id="2290c-174">InputTensor</span></span> | <span data-ttu-id="2290c-175">Entrada</span><span class="sxs-lookup"><span data-stu-id="2290c-175">Input</span></span> | <span data-ttu-id="2290c-176">4</span><span class="sxs-lookup"><span data-stu-id="2290c-176">4</span></span> | <span data-ttu-id="2290c-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2290c-177">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2290c-178">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="2290c-178">OutputValueTensor</span></span> | <span data-ttu-id="2290c-179">Resultados</span><span class="sxs-lookup"><span data-stu-id="2290c-179">Output</span></span> | <span data-ttu-id="2290c-180">4</span><span class="sxs-lookup"><span data-stu-id="2290c-180">4</span></span> | <span data-ttu-id="2290c-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="2290c-181">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="2290c-182">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="2290c-182">OutputIndexTensor</span></span> | <span data-ttu-id="2290c-183">Resultados</span><span class="sxs-lookup"><span data-stu-id="2290c-183">Output</span></span> | <span data-ttu-id="2290c-184">4</span><span class="sxs-lookup"><span data-stu-id="2290c-184">4</span></span> | <span data-ttu-id="2290c-185">UINT32</span><span class="sxs-lookup"><span data-stu-id="2290c-185">UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="2290c-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2290c-186">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="2290c-187">**Header**</span><span class="sxs-lookup"><span data-stu-id="2290c-187">**Header**</span></span> | <span data-ttu-id="2290c-188">directml.h</span><span class="sxs-lookup"><span data-stu-id="2290c-188">directml.h</span></span> |
