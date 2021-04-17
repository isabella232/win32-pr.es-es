---
UID: NS:directml.DML_ARGMIN_OPERATOR_DESC
title: DML_ARGMIN_OPERATOR_DESC
description: Genera los índices de los elementos con valores mínimos en una o más dimensiones de la tensores de entrada.
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
ms.openlocfilehash: 30d281c6ab35675e0cfce80b7eb025292c501041
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721232"
---
# <a name="dml_argmin_operator_desc-structure-directmlh"></a><span data-ttu-id="9f1d6-103">DML_ARGMIN_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="9f1d6-103">DML_ARGMIN_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="9f1d6-104">Genera los índices de los elementos con valores mínimos en una o más dimensiones de la tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-104">Outputs the indices of the minimum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="9f1d6-105">Cada elemento Output es el resultado de aplicar una reducción *argmin* en un subconjunto de la tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-105">Each output element is the result of applying an *argmin* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="9f1d6-106">La función *argmin* genera el índice del elemento de valor mínimo dentro de un conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-106">The *argmin* function outputs the index of the minimum-valued element within a set of input elements.</span></span> <span data-ttu-id="9f1d6-107">Los elementos de entrada implicados en cada reducción vienen determinados por los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="9f1d6-108">Del mismo modo, cada índice de salida es con respecto a los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="9f1d6-109">Si se especifican todos los ejes de entrada, el operador aplica una única reducción de *argmin* y genera un solo elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-109">If all input axes are specified, then the operator applies a single *argmin* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f1d6-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="9f1d6-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="9f1d6-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="9f1d6-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f1d6-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9f1d6-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="9f1d6-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="9f1d6-113">Members</span></span>

`InputTensor`

<span data-ttu-id="9f1d6-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9f1d6-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9f1d6-115">Tensores del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="9f1d6-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="9f1d6-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="9f1d6-117">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-117">The tensor to write the results to.</span></span> <span data-ttu-id="9f1d6-118">Cada elemento Output es el resultado de una reducción *argmin* en un subconjunto de elementos de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-118">Each output element is the result of an *argmin* reduction on a subset of elements from the *InputTensor*.</span></span>

- <span data-ttu-id="9f1d6-119">*DimensionCount* debe coincidir con *InputTensor. DimensionCount* (el rango de la tensores de entrada se conserva).</span><span class="sxs-lookup"><span data-stu-id="9f1d6-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="9f1d6-120">Los *tamaños* deben coincidir con *InputTensor. Sizes*, excepto para las dimensiones incluidas en los *ejes* reducidos, cuyo tamaño debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="9f1d6-121">Tipo: **[uint](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="9f1d6-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="9f1d6-122">Número de ejes que se van a reducir.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-122">The number of axes to reduce.</span></span> <span data-ttu-id="9f1d6-123">Este campo determina el tamaño de la matriz de *ejes* .</span><span class="sxs-lookup"><span data-stu-id="9f1d6-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="9f1d6-124">Tipo: \_ Field_size \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="9f1d6-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="9f1d6-125">Ejes en los que se va a reducir.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-125">The axes along which to reduce.</span></span> <span data-ttu-id="9f1d6-126">Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="9f1d6-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="9f1d6-127">DML_AXIS_DIRECTION AxisDirection;</span><span class="sxs-lookup"><span data-stu-id="9f1d6-127">DML_AXIS_DIRECTION AxisDirection;</span></span>

<span data-ttu-id="9f1d6-128">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="9f1d6-128">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="9f1d6-129">Determina qué índice se debe seleccionar cuando varios elementos de entrada tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-129">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="9f1d6-130">**DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valor mínimo (por ejemplo, `argmin({1,2,3,2,1}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="9f1d6-130">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first minimum-valued element (for example, `argmin({1,2,3,2,1}) = 0`)</span></span>
- <span data-ttu-id="9f1d6-131">**DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento de valor mínimo (por ejemplo, `argmin({1,2,3,2,1}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="9f1d6-131">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last minimum-valued element (for example, `argmin({1,2,3,2,1}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="9f1d6-132">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9f1d6-132">Examples</span></span>

<span data-ttu-id="9f1d6-133">Todos los ejemplos de esta sección usan esta misma tensores de entrada bidimensionales.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-133">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmin-to-columns"></a><span data-ttu-id="9f1d6-134">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-134">Example 1.</span></span> <span data-ttu-id="9f1d6-135">Aplicar *argmin* a columnas</span><span class="sxs-lookup"><span data-stu-id="9f1d6-135">Applying *argmin* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[0,  // argmin({1, 3, 2})
  1,  // argmin({2, 0, 5})
  2]] // argmin({3, 4, 2})
