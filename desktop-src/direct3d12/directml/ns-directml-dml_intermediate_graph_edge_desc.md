---
UID: NS:directml.DML_INTERMEDIATE_GRAPH_EDGE_DESC
title: DML_INTERMEDIATE_GRAPH_EDGE_DESC
description: Describe una conexión dentro de un gráfico de operadores directML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Esta estructura se usa para definir una conexión entre nodos internos.
helpviewer_keywords:
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- DML_INTERMEDIATE_GRAPH_EDGE_DESC structure
- direct3d12.dml_intermediate_graph_edge_desc
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INTERMEDIATE_GRAPH_EDGE_DESC, DML_INTERMEDIATE_GRAPH_EDGE_DESC structure, direct3d12.dml_intermediate_graph_edge_desc, directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
- directml/DML_INTERMEDIATE_GRAPH_EDGE_DESC
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
- DML_INTERMEDIATE_GRAPH_EDGE_DESC
ms.openlocfilehash: 17cf62def075e84ba86e97a5adfa48fb452f475e
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417939"
---
# <a name="dml_intermediate_graph_edge_desc-structure-directmlh"></a>DML_INTERMEDIATE_GRAPH_EDGE_DESC estructura (directml.h)
Describe una conexión dentro de un gráfico de operadores directML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Esta estructura se usa para definir una conexión entre nodos internos.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores). Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_INTERMEDIATE_GRAPH_EDGE_DESC {
  UINT       FromNodeIndex;
  UINT       FromNodeOutputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Miembros

`FromNodeIndex`

Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**

Índice del nodo de grafo desde el que se especifica una conexión a otro nodo.


`FromNodeOutputIndex`

Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**

Índice de la salida en el nodo en el índice *FromNodeIndex* donde se especifica la conexión.


`ToNodeIndex`

Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**

Índice del nodo de grafo en el que se especifica una conexión desde otro nodo.


`ToNodeInputIndex`

Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**

Índice de la entrada en el nodo en el índice *ToNodeIndex* donde se especifica la conexión.


`Name`

Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***

Un nombre opcional para la conexión de grafo. Si se proporciona, esto podría usarse dentro de determinados mensajes de error emitidos por la capa de depuración de DirectML.

## <a name="availability"></a>Disponibilidad

Esta API se introdujo en la versión de `1.1.0` DirectML.



## <a name="requirements"></a>Requisitos
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Header** | directml.h |

## <a name="see-also"></a>Vea también

* [Método IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [DML_GRAPH_DESC estructura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [DML_GRAPH_EDGE_DESC estructura](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)