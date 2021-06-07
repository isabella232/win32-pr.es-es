---
UID: NS:directml.DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
title: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
description: Suma los elementos de un tensor a lo largo de un eje, escribiendo el recuento en ejecución de la suma en el tensor de salida.
helpviewer_keywords:
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure
- direct3d12.dml_cumulative_summation_operator_desc
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
ms.keywords: DML_CUMULATIVE_SUMMATION_OPERATOR_DESC, DML_CUMULATIVE_SUMMATION_OPERATOR_DESC structure, direct3d12.dml_cumulative_summation_operator_desc, directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
- directml/DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
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
- DML_CUMULATIVE_SUMMATION_OPERATOR_DESC
ms.openlocfilehash: 2862a2add207b0bb6c41f5c1aabbc390797cba23
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418090"
---
# <a name="dml_cumulative_summation_operator_desc-structure-directmlh"></a>DML_CUMULATIVE_SUMMATION_OPERATOR_DESC estructura (directml.h)

Suma los elementos de un tensor a lo largo de un eje, escribiendo el recuento en ejecución de la suma en el tensor de salida.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_CUMULATIVE_SUMMATION_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  UINT                  Axis;
  DML_AXIS_DIRECTION    AxisDirection;
  BOOL                  HasExclusiveSum;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada que contiene los elementos que se suman.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben las sumas acumulativas resultantes. Este tensor debe tener los mismos tamaños y tipo de datos que *InputTensor*.

`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Índice de la dimensión sobre la que se suman los elementos. Este valor debe ser menor que *dimensionCount* de *InputTensor.*

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Uno de los valores de la [enumeración DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) datos. Si se establece **en DML_AXIS_DIRECTION_INCREASING**, la suma se produce recorriendo el tensor a lo largo del eje especificado por índice de elemento ascendente. Si se establece **en DML_AXIS_DIRECTION_DECREASING**, el valor inverso es true y la suma se produce recorriendo elementos por índice descendente.

`HasExclusiveSum`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Si **es TRUE**, el valor del elemento actual se excluye al escribir el recuento en ejecución en el tensor de salida. Si **es FALSE**, el valor del elemento actual se incluye en el recuento en ejecución.

## <a name="examples"></a>Ejemplos

Todos los ejemplos de esta sección usan un tensor de entrada con las siguientes propiedades.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-summation-across-horizontal-slivers"></a>Ejemplo 1. Suma acumulativa en los slivers horizontales

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  3,  6, 11],     // i.e. [2, 2+1, 2+1+3, 2+1+3+5]
   [3, 11, 18, 21],     //      [...                   ]
   [9, 15, 17, 21]]]]   //      [...                   ]
```

### <a name="example-2-exclusive-sums"></a>Ejemplo 2. Sumas exclusivas

Establecer *HasExclusiveSum* en **TRUE** tiene el efecto de excluir el valor del elemento actual del recuento en ejecución al escribir en el tensor de salida.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[0, 2,  3,  6],      // Notice the sum is written before adding the input,
   [0, 3, 11, 18],      // and the final total is not written to any output.
   [0, 9, 15, 17]]]]
```

### <a name="example-3-axis-direction"></a>Ejemplo 3. Dirección del eje

Establecer *AxisDirection en* [DML_AXIS_DIRECTION_DECREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction) tiene el efecto de invertir el orden transversal de los elementos al calcular el recuento en ejecución.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[11,  9,  8,  5],    // i.e. [2+1+3+5, 1+3+5, 3+5, 5]
   [21, 18, 10,  3],    //      [...                   ]
   [21, 12,  6,  4]]]]  //      [...                   ]
```

### <a name="example-4-summing-along-a-different-axis"></a>Ejemplo 4. Suma a lo largo de un eje diferente

En este ejemplo, la suma se produce verticalmente, a lo largo del eje de alto (segunda dimensión).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveSum: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 5,  9, 10,  8],   //      [2+3,  ...]
   [14, 15, 12, 12]]]] //      [2+3+9 ...]
```

## <a name="remarks"></a>Comentarios
Este operador admite la ejecución en contexto, lo que significa que *outputTensor* puede crear un alias de *InputTensor durante* el enlace.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*InputTensor* y *OutputTensor* deben tener los mismos *tipos de datos* y *tamaños.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16, UINT32, UINT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
