---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Genera los índices de los elementos con valores máximos dentro de una o más dimensiones de la tensores de entrada.
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
ms.openlocfilehash: 17ccadc1228ea833ea1f1b3235e97430ac000514
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721259"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a><span data-ttu-id="10da1-103">DML_ARGMAX_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="10da1-103">DML_ARGMAX_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="10da1-104">Genera los índices de los elementos con valores máximos dentro de una o más dimensiones de la tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="10da1-104">Outputs the indices of the maximum-valued elements within one or more dimensions of the input tensor.</span></span>

<span data-ttu-id="10da1-105">Cada elemento Output es el resultado de aplicar una reducción *argmax* en un subconjunto de la tensores de entrada.</span><span class="sxs-lookup"><span data-stu-id="10da1-105">Each output element is the result of applying an *argmax* reduction on a subset of the input tensor.</span></span> <span data-ttu-id="10da1-106">La función *argmax* genera el índice del elemento con valores máximos dentro de un conjunto de elementos de entrada.</span><span class="sxs-lookup"><span data-stu-id="10da1-106">The *argmax* function outputs the index of the maximum-valued element within a set of input elements.</span></span> <span data-ttu-id="10da1-107">Los elementos de entrada implicados en cada reducción vienen determinados por los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="10da1-107">The input elements involved in each reduction are determined by the provided input axes.</span></span> <span data-ttu-id="10da1-108">Del mismo modo, cada índice de salida es con respecto a los ejes de entrada proporcionados.</span><span class="sxs-lookup"><span data-stu-id="10da1-108">Similarly, each output index is with respect to the provided input axes.</span></span> <span data-ttu-id="10da1-109">Si se especifican todos los ejes de entrada, el operador aplica una única reducción de *argmax* y genera un solo elemento de salida.</span><span class="sxs-lookup"><span data-stu-id="10da1-109">If all input axes are specified, then the operator applies a single *argmax* reduction, and produces a single output element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="10da1-110">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="10da1-110">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="10da1-111">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="10da1-111">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="10da1-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="10da1-112">Syntax</span></span>
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

## <a name="members"></a><span data-ttu-id="10da1-113">Miembros</span><span class="sxs-lookup"><span data-stu-id="10da1-113">Members</span></span>

`InputTensor`

<span data-ttu-id="10da1-114">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="10da1-114">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="10da1-115">Tensores del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="10da1-115">The tensor to read from.</span></span>

`OutputTensor`

<span data-ttu-id="10da1-116">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="10da1-116">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="10da1-117">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="10da1-117">The tensor to write the results to.</span></span> <span data-ttu-id="10da1-118">Cada elemento Output es el resultado de una reducción *argmax* en un subconjunto de elementos de *InputTensor*.</span><span class="sxs-lookup"><span data-stu-id="10da1-118">Each output element is the result of an *argmax* reduction on a subset of elements from the *InputTensor*.</span></span> 

- <span data-ttu-id="10da1-119">*DimensionCount* debe coincidir con *InputTensor. DimensionCount* (el rango de la tensores de entrada se conserva).</span><span class="sxs-lookup"><span data-stu-id="10da1-119">*DimensionCount* must match *InputTensor.DimensionCount* (the rank of the input tensor is preserved).</span></span>
- <span data-ttu-id="10da1-120">Los *tamaños* deben coincidir con *InputTensor. Sizes*, excepto para las dimensiones incluidas en los *ejes* reducidos, cuyo tamaño debe ser 1.</span><span class="sxs-lookup"><span data-stu-id="10da1-120">*Sizes* must match *InputTensor.Sizes*, except for dimensions included in the reduced *Axes*, which must be size 1.</span></span>

`AxisCount`

<span data-ttu-id="10da1-121">Tipo: **[uint](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="10da1-121">Type: **[UINT](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="10da1-122">Número de ejes que se van a reducir.</span><span class="sxs-lookup"><span data-stu-id="10da1-122">The number of axes to reduce.</span></span> <span data-ttu-id="10da1-123">Este campo determina el tamaño de la matriz de *ejes* .</span><span class="sxs-lookup"><span data-stu-id="10da1-123">This field determines the size of the *Axes* array.</span></span>

`Axes`

<span data-ttu-id="10da1-124">Tipo: \_ Field_size \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***</span><span class="sxs-lookup"><span data-stu-id="10da1-124">Type: \_Field_size\_(AxisCount) **const [UINT](/windows/desktop/WinProg/windows-data-types)\***</span></span>

<span data-ttu-id="10da1-125">Ejes en los que se va a reducir.</span><span class="sxs-lookup"><span data-stu-id="10da1-125">The axes along which to reduce.</span></span> <span data-ttu-id="10da1-126">Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .</span><span class="sxs-lookup"><span data-stu-id="10da1-126">Values must be in the range `[0, InputTensor.DimensionCount - 1]`.</span></span>

`AxisDirection`

<span data-ttu-id="10da1-127">Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span><span class="sxs-lookup"><span data-stu-id="10da1-127">Type: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**</span></span>

<span data-ttu-id="10da1-128">Determina qué índice se debe seleccionar cuando varios elementos de entrada tienen el mismo valor.</span><span class="sxs-lookup"><span data-stu-id="10da1-128">Determines which index to select when multiple input elements have the same value.</span></span>
- <span data-ttu-id="10da1-129">**DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valor máximo (por ejemplo, `argmax({3,2,1,2,3}) = 0` )</span><span class="sxs-lookup"><span data-stu-id="10da1-129">**DML_AXIS_DIRECTION_INCREASING** returns the index of the first maximum-valued element (for example, `argmax({3,2,1,2,3}) = 0`)</span></span>
- <span data-ttu-id="10da1-130">**DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento con valor máximo (por ejemplo, `argmax({3,2,1,2,3}) = 4` )</span><span class="sxs-lookup"><span data-stu-id="10da1-130">**DML_AXIS_DIRECTION_DECREASING** returns the index of the last maximum-valued element (for example, `argmax({3,2,1,2,3}) = 4`)</span></span>

## <a name="examples"></a><span data-ttu-id="10da1-131">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="10da1-131">Examples</span></span>

<span data-ttu-id="10da1-132">Todos los ejemplos de esta sección usan esta misma tensores de entrada bidimensionales.</span><span class="sxs-lookup"><span data-stu-id="10da1-132">The examples in this section all use this same two-dimensional input tensor.</span></span>

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a><span data-ttu-id="10da1-133">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="10da1-133">Example 1.</span></span> <span data-ttu-id="10da1-134">Aplicar *argmax* a columnas</span><span class="sxs-lookup"><span data-stu-id="10da1-134">Applying *argmax* to columns</span></span>

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a><span data-ttu-id="10da1-135">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="10da1-135">Example 2.</span></span> <span data-ttu-id="10da1-136">Aplicar *argmax* a las filas</span><span class="sxs-lookup"><span data-stu-id="10da1-136">Applying *argmax* to rows</span></span>

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a><span data-ttu-id="10da1-137">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="10da1-137">Example 3.</span></span> <span data-ttu-id="10da1-138">Aplicar *argmax* a todos los ejes (todo el tensores)</span><span class="sxs-lookup"><span data-stu-id="10da1-138">Applying *argmax* to all axes (the entire tensor)</span></span>

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a><span data-ttu-id="10da1-139">Observaciones</span><span class="sxs-lookup"><span data-stu-id="10da1-139">Remarks</span></span>
<span data-ttu-id="10da1-140">Los tamaños de tensores de salida deben ser los mismos que los tamaños de tensores de entrada, salvo los ejes reducidos, que deben ser 1.</span><span class="sxs-lookup"><span data-stu-id="10da1-140">The output tensor sizes must be the same as the input tensor sizes, except for the reduced axes, which must be 1.</span></span>

<span data-ttu-id="10da1-141">Cuando *AxisDirection* se [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span><span class="sxs-lookup"><span data-stu-id="10da1-141">When *AxisDirection* is [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), this API is equivalent to [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) with [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).</span></span>

<span data-ttu-id="10da1-142">Un subconjunto de esta funcionalidad se expone a través del operador [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y es compatible con los niveles de características de DirectML anteriores.</span><span class="sxs-lookup"><span data-stu-id="10da1-142">A subset of this functionality is exposed through the [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) operator, and is supported on earlier DirectML feature levels.</span></span>

## <a name="availability"></a><span data-ttu-id="10da1-143">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="10da1-143">Availability</span></span>
<span data-ttu-id="10da1-144">Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .</span><span class="sxs-lookup"><span data-stu-id="10da1-144">This operator was introduced in `DML_FEATURE_LEVEL_3_0`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="10da1-145">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="10da1-145">Tensor constraints</span></span>
<span data-ttu-id="10da1-146">*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="10da1-146">*InputTensor* and *OutputTensor* must have the same *DimensionCount*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="10da1-147">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="10da1-147">Tensor support</span></span>
| <span data-ttu-id="10da1-148">Tensores</span><span class="sxs-lookup"><span data-stu-id="10da1-148">Tensor</span></span> | <span data-ttu-id="10da1-149">Clase</span><span class="sxs-lookup"><span data-stu-id="10da1-149">Kind</span></span> | <span data-ttu-id="10da1-150">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="10da1-150">Supported dimension counts</span></span> | <span data-ttu-id="10da1-151">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="10da1-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="10da1-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="10da1-152">InputTensor</span></span> | <span data-ttu-id="10da1-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="10da1-153">Input</span></span> | <span data-ttu-id="10da1-154">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="10da1-154">1 to 8</span></span> | <span data-ttu-id="10da1-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="10da1-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="10da1-156">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="10da1-156">OutputTensor</span></span> | <span data-ttu-id="10da1-157">Output</span><span class="sxs-lookup"><span data-stu-id="10da1-157">Output</span></span> | <span data-ttu-id="10da1-158">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="10da1-158">1 to 8</span></span> | <span data-ttu-id="10da1-159">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="10da1-159">INT64, INT32, UINT64, UINT32</span></span> |

## <a name="requirements"></a><span data-ttu-id="10da1-160">Requisitos</span><span class="sxs-lookup"><span data-stu-id="10da1-160">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="10da1-161">**Header**</span><span class="sxs-lookup"><span data-stu-id="10da1-161">**Header**</span></span> | <span data-ttu-id="10da1-162">directml. h</span><span class="sxs-lookup"><span data-stu-id="10da1-162">directml.h</span></span> |