---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: 'Describe una conexión dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Esta estructura se usa para definir una conexión de una entrada de gráfico a una entrada de un nodo interno.'
helpviewer_keywords:
- DML_INPUT_GRAPH_EDGE_DESC
- DML_INPUT_GRAPH_EDGE_DESC structure
- direct3d12.dml_input_graph_edge_desc
- directml/DML_INPUT_GRAPH_EDGE_DESC
ms.topic: reference
tech.root: directml
ms.date: 11/02/2020
ms.keywords: DML_INPUT_GRAPH_EDGE_DESC, DML_INPUT_GRAPH_EDGE_DESC structure, direct3d12.dml_input_graph_edge_desc, directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
- directml/DML_INPUT_GRAPH_EDGE_DESC
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
- DML_INPUT_GRAPH_EDGE_DESC
ms.openlocfilehash: 180bfc89a37aad2ba0b6f287c302aa30b0b04110
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/10/2021
ms.locfileid: "105721279"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a>DML_INPUT_GRAPH_EDGE_DESC estructura (directml. h)
Describe una conexión dentro de un gráfico de operadores DirectML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y que se pasa a [IDMLDevice1:: CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Esta estructura se usa para definir una conexión de una entrada de gráfico a una entrada de un nodo interno.

> [!IMPORTANT]
> Esta API está disponible como parte del paquete redistribuible de DirectML independiente (consulte [Microsoft. AI. DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/). Consulte también el [historial de versiones de DirectML](../dml-version-history.md).

## <a name="syntax"></a>Sintaxis
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a>Miembros

`GraphInputIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Índice de la entrada de gráfico desde la que se especifica una conexión a una entrada de nodo interna.


`ToNodeIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Índice del nodo interno en el que se especifica la conexión de la entrada del gráfico.


`ToNodeInputIndex`

Tipo: **[uint](/windows/desktop/winprog/windows-data-types)**

Índice de la entrada en el nodo interno en el que se especifica la conexión.


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
* [Estructura de DML_GRAPH_EDGE_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)