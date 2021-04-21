---
UID: NS:directml.DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
description: Realiza un desplazamiento lógico a la derecha de cada elemento de *ATensor* mediante una serie de bits dados por el elemento correspondiente de *BTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC structure
- direct3d12.dml_element_wise_bit_shift_right_operator_desc
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC
ms.openlocfilehash: 5803b40520e3735d24d00eb7260eb527ab857c33
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803203"
---
# <a name="dml_element_wise_bit_shift_right_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC estructura (directml.h)

Realiza un desplazamiento lógico a la derecha de cada elemento de *ATensor* mediante una serie de bits dados por el elemento correspondiente de *BTensor*, colocando el resultado en el elemento correspondiente de *OutputTensor*.

```
f(a, b) = (a >> b)
```

Este operador admite la ejecución en contexto, lo que significa que *OutputTensor* puede crear un alias de uno de los tensores de entrada durante el enlace.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_ELEMENT_WISE_BIT_SHIFT_RIGHT_OPERATOR_DESC {
  const DML_TENSOR_DESC *ATensor;
  const DML_TENSOR_DESC *BTensor;
  const DML_TENSOR_DESC *OutputTensor;
};
```



## <a name="members"></a>Miembros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene las entradas del lado izquierdo.


`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor que contiene las entradas del lado derecho.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *tamaños DataType,* *DimensionCount* y *.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | De 1 a 8 | UINT32, UINT16, UINT8 |
| BTensor | Entrada | De 1 a 8 | UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | De 1 a 8 | UINT32, UINT16, UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | 4 | UINT32, UINT16, UINT8 |
| BTensor | Entrada | 4 | UINT32, UINT16, UINT8 |
| OutputTensor | Resultados | 4 | UINT32, UINT16, UINT8 |



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |