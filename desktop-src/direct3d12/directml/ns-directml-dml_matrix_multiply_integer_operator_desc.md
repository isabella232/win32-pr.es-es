---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Realiza una función de multiplicación de matriz en datos enteros.
helpviewer_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure
- direct3d12.dml_matrix_multiply_integer_operator_desc
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/03/2020
ms.keywords: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC, DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC structure, direct3d12.dml_matrix_multiply_integer_operator_desc, directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
ms.custom: 19H1
f1_keywords:
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
- directml/DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
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
- DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
ms.openlocfilehash: f498e84208da451b5d25ffef90219c0037ce86fb
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417978"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC estructura (directml.h)
Realiza una función de multiplicación de matriz en datos enteros.

Este operador requiere que la matriz multiplique los tensores de entrada para que sean 4D, que tienen el formato `{ BatchCount, ChannelCount, Height, Width }` . El operador de multiplicación de matrices realizará BatchCount * ChannelCount número de multiplicaciones de matrices independientes.

Por ejemplo, si *ATensor* tiene tamaños de y  BTensor tiene tamaños de y OutputTensor tiene tamaños de , el operador de multiplicación de matrices realizará multiplicaciones de matrices independientes de BatchCount * ChannelCount de dimensiones `{ BatchCount, ChannelCount, M, K }`   `{ BatchCount, ChannelCount, K, N }`   `{ BatchCount, ChannelCount, M, N }` {M,K} x {K,N} = {M,N}.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *AZeroPointTensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *BZeroPointTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Miembros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos A. Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de ATensor. Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `AZeroPointTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, M, 1 }` cuantificación por fila. Estos valores de punto cero se usan para descuantizar los *valores de ATensor.*


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene los datos B. Las dimensiones de este tensor deben ser `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor opcional que contiene los datos de punto cero de *BTensor.* Las dimensiones esperadas de son si se requiere una cuantificación por tensor o si se requiere `BZeroPointTensor` `{ 1, 1, 1, 1 }` una `{ 1, 1, 1, N }` cuantificación por columna. Estos valores de punto cero se usan para descuantizar los valores de BTensor.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor con el que se escriben los resultados. Las dimensiones de este tensor son `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
* *ATensor* y `AZeroPointTensor` deben tener el mismo *datatype*.
* *BTensor* y `BZeroPointTensor` deben tener el mismo *datatype*.

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Dimensions | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Entrada | { BatchCount, ChannelCount, M, K } | 4 | INT8, UINT8 |
| AZeroPointTensor | Entrada opcional | { 1, 1, AZeroPointCount, 1 } | 4 | INT8, UINT8 |
| BTensor | Entrada | { BatchCount, ChannelCount, K, N } | 4 | INT8, UINT8 |
| BZeroPointTensor | Entrada opcional | { 1, 1, 1, BZeroPointCount } | 4 | INT8, UINT8 |
| OutputTensor | Resultados | { BatchCount, ChannelCount, M, N } | 4 | INT32 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |