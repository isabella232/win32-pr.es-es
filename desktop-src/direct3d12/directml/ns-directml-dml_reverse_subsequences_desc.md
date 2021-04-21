---
UID: NS:directml.DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
title: DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
description: Invierte los elementos de una o varias *subsecuencias* de un tensor. El conjunto de subsecuencias que se va a invertir se elige en función de las longitudes de eje y secuencia proporcionadas.
helpviewer_keywords:
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC structure
- direct3d12.dml_reverse_subsequences_operator_desc
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
- directml/DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
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
- DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC
ms.openlocfilehash: 3deddea3d60db1a8689ceabfac92ff17393b7606
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804000"
---
# <a name="dml_reverse_subsequences_operator_desc-structure-directmlh"></a>DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC estructura (directml.h)
Invierte los elementos de una o varias *subsecuencias* de un tensor. El conjunto de subsecuencias que se va a invertir se elige en función de las longitudes de eje y secuencia proporcionadas.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_REVERSE_SUBSEQUENCES_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *SequenceLengthsTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada que contiene los elementos que se invertirán.


`SequenceLengthsTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensor que contiene un valor para cada subsecuencia que se va a invertir, que indica la longitud de los elementos de esa subsecuencia. Solo se invierten los elementos dentro de la longitud de la subsecuencia; Los elementos restantes a lo largo de ese eje se copian en la salida sin cambios.

Este tensor debe tener un recuento de dimensiones  y tamaños iguales a *InputTensor,* excepto para la dimensión especificada por el *parámetro Axis.* El tamaño de la *dimensión Eje* debe ser 1. Por ejemplo, si *InputTensor* tiene tamaños de y Eje es 1, los tamaños de `{2,3,4,5}` *SequenceLengthsTensor* deben ser  `{2,1,4,5}` .

Si la longitud de una subsecuencia supera el número máximo de elementos a lo largo de ese eje, este operador se comporta como si el valor se fijara al máximo.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados. Este tensor debe tener los mismos tamaños y tipo de datos que *InputTensor.*


`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Índice de la dimensión sobre la que se invertirán los elementos. Este valor debe ser menor que dimensionCount de *InputTensor.*

## <a name="examples"></a>Ejemplos

### <a name="example-1"></a>Ejemplo 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,3,1}, DataType:UINT32)
[[[[2],
   [4],
   [3]]]]

Axis: 3

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  4],
   [ 8,  7,  6,  5],
   [11, 10,  9, 12]]]]
```

### <a name="example-2-reversing-along-a-different-axis"></a>Ejemplo 2. Invertir a lo largo de un eje diferente

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1,  2,  3,  4],
   [5,  6,  7,  8],
   [9, 10, 11, 12]]]]
   
SequenceTensor: (Sizes:{1,1,1,4}, DataType:UINT32)
[[[[2, 3, 1, 0]]]]

Axis: 2

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[5, 10,  3,  4], // Notice that sequence lengths of 1 and 0 are effective nops
   [1,  6,  7,  8],
   [9,  2, 11, 12]]]]
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
* *InputTensor*, *OutputTensor* y *SequenceLengthsTensor* deben tener el mismo *dimensioncount*.
* *InputTensor* y *OutputTensor* deben tener el mismo *tipo de datos*.

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| SequenceLengthsTensor | Entrada | De 4 a 5 | UINT32 |
| OutputTensor | Resultados | De 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| SequenceLengthsTensor | Entrada | 4 | UINT32 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |