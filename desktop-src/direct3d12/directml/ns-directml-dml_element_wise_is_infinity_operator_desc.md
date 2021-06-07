---
UID: NS:directml.DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
title: DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
description: Comprueba cada elemento de *InputTensor* para IEEE-754 -inf, inf o ambos, dependiendo del valor de *InfinityMode* especificado, y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor.*
ms.topic: reference
tech.root: directml
ms.date: 10/29/2020
targetos: Windows
req.construct-type: structure
req.ddi-compliance: ''
req.dll: ''
req.header: directml.h
req.include-header: ''
req.kmdf-ver: ''
req.lib: ''
req.max-support: ''
req.redist: ''
req.target-min-winverclnt: Windows 10, version 2004 (10.0; Build 19041)
req.target-min-winversvr: Windows Server, version 2004 (10.0; Build 19041)
req.target-type: Windows
req.typenames: ''
req.umdf-ver: ''
req.unicode-ansi: ''
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- directml.h
api_name:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
f1_keywords:
- DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC
dev_langs:
- c++
ms.openlocfilehash: 41be7751b542436b481da784c60ae79ad554cd12
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418007"
---
# <a name="dml_element_wise_is_infinity_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC estructura (directml.h)

Comprueba cada elemento de *InputTensor* para IEEE-754 -inf, inf o ambos, dependiendo del valor de *InfinityMode* especificado, y coloca el resultado (1 para true, 0 para false) en el elemento correspondiente de *OutputTensor.*

```
f(x) = isinf(x) && (
       (x > 0 && InfinityMode == DML_IS_INFINITY_MODE_POSITIVE) ||
       (x < 0 && InfinityMode == DML_IS_INFINITY_MODE_NEGATIVE) ||
                 InfinityMode == DML_IS_INFINITY_MODE_EITHER)
```

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_ELEMENT_WISE_IS_INFINITY_OPERATOR_DESC {
  const DML_TENSOR_DESC *InputTensor;
  const DML_TENSOR_DESC *OutputTensor;
  DML_IS_INFINITY_MODE  InfinityMode;
};
```

## <a name="members"></a>Miembros

`InputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada del que se leerá.


`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados.


`InfinityMode`

Tipo: **[DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode)**

Un [DML_IS_INFINITY_MODE](/windows/win32/api/directml/ne-directml-dml_is_infinity_mode) determinar el signo del infinito que se debe comprobar.

* Si **DML_IS_INFINITY_MODE_EITHER**, se devolverá 1 si el elemento es -inf o inf; en caso contrario, 0.
* Si **DML_IS_INFINITY_MODE_POSITIVE**, se devolverá 1 si el elemento es inf; de lo contrario, 0.
* Si **DML_IS_INFINITY_MODE_NEGATIVE**" , se devolverá 1 si el elemento es -inf; en caso contrario, 0.


## <a name="remarks"></a>Comentarios
## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_2_1` .

## <a name="tensor-constraints"></a>Restricciones de tensor
*InputTensor* y *OutputTensor* deben tener los mismos *DimensionCount* y *Sizes.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
### <a name="dml_feature_level_3_0-and-above"></a>DML_FEATURE_LEVEL_3_0 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | De 1 a 8 | UINT8 |

### <a name="dml_feature_level_2_1-and-above"></a>DML_FEATURE_LEVEL_2_1 y posteriores
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| InputTensor | Entrada | 4 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | 4 | UINT8 |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Cliente mínimo compatible** | Windows 10, versión 2004 (10.0; Compilación 19041) |
| **Servidor mínimo compatible** | Windows Server, versión 2004 (10.0; Compilación 19041) |
| **Header** | directml.h |