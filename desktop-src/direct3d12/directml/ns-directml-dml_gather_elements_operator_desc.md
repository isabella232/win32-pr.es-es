---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Recopila elementos del tensor de entrada a lo largo del eje dado mediante el tensor de índices para reasignar a la entrada.
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
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418006"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a><span data-ttu-id="42ebc-103">DML_GATHER_ELEMENTS_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="42ebc-103">DML_GATHER_ELEMENTS_OPERATOR_DESC structure (directml.h)</span></span>

<span data-ttu-id="42ebc-104">Recopila elementos del tensor de entrada a lo largo del eje dado mediante el tensor de índices para reasignar a la entrada.</span><span class="sxs-lookup"><span data-stu-id="42ebc-104">Gathers elements from the input tensor along the given axis using the indices tensor to remap into the input.</span></span> <span data-ttu-id="42ebc-105">Este operador realiza el pseudocódigo siguiente, con el comportamiento exacto dependiente del eje, el recuento de dimensiones de entrada y el recuento de dimensiones de índices.</span><span class="sxs-lookup"><span data-stu-id="42ebc-105">This operator performs the following pseudocode, with the exact behavior dependent on the axis, input dimension count, and indices dimension count.</span></span>

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> <span data-ttu-id="42ebc-106">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="42ebc-106">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="42ebc-107">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="42ebc-107">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="42ebc-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="42ebc-108">Syntax</span></span>
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a><span data-ttu-id="42ebc-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="42ebc-109">Members</span></span>

`InputTensor`

<span data-ttu-id="42ebc-110">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="42ebc-110">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="42ebc-111">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="42ebc-111">The tensor to read from.</span></span>


`IndicesTensor`

<span data-ttu-id="42ebc-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="42ebc-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="42ebc-113">Los índices en el tensor de entrada a lo largo del eje activo.</span><span class="sxs-lookup"><span data-stu-id="42ebc-113">The indices into the input tensor along the active axis.</span></span> <span data-ttu-id="42ebc-114">Los *tamaños deben* coincidir con *InputTensor.Sizes para* todas las dimensiones excepto el *eje*.</span><span class="sxs-lookup"><span data-stu-id="42ebc-114">The *Sizes* must match *InputTensor.Sizes* for every dimension except *Axis*.</span></span>

<span data-ttu-id="42ebc-115">A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor.</span><span class="sxs-lookup"><span data-stu-id="42ebc-115">Starting with `DML_FEATURE_LEVEL_3_0`, this operator supports negative index values when using a signed integral type with this tensor.</span></span> <span data-ttu-id="42ebc-116">Los índices negativos se interpretan como relativos al final de la dimensión del eje.</span><span class="sxs-lookup"><span data-stu-id="42ebc-116">Negative indices are interpreted as being relative to the end of the axis dimension.</span></span> <span data-ttu-id="42ebc-117">Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.</span><span class="sxs-lookup"><span data-stu-id="42ebc-117">For example, an index of -1 refers to the last element along that dimension.</span></span>


`OutputTensor`

<span data-ttu-id="42ebc-118">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="42ebc-118">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="42ebc-119">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="42ebc-119">The tensor to write the results to.</span></span> <span data-ttu-id="42ebc-120">Los *tamaños* deben coincidir *con IndicesTensor.Sizes* y *DataType* debe coincidir con *InputTensor.DataType.*</span><span class="sxs-lookup"><span data-stu-id="42ebc-120">The *Sizes* must match *IndicesTensor.Sizes*, and *DataType* must match *InputTensor.DataType*.</span></span>


`Axis`

<span data-ttu-id="42ebc-121">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="42ebc-121">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="42ebc-122">Dimensión de eje de *InputTensor que* se va a recopilar, que abarca `[0, *InputTensor.DimensionCount*)` .</span><span class="sxs-lookup"><span data-stu-id="42ebc-122">The axis dimension of *InputTensor* to gather along, ranging `[0, *InputTensor.DimensionCount*)`.</span></span>

## <a name="examples"></a><span data-ttu-id="42ebc-123">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="42ebc-123">Examples</span></span>

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

## <a name="availability"></a><span data-ttu-id="42ebc-124">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="42ebc-124">Availability</span></span>
<span data-ttu-id="42ebc-125">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="42ebc-125">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="42ebc-126">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-126">Tensor constraints</span></span>
* <span data-ttu-id="42ebc-127">`IndicesTensor`, *InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*</span><span class="sxs-lookup"><span data-stu-id="42ebc-127">`IndicesTensor`, *InputTensor*, and *OutputTensor* must have the same *DimensionCount*.</span></span>
* <span data-ttu-id="42ebc-128">*InputTensor* y *OutputTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="42ebc-128">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="42ebc-129">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-129">Tensor support</span></span>
### <a name="dml_feature_level_3_0-and-above"></a><span data-ttu-id="42ebc-130">DML_FEATURE_LEVEL_3_0 y posteriores</span><span class="sxs-lookup"><span data-stu-id="42ebc-130">DML_FEATURE_LEVEL_3_0 and above</span></span>
| <span data-ttu-id="42ebc-131">Tensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-131">Tensor</span></span> | <span data-ttu-id="42ebc-132">Tipo</span><span class="sxs-lookup"><span data-stu-id="42ebc-132">Kind</span></span> | <span data-ttu-id="42ebc-133">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="42ebc-133">Supported dimension counts</span></span> | <span data-ttu-id="42ebc-134">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="42ebc-134">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="42ebc-135">InputTensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-135">InputTensor</span></span> | <span data-ttu-id="42ebc-136">Entrada</span><span class="sxs-lookup"><span data-stu-id="42ebc-136">Input</span></span> | <span data-ttu-id="42ebc-137">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="42ebc-137">1 to 8</span></span> | <span data-ttu-id="42ebc-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="42ebc-138">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="42ebc-139">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-139">IndicesTensor</span></span> | <span data-ttu-id="42ebc-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="42ebc-140">Input</span></span> | <span data-ttu-id="42ebc-141">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="42ebc-141">1 to 8</span></span> | <span data-ttu-id="42ebc-142">INT64, INT32, UINT64, UINT32</span><span class="sxs-lookup"><span data-stu-id="42ebc-142">INT64, INT32, UINT64, UINT32</span></span> |
| <span data-ttu-id="42ebc-143">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-143">OutputTensor</span></span> | <span data-ttu-id="42ebc-144">Resultados</span><span class="sxs-lookup"><span data-stu-id="42ebc-144">Output</span></span> | <span data-ttu-id="42ebc-145">De 1 a 8</span><span class="sxs-lookup"><span data-stu-id="42ebc-145">1 to 8</span></span> | <span data-ttu-id="42ebc-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="42ebc-146">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |

### <a name="dml_feature_level_2_1-and-above"></a><span data-ttu-id="42ebc-147">DML_FEATURE_LEVEL_2_1 y posteriores</span><span class="sxs-lookup"><span data-stu-id="42ebc-147">DML_FEATURE_LEVEL_2_1 and above</span></span>
| <span data-ttu-id="42ebc-148">Tensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-148">Tensor</span></span> | <span data-ttu-id="42ebc-149">Tipo</span><span class="sxs-lookup"><span data-stu-id="42ebc-149">Kind</span></span> | <span data-ttu-id="42ebc-150">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="42ebc-150">Supported dimension counts</span></span> | <span data-ttu-id="42ebc-151">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="42ebc-151">Supported data types</span></span> |
| ------ | ---- | -------------------------- | -------------------- |
| <span data-ttu-id="42ebc-152">InputTensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-152">InputTensor</span></span> | <span data-ttu-id="42ebc-153">Entrada</span><span class="sxs-lookup"><span data-stu-id="42ebc-153">Input</span></span> | <span data-ttu-id="42ebc-154">4</span><span class="sxs-lookup"><span data-stu-id="42ebc-154">4</span></span> | <span data-ttu-id="42ebc-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="42ebc-155">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="42ebc-156">ÍndicesTensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-156">IndicesTensor</span></span> | <span data-ttu-id="42ebc-157">Entrada</span><span class="sxs-lookup"><span data-stu-id="42ebc-157">Input</span></span> | <span data-ttu-id="42ebc-158">4</span><span class="sxs-lookup"><span data-stu-id="42ebc-158">4</span></span> | <span data-ttu-id="42ebc-159">UINT32</span><span class="sxs-lookup"><span data-stu-id="42ebc-159">UINT32</span></span> |
| <span data-ttu-id="42ebc-160">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="42ebc-160">OutputTensor</span></span> | <span data-ttu-id="42ebc-161">Resultados</span><span class="sxs-lookup"><span data-stu-id="42ebc-161">Output</span></span> | <span data-ttu-id="42ebc-162">4</span><span class="sxs-lookup"><span data-stu-id="42ebc-162">4</span></span> | <span data-ttu-id="42ebc-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="42ebc-163">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |



## <a name="requirements"></a><span data-ttu-id="42ebc-164">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42ebc-164">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="42ebc-165">**Header**</span><span class="sxs-lookup"><span data-stu-id="42ebc-165">**Header**</span></span> | <span data-ttu-id="42ebc-166">directml.h</span><span class="sxs-lookup"><span data-stu-id="42ebc-166">directml.h</span></span> |