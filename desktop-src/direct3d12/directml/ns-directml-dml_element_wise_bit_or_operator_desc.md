---
UID: NS:directml.DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
title: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
description: Calcula la operación OR bit a bit entre cada elemento correspondiente de los diez de entrada y escribe el resultado en el tensores de salida.
helpviewer_keywords:
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure
- direct3d12.dml_convolution_integer_operator_desc
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/09/2020
ms.keywords: DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC, DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC structure, direct3d12.dml_convolution_integer_operator_desc, directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
- directml/DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
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
- DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
ms.openlocfilehash: e0afa89e18b6393efc976a782469d1a9765211f0
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721246"
---
# <a name="dml_element_wise_bit_or_operator_desc-structure-directmlh"></a>DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC estructura (directml. h)

Calcula la operación OR bit a bit entre cada elemento correspondiente de los diez de entrada y escribe el resultado en el tensores de salida.

Los tensores de entrada y salida deben tener los mismos *DimensionCount*, *tamaños* y *tipo* de datos.

Este operador admite la ejecución en contexto, lo que significa que el tensores de salida tiene permiso para asignar alias a uno o varios de los decenas de entradas durante el enlace.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis

```cpp
struct DML_ELEMENT_WISE_BIT_OR_OPERATOR_DESC
{
  const DML_TENSOR_DESC* ATensor;
  const DML_TENSOR_DESC* BTensor;
  const DML_TENSOR_DESC* OutputTensor;
};
```

## <a name="members"></a>Miembros

`ATensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores que contiene las entradas del lado izquierdo.

`BTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Un tensores que contiene las entradas del lado derecho.

`OutputTensor`

Tipo: **const [DML_TENSOR_DESC](/windows/win32/api/directml/ns-directml-dml_tensor_desc) \***

Tensores de salida en el que se van a escribir los resultados.

## <a name="availability"></a>Disponibilidad
Este operador se presentó en `DML_FEATURE_LEVEL_3_0` .

## <a name="tensor-constraints"></a>Restricciones de tensores
*ATensor*, *BTensor* y *OutputTensor* deben tener el mismo *tipo de DataType*, *DimensionCount* y *tamaños*.

## <a name="tensor-support"></a>Compatibilidad con tensores
| Tensores | Clase | Recuentos de dimensiones compatibles | Tipos de datos admitidos |
| ------ | ---- | -------------------------- | -------------------- |
| ATensor | Entrada | de 1 a 8 | UINT32, UINT16, UINT8 |
| BTensor | Entrada | de 1 a 8 | UINT32, UINT16, UINT8 |
| OutputTensor | Output | de 1 a 8 | UINT32, UINT16, UINT8 |

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |