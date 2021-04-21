---
UID: NS:directml.DML_OPERATOR_GRAPH_NODE_DESC
title: DML_OPERATOR_GRAPH_NODE_DESC
description: Describe un nodo dentro de un gráfico [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) de operadores de DirectML definidos por DML_GRAPH_DESC y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).
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
ms.openlocfilehash: 997f441de76a60229b76f2f7d67b7acf1a26ed5f
ms.sourcegitcommit: 8e1f04c7e3c5c850071bac8d173f9441aab0dfed
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/21/2021
ms.locfileid: "107803563"
---
# <a name="dml_operator_graph_node_desc-structure-directmlh"></a>DML_OPERATOR_GRAPH_NODE_DESC estructura (directml.h)
Describe un nodo dentro de un gráfico [](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) de operadores de DirectML definidos por DML_GRAPH_DESC y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

El comportamiento de este nodo se define mediante un operador directML.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

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

Operador directML que define el comportamiento del nodo.


`Name`

Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***

Un nombre opcional para la conexión de grafo. Si se proporciona, esto podría usarse dentro de determinados mensajes de error emitidos por la capa de depuración de DirectML.

## <a name="availability"></a>Disponibilidad

Esta API se introdujo en la versión de `1.1.0` DirectML.



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Consulta también

* [Método IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC estructura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_NODE_DESC estructura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_node_desc)