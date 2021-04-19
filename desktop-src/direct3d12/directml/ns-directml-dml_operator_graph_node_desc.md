---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: 'Describe un nodo dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).'
helpviewer_keywords:
- DML_OPERATOR_GRAPH_NODE_DESC
- DML_OPERATOR_GRAPH_NODE_DESC structure
- direct3d12.dml_operator_graph_node_desc
- directml/DML_OPERATOR_GRAPH_NODE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/05/2020
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
- DML_OPERATOR_GRAPH_NODE_DESC
- directml/DML_OPERATOR_GRAPH_NODE_DESC
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
- DML_OPERATOR_GRAPH_NODE_DESC
ms.openlocfilehash: 6081f81044ff2ce384f7906af9c6e80f6b06f774
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721271"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a>DML_OPERATOR_GRAPH_NODE_DESC estructura (directml. h)
Describe un nodo dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

El comportamiento de este nodo lo define un operador DirectML.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_OPERATOR_GRAPH_NODE_DESC {
  IDMLOperator *Operator;
  const char   *Name;
};
```



## <a name="members"></a>Miembros

`Operator`

Tipo: <b> [IDMLOperator](/windows/win32/api/directml/nn-directml-idmloperator)*</b>

Operador DirectML que define el comportamiento del nodo.


`Name`

Tipo: \_ campo \_ z \_ \_ Maybenull \_ **const char \***

Un nombre opcional para la conexión del grafo. Si se proporciona, se podría usar dentro de ciertos mensajes de error emitidos por la capa de depuración DirectML.

## <a name="availability"></a>Disponibilidad

Esta API se presentó en la versión DirectML `1.1.0` .



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Vea también

* [IDMLDevice1:: CompileGraph (método)](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [Estructura de DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [Estructura de DML_GRAPH_NODE_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)