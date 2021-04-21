---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Suma los elementos de un tensor a lo largo de un eje y escribe el recuento en ejecución de la suma en el tensor de salida.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803347"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a><span data-ttu-id="d05da-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d05da-103">DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d05da-104">Suma los elementos de un tensor a lo largo de un eje y escribe el recuento en ejecución de la suma en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="d05da-104">Sums the elements of a tensor along an axis, writing the running tally of the summation into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d05da-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="d05da-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d05da-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d05da-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d05da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d05da-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a><span data-ttu-id="d05da-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d05da-108">Members</span></span>

`InputTensor`

<span data-ttu-id="d05da-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d05da-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d05da-110">Tensor de entrada que contiene los elementos que se deben suman.</span><span class="sxs-lookup"><span data-stu-id="d05da-110">The input tensor containing elements to be summed.</span></span>

`OutputTensor`

<span data-ttu-id="d05da-111">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d05da-111">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d05da-112">Tensor de salida en el que se escriben las sumas acumulativas resultantes.</span><span class="sxs-lookup"><span data-stu-id="d05da-112">The output tensor to write the resulting cumulative summations to.</span></span> <span data-ttu-id="d05da-113">Este tensor debe tener los mismos tamaños y tipo de datos que *InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="d05da-113">This tensor must have the same sizes and data type as the *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="d05da-114">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="d05da-114">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="d05da-115">Índice de la dimensión sobre la que se suman los elementos.</span><span class="sxs-lookup"><span data-stu-id="d05da-115">The index of the dimension to sum elements over.</span></span> <span data-ttu-id="d05da-116">Este valor debe ser menor que *DimensionCount* del *inputTensor*.</span><span class="sxs-lookup"><span data-stu-id="d05da-116">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="d05da-117">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="d05da-117">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="d05da-118">Uno de los valores de la [enumeración DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) datos.</span><span class="sxs-lookup"><span data-stu-id="d05da-118">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="d05da-119">Si se establece **en DML_AXIS_DIRECTION_INCREASING**, la suma se produce recorriendo el tensor a lo largo del eje especificado por índice de elemento ascendente.</span><span class="sxs-lookup"><span data-stu-id="d05da-119">If set to **DML_AXIS_DIRECTION_INCREASING**, then the summation occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="d05da-120">Si se establece **en DML_AXIS_DIRECTION_DECREASING**, el valor inverso es true y la suma se produce recorriendo elementos por índice descendente.</span><span class="sxs-lookup"><span data-stu-id="d05da-120">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true, and the summation occurs by traversing elements by descending index.</span></span>

`HasExclusiveSum`

<span data-ttu-id="d05da-121">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="d05da-121">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="d05da-122">Si **es TRUE**, el valor del elemento actual se excluye al escribir el recuento en ejecución en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="d05da-122">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="d05da-123">Si **es FALSE**, el valor del elemento actual se incluye en el recuento en ejecución.</span><span class="sxs-lookup"><span data-stu-id="d05da-123">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="d05da-124">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d05da-124">Examples</span></span>

<span data-ttu-id="d05da-125">Todos los ejemplos de esta sección usan un tensor de entrada con las siguientes propiedades.</span><span class="sxs-lookup"><span data-stu-id="d05da-125">The examples in this section all use an input tensor with the following properties.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a><span data-ttu-id="d05da-126">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="d05da-126">Example 1.</span></span> <span data-ttu-id="d05da-127">Suma acumulativa en las slivers horizontales</span><span class="sxs-lookup"><span data-stu-id="d05da-127">Cumulative summation across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a><span data-ttu-id="d05da-128">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="d05da-128">Example 2.</span></span> <span data-ttu-id="d05da-129">Sumas exclusivas</span><span class="sxs-lookup"><span data-stu-id="d05da-129">Exclusive sums</span></span>

<span data-ttu-id="d05da-130">Establecer *HasExclusiveSum* en **TRUE** tiene el efecto de excluir el valor del elemento actual del recuento en ejecución al escribir en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="d05da-130">Setting *HasExclusiveSum* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="d05da-131">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="d05da-131">Example 3.</span></span> <span data-ttu-id="d05da-132">Dirección del eje</span><span class="sxs-lookup"><span data-stu-id="d05da-132">Axis direction</span></span>

<span data-ttu-id="d05da-133">Establecer *AxisDirection en* [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) tiene el efecto de invertir el orden transversal de los elementos al calcular el recuento en ejecución.</span><span class="sxs-lookup"><span data-stu-id="d05da-133">Setting the *AxisDirection* to [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a><span data-ttu-id="d05da-134">Ejemplo 4.</span><span class="sxs-lookup"><span data-stu-id="d05da-134">Example 4.</span></span> <span data-ttu-id="d05da-135">Suma a lo largo de un eje diferente</span><span class="sxs-lookup"><span data-stu-id="d05da-135">Summing along a different axis</span></span>

<span data-ttu-id="d05da-136">En este ejemplo, la suma se produce verticalmente, a lo largo del eje de alto (segunda dimensión).</span><span class="sxs-lookup"><span data-stu-id="d05da-136">In this example, the summation occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a><span data-ttu-id="d05da-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d05da-137">Remarks</span></span>
<span data-ttu-id="d05da-138">Este operador admite la ejecución en contexto, lo que significa que *outputTensor* puede crear un alias de *InputTensor durante* el enlace.</span><span class="sxs-lookup"><span data-stu-id="d05da-138">This operator supports in-place execution, meaning that the *OutputTensor* is permitted to alias the *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="d05da-139">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="d05da-139">Availability</span></span>
<span data-ttu-id="d05da-140">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="d05da-140">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d05da-141">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="d05da-141">Tensor constraints</span></span>
<span data-ttu-id="d05da-142">*InputTensor* y *OutputTensor* deben tener los mismos *tipos de datos* y *tamaños.*</span><span class="sxs-lookup"><span data-stu-id="d05da-142">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d05da-143">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="d05da-143">Tensor support</span></span>
| <span data-ttu-id="d05da-144">Tensor</span><span class="sxs-lookup"><span data-stu-id="d05da-144">Tensor</span></span> | <span data-ttu-id="d05da-145">Tipo</span><span class="sxs-lookup"><span data-stu-id="d05da-145">Kind</span></span> | <span data-ttu-id="d05da-146">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="d05da-146">Supported dimension counts</span></span> | <span data-ttu-id="d05da-147">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="d05da-147">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d05da-148">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d05da-148">InputTensor</span></span> | <span data-ttu-id="d05da-149">Entrada</span><span class="sxs-lookup"><span data-stu-id="d05da-149">Input</span></span> | <span data-ttu-id="d05da-150">4</span><span class="sxs-lookup"><span data-stu-id="d05da-150">4</span></span> | <span data-ttu-id="d05da-151">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="d05da-151">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="d05da-152">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d05da-152">OutputTensor</span></span> | <span data-ttu-id="d05da-153">Resultados</span><span class="sxs-lookup"><span data-stu-id="d05da-153">Output</span></span> | <span data-ttu-id="d05da-154">4</span><span class="sxs-lookup"><span data-stu-id="d05da-154">4</span></span> | <span data-ttu-id="d05da-155">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="d05da-155">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="d05da-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d05da-156">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d05da-157">**Header**</span><span class="sxs-lookup"><span data-stu-id="d05da-157">**Header**</span></span> | <span data-ttu-id="d05da-158">directml.h</span><span class="sxs-lookup"><span data-stu-id="d05da-158">directml.h</span></span> |
