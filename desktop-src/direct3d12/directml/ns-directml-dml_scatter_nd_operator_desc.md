---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia el tensor de entrada completo en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes del tensor de actualizaciones.
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
- DML_SCATTER_ND_OPERATOR_DESC
f1_keywords:
- DML_SCATTER_ND_OPERATOR_DESC
- directml/DML_SCATTER_ND_OPERATOR_DESC
ms.openlocfilehash: 6c987e01862d849c6215a2d25fe957ef0a22e7af
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803983"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>DML_SCATTER_ND_OPERATOR_DESC estructura (directml.h)
Copia el tensor de entrada completo en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes del tensor de actualizaciones. Este operador realiza el pseudocódigo siguiente, donde "..." representa una serie de coordenadas, con el comportamiento exacto determinado por el tamaño del eje y los índices.

```
output = input
output[indices[...]] = updates[...]
```

Si dos índices de elementos de salida se superponen (lo que no es válido), no hay ninguna garantía de cuál gana la última escritura.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_SCATTER_ND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *UpdatesTensor;
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

Tensor que contiene los índices. DimensionCount *de* este tensor debe coincidir *con InputTensor.DimensionCount.* La última dimensión de *IndicesTensor* es realmente el número de coordenadas por tupla de índice y no debe superar *InputTensor.DimensionCount.* Por ejemplo, un tensor de índices de tamaño `{1,4,5,2}` *con IndicesDimensionCount* = 3 significa una matriz 4x5 de tuplas de coordenadas de 2 valores que se indexan en *InputTensor*.

A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor. Los índices negativos se interpretan como relativos al final de la dimensión respectiva. Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.


`UpdatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los nuevos valores para reemplazar los valores de entrada existentes en los índices correspondientes. DimensionCount *de* este tensor debe coincidir *con InputTensor.DimensionCount.* Los valores *esperados de UpdatesTensor.Sizes* son la concatenación de los segmentos iniciales *IndicesTensor.Sizes* y *inputTensor.Sizes* para producir lo siguiente.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

Las dimensiones están alineadas a la derecha, con 1 valor inicial anteponer si es necesario para satisfacer *UpdatesTensor.DimensionCount*.

Aquí tiene un ejemplo.

```
InputTensor.Sizes = [3,4,5,6,7]
InputDimensionCount = 5
IndicesTensor.Sizes = [1,1, 1,2,3]
IndicesDimensionCount = 3 // can be thought of as a [1,2] array of 3-coordinate tuples

// The [1,2] comes from the indices tensor (ignoring last dimension, which is the tuple size),
// and the [6,7] comes from input tensor, ignoring the first 3 dimensions
// since the index tuples are 3 elements (from the indices tensor last dimension).
UpdatesTensor.Sizes = [1, 1,2,6,7]
```


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Los *tamaños* y *datatype* de este tensor deben coincidir *con InputTensor.Sizes.*


`InputDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones de entrada reales dentro de *InputTensor* después de omitir las iniciales irrelevantes, que abarcan [1, *InputTensor.DimensionCount*). Por ejemplo, *dados InputTensor.Sizes* = {1,1,4,6} y *InputDimensionCount* = 3, los índices significativos reales son {1,4,6} .


`IndicesDimensionCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir las iniciales irrelevantes, que abarcan [1, *IndicesTensor.DimensionCount*). Por ejemplo, *dados IndicesTensor.Sizes* = {1,1,4,6} e *IndicesDimensionCount* = 3, los índices significativos reales son {1,4,6} .

## <a name="examples"></a>Ejemplos

```
InputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 2, 3, 4, 5, 6, 7, 8]

IndicesTensor: (Sizes:{4,1}, DataType:FLOAT32)
    [[4], [3], [1], [7]]

UpdatesTensor: (Sizes:{4}, DataType:FLOAT32)
    [9, 10, 11, 12]

// output = input
// output[indices[x, 0]] = updates[x]
OutputTensor: (Sizes:{8}, DataType:FLOAT32)
    [1, 11, 3, 10, 9, 6, 7, 12]
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *IndicesTensor*, *InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *DimensionCount.*
* *InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | De 1 a 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | 4 | UINT32 |
| UpdatesTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |