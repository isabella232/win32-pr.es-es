---
UID: NE:directml.DML_GRAPH_EDGE_TYPE
title: DML_GRAPH_EDGE_TYPE
description: Define constantes que especifican un tipo de borde de grafo. Vea [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración.
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
ms.openlocfilehash: d65649fcd2115cc7cdcc1b01da20ef44b0436e6f
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418106"
---
# <a name="dml_graph_edge_type-enumeration-directmlh"></a>DML_GRAPH_EDGE_TYPE enumeración (directml.h)

Define constantes que especifican un tipo de borde de grafo. Vea [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) para el uso de esta enumeración.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

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
| DML_GRAPH_EDGE_TYPE_INVALID | Especifica un tipo de borde de grafo desconocido y nunca es válido. El uso de este valor produce un error. |
| DML_GRAPH_EDGE_TYPE_INPUT | Especifica que el borde del grafo se describe mediante la [estructura DML_INPUT_GRAPH_EDGE_DESC](./ns-directml-dml_input_graph_edge_desc.md) gráfico. |
| DML_GRAPH_EDGE_TYPE_OUTPUT | Especifica que el borde del grafo se describe mediante la [estructura DML_OUTPUT_GRAPH_EDGE_DESC](./ns-directml-dml_output_graph_edge_desc.md) gráfico. |
| DML_GRAPH_EDGE_TYPE_INTERMEDIATE | Especifica que el borde del grafo se describe mediante la [estructura DML_INTERMEDIATE_GRAPH_EDGE_DESC](./ns-directml-dml_intermediate_graph_edge_desc.md) gráfico.<br><br>Disponibilidad de ##<br><br>Esta API se introdujo en la versión de `1.1.0` DirectML. |


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Vea también

* [Método IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC estructura](./ns-directml-dml_graph_desc.md)     
* [DML_GRAPH_EDGE_DESC estructura](./ns-directml-dml_graph_edge_desc.md)
* [DML_INPUT_GRAPH_EDGE_DESC estructura](./ns-directml-dml_input_graph_edge_desc.md)
* [DML_OUTPUT_GRAPH_EDGE_DESC estructura](./ns-directml-dml_output_graph_edge_desc.md)
* [DML_INTERMEDIATE_GRAPH_EDGE_DESC estructura](./ns-directml-dml_intermediate_graph_edge_desc.md)