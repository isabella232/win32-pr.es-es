---
UID: NE:directml.DML_DEPTH_SPACE_ORDER
title: DML_DEPTH_SPACE_ORDER
description: Define constantes que controlan la transformación aplicada en los operadores directML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) y **DML_OPERATOR_SPACE_TO_DEPTH1**.
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
- DML_DEPTH_SPACE_ORDER
- directml/DML_DEPTH_SPACE_ORDER
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
- DML_DEPTH_SPACE_ORDER
ms.openlocfilehash: 009686adfc054c7b6344f01edafedaf2921693d5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417957"
---
# <a name="dml_depth_space_order-enumeration-directmlh"></a>DML_DEPTH_SPACE_ORDER enumeración (directml.h)

Define constantes que controlan la transformación aplicada en los operadores directML [DML_OPERATOR_DEPTH_TO_SPACE1](/windows/win32/api/directml/ne-directml-dml_operator_type) y **DML_OPERATOR_SPACE_TO_DEPTH1**. Se usan dentro de las [estructuras DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) [y DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) datos.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
typedef enum DML_DEPTH_SPACE_ORDER {
  DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW,
  DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH
} ;
```

## <a name="constants"></a>Constantes

| Nombre | Descripción |
| ---- |:---- |
| DML_DEPTH_SPACE_ORDER_DEPTH_COLUMN_ROW | Hace que los tensores usados [en DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) y [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) se interpreten con los diseños siguientes, donde las dimensiones entre paréntesis se aplana.<br><br>- **Versión de** profundidad: [Batch, (BlockHeight, BlockWidth, Channels), Height, Width]<br>- **Versión del** espacio: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)] |
| DML_DEPTH_SPACE_ORDER_COLUMN_ROW_DEPTH | Hace que los tensores usados [en DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) y [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) se interpreten con los diseños siguientes, donde las dimensiones entre paréntesis se aplana.<br><br>- **Versión de** profundidad: [Batch, (Channels, BlockHeight, BlockWidth), Height, Width]<br>- **Versión del** espacio: [Batch, Channels, (Height, BlockHeight), (Width, BlockWidth)] |

## <a name="remarks"></a>Comentarios

Consulte [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md) y [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md) para obtener ejemplos que muestren el efecto de estos valores.

## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Vea también

* [DML_DEPTH_TO_SPACE1_OPERATOR_DESC](./ns-directml-dml_depth_to_space1_operator_desc.md)
* [DML_SPACE_TO_DEPTH1_OPERATOR_DESC](./ns-directml-dml_space_to_depth1_operator_desc.md)

## <a name="availability"></a>Disponibilidad
Esta enumeración se introdujo en `DML_FEATURE_LEVEL_2_1` .