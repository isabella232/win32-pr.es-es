---
UID: NS:directml.DML_INPUT_GRAPH_EDGE_DESC
title: DML_INPUT_GRAPH_EDGE_DESC
description: Describe una conexión dentro de un gráfico de operadores directML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph). Esta estructura se usa para definir una conexión desde una entrada de grafo a una entrada de un nodo interno.
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
ms.openlocfilehash: 00fcece76f4cb7ac46589914df4d74321d957fbc
ms.sourcegitcommit: da68ed5718ec0e3aa0c252fc86ac3e275da91b82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/04/2021
ms.locfileid: "111417938"
---
# <a name="dml_input_graph_edge_desc-structure-directmlh"></a><span data-ttu-id="7e1ff-104">DML_INPUT_GRAPH_EDGE_DESC estructura (directml.h)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-104">DML_INPUT_GRAPH_EDGE_DESC structure (directml.h)</span></span>
<span data-ttu-id="7e1ff-105">Describe una conexión dentro de un gráfico de operadores directML definidos por [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) y pasados a [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span><span class="sxs-lookup"><span data-stu-id="7e1ff-105">Describes a connection within a graph of DirectML operators defined by [DML_GRAPH_DESC](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc) and passed to [IDMLDevice1::CompileGraph](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph).</span></span> <span data-ttu-id="7e1ff-106">Esta estructura se usa para definir una conexión desde una entrada de grafo a una entrada de un nodo interno.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-106">This structure is used to define a connection from a graph input to an input of an internal node.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7e1ff-107">Esta API está disponible como parte del paquete redistribuible independiente de DirectML (consulte [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) versión 1.4 y posteriores).</span><span class="sxs-lookup"><span data-stu-id="7e1ff-107">This API is available as part of the DirectML standalone redistributable package (see [Microsoft.AI.DirectML](https://www.nuget.org/packages/Microsoft.AI.DirectML/) version 1.4 and later.</span></span> <span data-ttu-id="7e1ff-108">Consulte también Historial [de versiones de DirectML.](../dml-version-history.md)</span><span class="sxs-lookup"><span data-stu-id="7e1ff-108">Also see [DirectML version history](../dml-version-history.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="7e1ff-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7e1ff-109">Syntax</span></span>
```cpp
struct DML_INPUT_GRAPH_EDGE_DESC {
  UINT       GraphInputIndex;
  UINT       ToNodeIndex;
  UINT       ToNodeInputIndex;
  const char *Name;
};
```



## <a name="members"></a><span data-ttu-id="7e1ff-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="7e1ff-110">Members</span></span>

`GraphInputIndex`

<span data-ttu-id="7e1ff-111">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7e1ff-111">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="7e1ff-112">Índice de la entrada del gráfico desde la que se especifica una conexión a una entrada de nodo interno.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-112">The index of the graph input from which a connection to an internal node input is specified.</span></span>


`ToNodeIndex`

<span data-ttu-id="7e1ff-113">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7e1ff-113">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="7e1ff-114">Índice del nodo interno en el que se especifica la conexión desde la entrada del gráfico.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-114">The index of the internal node onto which the connection from the graph input is specified.</span></span>


`ToNodeInputIndex`

<span data-ttu-id="7e1ff-115">Tipo: **[UINT](/windows/desktop/winprog/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="7e1ff-115">Type: **[UINT](/windows/desktop/winprog/windows-data-types)**</span></span>

<span data-ttu-id="7e1ff-116">Índice de la entrada en el nodo interno donde se especifica la conexión.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-116">The index of the input on the internal node where the connection is specified.</span></span>


`Name`

<span data-ttu-id="7e1ff-117">Tipo: \_ Campo \_ z \_ \_ Maybenull \_ **const char \***</span><span class="sxs-lookup"><span data-stu-id="7e1ff-117">Type: \_Field\_z\_ \_Maybenull\_ **const char\***</span></span>

<span data-ttu-id="7e1ff-118">Un nombre opcional para la conexión de grafo.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-118">An optional name for the graph connection.</span></span> <span data-ttu-id="7e1ff-119">Si se proporciona, esto podría usarse dentro de determinados mensajes de error emitidos por la capa de depuración de DirectML.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-119">If provided, this might be used within certain error messages emitted by the DirectML debug layer.</span></span>

## <a name="availability"></a><span data-ttu-id="7e1ff-120">Disponibilidad</span><span class="sxs-lookup"><span data-stu-id="7e1ff-120">Availability</span></span>

<span data-ttu-id="7e1ff-121">Esta API se introdujo en la versión de `1.1.0` DirectML.</span><span class="sxs-lookup"><span data-stu-id="7e1ff-121">This API was introduced in DirectML version `1.1.0`.</span></span>



## <a name="requirements"></a><span data-ttu-id="7e1ff-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e1ff-122">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="7e1ff-123">**Header**</span><span class="sxs-lookup"><span data-stu-id="7e1ff-123">**Header**</span></span> | <span data-ttu-id="7e1ff-124">directml.h</span><span class="sxs-lookup"><span data-stu-id="7e1ff-124">directml.h</span></span> |

## <a name="see-also"></a><span data-ttu-id="7e1ff-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="7e1ff-125">See also</span></span>

* [<span data-ttu-id="7e1ff-126">Método IDMLDevice1::CompileGraph</span><span class="sxs-lookup"><span data-stu-id="7e1ff-126">IDMLDevice1::CompileGraph method</span></span>](/windows/desktop/direct3d12/directml/nf-directml-idmldevice1-compilegraph)
* [<span data-ttu-id="7e1ff-127">DML_GRAPH_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="7e1ff-127">DML_GRAPH_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_desc)
* [<span data-ttu-id="7e1ff-128">DML_GRAPH_EDGE_DESC estructura</span><span class="sxs-lookup"><span data-stu-id="7e1ff-128">DML_GRAPH_EDGE_DESC structure</span></span>](/windows/desktop/direct3d12/directml/ns-directml-dml_graph_edge_desc)