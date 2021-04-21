---
UID: NS:directml.DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
title: DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
description: Rellena un tensor con una secuencia.
helpviewer_keywords:
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC structure
- direct3d12.dml_fill_value_sequence_operator_desc
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/30/2020
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
- directml/DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
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
- DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC
ms.openlocfilehash: 17b503630db2108dc4d9d2f5c2f32f7e324189d1
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803034"
---
# <a name="dml_fill_value_sequence_operator_desc-structure-directmlh"></a>DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC estructura (directml.h)

Rellena un tensor con una secuencia. Este operador realiza el pseudocódigo siguiente.

```
for each coordinate in OutputTensor
    OutputTensor[coordinate] = Value
    Value += Delta
endfor
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_FILL_VALUE_SEQUENCE_OPERATOR_DESC {
  const DML_TENSOR_DESC *OutputTensor;
  DML_TENSOR_DATA_TYPE  ValueDataType;
  DML_SCALAR_UNION      ValueStart;
  DML_SCALAR_UNION      ValueDelta;
};
```



## <a name="members"></a>Miembros

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Este tensor puede tener cualquier tamaño.


`ValueDataType`

Tipo: **[DML_TENSOR_DATA_TYPE](/windows/win32/api/directml/ne-directml-dml_tensor_data_type)**

Tipo de datos del *campo Value,* que debe coincidir con *OutputTensor.DataType*.


`ValueStart`

Tipo: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**

Valor inicial que se va a rellenar en el primer elemento de la salida, con *ValueDataType* que determina cómo interpretar el campo.


`ValueDelta`

Tipo: **[DML_SCALAR_UNION](./ns-directml-dml_scalar_union.md)**

Paso para agregar al valor de cada elemento escrito, donde *ValueDataType* determina cómo interpretar el campo.

## <a name="examples"></a>Ejemplos

### <a name="example-1-1d-ascending-step"></a>Ejemplo 1. Paso ascendente 1D

```
ValueStart = 3
ValueDelta = 2
ValueDataType = DML_TENSOR_DATA_TYPE_FLOAT32

OutputTensor: (Sizes:{1,1,1,3}, DataType:FLOAT32)
    [[[[3, 5, 7]]]]
```

### <a name="example-2-2d-ascending-step"></a>Ejemplo 2. Paso ascendente 2D

```
ValueStart = 10
ValueDelta = -2
ValueDataType = DML_TENSOR_DATA_TYPE_UINT8

OutputTensor: (Sizes:{1,1,2,2}, DataType:UINT8)
    [[[[10, 8],
       [ 6, 4]]]]
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |