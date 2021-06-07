---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Genera los índices de los elementos con valores máximos dentro de una o varias dimensiones del tensor de entrada.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 4c2852c3d301a12d318c5e3006b26830c6eaa6e1
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418034"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="901dc-103">DML_ARGMAX_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="901dc-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="901dc-104">Genera los índices de los elementos con valores máximos dentro de una o varias dimensiones del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="901dc-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="901dc-105">Cada elemento de salida es el resultado de aplicar una reducción *argmax* en un subconjunto del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="901dc-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="901dc-106">La *función argmax* genera el índice del elemento con valores máximos dentro de un conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="901dc-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="901dc-107">Los elementos de entrada implicados en cada reducción se determinan mediante los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="901dc-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="901dc-108">De forma similar, cada índice de salida es con respecto a los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="901dc-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="901dc-109">Si se especifican todos los ejes de entrada, el operador aplica una reducción *argmax* única y genera un único elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="901dc-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="901dc-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="901dc-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="901dc-111">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="901dc-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="901dc-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="901dc-112">Syntax</span></span>
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a><span data-ttu-id="901dc-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="901dc-113">Members</span></span>

`InputTensor`

<span data-ttu-id="901dc-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="901dc-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="901dc-115">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="901dc-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="901dc-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="901dc-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="901dc-117">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="901dc-117">The tensor to write the results to.</span></span> <span data-ttu-id="901dc-118">Cada elemento de salida es el resultado de una reducción *argmax* en un subconjunto de elementos de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="901dc-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="901dc-119">*DimensionCount* debe coincidir *con InputTensor.DimensionCount* (se conserva el rango del tensor de entrada).</span><span class="sxs-lookup"><span data-stu-id="901dc-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="901dc-120">*Los* tamaños deben *coincidir con InputTensor.Sizes,* excepto las dimensiones incluidas en los ejes reducidos, que deben tener el tamaño 1.</span><span class="sxs-lookup"><span data-stu-id="901dc-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="901dc-121">Tipo: **[UINT](../../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="901dc-121">Type: **[UINT](../../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="901dc-122">Número de ejes que se reducirán.</span><span class="sxs-lookup"><span data-stu-id="901dc-122">The number of axes to reduce.</span></span> <span data-ttu-id="901dc-123">Este campo determina el tamaño de la matriz *Axes.*</span><span class="sxs-lookup"><span data-stu-id="901dc-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="901dc-124">Tipo: \_ Field_size \_ (AxisCount) **const [UINT](../../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="901dc-124">Type: \_Field_size\_(AxisCount) **const [UINT](../../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="901dc-125">Ejes a lo largo de los cuales se va a reducir.</span><span class="sxs-lookup"><span data-stu-id="901dc-125">The axes along which to reduce.</span></span> <span data-ttu-id="901dc-126">Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="901dc-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="901dc-127">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="901dc-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="901dc-128">Determina qué índice se va a seleccionar cuando varios elementos de entrada tengan el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="901dc-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="901dc-129">**DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valores máximos (por ejemplo, `argmax({3,2,1,2,3}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="901dc-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="901dc-130">**DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento con valores máximos (por ejemplo, `argmax({3,2,1,2,3}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="901dc-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="901dc-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="901dc-131">Examples</span></span>

<span data-ttu-id="901dc-132">Todos los ejemplos de esta sección usan este mismo tensor de entrada bidimensional.</span><span class="sxs-lookup"><span data-stu-id="901dc-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="901dc-133">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="901dc-133">Example 1.</span></span> <span data-ttu-id="901dc-134">Aplicación de *argmax* a columnas</span><span class="sxs-lookup"><span data-stu-id="901dc-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="901dc-135">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="901dc-135">Example 2.</span></span> <span data-ttu-id="901dc-136">Aplicación de *argmax a* filas</span><span class="sxs-lookup"><span data-stu-id="901dc-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="901dc-137">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="901dc-137">Example 3.</span></span> <span data-ttu-id="901dc-138">Aplicar *argmax a* todos los ejes (todo el tensor)</span><span class="sxs-lookup"><span data-stu-id="901dc-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="901dc-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="901dc-139">Remarks</span></span>
<span data-ttu-id="901dc-140">Los tamaños de tensor de salida deben ser los mismos que los tamaños de tensor de entrada, excepto los ejes reducidos, que deben ser 1.</span><span class="sxs-lookup"><span data-stu-id="901dc-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="901dc-141">Cuando *AxisDirection* es [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="901dc-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="901dc-142">Un subconjunto de esta funcionalidad se expone a través [del operador DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y se admite en niveles de características anteriores de DirectML.</span><span class="sxs-lookup"><span data-stu-id="901dc-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="901dc-143">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="901dc-143">Availability</span></span>
<span data-ttu-id="901dc-144">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="901dc-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="901dc-145">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="901dc-145">Tensor constraints</span></span>
<span data-ttu-id="901dc-146">*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="901dc-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="901dc-147">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="901dc-147">Tensor support</span></span>
| <span data-ttu-id="901dc-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="901dc-148">Tensor</span></span> | <span data-ttu-id="901dc-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="901dc-149">Kind</span></span> | <span data-ttu-id="901dc-150">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="901dc-150">Supported dimension counts</span></span> | <span data-ttu-id="901dc-151">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="901dc-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="901dc-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="901dc-152">InputTensor</span></span> | <span data-ttu-id="901dc-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="901dc-153">Input</span></span> | <span data-ttu-id="901dc-154">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="901dc-154">1 to 8</span></span> | <span data-ttu-id="901dc-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="901dc-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="901dc-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="901dc-156">OutputTensor</span></span> | <span data-ttu-id="901dc-157">Resultados</span><span class="sxs-lookup"><span data-stu-id="901dc-157">Output</span></span> | <span data-ttu-id="901dc-158">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="901dc-158">1 to 8</span></span> | <span data-ttu-id="901dc-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="901dc-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="901dc-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="901dc-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="901dc-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="901dc-161">**Header**</span></span> | <span data-ttu-id="901dc-162">directml.h</span><span class="sxs-lookup"><span data-stu-id="901dc-162">directml.h</span></span> |