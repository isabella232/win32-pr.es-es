---
UID: NS:directml.DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
title: DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
description: Multiplica los elementos de un tensor a lo largo de un eje, escribiendo el recuento en ejecución del producto en el tensor de salida.
helpviewer_keywords:
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC structure
- direct3d12.dml_cumulative_product_operator_desc
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 03/15/2021
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
- directml/DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
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
- DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
ms.openlocfilehash: 2f0c6a6b6f12792a245027a7f8e86c05f7e85192
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804534"
---
# <a name="dml_cumulative_product_operator_desc-directmlh"></a>DML_CUMULATIVE_PRODUCT_OPERATOR_DESC (directml.h)

Multiplica los elementos de un tensor a lo largo de un eje, escribiendo el recuento en ejecución del producto en el tensor de salida.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_CUMULATIVE_PRODUCT_OPERATOR_DESC
{
    const DML_TENSOR_DESC* InputTensor;
    const DML_TENSOR_DESC* OutputTensor;
    UINT Axis;
    DML_AXIS_DIRECTION AxisDirection;
    BOOL HasExclusiveProduct;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de entrada. Suele ser el mismo tensor que se proporcionó que *inputTensor* para [**DML_BATCH_NORMALIZATION_OPERATOR_DESC**](/windows/win32/api/directml/ns-directml-dml_batch_normalization_operator_desc) en el paso de reenvío.

Tensor de entrada que contiene los elementos que se va a multiplicar.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los productos acumulativos resultantes. Este tensor debe tener los mismos tamaños y tipo de datos que *InputTensor.*

`Axis`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Índice de la dimensión por la que se multiplican los elementos. Este valor debe ser menor que *dimensionCount* de *InputTensor.*

`AxisDirection`

Tipo: **[DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md)**

Uno de los valores de la [enumeración DML_AXIS_DIRECTION](./ne-directml-dml_axis_direction.md) datos. Si se establece **en DML_AXIS_DIRECTION_INCREASING**, el producto se produce recorriendo el tensor a lo largo del eje especificado por índice de elemento ascendente. Si se establece **en DML_AXIS_DIRECTION_DECREASING**, el valor inverso es true y el producto se produce recorriendo elementos por índice descendente.

`HasExclusiveProduct`

Tipo: <b> <a href="/windows/win32/winprog/windows-data-types">BOOL</a></b>

Si **es TRUE**, el valor del elemento actual se excluye al escribir el recuento en ejecución en el tensor de salida. Si **es FALSE**, el valor del elemento actual se incluye en el recuento en ejecución.

## <a name="examples"></a>Ejemplos

Todos los ejemplos de esta sección usan este mismo tensor de entrada.

```
InputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2, 1, 3, 5],
   [3, 8, 7, 3],
   [9, 6, 2, 4]]]]
```

### <a name="example-1-cumulative-product-across-horizontal-slivers"></a>Ejemplo 1. Producto acumulativo en los slivers horizontales

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[2,  2,   6,  30],       // i.e. [2, 2*1, 2*1*3, 2*1*3*5]
   [3, 24, 168, 504],       //      [...                   ]
   [9, 54, 108, 432]]]]     //      [...                   ]
```

### <a name="example-2-exclusive-products"></a>Ejemplo 2. Productos exclusivos

Establecer *HasExclusiveProduct* en **TRUE** tiene el efecto de excluir el valor del elemento actual del recuento en ejecución al escribir en el tensor de salida.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: TRUE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[1, 2,  2,   6],      // Notice the product is written before multiplying the input,
   [1, 3, 24, 168],      // and the final total is not written to any output.
   [1, 9, 54, 108]]]]
```

### <a name="example-3-axis-direction"></a>Ejemplo 3. Dirección del eje

Establecer *AxisDirection en* [**DML_AXIS_DIRECTION_DECREASING**](/windows/win32/direct3d12/directml/ne-directml-dml_axis_direction) tiene el efecto de invertir el orden transversal de los elementos al calcular el recuento en ejecución.

```
Axis: 3
AxisDirection: DML_AXIS_DIRECTION_DECREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 30,  15, 15, 5],    // i.e. [2*1*3*5, 1*3*5, 3*5, 5]
   [504, 168, 21, 3],    //      [...                   ]
   [432,  48,  8, 4]]]]  //      [...                   ]
```

### <a name="example-4-multiplying-along-a-different-axis"></a>Ejemplo 4. Multiplicación a lo largo de un eje diferente

En este ejemplo, el producto se produce verticalmente, a lo largo del eje de alto (segunda dimensión).

```
Axis: 2
AxisDirection: DML_AXIS_DIRECTION_INCREASING
HasExclusiveProduct: FALSE

OutputTensor: (Sizes:{1,1,3,4}, DataType:FLOAT32)
[[[[ 2,  1,  3,  5],   // i.e. [2,    ...]
   [ 6,  8, 21, 15],   //      [2*3,  ...]
   [54, 48, 42, 60]]]] //      [2*3*9 ...]
```

## <a name="remarks"></a>Observaciones
Este operador admite la ejecución en contexto, lo que significa que el tensor de salida puede usar el alias *InputTensor durante* el enlace.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
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
