---
UID: NS:directml.DML_NONZERO_COORDINATES_OPERATOR_DESC
title: DML_NONZERO_COORDINATES_OPERATOR_DESC
description: Calcula las coordenadas de N dimensiones de todos los elementos distintos de cero de la tensores de entrada.
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
ms.openlocfilehash: a662ac3b341c07e512e11dcc15cbc9b11ec5f405
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721272"
---
# <a name="dml_nonzero_coordinates_operator_desc-structure-directmlh"></a>DML_NONZERO_COORDINATES_OPERATOR_DESC estructura (directml. h)

Calcula las coordenadas de N dimensiones de todos los elementos distintos de cero de la tensores de entrada.

Este operador genera una matriz de valores de MxN, donde cada fila M contiene una coordenada de N dimensiones de un valor distinto de cero de la entrada. Al usar entradas **FLOAT32** o **FLOAT16** , tanto 0 como positivos (0,0 f y-0.0 f) se tratan como cero para los fines de este operador.

El operador requiere que el valor de *OutputCoordinatesTensor* tenga un tamaño lo suficientemente grande como para dar cabida a un escenario en el peor de los casos, en el que cada elemento de la entrada es distinto de cero. Este operador devuelve el recuento de elementos distintos de cero a través de *OutputCountTensor*, que los llamadores pueden inspeccionar para determinar el número de coordenadas escritas en *OutputCoordinatesTensor*.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Una tensores de entrada.

`OutputCountTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene el recuento de elementos distintos de cero en el tensores de entrada. Este tensores debe ser un escalar &mdash; , es decir, los tamaños de este tensores deben ser todos 1. El tipo de este tensores debe ser **UINT32**.

`OutputCoordinatesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida que contiene las coordenadas de N dimensiones de los elementos de entrada que son distintos de cero. 

Este tensores debe tener *tamaños* de `{1,1,M,N}` (si *DimensionCount* es 4) o `{1,1,1,M,N}` (si *DimensionCount* es 5), donde M es el número total de elementos de la *InputTensor* y N es mayor o igual que la *clasificación efectiva* de *InputTensor*, hasta el *DimensionCount* de la entrada.

El rango efectivo de un tensores viene determinado por el *DimensionCount* de ese tensores excluyendo las dimensiones iniciales del tamaño 1. Por ejemplo, un tensores con tamaños de `{1,2,3,4}` tiene una clasificación 3 efectiva, como un tensores con tamaños de `{1,1,5,5,5}` . Un tensores con tamaños `{1,1,1,1}` tiene una clasificación 0 efectiva.

Considere un *InputTensor* con *tamaños* de `{1,1,12,5}` . Este tensores de entrada contiene 60 elementos y tiene un rango efectivo de 2. En este ejemplo, todos los tamaños válidos de *OutputCoordinatesTensor* tienen el formato `{1,1,60,N}` , donde N >= 2 pero no mayor que *DimensionCount* (4 en este ejemplo).

Se garantiza que las coordenadas escritas en este tensores se ordenan por índice de elemento ascendente. Por ejemplo, si la tensores de entrada tiene 3 valores distintos de cero en las coordenadas {1,0} , {1,2} y {0,5} , los valores escritos en *OutputCoordinatesTensor* serán `[[0,5], [1,0], [1,2]]` .

Aunque esta tensores requiere que la dimensión M sea igual al número de elementos de la tensores de entrada, este operador solo escribirá un máximo de elementos OutputCount en este tensores. El OutputCount se devuelve a través del *OutputCountTensor* escalar.

> [!NOTE]
> Los elementos restantes de este tensores más allá de OutputCount no se definen una vez que se completa este operador. No debe basarse en los valores de estos elementos.

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
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputTensor*, *OutputCoordinatesTensor* y `OutputCountTensor` deben tener el mismo *DimensionCount*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | {[D0], D1, D2, D3, D4} | de 4 a 5 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputCountTensor | Output | {[1], 1, 1, 1, 1} | de 4 a 5 | UINT32 |
| OutputCoordinatesTensor | Output | {[1], 1, 1, M, N} | de 4 a 5 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |