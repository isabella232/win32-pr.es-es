---
UID: NS:directml.DML_GATHER_ELEMENTS_OPERATOR_DESC
title: DML_GATHER_ELEMENTS_OPERATOR_DESC
description: Recopila elementos del tensor de entrada a lo largo del eje dado mediante el tensor de índices para reasignar a la entrada.
helpviewer_keywords:
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- DML_GATHER_ELEMENTS_OPERATOR_DESC structure
- direct3d12.dml_gather_elements_operator_desc
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
- directml/DML_GATHER_ELEMENTS_OPERATOR_DESC
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
- DML_GATHER_ELEMENTS_OPERATOR_DESC
ms.openlocfilehash: 89a4f2017f6adec8cce206e9261eb0fa6563e94c
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418006"
---
# <a name="dml_gather_elements_operator_desc-structure-directmlh"></a>DML_GATHER_ELEMENTS_OPERATOR_DESC estructura (directml.h)

Recopila elementos del tensor de entrada a lo largo del eje dado mediante el tensor de índices para reasignar a la entrada. Este operador realiza el pseudocódigo siguiente, con el comportamiento exacto dependiente del eje, el recuento de dimensiones de entrada y el recuento de dimensiones de índices.

```
output[i, j, k, ...] = input[index[i, j, k, ...], j, k, ...] // if axis == 0
output[i, j, k, ...] = input[i, index[i, j, k, ...], k, ...] // if axis == 1
output[i, j, k, ...] = input[i, j, index[i, j, k, ...], ...] // if axis == 2
...
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_GATHER_ELEMENTS_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *IndicesTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor del que se leerá.


`IndicesTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Los índices en el tensor de entrada a lo largo del eje activo. Los *tamaños deben* coincidir con *InputTensor.Sizes para* todas las dimensiones excepto el *eje*.

A partir `DML_FEATURE_LEVEL_3_0` de , este operador admite valores de índice negativos cuando se usa un tipo entero con signo con este tensor. Los índices negativos se interpretan como relativos al final de la dimensión del eje. Por ejemplo, un índice de -1 hace referencia al último elemento a lo largo de esa dimensión.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Los *tamaños* deben coincidir *con IndicesTensor.Sizes* y *DataType* debe coincidir con *InputTensor.DataType.*


`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Dimensión de eje de *InputTensor que* se va a recopilar, que abarca `[0, *InputTensor.DimensionCount*)` .

## <a name="examples"></a>Ejemplos

```
Axis = 0

InputTensor: (Sizes:{3,3}, DataType:FLOAT32)
    [[1, 2, 3],
     [4, 5, 6],
     [7, 8, 9]]

IndicesTensor: (Sizes:{2,3}, DataType:UINT32)
    [[1, 2, 0],
     [2, 0, 0]]

// output[y, x] = input[indices[y, x], x]
OutputTensor: (Sizes:{2,3}, DataType:UINT32)
    [[4, 8, 3], // select elements vertically from data
     [7, 2, 3]]
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* `IndicesTensor`, *InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount.*
* *InputTensor* y *OutputTensor* deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | De 1 a 8 | INT64, INT32, UINT64, UINT32 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| ÍndicesTensor | Entrada | 4 | UINT32 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |