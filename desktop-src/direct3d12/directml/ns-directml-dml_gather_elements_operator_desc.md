---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Recopila elementos de la tensores de entrada a lo largo del eje especificado mediante los índices tensores para reasignarlos a la entrada.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 19a3f19a19d0287dfcbff8b312b1d245fcfe6c09
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721201"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="bc245-103">DML_GATHER_ELEMENTS_OPERATOR_DESC estructura (directml. h)</span><span class="sxs-lookup"><span data-stu-id="bc245-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="bc245-104">Recopila elementos de la tensores de entrada a lo largo del eje especificado mediante los índices tensores para reasignarlos a la entrada.</span><span class="sxs-lookup"><span data-stu-id="bc245-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="bc245-105">Este operador realiza el siguiente pseudocódigo, con el comportamiento exacto que depende del eje, el número de dimensiones de entrada y el número de dimensiones de índices.</span><span class="sxs-lookup"><span data-stu-id="bc245-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="bc245-106">Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span><span class="sxs-lookup"><span data-stu-id="bc245-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/).</span></span> <span data-ttu-id="bc245-107">Consulte también el [historial de versiones de DirectML](../dml-version-history.md).</span><span class="sxs-lookup"><span data-stu-id="bc245-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="bc245-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="bc245-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="bc245-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="bc245-109">Members</span></span>

`InputTensor`

<span data-ttu-id="bc245-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bc245-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bc245-111">Tensores del que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="bc245-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="bc245-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bc245-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bc245-113">Los índices en la tensores de entrada a lo largo del eje activo.</span><span class="sxs-lookup"><span data-stu-id="bc245-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="bc245-114">Los *tamaños* deben coincidir con *InputTensor. Sizes* para cada dimensión excepto *AXIS*.</span><span class="sxs-lookup"><span data-stu-id="bc245-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="bc245-115">A partir de `DML_FEATURE_LEVEL_3_0` , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensores.</span><span class="sxs-lookup"><span data-stu-id="bc245-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="bc245-116">Los índices negativos se interpretan como en relación con el final de la dimensión del eje.</span><span class="sxs-lookup"><span data-stu-id="bc245-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="bc245-117">Por ejemplo, un índice de-1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="bc245-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="bc245-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="bc245-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="bc245-119">Tensores en el que se van a escribir los resultados.</span><span class="sxs-lookup"><span data-stu-id="bc245-119">The tensor to write the results to.</span></span> <span data-ttu-id="bc245-120">Los *tamaños* deben coincidir con *IndicesTensor. Sizes*, y *DataType* debe coincidir con *InputTensor. DataType*.</span><span class="sxs-lookup"><span data-stu-id="bc245-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="bc245-121">Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="bc245-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="bc245-122">La dimensión de eje de *InputTensor* que se va a recopilar, que abarca `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="bc245-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="bc245-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="bc245-123">Examples</span></span>

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a><span data-ttu-id="bc245-124">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="bc245-124">Availability</span></span>
<span data-ttu-id="bc245-125">Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="bc245-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="bc245-126">Restricciones de tensores</span><span class="sxs-lookup"><span data-stu-id="bc245-126">Tensor constraints</span></span>
* <span data-ttu-id="bc245-127">`IndicesTensor`, *InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.</span><span class="sxs-lookup"><span data-stu-id="bc245-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="bc245-128">*InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.</span><span class="sxs-lookup"><span data-stu-id="bc245-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="bc245-129">Compatibilidad con tensores</span><span class="sxs-lookup"><span data-stu-id="bc245-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="bc245-130">DML_FEATURE_LEVEL_3_0 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="bc245-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="bc245-131">Tensores</span><span class="sxs-lookup"><span data-stu-id="bc245-131">Tensor</span></span> | <span data-ttu-id="bc245-132">Clase</span><span class="sxs-lookup"><span data-stu-id="bc245-132">Kind</span></span> | <span data-ttu-id="bc245-133">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="bc245-133">Supported dimension counts</span></span> | <span data-ttu-id="bc245-134">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="bc245-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bc245-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bc245-135">InputTensor</span></span> | <span data-ttu-id="bc245-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="bc245-136">Input</span></span> | <span data-ttu-id="bc245-137">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="bc245-137">1 to 8</span></span> | <span data-ttu-id="bc245-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bc245-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bc245-139">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="bc245-139">IndicesTensor</span></span> | <span data-ttu-id="bc245-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="bc245-140">Input</span></span> | <span data-ttu-id="bc245-141">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="bc245-141">1 to 8</span></span> | <span data-ttu-id="bc245-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="bc245-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="bc245-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bc245-143">OutputTensor</span></span> | <span data-ttu-id="bc245-144">Output</span><span class="sxs-lookup"><span data-stu-id="bc245-144">Output</span></span> | <span data-ttu-id="bc245-145">de 1 a 8</span><span class="sxs-lookup"><span data-stu-id="bc245-145">1 to 8</span></span> | <span data-ttu-id="bc245-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bc245-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="bc245-147">DML_FEATURE_LEVEL_2_1 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="bc245-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="bc245-148">Tensores</span><span class="sxs-lookup"><span data-stu-id="bc245-148">Tensor</span></span> | <span data-ttu-id="bc245-149">Clase</span><span class="sxs-lookup"><span data-stu-id="bc245-149">Kind</span></span> | <span data-ttu-id="bc245-150">Recuentos de dimensiones compatibles</span><span class="sxs-lookup"><span data-stu-id="bc245-150">Supported dimension counts</span></span> | <span data-ttu-id="bc245-151">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="bc245-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="bc245-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="bc245-152">InputTensor</span></span> | <span data-ttu-id="bc245-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="bc245-153">Input</span></span> | <span data-ttu-id="bc245-154">4</span><span class="sxs-lookup"><span data-stu-id="bc245-154">4</span></span> | <span data-ttu-id="bc245-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bc245-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="bc245-156">IndicesTensor</span><span class="sxs-lookup"><span data-stu-id="bc245-156">IndicesTensor</span></span> | <span data-ttu-id="bc245-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="bc245-157">Input</span></span> | <span data-ttu-id="bc245-158">4</span><span class="sxs-lookup"><span data-stu-id="bc245-158">4</span></span> | <span data-ttu-id="bc245-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="bc245-159">UINT32</span></span> |
| <span data-ttu-id="bc245-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="bc245-160">OutputTensor</span></span> | <span data-ttu-id="bc245-161">Output</span><span class="sxs-lookup"><span data-stu-id="bc245-161">Output</span></span> | <span data-ttu-id="bc245-162">4</span><span class="sxs-lookup"><span data-stu-id="bc245-162">4</span></span> | <span data-ttu-id="bc245-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="bc245-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="bc245-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc245-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="bc245-165">**Header**</span><span class="sxs-lookup"><span data-stu-id="bc245-165">**Header**</span></span> | <span data-ttu-id="bc245-166">directml. h</span><span class="sxs-lookup"><span data-stu-id="bc245-166">directml.h</span></span> |