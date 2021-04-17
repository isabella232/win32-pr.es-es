---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Selecciona los *K* elementos más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente.
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
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721267"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a><span data-ttu-id="7bab2-103">DML_TOP_K1_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="7bab2-103">DML_TOP_K1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="7bab2-104">Selecciona los *K* elementos más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="7bab2-104">Selects the largest or smallest *K* elements from each sequence along an axis of the *InputTensor*, and returns the values and indices of those elements in the *OutputValueTensor* and *OutputIndexTensor*, respectively.</span></span> <span data-ttu-id="7bab2-105">Una *secuencia* hace referencia a uno de los conjuntos de elementos que existen a lo largo de la dimensión de *eje* de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-105">A *sequence* refers to one of the sets of elements that exist along the *Axis* dimension of the *InputTensor*.</span></span>

<span data-ttu-id="7bab2-106">La elección de si se seleccionan los K elementos mayores o los K más pequeños se pueden controlar mediante *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-106">The choice of whether to select the largest K elements or the smallest K elements can be controlled using *AxisDirection*.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7bab2-107">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="7bab2-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="7bab2-108">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="7bab2-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bab2-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bab2-109">Syntax</span></span>
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



## <a name="members"></a><span data-ttu-id="7bab2-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7bab2-110">Members</span></span>

`InputTensor`

<span data-ttu-id="7bab2-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7bab2-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7bab2-112">Tensores de entrada que contiene los elementos que se van a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="7bab2-112">The input tensor containing elements to select.</span></span>


`OutputValueTensor`

<span data-ttu-id="7bab2-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7bab2-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7bab2-114">Tensores de salida en la que se van a escribir los valores de los *K* elementos superiores.</span><span class="sxs-lookup"><span data-stu-id="7bab2-114">The output tensor to write the values of the top *K* elements to.</span></span> <span data-ttu-id="7bab2-115">Los *K* elementos superiores se seleccionan en función de si son el más grande o el más pequeño, en función del valor de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-115">The top *K* elements are selected based on whether they are the largest or the smallest, depending on the value of *AxisDirection*.</span></span> <span data-ttu-id="7bab2-116">Este tensores debe tener tamaños iguales a *InputTensor*, *salvo* la dimensión especificada por el parámetro de *eje* , que debe tener un tamaño igual a *K*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-116">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="7bab2-117">Se garantiza que los valores *K* seleccionados de cada secuencia de entrada están ordenados en orden descendente (de mayor a menor) si *AxisDirection* es [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span><span class="sxs-lookup"><span data-stu-id="7bab2-117">The *K* values selected from each input sequence are guaranteed to be sorted descending (largest to smallest) if *AxisDirection* is [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md).</span></span> <span data-ttu-id="7bab2-118">De lo contrario, el contrario es true y se garantiza que los valores seleccionados están ordenados de forma ascendente (de menor a mayor).</span><span class="sxs-lookup"><span data-stu-id="7bab2-118">Otherwise, the opposite is true and the values selected are guaranteed to be sorted ascending (smallest to largest).</span></span>


`OutputIndexTensor`

<span data-ttu-id="7bab2-119">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="7bab2-119">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="7bab2-120">La salida tensores para escribir los índices de los *K* elementos superiores en.</span><span class="sxs-lookup"><span data-stu-id="7bab2-120">The output tensor to write the indices of the top *K* elements to.</span></span> <span data-ttu-id="7bab2-121">Este tensores debe tener tamaños iguales a *InputTensor*, *salvo* la dimensión especificada por el parámetro de *eje* , que debe tener un tamaño igual a *K*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-121">This tensor must have sizes equal to the *InputTensor*, *except* for the dimension specified by the *Axis* parameter, which must have a size equal to *K*.</span></span>

<span data-ttu-id="7bab2-122">Los índices devueltos en este tensores se miden en relación con el principio de su secuencia (en oposición al principio del tensores).</span><span class="sxs-lookup"><span data-stu-id="7bab2-122">The indices returned in this tensor are measured relative to the beginning of their sequence (as opposed to the beginning of the tensor).</span></span> <span data-ttu-id="7bab2-123">Por ejemplo, un índice de 0 siempre hace referencia al primer elemento de todas las secuencias de un eje.</span><span class="sxs-lookup"><span data-stu-id="7bab2-123">For example, an index of 0 always refers to the first element for all sequences in an axis.</span></span>

<span data-ttu-id="7bab2-124">En los casos en que dos o más elementos de la parte superior-K tienen el mismo valor (es decir, cuando hay una empate), se incluyen los índices de ambos elementos y se garantiza que se ordenen por índice de elemento ascendente.</span><span class="sxs-lookup"><span data-stu-id="7bab2-124">In cases where two or more elements in the top-K have the same value (that is, when there is a tie), the indices of both elements are included, and are guaranteed to be ordered by ascending element index.</span></span> <span data-ttu-id="7bab2-125">Tenga en cuenta que esto es así independientemente del valor de *AxisDirection*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-125">Note that this is true irrespective of the value of *AxisDirection*.</span></span>


`Axis`

<span data-ttu-id="7bab2-126">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7bab2-126">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7bab2-127">Índice de la dimensión de la que se van a seleccionar elementos.</span><span class="sxs-lookup"><span data-stu-id="7bab2-127">The index of the dimension to select elements across.</span></span> <span data-ttu-id="7bab2-128">Este valor debe ser menor que el valor de *DimensionCount* de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-128">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>


`K`

<span data-ttu-id="7bab2-129">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="7bab2-129">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="7bab2-130">Número de elementos que se van a seleccionar.</span><span class="sxs-lookup"><span data-stu-id="7bab2-130">The number of elements to select.</span></span> <span data-ttu-id="7bab2-131">*K* debe ser mayor que 0, pero menor que el número de elementos de *InputTensor* a lo largo de la dimensión especificada por *AXIS*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-131">*K* must be greater than 0, but less than the number of elements in the *InputTensor* along the dimension specified by *Axis*.</span></span>


`AxisDirection`

<span data-ttu-id="7bab2-132">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="7bab2-132">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="7bab2-133">Un valor de la enumeración [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) .</span><span class="sxs-lookup"><span data-stu-id="7bab2-133">A value from the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="7bab2-134">Si se establece en **DML_AXIS_DIRECTION_INCREASING**, este operador devuelve los *K* elementos *más pequeños* en orden de valor creciente.</span><span class="sxs-lookup"><span data-stu-id="7bab2-134">If set to **DML_AXIS_DIRECTION_INCREASING**, then this operator returns the *smallest* *K* elements in order of increasing value.</span></span> <span data-ttu-id="7bab2-135">De lo contrario, devuelve los *K* elementos *mayores* en orden decreciente.</span><span class="sxs-lookup"><span data-stu-id="7bab2-135">Otherwise, it returns the *largest* *K* elements in decreasing order.</span></span>

## <a name="examples"></a><span data-ttu-id="7bab2-136">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="7bab2-136">Examples</span></span>

### <a name="example-1"></a><span data-ttu-id="7bab2-137">Ejemplo 1</span><span class="sxs-lookup"><span data-stu-id="7bab2-137">Example 1</span></span>

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

### <a name="example-2-using-a-different-axis"></a><span data-ttu-id="7bab2-138">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="7bab2-138">Example 2.</span></span> <span data-ttu-id="7bab2-139">Usar un eje diferente</span><span class="sxs-lookup"><span data-stu-id="7bab2-139">Using a different axis</span></span>

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

### <a name="example-3-tied-values"></a><span data-ttu-id="7bab2-140">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="7bab2-140">Example 3.</span></span> <span data-ttu-id="7bab2-141">Valores enlazados</span><span class="sxs-lookup"><span data-stu-id="7bab2-141">Tied values</span></span>

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

### <a name="example-4-increasing-axis-direction"></a><span data-ttu-id="7bab2-142">Ejemplo 4:</span><span class="sxs-lookup"><span data-stu-id="7bab2-142">Example 4.</span></span> <span data-ttu-id="7bab2-143">Aumentar la dirección del eje</span><span class="sxs-lookup"><span data-stu-id="7bab2-143">Increasing axis direction</span></span>

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


## <a name="remarks"></a><span data-ttu-id="7bab2-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7bab2-144">Remarks</span></span>
<span data-ttu-id="7bab2-145">Cuando *AxisDirection* se establece en [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), este operador es equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="7bab2-145">When *AxisDirection* is set to [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), this operator is equivalent to [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="7bab2-146">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="7bab2-146">Availability</span></span>
<span data-ttu-id="7bab2-147">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="7bab2-147">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="7bab2-148">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="7bab2-148">Tensor constraints</span></span>
* <span data-ttu-id="7bab2-149">*InputTensor* y *OutputValueTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-149">*InputTensor* and *OutputValueTensor* must have the same *DataType*.</span></span>
* <span data-ttu-id="7bab2-150">*OutputIndexTensor* y *OutputValueTensor* deben tener el mismo *tamaño*.</span><span class="sxs-lookup"><span data-stu-id="7bab2-150">*OutputIndexTensor* and *OutputValueTensor* must have the same *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="7bab2-151">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="7bab2-151">Tensor support</span></span>
| <span data-ttu-id="7bab2-152">Tensores</span><span class="sxs-lookup"><span data-stu-id="7bab2-152">Tensor</span></span> | <span data-ttu-id="7bab2-153">Clase</span><span class="sxs-lookup"><span data-stu-id="7bab2-153">Kind</span></span> | <span data-ttu-id="7bab2-154">Dimensions</span><span class="sxs-lookup"><span data-stu-id="7bab2-154">Dimensions</span></span> | <span data-ttu-id="7bab2-155">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="7bab2-155">Supported dimension counts</span></span> | <span data-ttu-id="7bab2-156">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="7bab2-156">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="7bab2-157">InputTensor</span><span class="sxs-lookup"><span data-stu-id="7bab2-157">InputTensor</span></span> | <span data-ttu-id="7bab2-158">Entrada</span><span class="sxs-lookup"><span data-stu-id="7bab2-158">Input</span></span> | <span data-ttu-id="7bab2-159">{ In0, In1, In2, In3 }</span><span class="sxs-lookup"><span data-stu-id="7bab2-159">{ In0, In1, In2, In3 }</span></span> | <span data-ttu-id="7bab2-160">4</span><span class="sxs-lookup"><span data-stu-id="7bab2-160">4</span></span> | <span data-ttu-id="7bab2-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="7bab2-161">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="7bab2-162">OutputValueTensor</span><span class="sxs-lookup"><span data-stu-id="7bab2-162">OutputValueTensor</span></span> | <span data-ttu-id="7bab2-163">Output</span><span class="sxs-lookup"><span data-stu-id="7bab2-163">Output</span></span> | <span data-ttu-id="7bab2-164">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="7bab2-164">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="7bab2-165">4</span><span class="sxs-lookup"><span data-stu-id="7bab2-165">4</span></span> | <span data-ttu-id="7bab2-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="7bab2-166">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="7bab2-167">OutputIndexTensor</span><span class="sxs-lookup"><span data-stu-id="7bab2-167">OutputIndexTensor</span></span> | <span data-ttu-id="7bab2-168">Output</span><span class="sxs-lookup"><span data-stu-id="7bab2-168">Output</span></span> | <span data-ttu-id="7bab2-169">{ Out0, Out1, Out2, Out3 }</span><span class="sxs-lookup"><span data-stu-id="7bab2-169">{ Out0, Out1, Out2, Out3 }</span></span> | <span data-ttu-id="7bab2-170">4</span><span class="sxs-lookup"><span data-stu-id="7bab2-170">4</span></span> | <span data-ttu-id="7bab2-171">UINT32</span><span class="sxs-lookup"><span data-stu-id="7bab2-171">UINT32</span></span> |


## <a name="requirements"></a><span data-ttu-id="7bab2-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bab2-172">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7bab2-173">**Header**</span><span class="sxs-lookup"><span data-stu-id="7bab2-173">**Header**</span></span> | <span data-ttu-id="7bab2-174">directml. h</span><span class="sxs-lookup"><span data-stu-id="7bab2-174">directml.h</span></span> |