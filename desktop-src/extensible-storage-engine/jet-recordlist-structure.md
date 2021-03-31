---
description: 'Más información acerca de: estructura de JET_RECORDLIST'
title: Estructura de JET_RECORDLIST
TOCTitle: JET_RECORDLIST Structure
ms:assetid: 6b4d97a0-4b42-4f7c-bb18-b6db3c92668a
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269287(v=EXCHG.10)
ms:contentKeyID: 32765579
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
ms.openlocfilehash: 16aca3a13bbae7c61bfe03aca49acea775820d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912990"
---
# <a name="jet_recordlist-structure"></a><span data-ttu-id="bb076-103">Estructura de JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="bb076-103">JET_RECORDLIST Structure</span></span>


<span data-ttu-id="bb076-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="bb076-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_recordlist-structure"></a><span data-ttu-id="bb076-105">Estructura de JET_RECORDLIST</span><span class="sxs-lookup"><span data-stu-id="bb076-105">JET_RECORDLIST Structure</span></span>

<span data-ttu-id="bb076-106">La estructura **JET_RECORDLIST** encuentra los registros que se encuentran en la intersección de los intervalos de índice especificados cuando se usan con la función [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="bb076-106">The **JET_RECORDLIST** structure finds records that are in the intersection of specified index ranges when they are used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      unsigned long cRecord;
      JET_COLUMNID columnidBookmark;
    } JET_RECORDLIST;
```

### <a name="members"></a><span data-ttu-id="bb076-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="bb076-107">Members</span></span>

<span data-ttu-id="bb076-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="bb076-108">**cbStruct**</span></span>

<span data-ttu-id="bb076-109">Tamaño de la estructura de **JET_RECORDLIST** , en bytes.</span><span class="sxs-lookup"><span data-stu-id="bb076-109">The size of the **JET_RECORDLIST** structure, in bytes.</span></span>

<span data-ttu-id="bb076-110">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="bb076-110">**tableid**</span></span>

<span data-ttu-id="bb076-111">Identificador de tabla de una tabla temporal que contiene los marcadores de los resultados de la consulta.</span><span class="sxs-lookup"><span data-stu-id="bb076-111">The table identifier of a temporary table that contains the bookmarks for the results of the query.</span></span> <span data-ttu-id="bb076-112">La tabla se cerrará automáticamente si la transacción actual se revierte con [JetRollback](./jetrollback-function.md); de lo contrario, debe cerrarse con [JetCloseTable](./jetclosetable-function.md).</span><span class="sxs-lookup"><span data-stu-id="bb076-112">The table will automatically be closed if the current transaction is rolled back with [JetRollback](./jetrollback-function.md); otherwise, it must be closed with [JetCloseTable](./jetclosetable-function.md).</span></span>

<span data-ttu-id="bb076-113">**cRecord**</span><span class="sxs-lookup"><span data-stu-id="bb076-113">**cRecord**</span></span>

<span data-ttu-id="bb076-114">Número de filas de la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="bb076-114">The number of rows in the temporary table.</span></span>

<span data-ttu-id="bb076-115">**columnidBookmark**</span><span class="sxs-lookup"><span data-stu-id="bb076-115">**columnidBookmark**</span></span>

<span data-ttu-id="bb076-116">El identificador de columna de la columna de marcador en la tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="bb076-116">The column identifier of the bookmark column in the temporary table.</span></span>

### <a name="remarks"></a><span data-ttu-id="bb076-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="bb076-117">Remarks</span></span>

<span data-ttu-id="bb076-118">La tabla temporal identificada por **TABLEID** tiene una sola columna.</span><span class="sxs-lookup"><span data-stu-id="bb076-118">The temporary table that is identified by **tableid** has a single column.</span></span> <span data-ttu-id="bb076-119">Esa columna única contiene marcadores y cada registro debe caber en un búfer de tamaño JET_cbBookmarkMost bytes.</span><span class="sxs-lookup"><span data-stu-id="bb076-119">That single column holds bookmarks, and each record should fit in a buffer of size JET_cbBookmarkMost bytes.</span></span>

### <a name="requirements"></a><span data-ttu-id="bb076-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bb076-120">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb076-121"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="bb076-121"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="bb076-122">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="bb076-122">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb076-123"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="bb076-123"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="bb076-124">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="bb076-124">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb076-125"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="bb076-125"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="bb076-126">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="bb076-126">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="bb076-127">Consulte también</span><span class="sxs-lookup"><span data-stu-id="bb076-127">See Also</span></span>

[<span data-ttu-id="bb076-128">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="bb076-128">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="bb076-129">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="bb076-129">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="bb076-130">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="bb076-130">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="bb076-131">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="bb076-131">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="bb076-132">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="bb076-132">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="bb076-133">JetRollback</span><span class="sxs-lookup"><span data-stu-id="bb076-133">JetRollback</span></span>](./jetrollback-function.md)
