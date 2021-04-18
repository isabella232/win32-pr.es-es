---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: 'Un contenedor genérico para un nodo dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_GRAPH_NODE_DESC
- DML_GRAPH_NODE_DESC structure
- direct3d12.dml_graph_node_desc
- directml/DML_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_NODE_DESC, DML_GRAPH_NODE_DESC structure, direct3d12.dml_graph_node_desc, directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
- directml/DML_GRAPH_NODE_DESC
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
- DML_GRAPH_NODE_DESC
ms.openlocfilehash: 8c79719f51efb4a59f9459a28765d3442ed3f4ee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721304"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a>DML_GRAPH_NODE_DESC estructura (directml. h)
Un contenedor genérico para un nodo dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_GRAPH_NODE_DESC {
  DML_GRAPH_NODE_TYPE Type;
  const void          *Desc;
};
```



## <a name="members"></a>Miembros

`Type`

Tipo: **[DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md)**

El tipo de nodo de gráfico. Vea [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) para ver los tipos disponibles.


`Desc`

Tipo: \_ \_ tamaño \_ del campo ( \_ inexpress \_ ("depende del tipo de nodo")) **const \* void**

Un puntero a la descripción del nodo del gráfico. El tipo del struct señalado debe coincidir con el valor especificado en el *tipo*.

## <a name="availability"></a>Disponibilidad

Esta API se presentó en la versión DirectML `1.1.0` .



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Vea también

* [IDMLDevice1:: CompileGraph (método)](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Estructura de DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md)