---
UID: NS:directml.DML_TOP_K1_OPERATOR_DESC
title: DML_TOP_K1_OPERATOR_DESC
description: Selecciona los elementos *K* más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente.
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
ms.openlocfilehash: 599541032e0f1711c0e747a4ca5906391849a932
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803822"
---
# <a name="dml_top_k1_operator_desc-structure-directmlh"></a>DML_TOP_K1_OPERATOR_DESC estructura (directml.h)
Selecciona los elementos *K* más grandes o más pequeños de cada secuencia a lo largo de un eje de *InputTensor* y devuelve los valores e índices de esos elementos en *OutputValueTensor* y *OutputIndexTensor*, respectivamente. Una *secuencia* hace referencia a uno de los conjuntos de elementos que existen a lo largo de la dimensión *Eje* de *InputTensor*.

La elección de si se seleccionan los elementos K más grandes o los elementos K más pequeños se puede controlar mediante *AxisDirection*.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

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

Tensor de entrada que contiene los elementos que se deben seleccionar.

`OutputValueTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los valores de los *elementos K* principales. Los elementos *K* principales se seleccionan en función de si son los más grandes o más pequeños, dependiendo del valor *de AxisDirection.* Este tensor debe tener tamaños iguales a *InputTensor* *,* excepto para la dimensión especificada por el parámetro *Axis,* que debe tener un tamaño igual a *K*.

Se *garantiza que* los valores K seleccionados de cada secuencia de entrada se ordenan de manera descendente (de mayor a [menor)](./ne-directml-dml_axis_direction.md)si *AxisDirection* DML_AXIS_DIRECTION_DECREASING . De lo contrario, lo contrario es true y se garantiza que los valores seleccionados se ordenan de forma ascendente (menor a mayor).

`OutputIndexTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los índices de los *elementos K* superiores. Este tensor debe tener tamaños iguales a *InputTensor* *,* excepto para la dimensión especificada por el parámetro *Axis,* que debe tener un tamaño igual a *K*.

Los índices devueltos en este tensor se miden con respecto al principio de su secuencia (en lugar del principio del tensor). Por ejemplo, un índice de 0 siempre hace referencia al primer elemento para todas las secuencias de un eje.

En los casos en los que dos o más elementos de la K superior tienen el mismo valor (es decir, cuando hay una vinculación), se incluyen los índices de ambos elementos y se garantiza que se ordenan por índice de elemento ascendente. Tenga en cuenta que esto es cierto independientemente del valor de *AxisDirection.*

`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Índice de la dimensión en la que se seleccionan los elementos. Este valor debe ser menor que *DimensionCount* de *InputTensor.*

`K`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de elementos que se seleccionan. *K* debe ser mayor que 0, pero menor que el número de elementos de *InputTensor* a lo largo de la dimensión especificada por *Eje*.

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Valor de la [enumeración DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) datos. Si se establece **en DML_AXIS_DIRECTION_INCREASING**, este operador devuelve *los* elementos *K* más pequeños en orden de valor creciente. De lo contrario, devuelve *los elementos* *K más grandes* en orden decreciente.

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

### <a name="example-2-using-a-different-axis"></a>Ejemplo 2. Uso de un eje diferente

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

### <a name="example-3-tied-values"></a>Ejemplo 3. Valores vinculados

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

### <a name="example-4-increasing-axis-direction"></a>Ejemplo 4. Aumentar la dirección del eje

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
Cuando *AxisDirection* se establece [en DML_AXIS_DIRECTION_DECREASING](./ne-directml-dml_axis_direction.md), este operador es equivalente a [DML_TOP_K_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_top_k_operator_desc).

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor

* *InputTensor,* *OutputIndexTensor y* *OutputValueTensor* deben tener el mismo *dimensioncount*.
* *InputTensor* y *OutputValueTensor* deben tener el mismo *datatype*.

## <a name="tensor-support"></a>Compatibilidad con Tensor

### <a name="dml_feature_level_3_1-and-above"></a>DML_FEATURE_LEVEL_3_1 y posteriores

| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Resultados | De 1 a 8 | UINT32 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores

| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputValueTensor | Resultados | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputIndexTensor | Resultados | 4 | UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
