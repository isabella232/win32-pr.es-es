---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Genera los índices de los elementos con valores mínimos dentro de una o varias dimensiones del tensor de entrada.
helpviewer_keywords:
- DML_ARGMIN_OPERATOR_DESC
- DML_ARGMIN_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMIN_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMIN_OPERATOR_DESC, DML_ARGMIN_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
- directml/DML_ARGMIN_OPERATOR_DESC
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
- DML_ARGMIN_OPERATOR_DESC
ms.openlocfilehash: da270ea5354e361067335ba1c789efe18310437a
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550480"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="d1160-103">DML_ARGMIN_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="d1160-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="d1160-104">Genera los índices de los elementos con valores mínimos dentro de una o varias dimensiones del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1160-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="d1160-105">Cada elemento de salida es el resultado de aplicar una reducción *argmin* en un subconjunto del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1160-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="d1160-106">La *función argmin* genera el índice del elemento con valores mínimos dentro de un conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="d1160-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="d1160-107">Los elementos de entrada implicados en cada reducción están determinados por los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="d1160-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="d1160-108">De forma similar, cada índice de salida es con respecto a los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="d1160-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="d1160-109">Si se especifican todos los ejes de entrada, el operador aplica una reducción *de argmin* única y genera un único elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="d1160-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d1160-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="d1160-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="d1160-111">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="d1160-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="d1160-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d1160-112">Syntax</span></span>
```cpp
struct DML_ARGMIN_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="d1160-113">Members</span><span class="sxs-lookup"><span data-stu-id="d1160-113">Members</span></span>

`InputTensor`

<span data-ttu-id="d1160-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d1160-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d1160-115">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="d1160-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="d1160-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="d1160-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="d1160-117">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="d1160-117">The tensor to write the results to.</span></span> <span data-ttu-id="d1160-118">Cada elemento de salida es el resultado de una reducción *argmin* en un subconjunto de elementos de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="d1160-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="d1160-119">*DimensionCount* debe coincidir *con InputTensor.DimensionCount* (se conserva la clasificación del tensor de entrada).</span><span class="sxs-lookup"><span data-stu-id="d1160-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="d1160-120">*Los* tamaños deben *coincidir con InputTensor.Sizes,* excepto las dimensiones incluidas en los ejes reducidos, que deben tener el tamaño 1.</span><span class="sxs-lookup"><span data-stu-id="d1160-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="d1160-121">Tipo: **[UINT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d1160-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d1160-122">Número de ejes que se reducirán.</span><span class="sxs-lookup"><span data-stu-id="d1160-122">The number of axes to reduce.</span></span> <span data-ttu-id="d1160-123">Este campo determina el tamaño de la matriz *Axes.*</span><span class="sxs-lookup"><span data-stu-id="d1160-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="d1160-124">Tipo: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="d1160-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d1160-125">Ejes a lo largo de los cuales se va a reducir.</span><span class="sxs-lookup"><span data-stu-id="d1160-125">The axes along which to reduce.</span></span> <span data-ttu-id="d1160-126">Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="d1160-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="d1160-127">DML_AXIS_DIRECTION AxisDirection;</span><span class="sxs-lookup"><span data-stu-id="d1160-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="d1160-128">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="d1160-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="d1160-129">Determina qué índice se va a seleccionar cuando varios elementos de entrada tengan el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="d1160-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="d1160-130">**DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valores mínimos (por ejemplo, `argmin({1,2,3,2,1}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="d1160-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="d1160-131">**DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento con valores mínimos (por ejemplo, `argmin({1,2,3,2,1}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="d1160-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="d1160-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="d1160-132">Examples</span></span>

<span data-ttu-id="d1160-133">Todos los ejemplos de esta sección usan este mismo tensor de entrada bidimensional.</span><span class="sxs-lookup"><span data-stu-id="d1160-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="d1160-134">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="d1160-134">Example 1.</span></span> <span data-ttu-id="d1160-135">Aplicación de *argmin* a columnas</span><span class="sxs-lookup"><span data-stu-id="d1160-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="d1160-136">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="d1160-136">Example 2.</span></span> <span data-ttu-id="d1160-137">Aplicación de *argmin* a filas</span><span class="sxs-lookup"><span data-stu-id="d1160-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="d1160-138">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="d1160-138">Example 3.</span></span> <span data-ttu-id="d1160-139">Aplicar *argmin* a todos los ejes (todo el tensor)</span><span class="sxs-lookup"><span data-stu-id="d1160-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="d1160-140">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d1160-140">Remarks</span></span>
<span data-ttu-id="d1160-141">Los tamaños de tensor de salida deben ser los mismos que los tamaños de tensor de entrada, excepto los ejes reducidos, que deben ser 1.</span><span class="sxs-lookup"><span data-stu-id="d1160-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="d1160-142">Cuando *AxisDirection* es [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="d1160-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="d1160-143">Un subconjunto de esta funcionalidad se expone a través [del operador DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y se admite en niveles de características anteriores de DirectML.</span><span class="sxs-lookup"><span data-stu-id="d1160-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="d1160-144">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="d1160-144">Availability</span></span>
<span data-ttu-id="d1160-145">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="d1160-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="d1160-146">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="d1160-146">Tensor constraints</span></span>
<span data-ttu-id="d1160-147">*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="d1160-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="d1160-148">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="d1160-148">Tensor support</span></span>
| <span data-ttu-id="d1160-149">Tensor</span><span class="sxs-lookup"><span data-stu-id="d1160-149">Tensor</span></span> | <span data-ttu-id="d1160-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="d1160-150">Kind</span></span> | <span data-ttu-id="d1160-151">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="d1160-151">Supported dimension counts</span></span> | <span data-ttu-id="d1160-152">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="d1160-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="d1160-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="d1160-153">InputTensor</span></span> | <span data-ttu-id="d1160-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="d1160-154">Input</span></span> | <span data-ttu-id="d1160-155">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d1160-155">1 to 8</span></span> | <span data-ttu-id="d1160-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="d1160-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="d1160-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="d1160-157">OutputTensor</span></span> | <span data-ttu-id="d1160-158">Resultados</span><span class="sxs-lookup"><span data-stu-id="d1160-158">Output</span></span> | <span data-ttu-id="d1160-159">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="d1160-159">1 to 8</span></span> | <span data-ttu-id="d1160-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="d1160-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="d1160-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1160-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="d1160-162">**Header**</span><span class="sxs-lookup"><span data-stu-id="d1160-162">**Header**</span></span> | <span data-ttu-id="d1160-163">directml.h</span><span class="sxs-lookup"><span data-stu-id="d1160-163">directml.h</span></span> |