---
description: 'Más información acerca de: JetDeleteTable (función)'
title: JetDeleteTable función)
TOCTitle: JetDeleteTable Function
ms:assetid: e8a4131f-a69b-41f3-94c6-a1607fc23c1f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294128(v=EXCHG.10)
ms:contentKeyID: 32765742
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDeleteTable
- JetDeleteTableA
- JetDeleteTableW
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c432f8e09ad706b6632e4e5ca49a89a263a84dbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717235"
---
# <a name="jetdeletetable-function"></a><span data-ttu-id="8221b-103">JetDeleteTable función)</span><span class="sxs-lookup"><span data-stu-id="8221b-103">JetDeleteTable Function</span></span>


<span data-ttu-id="8221b-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8221b-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdeletetable-function"></a><span data-ttu-id="8221b-105">JetDeleteTable función)</span><span class="sxs-lookup"><span data-stu-id="8221b-105">JetDeleteTable Function</span></span>

<span data-ttu-id="8221b-106">La función **JetDeleteTable** elimina una tabla en una base de datos ese.</span><span class="sxs-lookup"><span data-stu-id="8221b-106">The **JetDeleteTable** function deletes a table in an ESE database.</span></span>

```cpp
    JET_ERR JET_API JetDeleteTable(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          const tchar* szTableName
    );
```

### <a name="parameters"></a><span data-ttu-id="8221b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8221b-107">Parameters</span></span>

<span data-ttu-id="8221b-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8221b-108">*sesid*</span></span>

<span data-ttu-id="8221b-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="8221b-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="8221b-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="8221b-110">*dbid*</span></span>

<span data-ttu-id="8221b-111">Identificador de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="8221b-111">The database identifier to use for the API call.</span></span>

<span data-ttu-id="8221b-112">*szTableName*</span><span class="sxs-lookup"><span data-stu-id="8221b-112">*szTableName*</span></span>

<span data-ttu-id="8221b-113">Nombre de la tabla que se va a eliminar.</span><span class="sxs-lookup"><span data-stu-id="8221b-113">The name of the table to delete.</span></span>

### <a name="return-value"></a><span data-ttu-id="8221b-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8221b-114">Return Value</span></span>

<span data-ttu-id="8221b-115">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="8221b-115">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8221b-116">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8221b-116">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8221b-117">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8221b-117">Return code</span></span></p></th>
<th><p><span data-ttu-id="8221b-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="8221b-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8221b-119">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8221b-119">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8221b-120">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8221b-120">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8221b-121">JET_errTableInUse</span><span class="sxs-lookup"><span data-stu-id="8221b-121">JET_errTableInUse</span></span></p></td>
<td><p><span data-ttu-id="8221b-122">Se intentó eliminar una tabla mientras otra tiene un ID. de tabla abierta (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) con <a href="gg294118(v=exchg.10).md">JetOpenTable</a> o <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span><span class="sxs-lookup"><span data-stu-id="8221b-122">An attempt was made to delete a table while another session has an open table ID (<a href="gg269182(v=exchg.10).md">JET_TABLEID</a>) with <a href="gg294118(v=exchg.10).md">JetOpenTable</a> or <a href="gg269193(v=exchg.10).md">JetDupCursor</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8221b-123">JET_errCannotDeletetemporary tabla</span><span class="sxs-lookup"><span data-stu-id="8221b-123">JET_errCannotDeletetemporary table</span></span></p></td>
<td><p><span data-ttu-id="8221b-124">Se intentó eliminar una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="8221b-124">An attempt was made to delete a temporary table.</span></span> <span data-ttu-id="8221b-125">Una tabla temporal se elimina automáticamente cuando se cierra con <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span><span class="sxs-lookup"><span data-stu-id="8221b-125">A temporary table is automatically deleted when it is closed with <a href="gg294087(v=exchg.10).md">JetCloseTable</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8221b-126">JET_errCannotDeleteTemplateTable</span><span class="sxs-lookup"><span data-stu-id="8221b-126">JET_errCannotDeleteTemplateTable</span></span></p></td>
<td><p><span data-ttu-id="8221b-127">Se intentó eliminar una tabla de plantilla, es decir, una tabla de la que se puede heredar DDL.</span><span class="sxs-lookup"><span data-stu-id="8221b-127">An attempt was made to delete a template table, that is, a table from which DDL can be inherited.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="8221b-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8221b-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8221b-129"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8221b-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8221b-130">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8221b-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8221b-131"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8221b-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8221b-132">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8221b-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8221b-133"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8221b-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8221b-134">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8221b-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8221b-135"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="8221b-135"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8221b-136">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8221b-136">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8221b-137"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8221b-137"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8221b-138">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8221b-138">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8221b-139"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8221b-139"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8221b-140">Se implementa como <strong>JetDeleteTableW</strong> (Unicode) y <strong>JetDeleteTableA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8221b-140">Implemented as <strong>JetDeleteTableW</strong> (Unicode) and <strong>JetDeleteTableA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8221b-141">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8221b-141">See Also</span></span>

[<span data-ttu-id="8221b-142">JET_DBID</span><span class="sxs-lookup"><span data-stu-id="8221b-142">JET_DBID</span></span>](./jet-dbid.md)  
[<span data-ttu-id="8221b-143">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8221b-143">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8221b-144">JetCloseTable</span><span class="sxs-lookup"><span data-stu-id="8221b-144">JetCloseTable</span></span>](./jetclosetable-function.md)
