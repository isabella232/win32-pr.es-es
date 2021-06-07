---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Calcula las coordenadas dimensionales N de todos los elementos distintos de cero del tensor de entrada.
helpviewer_keywords:
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- DML_NONZERO_COORDINATES_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_NONZERO_COORDINATES_OPERATOR_DESC, DML_NONZERO_COORDINATES_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
- directml/DML_NONZERO_COORDINATES_OPERATOR_DESC
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
- DML_NONZERO_COORDINATES_OPERATOR_DESC
ms.openlocfilehash: 39463ba57bc90b35d5ac5dc7fc43993169137221
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417964"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>DML_NONZERO_COORDINATES_OPERATOR_DESC estructura (directml.h)

Calcula las coordenadas dimensionales N de todos los elementos distintos de cero del tensor de entrada.

Este operador genera una matriz MxN de valores, donde cada fila M contiene una coordenada de N dimensiones de un valor distinto de cero de la entrada. Cuando se usan entradas **FLOAT32** o **FLOAT16,** 0 negativo y positivo (0,0f y -0,0f) se tratan como cero para los fines de este operador.

El operador requiere que *OutputCoordinatesTensor* tenga un tamaño lo suficientemente grande como para dar cabida a un escenario en el peor de los casos en el que cada elemento de la entrada es distinto de cero. Este operador devuelve el recuento de elementos distintos de cero a través de *OutputCountTensor*, que los autores de la llamada pueden inspeccionar para determinar el número de coordenadas escritas en *OutputCoordinatesTensor*.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_NONZERO_COORDINATES_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputCountTensor;
  const DML_TENSOR_DESC* OutputCoordinatesTensor;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensor de entrada.

`OutputCountTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene el recuento de elementos distintos de cero en el tensor de entrada. Este tensor debe ser &mdash; escalar, es decir, los tamaños de este tensor deben ser 1. El tipo de este tensor debe ser **UINT32.**

`OutputCoordinatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida que contiene las coordenadas dimensionales N de los elementos de entrada que no son cero. 

Este tensor  debe tener tamaños de `{1,1,M,N}` (si *DimensionCount* es 4) o (si DimensionCount es 5), donde M es el número total de elementos de `{1,1,1,M,N}` *InputTensor* y  N  es mayor o igual que el rango efectivo de *InputTensor,* hasta *dimensioncount* de la entrada.

El rango efectivo de un tensor viene determinado por *dimensioncount* de ese tensor, excepto las dimensiones iniciales del tamaño 1. Por ejemplo, un tensor con tamaños de tiene el rango 3 efectivo, al igual que `{1,2,3,4}` un tensor con tamaños de `{1,1,5,5,5}` . Un tensor con tamaños `{1,1,1,1}` tiene el rango 0 efectivo.

Considere la *posibilidad de usar inputTensor* *con tamaños* de `{1,1,12,5}` . Este tensor de entrada contiene 60 elementos y tiene un rango efectivo de 2. En este ejemplo, todos los tamaños válidos de *OutputCoordinatesTensor* tienen el formato , donde N >= 2 pero no mayor que `{1,1,60,N}` *DimensionCount* (4 en este ejemplo).

Se garantiza que las coordenadas escritas en este tensor se ordenan por índice de elemento ascendente. Por ejemplo, si el tensor de entrada tiene 3 valores distintos de cero en las coordenadas , y , los valores escritos en {1,0} {1,2} {0,5} *OutputCoordinatesTensor* serán `[[0,5], [1,0], [1,2]]` .

Aunque este tensor requiere que su dimensión M sea igual al número de elementos del tensor de entrada, este operador solo escribirá un máximo de elementos OutputCount en este tensor. OutputCount se devuelve a través de *outputCountTensor escalar.*

> [!NOTE]
> Los elementos restantes de este tensor más allá de OutputCount no están definidos una vez que se completa este operador. No debe confiar en los valores de estos elementos.

## <a name="example"></a>Ejemplo

```
InputTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[1.0f,  0.0f, 0.0f,  2.0f],
 [-0.0f, 3.5f, 0.0f, -5.2f]]

OutputCountTensor: (Sizes:{1,1,1,1}, DataType:UINT32)
[4]

OutputCoordinatesTensor: (Sizes:{1,1,8,3}, DataType:UINT32)
[[0, 0, 0],
 [0, 0, 3],
 [0, 1, 1],
 [0, 1, 3],
 [0, 0, 0], // 
 [0, 0, 0], // Values in rows >= OutputCountTensor (4 in
 [0, 0, 0], // this case) are left undefined
 [0, 0, 0]] // 
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputTensor*, *OutputCoordinatesTensor* y `OutputCountTensor` deben tener el mismo *DimensionCount.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Dimensions | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | { [D0], D1, D2, D3, D4 } | De 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Resultados | { [1], 1, 1, 1, 1 } | De 4 a 5 | UINT32 |
| OutputCoordinatesTensor | Resultados | { [1], 1, 1, M, N } | De 4 a 5 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |