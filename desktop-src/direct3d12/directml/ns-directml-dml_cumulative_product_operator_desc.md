---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multiplica los elementos de un tensor a lo largo de un eje, escribiendo el recuento en ejecución del producto en el tensor de salida.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 71a078ad0f47c19ad1964d8d21f22e06822b5d01
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/27/2021
ms.locfileid: "110550220"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a><span data-ttu-id="cd120-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span><span class="sxs-lookup"><span data-stu-id="cd120-103">DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)</span></span>

<span data-ttu-id="cd120-104">Multiplica los elementos de un tensor a lo largo de un eje, escribiendo el recuento en ejecución del producto en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="cd120-104">Multiplies the elements of a tensor along an axis, writing the running tally of the product into the output tensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd120-105">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="cd120-105">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.5 and later.</span></span> <span data-ttu-id="cd120-106">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="cd120-106">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd120-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="cd120-107">Syntax</span></span>
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a><span data-ttu-id="cd120-108">Members</span><span class="sxs-lookup"><span data-stu-id="cd120-108">Members</span></span>

`InputTensor`

<span data-ttu-id="cd120-109">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd120-109">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd120-110">Tensor que contiene los datos de entrada.</span><span class="sxs-lookup"><span data-stu-id="cd120-110">A tensor containing the input data.</span></span> <span data-ttu-id="cd120-111">Suele ser el mismo tensor que se proporcionó que *inputTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso hacia delante.</span><span class="sxs-lookup"><span data-stu-id="cd120-111">This is typically the same tensor that was provided as the *InputTensor* to [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) in the forward pass.</span></span>

<span data-ttu-id="cd120-112">Tensor de entrada que contiene los elementos que se deben multiplicar.</span><span class="sxs-lookup"><span data-stu-id="cd120-112">The input tensor containing elements to be multiplied.</span></span>

`OutputTensor`

<span data-ttu-id="cd120-113">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="cd120-113">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="cd120-114">Tensor de salida en el que se escriben los productos acumulativos resultantes.</span><span class="sxs-lookup"><span data-stu-id="cd120-114">The output tensor to write the resulting cumulative products to.</span></span> <span data-ttu-id="cd120-115">Este tensor debe tener los mismos tamaños y tipo de datos *que InputTensor.*</span><span class="sxs-lookup"><span data-stu-id="cd120-115">This tensor must have the same sizes and data type as *InputTensor*.</span></span>

`Axis`

<span data-ttu-id="cd120-116">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="cd120-116">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="cd120-117">Índice de la dimensión por la que se multiplican los elementos.</span><span class="sxs-lookup"><span data-stu-id="cd120-117">The index of the dimension to multiply elements over.</span></span> <span data-ttu-id="cd120-118">Este valor debe ser menor que *DimensionCount* del *inputTensor*.</span><span class="sxs-lookup"><span data-stu-id="cd120-118">This value must be less than the *DimensionCount* of the *InputTensor*.</span></span>

`AxisDirection`

<span data-ttu-id="cd120-119">Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span><span class="sxs-lookup"><span data-stu-id="cd120-119">Type: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**</span></span>

<span data-ttu-id="cd120-120">Uno de los valores de la [enumeración DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) datos.</span><span class="sxs-lookup"><span data-stu-id="cd120-120">One of the values of the [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) enumeration.</span></span> <span data-ttu-id="cd120-121">Si se establece **en DML_AXIS_DIRECTION_INCREASING**, el producto se produce recorriendo el tensor a lo largo del eje especificado por índice de elemento ascendente.</span><span class="sxs-lookup"><span data-stu-id="cd120-121">If set to **DML_AXIS_DIRECTION_INCREASING**, then the product occurs by traversing the tensor along the specified axis by ascending element index.</span></span> <span data-ttu-id="cd120-122">Si se establece **en DML_AXIS_DIRECTION_DECREASING**, el valor inverso es true y el producto se produce recorriendo elementos por índice descendente.</span><span class="sxs-lookup"><span data-stu-id="cd120-122">If set to **DML_AXIS_DIRECTION_DECREASING**, the reverse is true and the product occurs by traversing elements by descending index.</span></span>

`HasExclusiveProduct`

<span data-ttu-id="cd120-123">Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span><span class="sxs-lookup"><span data-stu-id="cd120-123">Type: <b><a href="/windows/win32/winprog/windows-data-types">BOOL</a></b></span></span>

<span data-ttu-id="cd120-124">Si **es TRUE**, el valor del elemento actual se excluye al escribir el recuento en ejecución en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="cd120-124">If **TRUE**, then the value of the current element is excluded when writing the running tally to the output tensor.</span></span> <span data-ttu-id="cd120-125">Si **es FALSE,** el valor del elemento actual se incluye en el recuento en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cd120-125">If **FALSE**, then the value of the current element is included in the running tally.</span></span>

## <a name="examples"></a><span data-ttu-id="cd120-126">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="cd120-126">Examples</span></span>

<span data-ttu-id="cd120-127">Todos los ejemplos de esta sección usan este mismo tensor de entrada.</span><span class="sxs-lookup"><span data-stu-id="cd120-127">The examples in this section all use this same input tensor.</span></span>

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a><span data-ttu-id="cd120-128">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="cd120-128">Example 1.</span></span> <span data-ttu-id="cd120-129">Producto acumulativo a través de slivers horizontales</span><span class="sxs-lookup"><span data-stu-id="cd120-129">Cumulative product across horizontal slivers</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a><span data-ttu-id="cd120-130">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="cd120-130">Example 2.</span></span> <span data-ttu-id="cd120-131">Productos exclusivos</span><span class="sxs-lookup"><span data-stu-id="cd120-131">Exclusive products</span></span>

<span data-ttu-id="cd120-132">Establecer *HasExclusiveProduct* en **TRUE** tiene el efecto de excluir el valor del elemento actual del recuento en ejecución al escribir en el tensor de salida.</span><span class="sxs-lookup"><span data-stu-id="cd120-132">Setting *HasExclusiveProduct* to **TRUE** has the effect of excluding the current element's value from the running tally when writing to the output tensor.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a><span data-ttu-id="cd120-133">Ejemplo 3.</span><span class="sxs-lookup"><span data-stu-id="cd120-133">Example 3.</span></span> <span data-ttu-id="cd120-134">Dirección del eje</span><span class="sxs-lookup"><span data-stu-id="cd120-134">Axis direction</span></span>

<span data-ttu-id="cd120-135">Establecer *AxisDirection en* [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) tiene el efecto de invertir el orden transversal de los elementos al calcular el recuento en ejecución.</span><span class="sxs-lookup"><span data-stu-id="cd120-135">Setting the *AxisDirection* to [**DML_AXIS_DIRECTION_DECREASING**](./ne-directml-dml_axis_direction.md) has the effect of reversing the traversal order of elements when computing the running tally.</span></span>

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a><span data-ttu-id="cd120-136">Ejemplo 4.</span><span class="sxs-lookup"><span data-stu-id="cd120-136">Example 4.</span></span> <span data-ttu-id="cd120-137">Multiplicación a lo largo de un eje diferente</span><span class="sxs-lookup"><span data-stu-id="cd120-137">Multiplying along a different axis</span></span>

<span data-ttu-id="cd120-138">En este ejemplo, el producto se produce verticalmente, a lo largo del eje de altura (segunda dimensión).</span><span class="sxs-lookup"><span data-stu-id="cd120-138">In this example, the product occurs vertically, along the height axis (second dimension).</span></span>

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a><span data-ttu-id="cd120-139">Comentarios</span><span class="sxs-lookup"><span data-stu-id="cd120-139">Remarks</span></span>
<span data-ttu-id="cd120-140">Este operador admite la ejecución en contexto, lo que significa que el tensor de salida puede usar el alias *InputTensor* durante el enlace.</span><span class="sxs-lookup"><span data-stu-id="cd120-140">This operator supports in-place execution, meaning that the output tensor is permitted to alias *InputTensor* during binding.</span></span>

## <a name="availability"></a><span data-ttu-id="cd120-141">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="cd120-141">Availability</span></span>
<span data-ttu-id="cd120-142">Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .</span><span class="sxs-lookup"><span data-stu-id="cd120-142">This operator was introduced in `DML_FEATURE_LEVEL_3_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="cd120-143">Restricciones de Tensor</span><span class="sxs-lookup"><span data-stu-id="cd120-143">Tensor constraints</span></span>
<span data-ttu-id="cd120-144">*InputTensor* y *OutputTensor* deben tener los mismos *tipos de datos* y *tamaños.*</span><span class="sxs-lookup"><span data-stu-id="cd120-144">*InputTensor* and *OutputTensor* must have the same *DataType* and *Sizes*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="cd120-145">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="cd120-145">Tensor support</span></span>
| <span data-ttu-id="cd120-146">Tensor</span><span class="sxs-lookup"><span data-stu-id="cd120-146">Tensor</span></span> | <span data-ttu-id="cd120-147">Tipo</span><span class="sxs-lookup"><span data-stu-id="cd120-147">Kind</span></span> | <span data-ttu-id="cd120-148">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="cd120-148">Supported dimension counts</span></span> | <span data-ttu-id="cd120-149">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="cd120-149">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="cd120-150">InputTensor</span><span class="sxs-lookup"><span data-stu-id="cd120-150">InputTensor</span></span> | <span data-ttu-id="cd120-151">Entrada</span><span class="sxs-lookup"><span data-stu-id="cd120-151">Input</span></span> | <span data-ttu-id="cd120-152">4</span><span class="sxs-lookup"><span data-stu-id="cd120-152">4</span></span> | <span data-ttu-id="cd120-153">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="cd120-153">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |
| <span data-ttu-id="cd120-154">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="cd120-154">OutputTensor</span></span> | <span data-ttu-id="cd120-155">Resultados</span><span class="sxs-lookup"><span data-stu-id="cd120-155">Output</span></span> | <span data-ttu-id="cd120-156">4</span><span class="sxs-lookup"><span data-stu-id="cd120-156">4</span></span> | <span data-ttu-id="cd120-157">FLOAT32, FLOAT16, UINT32, UINT16</span><span class="sxs-lookup"><span data-stu-id="cd120-157">FLOAT32, FLOAT16, UINT32, UINT16</span></span> |

## <a name="requirements"></a><span data-ttu-id="cd120-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cd120-158">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="cd120-159">**Header**</span><span class="sxs-lookup"><span data-stu-id="cd120-159">**Header**</span></span> | <span data-ttu-id="cd120-160">directml.h</span><span class="sxs-lookup"><span data-stu-id="cd120-160">directml.h</span></span> |