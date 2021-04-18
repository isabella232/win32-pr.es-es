---
description: 'Más información acerca de: estructura de JET_ENUMCOLUMNVALUE'
title: Estructura de JET_ENUMCOLUMNVALUE
TOCTitle: JET_ENUMCOLUMNVALUE Structure
ms:assetid: a9882d7b-0c53-4a5d-bc98-0979e6e68c88
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294052(v=EXCHG.10)
ms:contentKeyID: 32765652
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
ms.openlocfilehash: bc95c6b8403a64432451ea29dbb66868fad25264
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697530"
---
# <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="8e73b-103">Estructura de JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="8e73b-103">JET_ENUMCOLUMNVALUE Structure</span></span>


<span data-ttu-id="8e73b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8e73b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_enumcolumnvalue-structure"></a><span data-ttu-id="8e73b-105">Estructura de JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="8e73b-105">JET_ENUMCOLUMNVALUE Structure</span></span>

<span data-ttu-id="8e73b-106">La estructura **JET_ENUMCOLUMNVALUE** enumera los valores de columna de un registro mediante la función [JetEnumerateColumns](./jetenumeratecolumns-function.md) .</span><span class="sxs-lookup"><span data-stu-id="8e73b-106">The **JET_ENUMCOLUMNVALUE** structure enumerates the column values of a record using the [JetEnumerateColumns](./jetenumeratecolumns-function.md) function.</span></span> <span data-ttu-id="8e73b-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) devuelve una matriz de estructuras **JET_ENUMCOLUMNVALUE** .</span><span class="sxs-lookup"><span data-stu-id="8e73b-107">[JetEnumerateColumns](./jetenumeratecolumns-function.md) returns an array of **JET_ENUMCOLUMNVALUE** structures.</span></span> <span data-ttu-id="8e73b-108">La matriz se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a esa función.</span><span class="sxs-lookup"><span data-stu-id="8e73b-108">The array is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to that function.</span></span>

```cpp
    typedef struct {
      unsigned long itagSequence;
      JET_ERR err;
      unsigned long cbData;
      void* pvData;
    } JET_ENUMCOLUMNVALUE;
```

### <a name="members"></a><span data-ttu-id="8e73b-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="8e73b-109">Members</span></span>

<span data-ttu-id="8e73b-110">**itagSequence**</span><span class="sxs-lookup"><span data-stu-id="8e73b-110">**itagSequence**</span></span>

<span data-ttu-id="8e73b-111">Valor de columna (por índice de base uno) que se enumeró.</span><span class="sxs-lookup"><span data-stu-id="8e73b-111">The column value (by one-based index) that was enumerated.</span></span>

<span data-ttu-id="8e73b-112">**ERR**</span><span class="sxs-lookup"><span data-stu-id="8e73b-112">**err**</span></span>

<span data-ttu-id="8e73b-113">El código de estado de la columna resultante de la enumeración del valor de la columna.</span><span class="sxs-lookup"><span data-stu-id="8e73b-113">The column status code resulting from the enumeration of the column value.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8e73b-114">Value</span><span class="sxs-lookup"><span data-stu-id="8e73b-114">Value</span></span></p></th>
<th><p><span data-ttu-id="8e73b-115">Significado</span><span class="sxs-lookup"><span data-stu-id="8e73b-115">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e73b-116">JET_wrnColumnNull</span><span class="sxs-lookup"><span data-stu-id="8e73b-116">JET_wrnColumnNull</span></span></p></td>
<td><p><span data-ttu-id="8e73b-117">El valor de la columna solicitada es NULL.</span><span class="sxs-lookup"><span data-stu-id="8e73b-117">The requested column value is NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e73b-118">JET_wrnColumnSkipped</span><span class="sxs-lookup"><span data-stu-id="8e73b-118">JET_wrnColumnSkipped</span></span></p></td>
<td><p><span data-ttu-id="8e73b-119">El <em>itagSequence</em> que se especifica en el elemento de la matriz <em>rgtagSequence</em> en el <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct correspondiente a este <strong>JET_ENUMCOLUMNVALUE</strong> struct era cero.</span><span class="sxs-lookup"><span data-stu-id="8e73b-119">The <em>itagSequence</em> that is specified in the element of the <em>rgtagSequence</em> array in the <a href="gg294138(v=exchg.10).md">JET_ENUMCOLUMN</a> struct corresponding to this <strong>JET_ENUMCOLUMNVALUE</strong> struct was zero.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e73b-120">JET_wrnColumnTruncated</span><span class="sxs-lookup"><span data-stu-id="8e73b-120">JET_wrnColumnTruncated</span></span></p></td>
<td><p><span data-ttu-id="8e73b-121">El valor de la columna solicitada se truncó hasta el tamaño especificado antes de devolverse.</span><span class="sxs-lookup"><span data-stu-id="8e73b-121">The requested column value was truncated to the specified size before being returned.</span></span></p>
<p><span data-ttu-id="8e73b-122">Este truncamiento solo se produce para las columnas de texto largo y Long Binary que contienen grandes cantidades de datos.</span><span class="sxs-lookup"><span data-stu-id="8e73b-122">This truncation occurs only for long text and long binary columns that contain large amounts of data.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8e73b-123">**cbData**</span><span class="sxs-lookup"><span data-stu-id="8e73b-123">**cbData**</span></span>

<span data-ttu-id="8e73b-124">Valor de columna que se enumeró para la columna.</span><span class="sxs-lookup"><span data-stu-id="8e73b-124">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="8e73b-125">El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="8e73b-125">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

<span data-ttu-id="8e73b-126">**pvData**</span><span class="sxs-lookup"><span data-stu-id="8e73b-126">**pvData**</span></span>

<span data-ttu-id="8e73b-127">Valor de columna que se enumeró para la columna.</span><span class="sxs-lookup"><span data-stu-id="8e73b-127">The column value that was enumerated for the column.</span></span>

<span data-ttu-id="8e73b-128">El búfer de salida se devuelve en memoria que se asignó mediante la devolución de llamada compatible con [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) que se proporcionó a [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span><span class="sxs-lookup"><span data-stu-id="8e73b-128">The output buffer is returned in memory that was allocated using the [realloc](/cpp/c-runtime-library/reference/realloc?view=vs-2019) compatible callback that was supplied to [JetEnumerateColumns](./jetenumeratecolumns-function.md).</span></span>

### <a name="requirements"></a><span data-ttu-id="8e73b-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8e73b-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8e73b-130"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8e73b-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8e73b-131">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8e73b-131">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8e73b-132"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8e73b-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8e73b-133">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8e73b-133">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8e73b-134"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8e73b-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8e73b-135">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8e73b-135">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="8e73b-136">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8e73b-136">See Also</span></span>

[<span data-ttu-id="8e73b-137">JET_ENUMCOLUMN</span><span class="sxs-lookup"><span data-stu-id="8e73b-137">JET_ENUMCOLUMN</span></span>](./jet-enumcolumn-structure.md)  
[<span data-ttu-id="8e73b-138">JET_ENUMCOLUMNVALUE</span><span class="sxs-lookup"><span data-stu-id="8e73b-138">JET_ENUMCOLUMNVALUE</span></span>]()  
[<span data-ttu-id="8e73b-139">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8e73b-139">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8e73b-140">JetEnumerateColumns</span><span class="sxs-lookup"><span data-stu-id="8e73b-140">JetEnumerateColumns</span></span>](./jetenumeratecolumns-function.md)  
[<span data-ttu-id="8e73b-141">realloc</span><span class="sxs-lookup"><span data-stu-id="8e73b-141">realloc</span></span>](/cpp/c-runtime-library/reference/realloc?view=vs-2019)
