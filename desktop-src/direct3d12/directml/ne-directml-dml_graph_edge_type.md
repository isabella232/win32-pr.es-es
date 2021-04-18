---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Define constantes que especifican un tipo de borde del gráfico. Consulte [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración.
helpviewer_keywords:
- DML_GRAPH_EDGE_TYPE
- DML_GRAPH_EDGE_TYPE structure
- direct3d12.dml_graph_edge_type
- directml/DML_GRAPH_EDGE_TYPE
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_EDGE_TYPE, DML_GRAPH_EDGE_TYPE structure, direct3d12.dml_graph_edge_type, directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
- directml/DML_GRAPH_EDGE_TYPE
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
- DML_GRAPH_EDGE_TYPE
ms.openlocfilehash: 19b11686f3741c386ca03e84af5a41af1ce5cb52
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721311"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>Enumeración DML_GRAPH_EDGE_TYPE (directml. h)

Define constantes que especifican un tipo de borde del gráfico. Consulte [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
typedef enum DML_GRAPH_EDGE_TYPE {
  DML_GRAPH_EDGE_TYPE_INVALID,
  DML_GRAPH_EDGE_TYPE_INPUT,
  DML_GRAPH_EDGE_TYPE_OUTPUT,
  DML_GRAPH_EDGE_TYPE_INTERMEDIATE
} ;
```

## <a name="constants"></a>Constantes

| Nombre | Descripción |
| ---- |:---- |
| DML_GRAPH_EDGE_TYPE_INVALID | Especifica un tipo de borde de gráfico desconocido y nunca es válido. Si se usa este valor, se producirá un error. |
| DML_GRAPH_EDGE_TYPE_INPUT | Especifica que la estructura de [DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) describe el borde del gráfico. |
| DML_GRAPH_EDGE_TYPE_OUTPUT | Especifica que la estructura de [DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) describe el borde del gráfico. |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | Especifica que la estructura de [DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) describe el borde del gráfico.<br><br># # Disponibilidad<br><br>Esta API se presentó en la versión DirectML `1.1.0` . |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Vea también

* [IDMLDevice1:: CompileGraph (método)](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Estructura de DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)     
* [Estructura de DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md)
* [Estructura de DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md)
* [Estructura de DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md)
* [Estructura de DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md)