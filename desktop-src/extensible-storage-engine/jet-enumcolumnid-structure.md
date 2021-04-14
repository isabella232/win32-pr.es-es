---
description: 'Más información acerca de: estructura de JET_ENUMCOLUMNID'
title: Estructura de JET_ENUMCOLUMNID
TOCTitle: JET_ENUMCOLUMNID Structure
ms:assetid: 5480ebf1-4fc9-49b5-bbb3-12542b86c8f1
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269251(v=EXCHG.10)
ms:contentKeyID: 32765553
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
ms.openlocfilehash: 356b2a31c682a6ed0392a875c606cfaf20f1aeea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541470"
---
# <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="d7a3f-103">Estructura de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="d7a3f-103">JET_ENUMCOLUMNID Structure</span></span>


<span data-ttu-id="d7a3f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d7a3f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnid-structure"></a><span data-ttu-id="d7a3f-105">Estructura de JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="d7a3f-105">JET_ENUMCOLUMNID Structure</span></span>

<span data-ttu-id="d7a3f-106">La estructura **JET_ENUMCOLUMNID** enumera un conjunto específico de columnas y, opcionalmente, un conjunto específico de varios valores para esas columnas cuando se usa la función [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="d7a3f-106">The **JET_ENUMCOLUMNID** structure enumerates a specific set of columns and, optionally, a specific set of multiple values for those columns when the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function is used.</span></span> <span data-ttu-id="d7a3f-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de estructuras **JET_ENUMCOLUMNID** .</span><span class="sxs-lookup"><span data-stu-id="d7a3f-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNID** structures.</span></span>

```cpp
    typedef struct {
      JET_COLUMNID columnid;
      unsigned long ctagSequence;
      unsigned long* rgtagSequence;
    } JET_ENUMCOLUMNID;
```

### <a name="members"></a><span data-ttu-id="d7a3f-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="d7a3f-108">Members</span></span>

<span data-ttu-id="d7a3f-109">**columnid**</span><span class="sxs-lookup"><span data-stu-id="d7a3f-109">**columnid**</span></span>

<span data-ttu-id="d7a3f-110">IDENTIFICADOR de columna que se va a enumerar.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-110">The column ID to enumerate.</span></span>

<span data-ttu-id="d7a3f-111">Si el ID. de columna es 0 (cero), la enumeración de esta columna se omite y se generará una ranura correspondiente en la matriz de salida de [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) estructuras con un estado de columna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-111">If the column ID is 0 (zero) then the enumeration of this column is skipped and a corresponding slot in the output array of [JET_ENUMCOLUMN](./jet-enumcolumn-structure.md) structures will be generated with a column state of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="d7a3f-112">**ctagSequence**</span><span class="sxs-lookup"><span data-stu-id="d7a3f-112">**ctagSequence**</span></span>

<span data-ttu-id="d7a3f-113">Opcionalmente, identifica una matriz de valores de columna (por índice de base uno) que se va a enumerar para el ID. de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-113">Optionally identifies an array of column values (by one-based index) to enumerate for the specified column ID.</span></span>

<span data-ttu-id="d7a3f-114">Si **ctagSequence** es 0 (cero), se omite **rgtagSequence** y se enumeran todos los valores de columna para el ID. de columna especificado.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-114">If **ctagSequence** is 0 (zero) then **rgtagSequence** is ignored and all column values for the specified column ID will be enumerated.</span></span>

<span data-ttu-id="d7a3f-115">Si un elemento de **rgtagSequence** es 0 (cero), se omitirá la enumeración de ese valor de columna (por índice basado en uno).</span><span class="sxs-lookup"><span data-stu-id="d7a3f-115">If an element of **rgtagSequence** is 0 (zero), then the enumeration of that column value (by one-based index) will be skipped.</span></span> <span data-ttu-id="d7a3f-116">Se generará una ranura correspondiente en la matriz de salida de la estructura **JET_ENUMCOLUMNID** con un valor de estado de columna de JET_wrnColumnSkipped.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-116">A corresponding slot in the output array of the **JET_ENUMCOLUMNID** structure will be generated with a column status value of JET_wrnColumnSkipped.</span></span>

<span data-ttu-id="d7a3f-117">**rgtagSequence**</span><span class="sxs-lookup"><span data-stu-id="d7a3f-117">**rgtagSequence**</span></span>

<span data-ttu-id="d7a3f-118">Matriz de índices basados en uno en la matriz de valores de columna de una columna determinada.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-118">An array of one-based indices into the array of column values for a given column.</span></span> <span data-ttu-id="d7a3f-119">Un único elemento es un **itagSequence** que se define en [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d7a3f-119">A single element is an **itagSequence** which is defined in [JET_RETRIEVECOLUMN](./jet-retrievecolumn-structure.md).</span></span> <span data-ttu-id="d7a3f-120">Un valor de **itagSequence** de 0 (cero) significa "SKIP".</span><span class="sxs-lookup"><span data-stu-id="d7a3f-120">An **itagSequence** of 0 (zero) means "skip".</span></span> <span data-ttu-id="d7a3f-121">Un **itagSequence** de 1 significa devolver el valor de la primera columna de la columna, 2 significa el segundo, etc.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-121">An **itagSequence** of 1 means return the first column value of the column, 2 means the second, and so on.</span></span>

### <a name="requirements"></a><span data-ttu-id="d7a3f-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7a3f-122">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d7a3f-123"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d7a3f-123"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d7a3f-124">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-124">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d7a3f-125"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d7a3f-125"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d7a3f-126">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-126">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d7a3f-127"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d7a3f-127"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d7a3f-128">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="d7a3f-128">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d7a3f-129">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d7a3f-129">See Also</span></span>

[<span data-ttu-id="d7a3f-130">JET_COLUMNID</span><span class="sxs-lookup"><span data-stu-id="d7a3f-130">JET_COLUMNID</span></span>](./jet-columnid.md)  
[<span data-ttu-id="d7a3f-131">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="d7a3f-131">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="d7a3f-132">JET_ENUMCOLUMNID</span><span class="sxs-lookup"><span data-stu-id="d7a3f-132">JET_ENUMCOLUMNID</span></span>]()  
[<span data-ttu-id="d7a3f-133">JET_RETRIEVECOLUMN</span><span class="sxs-lookup"><span data-stu-id="d7a3f-133">JET_RETRIEVECOLUMN</span></span>](./jet-retrievecolumn-structure.md)  
[<span data-ttu-id="d7a3f-134">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="d7a3f-134">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)
