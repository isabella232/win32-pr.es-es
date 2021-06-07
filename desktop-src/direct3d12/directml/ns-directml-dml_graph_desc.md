---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Describe un gráfico de operadores directML usados para compilar un operador optimizado combinado.
helpviewer_keywords:
- DML_GRAPH_DESC
- DML_GRAPH_DESC structure
- direct3d12.dml_graph_desc
- directml/DML_GRAPH_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_GRAPH_DESC, DML_GRAPH_DESC structure, direct3d12.dml_graph_desc, directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
- directml/DML_GRAPH_DESC
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
- DML_GRAPH_DESC
ms.openlocfilehash: a42996fc9fd7825e13232b245ab764c6439f9489
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111418046"
---
# <a name="dml_graph_desc-structure-directmlh"></a>DML_GRAPH_DESC estructura (directml.h)

Describe un gráfico de operadores directML usados para compilar un operador optimizado combinado. Vea [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_GRAPH_DESC {
  UINT                      InputCount;
  UINT                      OutputCount;
  UINT                      NodeCount;
  const DML_GRAPH_NODE_DESC *Nodes;
  UINT                      InputEdgeCount;
  const DML_GRAPH_EDGE_DESC *InputEdges;
  UINT                      OutputEdgeCount;
  const DML_GRAPH_EDGE_DESC *OutputEdges;
  UINT                      IntermediateEdgeCount;
  const DML_GRAPH_EDGE_DESC *IntermediateEdges;
};
```



## <a name="members"></a>Miembros

`InputCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de entradas del gráfico general. Cada entrada de grafo puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *InputEdgeCount.*


`OutputCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de salidas del gráfico general. Cada salida de grafo puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *OutputEdgeCount.*


`NodeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de nodos internos del gráfico.


`Nodes`

Tipo: \_ Tamaño de campo \_ \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Nodos internos del gráfico.


`InputEdgeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de conexiones entre las entradas del grafo y las entradas de los nodos internos del gráfico.


`InputEdges`

Tipo: \_ Tamaño de campo \_ \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matriz de conexiones entre las entradas del grafo y las entradas de los nodos internos del gráfico. El *campo Type* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de conexiones entre las salidas del grafo y las salidas de los nodos internos del gráfico.


`OutputEdges`

Tipo: \_ Tamaño de campo \_ \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matriz de conexiones entre las salidas del grafo y las salidas de los nodos internos del gráfico. El *campo Type* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Tipo: [ **UINT**](/windows/desktop/winprog/windows-data-types)

Número de conexiones internas entre nodos del gráfico.


`IntermediateEdges`

Tipo: \_ Tamaño de campo \_ \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matriz de conexiones entre las entradas y salidas de los nodos internos del gráfico. El campo Type dentro de cada elemento debe establecerse [en DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Comentarios
El gráfico descrito por esta estructura debe ser un grafo acíclico dirigido. Debe definir una conexión para la entrada y salida de cada nodo proporcionado, excepto las entradas y salidas que son opcionales para el operador asociado.

Los nodos pueden usar operadores que se crearon [mediante la DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) para determinadas entradas. Todas las entradas de operador que usan esta marca deben estar conectadas a entradas de grafo. Todas las entradas de operador conectadas a la misma entrada de grafo deben usar u omitir esta marca de forma equivalente.

Es legal conectar operadores cuyas entradas y salidas conectadas usan diferentes recuentos de dimensiones, tamaños y tipos de datos. Esto implica que cada operador interpreta de forma diferente el blob de datos tensor. Sin embargo, el campo *TotalTensorSizeInBytes* de entradas y salidas del tensor conectado debe ser idéntico. Los operadores solo deben leer regiones de tensores escritas por operadores anteriores. No se garantiza que los operadores de flujo inferior lean como cero las regiones de relleno de la salida de una operación (resultante del uso de strides).

## <a name="availability"></a>Disponibilidad

Esta API se introdujo en la versión de `1.1.0` DirectML.


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Vea también

* [Método IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC struct](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC struct](./ns-directml-dml_graph_edge_desc.md)