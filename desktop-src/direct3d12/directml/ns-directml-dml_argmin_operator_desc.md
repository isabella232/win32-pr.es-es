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
ms.openlocfilehash: 2e12a81593504a4eb7a0917e545bfa20c70647ff
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804080"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="801cd-103">DML_ARGMIN_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="801cd-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="801cd-104">Genera los índices de los elementos con valores mínimos dentro de una o varias dimensiones del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="801cd-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="801cd-105">Cada elemento de salida es el resultado de aplicar una *reducción argmin* en un subconjunto del tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="801cd-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="801cd-106">La *función argmin* genera el índice del elemento con valores mínimos dentro de un conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="801cd-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="801cd-107">Los elementos de entrada implicados en cada reducción se determinan mediante los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="801cd-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="801cd-108">De forma similar, cada índice de salida es con respecto a los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="801cd-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="801cd-109">Si se especifican todos los ejes de entrada, el operador aplica una reducción *argmin* única y genera un único elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="801cd-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="801cd-110">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="801cd-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="801cd-111">Consulte también historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="801cd-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="801cd-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="801cd-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="801cd-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="801cd-113">Members</span></span>

`InputTensor`

<span data-ttu-id="801cd-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="801cd-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="801cd-115">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="801cd-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="801cd-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="801cd-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="801cd-117">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="801cd-117">The tensor to write the results to.</span></span> <span data-ttu-id="801cd-118">Cada elemento de salida es el resultado de una *reducción argmin* en un subconjunto de elementos de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="801cd-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="801cd-119">*DimensionCount* debe coincidir *con InputTensor.DimensionCount* (se conserva el rango del tensor de entrada).</span><span class="sxs-lookup"><span data-stu-id="801cd-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="801cd-120">*Los* tamaños deben *coincidir con InputTensor.Sizes,* excepto las dimensiones incluidas en los ejes reducidos, que deben tener el tamaño 1.</span><span class="sxs-lookup"><span data-stu-id="801cd-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="801cd-121">Tipo: **[UINT](/windows/win32/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="801cd-121">Type: **[UINT](/windows/win32/winprog/windows-data-types)**</span></span>

<span data-ttu-id="801cd-122">Número de ejes que se reducirán.</span><span class="sxs-lookup"><span data-stu-id="801cd-122">The number of axes to reduce.</span></span> <span data-ttu-id="801cd-123">Este campo determina el tamaño de la matriz *Axes.*</span><span class="sxs-lookup"><span data-stu-id="801cd-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="801cd-124">Tipo: \_ Field_size \_ (AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="801cd-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/win32/winprog/windows-data-types)\***</span></span>

<span data-ttu-id="801cd-125">Ejes a lo largo de los que se va a reducir.</span><span class="sxs-lookup"><span data-stu-id="801cd-125">The axes along which to reduce.</span></span> <span data-ttu-id="801cd-126">Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="801cd-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="801cd-127">DML_AXIS_DIRECTION AxisDirection;</span><span class="sxs-lookup"><span data-stu-id="801cd-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="801cd-128">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="801cd-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="801cd-129">Determina qué índice seleccionar cuando varios elementos de entrada tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="801cd-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="801cd-130">**DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valores mínimos (por ejemplo, `argmin({1,2,3,2,1}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="801cd-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="801cd-131">**DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento con valores mínimos (por ejemplo, `argmin({1,2,3,2,1}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="801cd-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="801cd-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="801cd-132">Examples</span></span>

<span data-ttu-id="801cd-133">Todos los ejemplos de esta sección usan este mismo tensor de entrada bidimensional.</span><span class="sxs-lookup"><span data-stu-id="801cd-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="801cd-134">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="801cd-134">Example 1.</span></span> <span data-ttu-id="801cd-135">Aplicación de *argmin* a columnas</span><span class="sxs-lookup"><span data-stu-id="801cd-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="801cd-136">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="801cd-136">Example 2.</span></span> <span data-ttu-id="801cd-137">Aplicación de *argmin* a filas</span><span class="sxs-lookup"><span data-stu-id="801cd-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="801cd-138">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="801cd-138">Example 3.</span></span> <span data-ttu-id="801cd-139">Aplicar *argmin* a todos los ejes (todo el tensor)</span><span class="sxs-lookup"><span data-stu-id="801cd-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="801cd-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="801cd-140">Remarks</span></span>
<span data-ttu-id="801cd-141">Los tamaños de tensor de salida deben ser los mismos que los tamaños de tensor de entrada, excepto para los ejes reducidos, que deben ser 1.</span><span class="sxs-lookup"><span data-stu-id="801cd-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="801cd-142">Cuando *AxisDirection* es [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="801cd-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="801cd-143">Un subconjunto de esta funcionalidad se expone a través [del operador DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y se admite en niveles de características anteriores de DirectML.</span><span class="sxs-lookup"><span data-stu-id="801cd-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="801cd-144">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="801cd-144">Availability</span></span>
<span data-ttu-id="801cd-145">Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="801cd-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="801cd-146">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="801cd-146">Tensor constraints</span></span>
<span data-ttu-id="801cd-147">*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="801cd-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="801cd-148">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="801cd-148">Tensor support</span></span>
| <span data-ttu-id="801cd-149">Tensor</span><span class="sxs-lookup"><span data-stu-id="801cd-149">Tensor</span></span> | <span data-ttu-id="801cd-150">Tipo</span><span class="sxs-lookup"><span data-stu-id="801cd-150">Kind</span></span> | <span data-ttu-id="801cd-151">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="801cd-151">Supported dimension counts</span></span> | <span data-ttu-id="801cd-152">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="801cd-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="801cd-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="801cd-153">InputTensor</span></span> | <span data-ttu-id="801cd-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="801cd-154">Input</span></span> | <span data-ttu-id="801cd-155">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="801cd-155">1 to 8</span></span> | <span data-ttu-id="801cd-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="801cd-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="801cd-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="801cd-157">OutputTensor</span></span> | <span data-ttu-id="801cd-158">Resultados</span><span class="sxs-lookup"><span data-stu-id="801cd-158">Output</span></span> | <span data-ttu-id="801cd-159">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="801cd-159">1 to 8</span></span> | <span data-ttu-id="801cd-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="801cd-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="801cd-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="801cd-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="801cd-162">**Header**</span><span class="sxs-lookup"><span data-stu-id="801cd-162">**Header**</span></span> | <span data-ttu-id="801cd-163">directml.h</span><span class="sxs-lookup"><span data-stu-id="801cd-163">directml.h</span></span> |