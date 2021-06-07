---
UID: NS:directml.DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
description: Calcula el recuento de población bit a bit (el número de bits establecido en 1) para cada elemento del tensor de entrada y escribe el resultado en el tensor de salida.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
ms.openlocfilehash: 3c8dddc3159ebcd857c7423b76856fbeba465d2e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417998"
---
# <a name="dml_element_wise_bit_count_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC estructura (directml.h)

Calcula el recuento de población bit a bit (el número de bits establecido en 1) para cada elemento del tensor de entrada y escribe el resultado en el tensor de salida.

El tensor de entrada y salida debe tener los mismos *dimensioncount* y *sizes,* aunque pueden diferir *en DataType.*

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_ELEMENT_WISE_BIT_COUNT_OPERATOR_DESC
{
  const DML_TENSOR_DESC* InputTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada del que se leerá.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados.

## <a name="example"></a>Ejemplo

```
InputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0,   123], // 0b0000000000, 0b0001111011
 [456, 789]] // 0b0111001000, 0b1100010101

OutputTensor: (Sizes:{2,2}, DataType:UINT32)
[[0, 6],
 [4, 5]]
```

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*InputTensor* y *OutputTensor* deben tener los mismos *dimensioncount* y *sizes.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | De 1 a 8 | UINT32, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |