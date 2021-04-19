---
UID: NS:directml.DML_SCATTER_ND_OPERATOR_DESC
title: DML_SCATTER_ND_OPERATOR_DESC (DML_SCATTER_ELEMENTS_OPERATOR_DESC)
description: Copia todo el tensores de entrada en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes de la tensores de actualizaciones.
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
ms.openlocfilehash: ae9a3022a7070bbf0253e71550f2ca1ceced6768
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721297"
---
# <a name="dml_scatter_nd_operator_desc-structure-directmlh"></a>DML_SCATTER_ND_OPERATOR_DESC estructura (directml. h)
Copia todo el tensores de entrada en la salida y, a continuación, sobrescribe los índices seleccionados con los valores correspondientes de la tensores de actualizaciones. Este operador realiza el siguiente pseudocódigo, donde "..." representa una serie de coordenadas, con el comportamiento exacto determinado por el tamaño del eje y de los índices.

```
output = input
output[indices[...]] = updates[...]
```

Si dos índices de elementos de salida se superponen (que no son válidos), no hay ninguna garantía de la última escritura que gana.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores del que se va a leer.


`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los índices. El *DimensionCount* de este tensores debe coincidir con *InputTensor. DimensionCount*. La última dimensión de *IndicesTensor* es en realidad el número de coordenadas por tupla de índice y no debe supera *InputTensor. DimensionCount*. Por ejemplo, un tensores de índices de tamaño `{1,4,5,2}` con *IndicesDimensionCount* = 3 significa una matriz 4x5 de tuplas de coordenadas de dos valores que indexan en *InputTensor*.

A partir de `DML_FEATURE_LEVEL_3_0` , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensores. Los índices negativos se interpretan como en relación con el final de la dimensión respectiva. Por ejemplo, un índice de-1 hace referencia al último elemento a lo largo de esa dimensión.


`UpdatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los nuevos valores para reemplazar los valores de entrada existentes en los índices correspondientes. El *DimensionCount* de este tensores debe coincidir con *InputTensor. DimensionCount*. El *UpdatesTensor esperado. los tamaños* son la concatenación de los segmentos iniciales *IndicesTensor. Sizes* y *InputTensor. Sizes* final para producir lo siguiente.

```
indexTupleSize = IndicesTensor.Sizes[IndicesTensor.DimensionCount - 1]
UpdatesTensor.Sizes = [
    1...,
    IndicesTensor.Sizes[(IndicesTensor.DimensionCount - IndicesDimensionCount) .. (IndicesTensor.DimensionCount - 1)],
    InputTensor.Sizes[(InputTensor.DimensionCount - indexTupleSize) .. InputTensor.DimensionCount]
]
```

Las dimensiones están alineadas a la derecha, con un valor inicial de 1 delante, si es necesario, para satisfacer *UpdatesTensor. DimensionCount*.

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

Tensores en el que se van a escribir los resultados. Los *tamaños* y el *tipo* de los tipos de tensores deben coincidir con *InputTensor. Sizes*.


`InputDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de dimensiones de entrada reales dentro de *InputTensor* después de omitir cualquier otro que sea irrelevante, que oscila entre [1, *InputTensor. DimensionCount*). Por ejemplo, dado *InputTensor. Sizes* = {1,1,4,6} y *InputDimensionCount* = 3, los índices significativos reales son {1,4,6} .


`IndicesDimensionCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de dimensiones de índice reales dentro de *IndicesTensor* después de omitir cualquier otro que sea irrelevante, que oscila entre [1, *IndicesTensor. DimensionCount*). Por ejemplo, dado *IndicesTensor. Sizes* = {1,1,4,6} y *IndicesDimensionCount* = 3, los índices significativos reales son {1,4,6} .

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
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *IndicesTensor*, *InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *DimensionCount*.
* *InputTensor*, *OutputTensor* y `UpdatesTensor` deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | de 1 a 8 | INT64, INT32, UINT64, UINT32 |
| UpdatesTensor | Entrada | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y versiones posteriores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| IndicesTensor | Entrada | 4 | UINT32 |
| UpdatesTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |