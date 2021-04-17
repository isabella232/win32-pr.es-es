---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Selecciona los *K* elementos más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente.
helpviewer_keywords:
- DML_TOP_K1_OPERATOR_DESC
- DML_TOP_K1_OPERATOR_DESC structure
- direct3d12.dml_top_k1_operator_desc
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
- directml/DML_TOP_K1_OPERATOR_DESC
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
- DML_TOP_K1_OPERATOR_DESC
ms.openlocfilehash: 8c5b9bf58a8582588d19878c7e06c602584777fa
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721267"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>DML_TOP_K1_OPERATOR_DESC estructura (directml. h)
Selecciona los *K* elementos más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente. Una *secuencia* hace referencia a uno de los conjuntos de elementos que existen a lo largo de la dimensión de *eje* de *InputTensor*.

La elección de si se seleccionan los K elementos mayores o los K más pequeños se pueden controlar mediante *AxisDirection*.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_TOP_K1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputValueTensor;
  const DML_TENSOR_DESC *OutputIndexTensor;
  UINT                  Axis;
  UINT                  K;
  DML_AXIS_DIRECTION    AxisDirection;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de entrada que contiene los elementos que se van a seleccionar.


`OutputValueTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida en la que se van a escribir los valores de los *K* elementos superiores. Los *K* elementos superiores se seleccionan en función de si son el más grande o el más pequeño, en función del valor de *AxisDirection*. Este tensores debe tener tamaños iguales a *InputTensor*, *salvo* la dimensión especificada por el parámetro de *eje* , que debe tener un tamaño igual a *K*.

Se garantiza que los valores *K* seleccionados de cada secuencia de entrada están ordenados en orden descendente (de mayor a menor) si *AxisDirection* es [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md). De lo contrario, el contrario es true y se garantiza que los valores seleccionados están ordenados de forma ascendente (de menor a mayor).


`OutputIndexTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

La salida tensores para escribir los índices de los *K* elementos superiores en. Este tensores debe tener tamaños iguales a *InputTensor*, *salvo* la dimensión especificada por el parámetro de *eje* , que debe tener un tamaño igual a *K*.

Los índices devueltos en este tensores se miden en relación con el principio de su secuencia (en oposición al principio del tensores). Por ejemplo, un índice de 0 siempre hace referencia al primer elemento de todas las secuencias de un eje.

En los casos en que dos o más elementos de la parte superior-K tienen el mismo valor (es decir, cuando hay una empate), se incluyen los índices de ambos elementos y se garantiza que se ordenen por índice de elemento ascendente. Tenga en cuenta que esto es así independientemente del valor de *AxisDirection*.


`Axis`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Índice de la dimensión de la que se van a seleccionar elementos. Este valor debe ser menor que el valor de *DimensionCount* de *InputTensor*.


`K`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Número de elementos que se van a seleccionar. *K* debe ser mayor que 0, pero menor que el número de elementos de *InputTensor* a lo largo de la dimensión especificada por *AXIS*.


`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Un valor de la enumeración [DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) . Si se establece en **DML_AXIS_DIRECTION_INCREASING**, este operador devuelve los *K* elementos *más pequeños* en orden de valor creciente. De lo contrario, devuelve los *K* elementos *mayores* en orden decreciente.

## <a name="examples"></a>Ejemplos

### <a name="example-1"></a>Ejemplo 1

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 3
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,2}, DataType:FLOAT32)
[[[[11, 10],
   [ 9,  8],
   [ 7,  6]]]]

OutputIndexTensor: (Sizes:{1,1,3,2}, DataType:UINT32)
[[[[3, 2],
   [2, 3],
   [3, 2]]]]
```

### <a name="example-2-using-a-different-axis"></a>Ejemplo 2. Usar un eje diferente

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 0,  1, 10, 11],
   [ 3,  2,  9,  8],
   [ 4,  5,  6,  7]]]]

Axis: 2
K:    2
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,2,4}, DataType:FLOAT32)
[[[[ 4,  5, 10, 11],
   [ 3,  2,  9,  8]]]]

OutputIndexTensor: (Sizes:{1,1,2,4}, DataType:UINT32)
[[[[2, 2, 0, 0],
   [1, 1, 1, 1]]]]
```

### <a name="example-3-tied-values"></a>Ejemplo 3. Valores enlazados

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[3, 2, 2],
   [5, 5, 4],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[3, 1, 2],
   [2, 3, 1],
   [0, 1, 2]]]]
```

### <a name="example-4-increasing-axis-direction"></a>Ejemplo 4: Aumentar la dirección del eje

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2, 2, 3],
   [3, 4, 5, 5],
   [6, 6, 6, 6]]]]

Axis: 3
K:    3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
   
OutputValueTensor: (Sizes:{1,1,3,3}, DataType:FLOAT32)
[[[[1, 2, 2],
   [3, 4, 5],
   [6, 6, 6]]]]

OutputIndexTensor: (Sizes:{1,1,3,3}, DataType:UINT32)
[[[[0, 1, 2],
   [0, 1, 2],
   [0, 1, 2]]]]
```


## <a name="remarks"></a>Observaciones
Cuando *AxisDirection* se establece en [DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), este operador es equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *InputTensor* y *OutputValueTensor* deben tener el mismo *tipo de texto*.
* *OutputIndexTensor* y *OutputValueTensor* deben tener el mismo *tamaño*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | { In0, In1, In2, In3 } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Output | { Out0, Out1, Out2, Out3 } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Output | { Out0, Out1, Out2, Out3 } | 4 | UINT32 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |