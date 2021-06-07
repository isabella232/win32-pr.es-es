---
UID: NS:directml.DML_GRAPH_NODE_DESC
title: DML_GRAPH_NODE_DESC
description: Contenedor genérico para un nodo dentro de un gráfico de operadores directML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).
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
ms.openlocfilehash: 5f59978f6b62572000a95ee3be5a3b8a685c8231
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418039"
---
# <a name="dml_graph_node_desc-structure-directmlh"></a>DML_GRAPH_NODE_DESC estructura (directml.h)
Contenedor genérico para un nodo dentro de un gráfico de operadores directML definidos por [DML_GRAPH_DESC](./ns-directml-dml_graph_desc.md) y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

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

Tipo de nodo de grafo. Consulte [DML_GRAPH_NODE_TYPE](./ne-directml-dml_graph_node_type.md) para ver los tipos disponibles.


`Desc`

Tipo: \_ Tamaño del campo ( \_ \_ \_ inexpresable \_ ("Dependiente del tipo de nodo")) **const void \***

Puntero a la descripción del nodo de grafo. El tipo de la estructura a la que se apunta debe coincidir con el valor especificado en *Tipo*.

## <a name="availability"></a>Disponibilidad

Esta API se introdujo en la versión de `1.1.0` DirectML.



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Vea también

* [Método IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC estructura](./ns-directml-dml_graph_desc.md)