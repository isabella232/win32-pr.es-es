---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Realiza una función de multiplicación de matrices en datos cuantificados. Este operador es matemáticamente equivalente a descuantificar las entradas y, a continuación, realizar la multiplicación de la matriz y cuantificar la salida.
helpviewer_keywords:
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC structure
- direct3d12.dml_quantized_linear_matrix_multiply_operator_desc
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
- directml/DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
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
- DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
ms.openlocfilehash: d0b20a37bca6ddf6083b116b53290a6b6b2084f4
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721301"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC estructura (directml. h)
Realiza una función de multiplicación de matrices en datos cuantificados. Este operador es matemáticamente equivalente a descuantificar las entradas y, a continuación, realizar la multiplicación de la matriz y cuantificar la salida.

Este operador requiere que la matriz multiplique los idiomas de entrada a 4D, cuyo formato es `{ BatchCount, ChannelCount, Height, Width }` . El operador de multiplicación de la matriz realizará el BatchCount * ChannelCount número de multiplicaciones de matriz independiente. 

Por ejemplo, si *ATensor* tiene  los tamaños `{ BatchCount, ChannelCount, M, K }` , y *BTensor* tiene *tamaños* `{ BatchCount, ChannelCount, K, N }` , y *OutputTensor* tiene *tamaños* `{ BatchCount, ChannelCount, M, N }` , el operador de multiplicación de la matriz realizará la multiplicación de las dimensiones de la matriz independiente BatchCount * ChannelCount {m, K} x {k, n} = {m, n}. 

### <a name="dequantize-function"></a>Descuantificar función

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Función cuantificate

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AScaleTensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BScaleTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputScaleTensor;
  const DML_TENSOR_DESC *OutputZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Miembros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de la escala ATensor. Las dimensiones esperadas de `AScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila. Estos valores de escala se usan para descuantificar los valores de un.


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de cero puntos de *ATensor* . Las dimensiones esperadas de AZeroPointTensor son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila. Estos valores de punto cero se usan para descuantificar los valores de ATensor.


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de B. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de la escala *BTensor* . Las dimensiones esperadas de `BScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, 1, N }` si se requiere la cuantificación por columna. Estos valores de escala se usan para descuantificar los valores de *BTensor* .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de cero puntos de *BTensor* . Las dimensiones esperadas de `BZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, 1, N }` si se requiere la cuantificación por columna. Estos valores de punto cero se usan para descuantificar los valores de *BTensor* .


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de la escala del filtro. Las dimensiones esperadas de `OutputScaleTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila. Este valor de escala se usa para descuantificar los valores de filtro.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos del punto cero del filtro. Las dimensiones esperadas de `OutputZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila. Este valor de punto cero se usa para descuantificar los valores de filtro.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores en el que se van a escribir los resultados. Las dimensiones de este tensores son `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *ATensor* y `AZeroPointTensor` deben tener el mismo *tipo de texto*.
* *BTensor* y `BZeroPointTensor` deben tener el mismo *tipo de texto*.
* *OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | 4 | INT8, UINT8 |
| AScaleTensor | Entrada | 4 | FLOAT32 |
| AZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| BTensor | Entrada | 4 | INT8, UINT8 |
| BScaleTensor | Entrada | 4 | FLOAT32 |
| BZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputScaleTensor | Entrada | 4 | FLOAT32 |
| OutputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputTensor | Output | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |