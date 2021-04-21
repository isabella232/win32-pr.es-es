---
UID: NS:directml.DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
title: DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
description: Calcula la arcotangente de 2 argumentos para cada elemento de *ATensor* y *BTensor,* donde *ATensor* es el eje *Y* y *BTensor* es el eje *X,* colocando el resultado en el elemento correspondiente de *OutputTensor*.
helpviewer_keywords:
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC structure
- direct3d12.dml_element_wise_atan_yx_operator_desc
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
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
- DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
ms.openlocfilehash: 6031f08dc99db943d26ab5212896b4fb44987269
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107804495"
---
# <a name="dml_element_wise_atan_yx_operator_desc-directmlh"></a>DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC (directml.h)

Calcula la arcotangente de 2 argumentos para cada elemento de *ATensor* y *BTensor,* donde *ATensor* es el eje *Y* y *BTensor* es el eje *X,* colocando el resultado en el elemento correspondiente de *OutputTensor*. Este operador no está definido para el origen (es decir, cuando *ATensor* y *BTensor* son 0 para los elementos correspondientes).

![GRU_Forward](../images/atan2.png)

```
f(y, x) = atan2(y, x)
```

Este operador admite la ejecución en contexto, lo que significa que se permite al tensor de salida el alias *ATensor* o *BTensor* durante el enlace.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.5 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_ELEMENT_WISE_ATAN_YX_OPERATOR_DESC
{
    const DML_TENSOR_DESC* ATensor;
    const DML_TENSOR_DESC* BTensor;
    const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Miembros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada del que se leerán los valores del eje Y.

`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de entrada del que se leerán los valores del eje X.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensor de salida en el que se escriben los resultados.

## <a name="availability"></a>Disponibilidad
Este operador se introdujo en `DML_FEATURE_LEVEL_3_1` .

## <a name="tensor-constraints"></a>Restricciones de Tensor
*ATensor,* *BTensor* y *OutputTensor* deben tener los mismos *DataType,* *DimensionCount* y *Sizes.*

## <a name="tensor-support"></a>Compatibilidad con Tensor
| Tensor | Tipo | Recuentos de dimensiones admitidos | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| BTensor | Entrada | De 1 a 8 | FLOAT32, FLOAT16 |
| OutputTensor | Resultados | De 1 a 8 | FLOAT32, FLOAT16 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |
