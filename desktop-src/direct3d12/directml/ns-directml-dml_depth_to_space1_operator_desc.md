---
UID: NS:directml.DML_DEPTH_TO_SPACE1_OPERATOR_DESC
title: DML_DEPTH_TO_SPACE1_OPERATOR_DESC
description: Reorganiza (permuta) los datos de profundidad en bloques de datos espaciales. El operador genera una copia del tensor de entrada donde los valores de la dimensión de profundidad se mueven en bloques espaciales a las dimensiones de alto y ancho.
helpviewer_keywords:
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC structure
- direct3d12.dml_depth_to_space1_operator_desc
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
- directml/DML_DEPTH_TO_SPACE1_OPERATOR_DESC
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
- DML_DEPTH_TO_SPACE1_OPERATOR_DESC
ms.openlocfilehash: 89b62a9916ee77dd6907d01710624d6e9a40a20a
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418078"
---
# <a name="dml_depth_to_space1_operator_desc-structure-directmlh"></a>DML_DEPTH_TO_SPACE1_OPERATOR_DESC estructura (directml.h)

Reorganiza (permuta) los datos de profundidad en bloques de datos espaciales. El operador genera una copia del tensor de entrada donde los valores de la dimensión de profundidad se mueven en bloques espaciales a las dimensiones de alto y ancho.

Se trata de la transformación inversa de [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md).

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_DEPTH_TO_SPACE1_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  BlockSize;
  DML_DEPTH_SPACE_ORDER Order;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor del que se leerá. Las dimensiones del tensor de entrada son `{ BatchCount, InputChannelCount, InputHeight, InputWidth }` .


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Las dimensiones del tensor de salida son `{ BatchCount, OutputChannelCount, OutputHeight, OutputWidth }` , donde:

* OutputChannelCount se calcula como InputChannelCount / ( `BlockSize`  *  `BlockSize` )
* OutputHeight se calcula como InputHeight * `BlockSize`
* OutputWidth se calcula como InputWidth * `BlockSize`


`BlockSize`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Ancho y alto de los bloques que se mueven.


`Order`

Tipo: **[DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md)**

Vea [DML_DEPTH_SPACE_ORDER](./ne-directml-dml_depth_space_order.md).

## <a name="examples"></a>Ejemplos

Todos los ejemplos de esta sección usan la entrada siguiente.

```
InputTensor: (Sizes:{1, 8, 2, 3}, DataType:UINT32)
[[[[0,   1,  2],
   [3,   4,  5]],
  [[9,  10, 11],
   [12, 13, 14]],
  [[18, 19, 20],
   [21, 22, 23]],
  [[27, 28, 29],
   [30, 31, 32]],
  [[36, 37, 38],
   [39, 40, 41]],
  [[45, 46, 47],
   [48, 49, 50]],
  [[54, 55, 56],
   [57, 58, 59]],
  [[63, 64, 65],
   [66, 67, 68]]]]
```

### <a name="example-1-depth-column-row-order"></a>Ejemplo 1. Orden de fila de columna de profundidad

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
 [[[[ 0, 18,  1, 19,  2, 20],
    [36, 54, 37, 55, 38, 56],
    [ 3, 21,  4, 22,  5, 23],
    [39, 57, 40, 58, 41, 59]],
   [[ 9, 27, 10, 28, 11, 29],
    [45, 63, 46, 64, 47, 65],
    [12, 30, 13, 31, 14, 32],
    [48, 66, 49, 67, 50, 68]]]]
```

### <a name="example-2-column-row-depth-order"></a>Ejemplo 2. Orden de profundidad de fila de columna

```
BlockSize: 2
Order: DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
OutputTensor: (Sizes:{1, 2, 4, 6}, DataType:UINT32)
[[[[ 0,  9,  1, 10,  2, 11],
   [18, 27, 19, 28, 20, 29],
   [ 3, 12,  4, 13,  5, 14],
   [21, 30, 22, 31, 23, 32]],
  [[36, 45, 37, 46, 38, 47],
   [54, 63, 55, 64, 56, 65],
   [39, 48, 40, 49, 41, 50],
   [57, 66, 58, 67, 59, 68]]]]
```


## <a name="remarks"></a>Comentarios
Cuando *Order* se establece [en DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW](./ne-directml-dml_depth_space_order.md), **DML_DEPTH_TO_SPACE1_OPERATOR_DESC** equivale a [DML_DEPTH_TO_SPACE_OPERATOR_DESC]().

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputTensor* y *OutputTensor* deben tener el mismo *tipo de datos*.

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Dimensions | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| InputTensor | Entrada | { BatchCount, InputChannelCount, InputHeight, InputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | { BatchCount, OutputChannelCount, OutputHeight, OutputWidth } | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Vea también

* [DML_DEPTH_TO_SPACE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_depth_to_space_operator_desc)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)