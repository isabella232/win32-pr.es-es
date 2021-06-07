---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a los subbloques completos de la entrada. | DML_GATHER_ND_OPERATOR_DESC
helpviewer_keywords:
- DML_GATHER_ND_OPERATOR_DESC
- DML_GATHER_ND_OPERATOR_DESC structure
- direct3d12.dml_gather_nd_operator_desc
- directml/DML_GATHER_ND_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/31/2020
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
- DML_GATHER_ND_OPERATOR_DESC
- directml/DML_GATHER_ND_OPERATOR_DESC
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
- DML_GATHER_ND_OPERATOR_DESC
ms.openlocfilehash: 8e74078eaf55f209fba92ba97737d22047a5e67c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417979"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>DML_GATHER_ND_OPERATOR_DESC estructura (directml.h)

Recopila elementos del tensor de entrada, usando el tensor de índices para reasignar índices a los subbloques completos de la entrada. Este operador realiza el pseudocódigo siguiente, donde "..." representa una serie de coordenadas, con el comportamiento exacto dependiente del recuento de dimensiones de entrada e índices.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_GATHER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  InputDimensionCount;
  UINT                  IndicesDimensionCount;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor del que se leerá.


`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los índices. DimensionCount de este tensor debe coincidir *con InputTensor.DimensionCount.*  La última dimensión de *IndicesTensor* es realmente el número de coordenadas por tupla de índice y no puede superar *InputTensor.DimensionCount*. Por ejemplo, un tensor de índices de *tamaños* con ÍndicesDimensionCount = 3 significa una matriz 4x5 de tuplas de dos coordenadas que indexan en `{1,4,5,2}`  *InputTensor*.

A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor. Los índices negativos se interpretan como relativos al final de la dimensión respectiva. Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. DimensionCount *y* *DataType de* este tensor deben coincidir *con InputTensor.DimensionCount.* Los *outputTensor.Sizes esperados* son la concatenación de los segmentos iniciales *IndicesTensor.Sizes* y *inputTensor.Sizes* para producir:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Las dimensiones de salida están alineadas a la derecha, con 1 valor inicial anteponer si es necesario para satisfacer hasta *OutputTensor.DimensionCount*.

Este es un ejemplo.

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

Número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las iniciales irrelevantes, que van [1, *IndicesTensor.DimensionCount*]. Por ejemplo, *dados IndicesTensor.Sizes* e  =  `{1,1,4,6}` *IndicesDimensionCount* = 3, los índices significativos reales son `{1,4,6}` .

## <a name="examples"></a>Ejemplos

### <a name="example-1-1d-remapping"></a>Ejemplo 1. Remapping 1D

```
InputDimensionCount: 2
IndicesDimensionCount: 2

InputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[0,1],[2,3]]

IndicesTensor: (Sizes:{2,1}, DataType:UINT32)
    [[1],[0]]

// output[y, x] = input[indices[y], x]
OutputTensor: (Sizes:{2,2}, DataType:FLOAT32)
    [[2,3],[0,1]]
```

### <a name="example-2-2d-remapping"></a>Ejemplo 2. Remapping 2D

```
InputDimensionCount: 3
IndicesDimensionCount: 2

InputTensor: (Sizes:{1, 2,2,2}, DataType:FLOAT32)
    [ [[[0,1],[2,3]],[[4,5],[6,7]]] ]

IndicesTensor: (Sizes:{1,1, 2,2}, DataType:UINT32)
    [[ [[0,1],[1,0]] ]]

// output[y, x] = input[indices[y, 0], indices[y, 1], x]
OutputTensor: (Sizes:{1,1, 2,2}, DataType:FLOAT32)
    [[ [[2,3],[4,5]] ]]
```


## <a name="remarks"></a>Comentarios
Se introdujo una versión más reciente de este operador, `DML_OPERATOR_GATHER_ND1` , en `DML_FEATURE_LEVEL_3_0` .

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *Los índicesTensor*, *InputTensor* y *OutputTensor* deben tener el mismo *dimensioncount.*
* *InputTensor* y *OutputTensor* deben tener el mismo *tipo de datos*.

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | De 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | 4 | UINT32 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