```

### <a name="example-2-applying-argmin-to-rows"></a><span data-ttu-id="9f1d6-136">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-136">Example 2.</span></span> <span data-ttu-id="9f1d6-137">Aplicar *argmin* a las filas</span><span class="sxs-lookup"><span data-stu-id="9f1d6-137">Applying *argmin* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[0], // argmin({1, 2, 3})
 [1], // argmin({3, 0, 4})
 [0]] // argmin({2, 5, 2})
```

### <a name="example-3-applying-argmin-to-all-axes-the-entire-tensor"></a><span data-ttu-id="9f1d6-138">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-138">Example 3.</span></span> <span data-ttu-id="9f1d6-139">Aplicar *argmin* a todos los ejes (todo el tensores)</span><span class="sxs-lookup"><span data-stu-id="9f1d6-139">Applying *argmin* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[4]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="9f1d6-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9f1d6-140">Remarks</span></span>
<span data-ttu-id="9f1d6-141">Los tamaños de tensores de salida deben ser los mismos que los tamaños de tensores de entrada, salvo los ejes reducidos, que deben ser 1.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-141">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="9f1d6-142">Cuando *AxisDirection* se [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="9f1d6-142">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMIN](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="9f1d6-143">Un subconjunto de esta funcionalidad se expone a través del operador [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y es compatible con los niveles de características de DirectML anteriores.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-143">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="9f1d6-144">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="9f1d6-144">Availability</span></span>
<span data-ttu-id="9f1d6-145">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="9f1d6-145">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="9f1d6-146">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="9f1d6-146">Tensor constraints</span></span>
<span data-ttu-id="9f1d6-147">*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="9f1d6-147">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="9f1d6-148">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="9f1d6-148">Tensor support</span></span>
| <span data-ttu-id="9f1d6-149">Tensores</span><span class="sxs-lookup"><span data-stu-id="9f1d6-149">Tensor</span></span> | <span data-ttu-id="9f1d6-150">Clase</span><span class="sxs-lookup"><span data-stu-id="9f1d6-150">Kind</span></span> | <span data-ttu-id="9f1d6-151">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="9f1d6-151">Supported dimension counts</span></span> | <span data-ttu-id="9f1d6-152">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="9f1d6-152">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="9f1d6-153">InputTensor</span><span class="sxs-lookup"><span data-stu-id="9f1d6-153">InputTensor</span></span> | <span data-ttu-id="9f1d6-154">Entrada</span><span class="sxs-lookup"><span data-stu-id="9f1d6-154">Input</span></span> | <span data-ttu-id="9f1d6-155">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="9f1d6-155">1 to 8</span></span> | <span data-ttu-id="9f1d6-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="9f1d6-156">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="9f1d6-157">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="9f1d6-157">OutputTensor</span></span> | <span data-ttu-id="9f1d6-158">Output</span><span class="sxs-lookup"><span data-stu-id="9f1d6-158">Output</span></span> | <span data-ttu-id="9f1d6-159">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="9f1d6-159">1 to 8</span></span> | <span data-ttu-id="9f1d6-160">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="9f1d6-160">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="9f1d6-161">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f1d6-161">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="9f1d6-162">**Header**</span><span class="sxs-lookup"><span data-stu-id="9f1d6-162">**Header**</span></span> | <span data-ttu-id="9f1d6-163">directml. h</span><span class="sxs-lookup"><span data-stu-id="9f1d6-163">directml.h</span></span> |