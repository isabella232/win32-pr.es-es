---
description: 'Más información acerca de: estructura de JET_INDEXRANGE'
title: Estructura de JET_INDEXRANGE
TOCTitle: JET_INDEXRANGE Structure
ms:assetid: 8e437f7d-1e21-4a0b-a5a5-1c78235a4f80
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269335(v=EXCHG.10)
ms:contentKeyID: 32765624
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
ms.openlocfilehash: ecbd8151be8ef278fc1bddc12323f41abd05b09e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716541"
---
# <a name="jet_indexrange-structure"></a><span data-ttu-id="7de46-103">Estructura de JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="7de46-103">JET_INDEXRANGE Structure</span></span>


<span data-ttu-id="7de46-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7de46-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_indexrange-structure"></a><span data-ttu-id="7de46-105">Estructura de JET_INDEXRANGE</span><span class="sxs-lookup"><span data-stu-id="7de46-105">JET_INDEXRANGE Structure</span></span>

<span data-ttu-id="7de46-106">La estructura **JET_INDEXRANGE** identifica un intervalo de índice cuando se usa con la función [JetIntersectIndexes](./jetintersectindexes-function.md) .</span><span class="sxs-lookup"><span data-stu-id="7de46-106">The **JET_INDEXRANGE** structure identifies an index range when it is used with the [JetIntersectIndexes](./jetintersectindexes-function.md) function.</span></span>

```cpp
    typedef struct {
      unsigned long cbStruct;
      JET_TABLEID tableid;
      JET_GRBIT grbit;
    } JET_INDEXRANGE;
```

### <a name="members"></a><span data-ttu-id="7de46-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7de46-107">Members</span></span>

<span data-ttu-id="7de46-108">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="7de46-108">**cbStruct**</span></span>

<span data-ttu-id="7de46-109">Tamaño, en bytes, del **JET_INDEXRANGE**.</span><span class="sxs-lookup"><span data-stu-id="7de46-109">The size, in bytes, of the **JET_INDEXRANGE**.</span></span>

<span data-ttu-id="7de46-110">**TABLEID**</span><span class="sxs-lookup"><span data-stu-id="7de46-110">**tableid**</span></span>

<span data-ttu-id="7de46-111">Un cursor que previamente tenía un intervalo de índice establecido con [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="7de46-111">A cursor that has previously had an index range set with [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

<span data-ttu-id="7de46-112">**grbit**</span><span class="sxs-lookup"><span data-stu-id="7de46-112">**grbit**</span></span>

<span data-ttu-id="7de46-113">Máscara de código formada por exactamente uno de los siguientes elementos.</span><span class="sxs-lookup"><span data-stu-id="7de46-113">A bitmask composed of exactly one of the following.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7de46-114">Value</span><span class="sxs-lookup"><span data-stu-id="7de46-114">Value</span></span></p></th>
<th><p><span data-ttu-id="7de46-115">Significado</span><span class="sxs-lookup"><span data-stu-id="7de46-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7de46-116">JET_bitRecordInIndex</span><span class="sxs-lookup"><span data-stu-id="7de46-116">JET_bitRecordInIndex</span></span></p></td>
<td><p><span data-ttu-id="7de46-117">Especifica que el intervalo de índice se debe tratar normalmente.</span><span class="sxs-lookup"><span data-stu-id="7de46-117">Specifies that the index range should be treated normally.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7de46-118">JET_bitRecordNotInIndex</span><span class="sxs-lookup"><span data-stu-id="7de46-118">JET_bitRecordNotInIndex</span></span></p></td>
<td><p><span data-ttu-id="7de46-119">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="7de46-119">Reserved for future use.</span></span> <span data-ttu-id="7de46-120">No debe usarse.</span><span class="sxs-lookup"><span data-stu-id="7de46-120">Do not use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="7de46-121">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7de46-121">Remarks</span></span>

<span data-ttu-id="7de46-122">Cada estructura de **JET_INDEXRANGE** que se pasa a [JetIntersectIndexes](./jetintersectindexes-function.md) representa un intervalo de índice, que se intersectará con la llamada a la API.</span><span class="sxs-lookup"><span data-stu-id="7de46-122">Each **JET_INDEXRANGE** structure that is passed to [JetIntersectIndexes](./jetintersectindexes-function.md) represents an index range, which will be intersected by the API call.</span></span> <span data-ttu-id="7de46-123">El cursor que se proporciona en **JET_INDEXRANGE** debe tener un intervalo de índices válido establecido en él, con una llamada correcta a [JetSetIndexRange](./jetsetindexrange-function.md).</span><span class="sxs-lookup"><span data-stu-id="7de46-123">The cursor that is given in **JET_INDEXRANGE** must have a valid index range set on it already, with a successful call to [JetSetIndexRange](./jetsetindexrange-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="7de46-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7de46-124">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7de46-125"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7de46-125"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7de46-126">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="7de46-126">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7de46-127"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7de46-127"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7de46-128">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="7de46-128">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7de46-129"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7de46-129"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7de46-130">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7de46-130">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7de46-131">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7de46-131">See Also</span></span>

[<span data-ttu-id="7de46-132">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="7de46-132">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="7de46-133">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="7de46-133">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="7de46-134">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="7de46-134">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="7de46-135">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="7de46-135">JetCloseTable</span></span>](./jetclosetable-function.md)  
[<span data-ttu-id="7de46-136">JetIntersectIndexes</span><span class="sxs-lookup"><span data-stu-id="7de46-136">JetIntersectIndexes</span></span>](./jetintersectindexes-function.md)  
[<span data-ttu-id="7de46-137">JetSetIndexRange</span><span class="sxs-lookup"><span data-stu-id="7de46-137">JetSetIndexRange</span></span>](./jetsetindexrange-function.md)
