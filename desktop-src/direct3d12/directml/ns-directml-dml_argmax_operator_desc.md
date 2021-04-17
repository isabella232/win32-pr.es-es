---
UID: NS:directml.DML_ARGMAX_OPERATOR_DESC
title: DML_ARGMAX_OPERATOR_DESC
description: Genera los índices de los elementos con valores máximos dentro de una o más dimensiones de la tensores de entrada.
helpviewer_keywords:
- DML_ARGMAX_OPERATOR_DESC
- DML_ARGMAX_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ARGMAX_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ARGMAX_OPERATOR_DESC, DML_ARGMAX_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
- directml/DML_ARGMAX_OPERATOR_DESC
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
- DML_ARGMAX_OPERATOR_DESC
ms.openlocfilehash: 17ccadc1228ea833ea1f1b3235e97430ac000514
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721259"
---
# <a name="dml_argmax_operator_desc-structure-directmlh"></a>DML_ARGMAX_OPERATOR_DESC estructura (directml. h)

Genera los índices de los elementos con valores máximos dentro de una o más dimensiones de la tensores de entrada.

Cada elemento Output es el resultado de aplicar una reducción *argmax* en un subconjunto de la tensores de entrada. La función *argmax* genera el índice del elemento con valores máximos dentro de un conjunto de elementos de entrada. Los elementos de entrada implicados en cada reducción vienen determinados por los ejes de entrada proporcionados. Del mismo modo, cada índice de salida es con respecto a los ejes de entrada proporcionados. Si se especifican todos los ejes de entrada, el operador aplica una única reducción de *argmax* y genera un solo elemento de salida.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_ARGMAX_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
  UINT AxisCount;
  _Field_size_(AxisCount) const UINT* Axes;
  DML_AXIS_DIRECTION AxisDirection;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores del que se va a leer.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los resultados. Cada elemento Output es el resultado de una reducción *argmax* en un subconjunto de elementos de *InputTensor*. 

- *DimensionCount* debe coincidir con *InputTensor. DimensionCount* (el rango de la tensores de entrada se conserva).
- Los *tamaños* deben coincidir con *InputTensor. Sizes*, excepto para las dimensiones incluidas en los *ejes* reducidos, cuyo tamaño debe ser 1.

`AxisCount`

Tipo: **[uint](/windows/desktop/WinProg/windows-data-types)**

Número de ejes que se van a reducir. Este campo determina el tamaño de la matriz de *ejes* .

`Axes`

Tipo: \_ Field_size \_ (AxisCount) **const [uint](/windows/desktop/WinProg/windows-data-types) \***

Ejes en los que se va a reducir. Los valores deben estar en el intervalo `[0, InputTensor.DimensionCount - 1]` .

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](/windows/win32/api/directml/ne-directml-dml_axis_direction)**

Determina qué índice se debe seleccionar cuando varios elementos de entrada tienen el mismo valor.
- **DML_AXIS_DIRECTION_INCREASING** devuelve el índice del primer elemento con valor máximo (por ejemplo, `argmax({3,2,1,2,3}) = 0` )
- **DML_AXIS_DIRECTION_DECREASING** devuelve el índice del último elemento con valor máximo (por ejemplo, `argmax({3,2,1,2,3}) = 4` )

## <a name="examples"></a>Ejemplos

Todos los ejemplos de esta sección usan esta misma tensores de entrada bidimensionales.

```
InputTensor: (Sizes:{3, 3}, DataType:FLOAT32)
[[1, 2, 3],
 [3, 0, 4],
 [2, 5, 2]]
```

### <a name="example-1-applying-argmax-to-columns"></a>Ejemplo 1. Aplicar *argmax* a columnas

```
AxisCount: 1
Axes: {0}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 3}, DataType:UINT32)
[[1,  // argmax({1, 3, 2})
  2,  // argmax({2, 0, 5})
  1]] // argmax({3, 4, 2})
```

### <a name="example-2-applying-argmax-to-rows"></a>Ejemplo 2. Aplicar *argmax* a las filas

```
AxisCount: 1
Axes: {1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{3, 1}, DataType:UINT32)
[[2], // argmax({1, 2, 3})
 [2], // argmax({3, 0, 4})
 [1]] // argmax({2, 5, 2})
```

### <a name="example-3-applying-argmax-to-all-axes-the-entire-tensor"></a>Ejemplo 3. Aplicar *argmax* a todos los ejes (todo el tensores)

```
AxisCount: 2
Axes: {0, 1}
AxisDirection: DML_AXIS_DIRECTION_INCREASING
OutputTensor: (Sizes:{1, 1}, DataType:UINT32)
[[7]]  // argmin({1, 2, 3, 3, 0, 4, 2, 5, 2})
```

## <a name="remarks"></a>Observaciones
Los tamaños de tensores de salida deben ser los mismos que los tamaños de tensores de entrada, salvo los ejes reducidos, que deben ser 1.

Cuando *AxisDirection* se [DML_AXIS_DIRECTION_INCREASING](/windows/win32/api/directml/ne-directml-dml_axis_direction), esta API es equivalente a [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) con [DML_REDUCE_FUNCTION_ARGMAX](/windows/win32/api/directml/ne-directml-dml_reduce_function).

Un subconjunto de esta funcionalidad se expone a través del operador [DML_REDUCE_OPERATOR_DESC](/windows/win32/api/directml/ns-directml-dml_reduce_operator_desc) y es compatible con los niveles de características de DirectML anteriores.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*InputTensor* y *OutputTensor* deben tener el mismo *DimensionCount*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | de 1 a 8 | FLOAT32, FLOAT16, INT32, INT16, INT8, UINT32, UINT16, UINT8 |
| OutputTensor | Output | de 1 a 8 | INT64, INT32, UINT64, UINT32 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |