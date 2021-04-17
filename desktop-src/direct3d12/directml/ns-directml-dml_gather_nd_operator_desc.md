---
UID: NS:directml.DML_GATHER_ND_OPERATOR_DESC
title: DML_GATHER_ND_OPERATOR_DESC
description: Recopila elementos de la tensores de entrada, mediante los índices tensores para reasignar los índices a subbloqueos completos de la entrada. | DML_GATHER_ND_OPERATOR_DESC
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
ms.openlocfilehash: 6a48fd19621bed100a13412dbb1992974d125323
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105721417"
---
# <a name="dml_gather_nd_operator_desc-structure-directmlh"></a>DML_GATHER_ND_OPERATOR_DESC estructura (directml. h)

Recopila elementos de la tensores de entrada, mediante los índices tensores para reasignar los índices a subbloqueos completos de la entrada. Este operador realiza el siguiente pseudocódigo, donde "..." representa una serie de coordenadas, con el comportamiento exacto que depende del número de dimensiones de entrada e índices.

```
output[...] = input[indices[...]]
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores del que se va a leer.


`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los índices. El *DimensionCount* de este tensores debe coincidir con *InputTensor. DimensionCount*. La última dimensión de *IndicesTensor* es en realidad el número de coordenadas por tupla de índice y no puede superar *InputTensor. DimensionCount*. Por ejemplo, un índice tensores de *tamaños* `{1,4,5,2}` con *IndicesDimensionCount* = 3 significa una matriz 4x5 de tuplas de 2 coordenadas que indexan en *InputTensor*.

A partir de `DML_FEATURE_LEVEL_3_0` , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensores. Los índices negativos se interpretan como en relación con el final de la dimensión respectiva. Por ejemplo, un índice de-1 hace referencia al último elemento a lo largo de esa dimensión.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los resultados. *DimensionCount* y *DataType* de este tensores deben coincidir con *InputTensor. DimensionCount*. El *OutputTensor esperado. los tamaños* son la concatenación de los segmentos de *IndicesTensor. Sizes* iniciales y *InputTensor. Sizes* final del segmento que se va a producir:

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
OutputTensor.Sizes = {
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
}
```

Las dimensiones de salida están alineadas a la derecha, con un valor inicial de 1 delante, si es necesario, para satisfacer hasta *OutputTensor. DimensionCount*.

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

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las principales que no son relevantes, que van `[1, *InputTensor.DimensionCount*]` . Por ejemplo, dado *InputTensor. Sizes*  =  `{1,1,4,6}` y `InputDimensionCount` = 3, los índices significativos reales son `{1,4,6}` .


`IndicesDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las principales que no sean importantes, que abarcan [1, *IndicesTensor. DimensionCount*]. Por ejemplo, dado *IndicesTensor. Sizes*  =  `{1,1,4,6}` y *IndicesDimensionCount* = 3, los índices significativos reales son `{1,4,6}` .

## <a name="examples"></a>Ejemplos

### <a name="example-1-1d-remapping"></a>Ejemplo 1. reasignación 1D

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

### <a name="example-2-2d-remapping"></a>Ejemplo 2. reasignación 2D

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


## <a name="remarks"></a>Observaciones
Se presentó una versión más reciente de este operador, `DML_OPERATOR_GATHER_ND1` , en `DML_FEATURE_LEVEL_3_0` .

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *IndicesTensor*, *InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.
* *InputTensor* y *OutputTensor* deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | de 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Output | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 4 | UINT32 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |
