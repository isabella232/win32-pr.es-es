---
UID: NS:directml.DML_GRAPH_DESC
title: DML_GRAPH_DESC
description: Describe un gráfico de operadores de DirectML utilizados para compilar un operador combinado y optimizado.
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
ms.openlocfilehash: e72209d19bb26524576783becbbfbf94566d8370
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721282"
---
# <a name="dml_graph_desc-structure-directmlh"></a>DML_GRAPH_DESC estructura (directml. h)

Describe un gráfico de operadores de DirectML utilizados para compilar un operador combinado y optimizado. Vea [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

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

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de entradas del gráfico global. Cada entrada de gráfico puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *InputEdgeCount*.


`OutputCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de salidas del gráfico global. Cada salida del gráfico puede estar conectada a un número variable de nodos internos, por lo que puede ser diferente de *OutputEdgeCount*.


`NodeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

Número de nodos internos del gráfico.


`Nodes`

Tipo: \_ tamaño de campo \_ \_ (NodeCount) **const [DML_GRAPH_NODE_DESC](./ns-directml-dml_graph_node_desc.md) \***

Los nodos internos del gráfico.


`InputEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de conexiones entre las entradas del gráfico y las entradas de los nodos internos del gráfico.


`InputEdges`

Tipo: \_ tamaño de campo \_ \_ (InputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matriz de conexiones entre las entradas del gráfico y las entradas de los nodos internos del gráfico. El campo de *tipo* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_INPUT](./ne-directml-dml_graph_edge_type.md).


`OutputEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de conexiones entre las salidas del gráfico y las salidas de los nodos internos del gráfico.


`OutputEdges`

Tipo: \_ tamaño de campo \_ \_ (OutputEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matriz de conexiones entre las salidas del gráfico y las salidas de los nodos internos del gráfico. El campo de *tipo* dentro de cada elemento debe establecerse en [DML_GRAPH_EDGE_TYPE_OUTPUT](./ne-directml-dml_graph_edge_type.md).


`IntermediateEdgeCount`

Tipo: [ **uint**](/windows/desktop/winprog/windows-data-types)

El número de conexiones internas entre los nodos del gráfico.


`IntermediateEdges`

Tipo: \_ tamaño de campo \_ \_ (IntermediateEdgeCount) **const [DML_GRAPH_EDGE_DESC](./ns-directml-dml_graph_edge_desc.md) \***

Matriz de conexiones entre las entradas y las salidas de los nodos internos del gráfico. El campo de tipo dentro de cada elemento se debe establecer en [DML_GRAPH_EDGE_TYPE_INTERMEDIATE](./ne-directml-dml_graph_edge_type.md)


## <a name="remarks"></a>Observaciones
El gráfico descrito por esta estructura debe ser un gráfico acíclicos dirigido. Debe definir una conexión para la entrada y la salida de cada nodo proporcionado, excepto las entradas y salidas que son opcionales para el operador asociado.

Los nodos pueden usar operadores que se crearon con la marca [DML_TENSOR_FLAG_OWNED_BY_DML](/windows/win32/api/directml/ne-directml-dml_tensor_flags) para ciertas entradas. Cualquier entrada de operador que use esta marca debe estar conectada a entradas de grafos. Todas las entradas de operador conectadas a la misma entrada de gráfico deben usar u omitir esta marca de forma equivalente.

Es válido conectar los operadores cuyas entradas y salidas conectadas usan recuentos de dimensiones, tamaños y tipos de datos diferentes. Esto implica que cada operador interpreta de forma diferente el BLOB de datos tensores. Sin embargo, el campo *TotalTensorSizeInBytes* de entradas y salidas de tensores conectadas debe ser idéntico. Los operadores solo deben leer las regiones de los que han escrito los operadores anteriores. No se garantiza que las regiones de relleno de la salida de una operación (que resulten del uso de los progresos) se lean como cero por operadores de nivel inferior.

## <a name="availability"></a>Disponibilidad

Esta API se presentó en la versión DirectML `1.1.0` .


## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml. h |

## <a name="see-also"></a>Vea también

* [IDMLDevice1:: CompileGraph (método)](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_NODE_DESC struct](./ns-directml-dml_graph_node_desc.md)
* [DML_GRAPH_EDGE_DESC struct](./ns-directml-dml_graph_edge_desc.md)