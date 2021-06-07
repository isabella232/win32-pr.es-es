---
UID: NS:directml.DML_SPACE_TO_DEPTH1_OPERATOR_DESC
title: DML_SPACE_TO_DEPTH1_OPERATOR_DESC
description: Reorganiza los bloques de datos espaciales en profundidad. El operador genera una copia del tensor de entrada donde los valores de las dimensiones de alto y ancho se mueven a la dimensión de profundidad.
helpviewer_keywords:
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure
- direct3d12.dml_space_to_depth1_operator_desc
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
- directml/DML_SPACE_TO_DEPTH1_OPERATOR_DESC
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
- DML_SPACE_TO_DEPTH1_OPERATOR_DESC
ms.openlocfilehash: 35e64d83fa6b8df42428869f72249e9846e50596
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418038"
---
# <a name="dml_space_to_depth1_operator_desc-structure-directmlh"></a><span data-ttu-id="71dde-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="71dde-104">DML_SPACE_TO_DEPTH1_OPERATOR_DESC structure (directml.h)</span></span>
<span data-ttu-id="71dde-105">Reorganiza los bloques de datos espaciales en profundidad.</span><span class="sxs-lookup"><span data-stu-id="71dde-105">Rearranges blocks of spatial data into depth.</span></span> <span data-ttu-id="71dde-106">El operador genera una copia del tensor de entrada donde los valores de las dimensiones de alto y ancho se mueven a la dimensión de profundidad.</span><span class="sxs-lookup"><span data-stu-id="71dde-106">The operator outputs a copy of the input tensor where values from the height and width dimensions are moved to the depth dimension.</span></span>

<span data-ttu-id="71dde-107">Esta es la transformación inversa de [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span><span class="sxs-lookup"><span data-stu-id="71dde-107">This is the inverse transformation of [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="71dde-108">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="71dde-108">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="71dde-109">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="71dde-109">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="71dde-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="71dde-110">Syntax</span></span>
```cpp
struct DML_SPACE_TO_DEPTH1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a><span data-ttu-id="71dde-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="71dde-111">Members</span></span>

`InputTensor`

<span data-ttu-id="71dde-112">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="71dde-112">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="71dde-113">Tensor del que se leerá.</span><span class="sxs-lookup"><span data-stu-id="71dde-113">The tensor to read from.</span></span> <span data-ttu-id="71dde-114">Las dimensiones del tensor de entrada son `{ Batch, Channels, Height, Width }` .</span><span class="sxs-lookup"><span data-stu-id="71dde-114">The input tensor's dimensions are `{ Batch, Channels, Height, Width }`.</span></span>


`OutputTensor`

<span data-ttu-id="71dde-115">Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***</span><span class="sxs-lookup"><span data-stu-id="71dde-115">Type: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc)\***</span></span>

<span data-ttu-id="71dde-116">Tensor en el que se escriben los resultados.</span><span class="sxs-lookup"><span data-stu-id="71dde-116">The tensor to write the results to.</span></span> <span data-ttu-id="71dde-117">Las dimensiones del tensor de salida son `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }` .</span><span class="sxs-lookup"><span data-stu-id="71dde-117">The output tensor's dimensions are `{ Batch, Channels / (BlockSize * BlockSize), Height * BlockSize, Width * BlockSize }`.</span></span>


`BlockSize`

<span data-ttu-id="71dde-118">Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)</span><span class="sxs-lookup"><span data-stu-id="71dde-118">Type: [**UINT**](/windows/desktop/winprog/windows-data-types)</span></span>

<span data-ttu-id="71dde-119">Ancho y alto de los bloques que se mueven.</span><span class="sxs-lookup"><span data-stu-id="71dde-119">The width and height of the Blocks that are moved.</span></span>


`Order`

<span data-ttu-id="71dde-120">Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span><span class="sxs-lookup"><span data-stu-id="71dde-120">Type: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**</span></span>

<span data-ttu-id="71dde-121">Vea [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span><span class="sxs-lookup"><span data-stu-id="71dde-121">See [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).</span></span>

## <a name="examples"></a><span data-ttu-id="71dde-122">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="71dde-122">Examples</span></span>

### <a name="example-1-depth-column-row-order"></a><span data-ttu-id="71dde-123">Ejemplo 1.</span><span class="sxs-lookup"><span data-stu-id="71dde-123">Example 1.</span></span> <span data-ttu-id="71dde-124">Orden de fila de columna de profundidad</span><span class="sxs-lookup"><span data-stu-id="71dde-124">Depth-column-row order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]

OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a><span data-ttu-id="71dde-125">Ejemplo 2.</span><span class="sxs-lookup"><span data-stu-id="71dde-125">Example 2.</span></span> <span data-ttu-id="71dde-126">Orden de profundidad de fila de columna</span><span class="sxs-lookup"><span data-stu-id="71dde-126">Column-row-depth order</span></span>

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
InputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
OutputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```


## <a name="remarks"></a><span data-ttu-id="71dde-127">Comentarios</span><span class="sxs-lookup"><span data-stu-id="71dde-127">Remarks</span></span>
<span data-ttu-id="71dde-128">Cuando el *parámetro Order* se establece [en DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), este operador es equivalente a [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span><span class="sxs-lookup"><span data-stu-id="71dde-128">When the *Order* parameter is set to [DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), this operator is equivalent to [DML_SPACE_TO_DEPTH_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_space_to_depth_operator_desc).</span></span>

## <a name="availability"></a><span data-ttu-id="71dde-129">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="71dde-129">Availability</span></span>
<span data-ttu-id="71dde-130">Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .</span><span class="sxs-lookup"><span data-stu-id="71dde-130">This operator was introduced in `DML_FEATURE_LEVEL_2_1`.</span></span>

## <a name="tensor-constraints"></a><span data-ttu-id="71dde-131">Restricciones de tensor</span><span class="sxs-lookup"><span data-stu-id="71dde-131">Tensor constraints</span></span>
<span data-ttu-id="71dde-132">*InputTensor* y *OutputTensor* deben tener el mismo *DataType.*</span><span class="sxs-lookup"><span data-stu-id="71dde-132">*InputTensor* and *OutputTensor* must have the same *DataType*.</span></span>

## <a name="tensor-support"></a><span data-ttu-id="71dde-133">Compatibilidad con Tensor</span><span class="sxs-lookup"><span data-stu-id="71dde-133">Tensor support</span></span>
| <span data-ttu-id="71dde-134">Tensor</span><span class="sxs-lookup"><span data-stu-id="71dde-134">Tensor</span></span> | <span data-ttu-id="71dde-135">Tipo</span><span class="sxs-lookup"><span data-stu-id="71dde-135">Kind</span></span> | <span data-ttu-id="71dde-136">Dimensions</span><span class="sxs-lookup"><span data-stu-id="71dde-136">Dimensions</span></span> | <span data-ttu-id="71dde-137">Recuentos de dimensiones admitidos</span><span class="sxs-lookup"><span data-stu-id="71dde-137">Supported dimension counts</span></span> | <span data-ttu-id="71dde-138">Tipos de datos admitidos</span><span class="sxs-lookup"><span data-stu-id="71dde-138">Supported data types</span></span> |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| <span data-ttu-id="71dde-139">InputTensor</span><span class="sxs-lookup"><span data-stu-id="71dde-139">InputTensor</span></span> | <span data-ttu-id="71dde-140">Entrada</span><span class="sxs-lookup"><span data-stu-id="71dde-140">Input</span></span> | <span data-ttu-id="71dde-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span><span class="sxs-lookup"><span data-stu-id="71dde-141">{ BatchCount, InputChannelCount, InputHeight, InputWidth }</span></span> | <span data-ttu-id="71dde-142">4</span><span class="sxs-lookup"><span data-stu-id="71dde-142">4</span></span> | <span data-ttu-id="71dde-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="71dde-143">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |
| <span data-ttu-id="71dde-144">OutputTensor</span><span class="sxs-lookup"><span data-stu-id="71dde-144">OutputTensor</span></span> | <span data-ttu-id="71dde-145">Resultados</span><span class="sxs-lookup"><span data-stu-id="71dde-145">Output</span></span> | <span data-ttu-id="71dde-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span><span class="sxs-lookup"><span data-stu-id="71dde-146">{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }</span></span> | <span data-ttu-id="71dde-147">4</span><span class="sxs-lookup"><span data-stu-id="71dde-147">4</span></span> | <span data-ttu-id="71dde-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span><span class="sxs-lookup"><span data-stu-id="71dde-148">FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8</span></span> |


## <a name="requirements"></a><span data-ttu-id="71dde-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="71dde-149">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="71dde-150">**Header**</span><span class="sxs-lookup"><span data-stu-id="71dde-150">**Header**</span></span> | <span data-ttu-id="71dde-151">directml.h</span><span class="sxs-lookup"><span data-stu-id="71dde-151">directml.h</span></span> |