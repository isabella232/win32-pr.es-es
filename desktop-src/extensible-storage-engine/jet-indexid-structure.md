---
description: 'Más información acerca de: estructura de JET_INDEXID'
title: Estructura de JET_INDEXID
TOCTitle: JET_INDEXID Structure
ms:assetid: 8b1d90f0-bc93-4b30-90d1-b9e93ad26654
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269327(v=EXCHG.10)
ms:contentKeyID: 32765617
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e1a9c6a971e44604240d750163f0570937f9d4db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717244"
---
# <a name="jet_indexid-structure"></a><span data-ttu-id="c69d8-103">Estructura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="c69d8-103">JET_INDEXID Structure</span></span>


<span data-ttu-id="c69d8-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c69d8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexid-structure"></a><span data-ttu-id="c69d8-105">Estructura de JET_INDEXID</span><span class="sxs-lookup"><span data-stu-id="c69d8-105">JET_INDEXID Structure</span></span>

<span data-ttu-id="c69d8-106">La estructura de **JET_INDEXID** contiene un identificador de índice.</span><span class="sxs-lookup"><span data-stu-id="c69d8-106">The **JET_INDEXID** structure holds an index ID.</span></span> <span data-ttu-id="c69d8-107">Un ID. de índice es una sugerencia que se usa para acelerar la selección del índice actual mediante [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span><span class="sxs-lookup"><span data-stu-id="c69d8-107">An index ID is a hint that is used to accelerate the selection of the current index using [JetSetCurrentIndex](./jetsetcurrentindex-function.md).</span></span> <span data-ttu-id="c69d8-108">Resulta muy útil cuando hay un gran número de índices en una tabla.</span><span class="sxs-lookup"><span data-stu-id="c69d8-108">It is most useful when there is a very large number of indexes over a table.</span></span> <span data-ttu-id="c69d8-109">El identificador de índice se puede recuperar mediante [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="c69d8-109">The index ID can be retrieved using [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

```cpp
    typedef struct tagJET_INDEXID {
      unsigned long cbStruct;
      char rgbIndexId[sizeof(JET_API_PRT) + sizeof(unsigned long) + sizeof(unsigned long)];
    } JET_INDEXID;
```

### <a name="members"></a><span data-ttu-id="c69d8-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="c69d8-110">Members</span></span>

<span data-ttu-id="c69d8-111">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="c69d8-111">**cbStruct**</span></span>

<span data-ttu-id="c69d8-112">Tamaño, en bytes, del identificador de índice.</span><span class="sxs-lookup"><span data-stu-id="c69d8-112">The size, in bytes, of the index ID.</span></span>

<span data-ttu-id="c69d8-113">Es el tamaño real del ID. de índice que se devuelve en el búfer de salida de [JetGetIndexInfo](./jetgetindexinfo-function.md) o [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span><span class="sxs-lookup"><span data-stu-id="c69d8-113">This is the actual size of the index ID that is returned in the output buffer from [JetGetIndexInfo](./jetgetindexinfo-function.md) or [JetGetTableIndexInfo](./jetgettableindexinfo-function.md).</span></span>

<span data-ttu-id="c69d8-114">**rgbIndexId**</span><span class="sxs-lookup"><span data-stu-id="c69d8-114">**rgbIndexId**</span></span>

<span data-ttu-id="c69d8-115">Un BLOB opaco de información que utiliza el motor para identificar rápidamente un índice en su caché de esquema.</span><span class="sxs-lookup"><span data-stu-id="c69d8-115">An opaque BLOB of information that is used by the engine to quickly identify an index in its schema cache.</span></span>

<span data-ttu-id="c69d8-116">No intente interpretar el BLOB de información.</span><span class="sxs-lookup"><span data-stu-id="c69d8-116">Do not attempt to interpret the BLOB of information.</span></span> <span data-ttu-id="c69d8-117">No es un tamaño establecido.</span><span class="sxs-lookup"><span data-stu-id="c69d8-117">It is not a set size.</span></span>

### <a name="requirements"></a><span data-ttu-id="c69d8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c69d8-118">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c69d8-119"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c69d8-119"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c69d8-120">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c69d8-120">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c69d8-121"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c69d8-121"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c69d8-122">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c69d8-122">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c69d8-123"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c69d8-123"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c69d8-124">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c69d8-124">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="c69d8-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c69d8-125">See Also</span></span>

[<span data-ttu-id="c69d8-126">JetGetIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c69d8-126">JetGetIndexInfo</span></span>](./jetgetindexinfo-function.md)  
[<span data-ttu-id="c69d8-127">JetGetTableIndexInfo</span><span class="sxs-lookup"><span data-stu-id="c69d8-127">JetGetTableIndexInfo</span></span>](./jetgettableindexinfo-function.md)  
[<span data-ttu-id="c69d8-128">JetGetTableInfo</span><span class="sxs-lookup"><span data-stu-id="c69d8-128">JetGetTableInfo</span></span>](./jetgettableinfo-function.md)  
[<span data-ttu-id="c69d8-129">JetSetCurrentIndex</span><span class="sxs-lookup"><span data-stu-id="c69d8-129">JetSetCurrentIndex</span></span>](./jetsetcurrentindex-function.md)
