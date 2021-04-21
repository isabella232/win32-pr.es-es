---
UID: NS:directml.DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
title: DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
description: Redondea cada elemento de *InputTensor* a un valor entero, colocando el resultado en el elemento correspondiente de *OutputTensor.*
helpviewer_keywords:
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC structure
- direct3d12.dml_element_wise_round_operator_desc
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ROUND_OPERATOR_DESC
ms.openlocfilehash: cb9414d0c3e628fa95784480c7402b242d12095b
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803048"
---
# <a name="dml_element_wise_round_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_ROUND_OPERATOR_DESC estructura (directml.h)

Redondea cada elemento de *InputTensor* a un valor entero, colocando el resultado en el elemento correspondiente de *OutputTensor.*

Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede usar el alias *InputTensor* durante el enlace.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_ELEMENT_WISE_ROUND_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_ROUNDING_MODE     RoundingMode;
};
```



## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada del que se leerá.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados.


`RoundingMode`

Tipo: **[DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode)**

Un [DML_ROUNDING_MODE](/windows/win32/api/directml/ne-directml-dml_rounding_mode) determinar la dirección hacia la que se redondea.

* Si **DML_ROUNDING_MODE_HALVES_TO_NEAREST_EVEN**: los valores se redondea al entero más cercano, con valores a medio camino (por ejemplo, 0,5) redondeados hacia el entero par más cercano.
* Si **DML_ROUNDING_MODE_TOWARD_ZERO**: los valores se redondea hacia cero. Esto trunca eficazmente la parte fraccionera.
* Si **DML_ROUNDING_MODE_TOWARD_INFINITY**: los valores se redondean al entero más cercano, con valores a medio camino (por ejemplo, 0,5) redondeados lejos de cero (hacia infinito positivo o negativo, según el signo del valor).

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*InputTensor* y *OutputTensor* deben tener los mismos *datatype,* *dimensioncount* y *tamaños.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | 4 | FLOAT32, FLOAT16 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |