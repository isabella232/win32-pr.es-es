---
UID: NE:directml.DML_AXIS_DIRECTION
title: DML_AXIS_DIRECTION
description: Define constantes que especifican la dirección de una operación a lo largo del eje dado para el operador (por ejemplo, suma, selección de los elementos superiores k y selección del elemento mínimo).
ms.topic: reference
tech.root: directml
ms.date: 10/28/2020
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
- DML_AXIS_DIRECTION
- directml/DML_AXIS_DIRECTION
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
- DML_AXIS_DIRECTION
ms.openlocfilehash: e54d2abed3843ea9b2a22cb3c385f9edd1541ba5
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417958"
---
# <a name="dml_axis_direction-enumeration-directmlh"></a>DML_AXIS_DIRECTION enumeración (directml.h)

Define constantes que especifican la dirección de una operación a lo largo del eje dado para el operador (por ejemplo, suma, selección de los elementos superiores k y selección del elemento mínimo).

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
typedef enum DML_AXIS_DIRECTION {
  DML_AXIS_DIRECTION_INCREASING,
  DML_AXIS_DIRECTION_DECREASING
} ;
```

## <a name="constants"></a>Constantes

| Nombre | Descripción |
| ---- |:---- |
| DML_AXIS_DIRECTION_INCREASING | Especifica el orden creciente (del índice bajo al índice alto). |
| DML_AXIS_DIRECTION_DECREASING | Especifica el orden decreciente (del índice alto al índice bajo). |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |