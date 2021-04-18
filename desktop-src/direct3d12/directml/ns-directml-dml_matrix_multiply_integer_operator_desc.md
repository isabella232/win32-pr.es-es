---
UID: NS:directml.DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
title: DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC
description: Realiza una función de multiplicación de matrices en datos enteros.
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
ms.openlocfilehash: f6ecccf49b0d7123e6f41321c7ba1bf8e8d4ad87
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721245"
---
# <a name="dml_matrix_multiply_integer_operator_desc-structure-directmlh"></a>DML_MATRIX_MULTIPLY_INTEGER_OPERATOR_DESC estructura (directml. h)
Realiza una función de multiplicación de matrices en datos enteros.

Este operador requiere que la matriz multiplique los idiomas de entrada a 4D, cuyo formato es `{ BatchCount, ChannelCount, Height, Width }` . El operador de multiplicación de la matriz realizará el BatchCount * ChannelCount número de multiplicaciones de matriz independiente.

Por ejemplo, si *ATensor* tiene  los tamaños `{ BatchCount, ChannelCount, M, K }` , y *BTensor* tiene *tamaños* `{ BatchCount, ChannelCount, K, N }` , y *OutputTensor* tiene *tamaños* `{ BatchCount, ChannelCount, M, N }` , el operador de multiplicación de la matriz realizará la multiplicación de las dimensiones de la matriz independiente BatchCount * ChannelCount {m, K} x {k, n} = {m, n}.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tensores que contiene los datos. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, M, K }` .


`AZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de cero puntos de ATensor. Las dimensiones esperadas de `AZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores o `{ 1, 1, M, 1 }` si se requiere la cuantificación por fila. Estos valores de punto cero se usan para descuantificar los valores de *ATensor* .


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores que contiene los datos de B. Las dimensiones de este tensores deben ser `{ BatchCount, ChannelCount, K, N }` .


`BZeroPointTensor`

Tipo: _Maybenull \_ **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores opcional que contiene los datos de cero puntos de *BTensor* . Las dimensiones esperadas de `BZeroPointTensor` son `{ 1, 1, 1, 1 }` si se requiere la cuantificación por tensores, o `{ 1, 1, 1, N }` si se requiere la cuantificación por columna. Estos valores de punto cero se usan para descuantificar los valores de BTensor.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores con el que se van a escribir los resultados. Las dimensiones de este tensores son `{ BatchCount, ChannelCount, M, N }` .

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensores
* *ATensor* y `AZeroPointTensor` deben tener el mismo *tipo de texto*.
* *BTensor* y `BZeroPointTensor` deben tener el mismo *tipo de texto*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Dimensions | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | ---------- | -------------------------- | -------------------- |
| ATensor | Entrada | {BatchCount, ChannelCount, M, K} | 4 | INT8, UINT8 |
| AZeroPointTensor | Entrada opcional | {1, 1, AZeroPointCount, 1} | 4 | INT8, UINT8 |
| BTensor | Entrada | {BatchCount, ChannelCount, K, N} | 4 | INT8, UINT8 |
| BZeroPointTensor | Entrada opcional | {1, 1, 1, BZeroPointCount} | 4 | INT8, UINT8 |
| OutputTensor | Output | {BatchCount, ChannelCount, M, N} | 4 | INT32 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |