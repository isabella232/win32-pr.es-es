---
UID: NS:directml.DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
title: DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC
description: Realiza una función de multiplicación de matriz en datos cuantificados. Este operador es matemáticamente equivalente a descuantizar las entradas, después realizar la multiplicación de la matriz y, a continuación, cuantificar la salida.
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
ms.openlocfilehash: 0daeab63559a2d842582087d8874e802645f7809
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418051"
---
# <a name="dml_quantized_linear_matrix_multiply_operator_desc-structure-directmlh"></a>DML_QUANTIZED_LINEAR_MATRIX_MULTIPLY_OPERATOR_DESC estructura (directml.h)
Realiza una función de multiplicación de matriz en datos cuantificados. Este operador es matemáticamente equivalente a descuantizar las entradas, después realizar la multiplicación de la matriz y, a continuación, cuantificar la salida.

Este operador requiere que la matriz multiplique los tensores de entrada sea 4D, cuyo formato es `{ BatchCount, ChannelCount, Height, Width }` . El operador de multiplicación de matriz realizará batchcount * channelcount número de multiplicaciones de matrices independientes. 

Por ejemplo, si *ATensor* tiene tamaños de y  BTensor tiene tamaños de y OutputTensor tiene tamaños de , el operador de multiplicación de matriz realizará multiplicaciones de matrices independientes de BatchCount * ChannelCount de dimensiones `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}. 

### <a name="dequantize-function"></a>Función Dequantize

```
f(Input, Scale, ZeroPoint) = (Input - ZeroPoint) * Scale
```

### <a name="quantize-function"></a>Función Quantize

```
f(Input, Scale, ZeroPoint) = clamp(round(Input / Scale) + ZeroPoint, Min, Max)
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

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

Tensor que contiene los datos A. Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, M, K }` .


`AScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala de ATensor. Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `AScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, M, 1 }` cuantificación por fila. Estos valores de escala se usan para descuantizar los valores A.


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de *ATensor.* Las dimensiones esperadas de AZeroPointTensor son si se requiere una cuantificación por tensor o si se requiere una `{ 1, 1, 1, 1 }` `{ 1, 1, M, 1 }` cuantificación por fila. Estos valores de punto cero se usan para descuantizar los valores de ATensor.


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos B. Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, K, N }` .


`BScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala *de BTensor.* Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `BScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, 1, N }` cuantificación por columna. Estos valores de escala se usan para descuantizar los *valores de BTensor.*


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de *BTensor.* Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `BZeroPointTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, 1, N }` cuantificación por columna. Estos valores de punto cero se usan para descuantizar los *valores de BTensor.*


`OutputScaleTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos de escala de filtro. Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `OutputScaleTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, M, 1 }` cuantificación por fila. Este valor de escala se usa para descuantizar los valores de filtro.


`OutputZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de filtro. Las dimensiones esperadas de son si se requiere una cuantificación por `OutputZeroPointTensor` `{ 1, 1, 1, 1 }` tensor o si se requiere una `{ 1, 1, M, 1 }` cuantificación por fila. Este valor de punto cero se usa para descuantizar los valores de filtro.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor en el que se escriben los resultados. Las dimensiones de este tensor son `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
* *ATensor* y `AZeroPointTensor` deben tener el mismo *DataType.*
* *BTensor* y `BZeroPointTensor` deben tener el mismo *DataType.*
* *OutputTensor* y `OutputZeroPointTensor` deben tener el mismo *DataType.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | 4 | INT8, UINT8 |
| AScaleTensor | Entrada | 4 | FLOAT32 |
| AZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| BTensor | Entrada | 4 | INT8, UINT8 |
| BScaleTensor | Entrada | 4 | FLOAT32 |
| BZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputScaleTensor | Entrada | 4 | FLOAT32 |
| OutputZeroPointTensor | Entrada opcional | 4 | INT8, UINT8 |
| OutputTensor | Resultados | 4 | INT8, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |