---
UID: NS:directml.DML_GATHER_ND1_OPERATOR_DESC
title: DML_GATHER_ND1_OPERATOR_DESC
description: Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a todos los subbloqueos de la entrada. | DML_GATHER_ND1_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND1_OPERATOR_DESC
- DML_GATHER_ND1_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_GATHER_ND1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_GATHER_ND1_OPERATOR_DESC, DML_GATHER_ND1_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
- directml/DML_GATHER_ND1_OPERATOR_DESC
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
- DML_GATHER_ND1_OPERATOR_DESC
ms.openlocfilehash: b92c8aece88d8466357bb8e48fd3ce5a3b73d2e3
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107802857"
---
# <a name="dml_gather_nd1_operator_desc-structure-directmlh"></a>DML_GATHER_ND1_OPERATOR_DESC estructura (directml.h)

Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a todos los subbloqueos de la entrada. Este operador realiza el pseudocódigo siguiente, donde "..." representa una serie de coordenadas, con el comportamiento exacto dependiente del recuento de dimensiones de lote, entrada e índices.

```
output[batch, ...] = input[batch, indices[batch, ...], ...]
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_GATHER_ND1_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* IndicesTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT InputDimensionCount;
  UINT IndicesDimensionCount;
  UINT BatchDimensionCount;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor del que se leerá.

`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los índices. DimensionCount *de* este tensor debe coincidir *con InputTensor.DimensionCount.* La última dimensión de *IndicesTensor* es realmente el número de coordenadas por tupla de índice y no puede superar *InputTensor.DimensionCount*. Por ejemplo, un tensor de índices de *tamaños* con ÍndicesDimensionCount = 3 significa una matriz 4x5 de tuplas de dos coordenadas que se indexan en `{1,4,5,2}`  *InputTensor*.

A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor. Los índices negativos se interpretan como relativos al final de la dimensión correspondiente. Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. DimensionCount *y* *DataType de* este tensor deben coincidir *con InputTensor.DimensionCount.* Los *outputTensor.Sizes esperados* son la concatenación de los segmentos iniciales *IndicesTensor.Sizes* y *inputTensor.Sizes,* que produce lo siguiente.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Las dimensiones están alineadas a la derecha, con 1 valor inicial anteponer si es necesario para satisfacer *OutputTensor.DimensionCount*.

Aquí tiene un ejemplo.

```
InputTensor.Sizes = {3,4,5,6,7}
InputDimensionCount = 5
IndicesTensor.Sizes = {1,1, 1,2,3}
IndicesDimensionCount = 3 // can be thought of as a {1,2} array of 3-coordinate tuples

// The {1,2} comes from the indices tensor (ignoring last dimension which is the tuple size),
// and the {6,7} comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
OutputTensor.Sizes = {1, 1,2,6,7}
```

`InputDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las iniciales irrelevantes, que abarcan `[1, *InputTensor.DimensionCount*]` . Por ejemplo, *dados InputTensor.Sizes*  =  `{1,1,4,6}` y = `InputDimensionCount` 3, los índices significativos reales son `{1,4,6}` .

`IndicesDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las iniciales irrelevantes, que abarcan [1, *IndicesTensor.DimensionCount*]. Por ejemplo, *dados IndicesTensor.Sizes* e  =  `{1,1,4,6}` *IndicesDimensionCount* = 3, los índices significativos reales son `{1,4,6}` .

`BatchDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones dentro de cada tensor (*InputTensor*, *IndicesTensor*, *OutputTensor*) que se consideran lotes independientes, que abarcan [0, *InputTensor.DimensionCount*) y [0, *IndicesTensor.DimensionCount*). El número de lotes puede ser 0, lo que implica un único lote. Por ejemplo, *dados IndicesTensor.Sizes* y  =  `{1,3,4,5,6,7}` *IndicesDimensionCount* = 5 y = 2, hay lotes e índices `BatchDimensionCount` `{3,4}` `{5,6,7}` significativos.

## <a name="remarks"></a>Observaciones
**DML_GATHER_ND1_OPERATOR_DESC** agrega *BatchDimensionCount* y equivale a [DML_GATHER_ND_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_gather_nd_operator_desc) cuando *BatchDimensionCount* = 0.

## <a name="examples"></a>Ejemplos

### <a name="example-1-1d-remapping"></a>Ejemplo 1. Remapping 1D

```
InputDimensionCount: 2
IndicesDimensionCount: 2
BatchDimensionCount: 0

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping-with-batch-count"></a>Ejemplo 2. Remapping 2D with batch count (Remapping 2D con recuento de lotes)

```
InputDimensionCount: 3
IndicesDimensionCount: 3
BatchDimensionCount: 1

// 3 batches.
InputTensor: (Sizes:{1, 3,2,2}, DataType:FLOAT32)
    [
        [[[0,1],[2,3]],   // batch 0
         [[4,5],[6,7]],   // batch 1
         [[8,9],[10,11]]] // batch 2
    ]

// A 3x2 array of 2D tuples indexing into InputTensor.
// e.g. a tuple of <1,0> in batch 1 corresponds to input value 6.
IndicesTensor: (Sizes:{1, 3,2,2}, DataType:UINT32)
    [
        [[[0,0],[1,1]],
         [[1,1],[0,0]],
         [[0,1],[1,0]]]
    ]

// output[batch, x] = input[batch, indices[batch, x, 0], indices[batch, x, 1]]
OutputTensor: (Sizes:{1,1, 3,2}, DataType:FLOAT32)
    [[
        [[0,3],
         [7,4],
         [9,10]]
    ]]
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *IndicesTensor,* *InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*
* *InputTensor* y *OutputTensor* deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | De 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
