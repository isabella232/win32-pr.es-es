---
description: 'Más información acerca de: JetDetachDatabase (función)'
title: Función JetDetachDatabase
TOCTitle: JetDetachDatabase Function
ms:assetid: 629f19e5-99f3-425a-b6ba-de18daec7efe
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269266(v=EXCHG.10)
ms:contentKeyID: 32765568
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetDetachDatabaseW
- JetDetachDatabase
- JetDetachDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2e4437955acc0ed5714f7fbfb9f42fd4abafa58d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361584"
---
# <a name="jetdetachdatabase-function"></a><span data-ttu-id="17dea-103">Función JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="17dea-103">JetDetachDatabase Function</span></span>


<span data-ttu-id="17dea-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="17dea-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetdetachdatabase-function"></a><span data-ttu-id="17dea-105">Función JetDetachDatabase</span><span class="sxs-lookup"><span data-stu-id="17dea-105">JetDetachDatabase Function</span></span>

<span data-ttu-id="17dea-106">La función **JetDetachDatabase** libera un archivo de base de datos que se adjuntó previamente a una sesión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="17dea-106">The **JetDetachDatabase** function releases a database file that was previously attached to a database session.</span></span>

```cpp
    JET_ERR JET_API JetDetachDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename
    );
```

### <a name="parameters"></a><span data-ttu-id="17dea-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17dea-107">Parameters</span></span>

<span data-ttu-id="17dea-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="17dea-108">*sesid*</span></span>

<span data-ttu-id="17dea-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="17dea-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="17dea-110">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="17dea-110">*szFilename*</span></span>

<span data-ttu-id="17dea-111">Nombre de la base de datos que se va a desasociar.</span><span class="sxs-lookup"><span data-stu-id="17dea-111">The name of the database to detach.</span></span> <span data-ttu-id="17dea-112">Si *szFilename* es **null** o una cadena vacía, se desasociarán todas las bases de datos adjuntas a *sesid* .</span><span class="sxs-lookup"><span data-stu-id="17dea-112">If *szFilename* is **NULL** or an empty string, all databases attached to *sesid* will be detached.</span></span>

### <a name="return-value"></a><span data-ttu-id="17dea-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17dea-113">Return Value</span></span>

<span data-ttu-id="17dea-114">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="17dea-114">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="17dea-115">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="17dea-115">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17dea-116">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="17dea-116">Return code</span></span></p></th>
<th><p><span data-ttu-id="17dea-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="17dea-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17dea-118">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="17dea-118">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="17dea-119">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="17dea-119">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dea-120">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="17dea-120">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="17dea-121">Se está realizando una copia de seguridad de la base de datos y no se puede desasociar.</span><span class="sxs-lookup"><span data-stu-id="17dea-121">The database is being backed up, and cannot be detached.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17dea-122">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="17dea-122">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="17dea-123"><a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>ha abierto la base de datos.</span><span class="sxs-lookup"><span data-stu-id="17dea-123">The database has been opened by <a href="gg269299(v=exchg.10).md">JetOpenDatabase</a>.</span></span> <span data-ttu-id="17dea-124">Las bases de datos deben cerrarse antes de desasociar.</span><span class="sxs-lookup"><span data-stu-id="17dea-124">Databases must be closed prior to detaching.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dea-125">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="17dea-125">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="17dea-126">La base de datos no se adjuntó previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> o <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span><span class="sxs-lookup"><span data-stu-id="17dea-126">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a> or <a href="gg269322(v=exchg.10).md">JetAttachDatabase2</a>).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17dea-127">JET_errInTransaction</span><span class="sxs-lookup"><span data-stu-id="17dea-127">JET_errInTransaction</span></span></p></td>
<td><p><span data-ttu-id="17dea-128">Se intentó separar una base de datos mientras estaba en una transacción.</span><span class="sxs-lookup"><span data-stu-id="17dea-128">An attempt was made to detach a database while in a transaction.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="17dea-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17dea-129">Remarks</span></span>

<span data-ttu-id="17dea-130">Si se ha abierto una base de datos adjunta (con [JetAttachDatabase](./jetattachdatabase-function.md)), debe cerrarse con [JetCloseDatabase](./jetclosedatabase-function.md) antes de desasociar.</span><span class="sxs-lookup"><span data-stu-id="17dea-130">If an attached database was opened (with [JetAttachDatabase](./jetattachdatabase-function.md)), it must be closed with [JetCloseDatabase](./jetclosedatabase-function.md) prior to detaching.</span></span>

<span data-ttu-id="17dea-131">Solo Windows 2000: las bases de datos que no se han desasociado antes de llamar a [JetTerm](./jetterm-function.md) se volverán a adjuntar automáticamente cuando se llame a [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="17dea-131">Windows 2000 only: Databases which have not been detached prior to calling [JetTerm](./jetterm-function.md) will automatically be re-attached when [JetInit](./jetinit-function.md) is next called.</span></span>

#### <a name="requirements"></a><span data-ttu-id="17dea-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17dea-132">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17dea-133"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="17dea-133"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="17dea-134">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="17dea-134">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dea-135"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="17dea-135"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="17dea-136">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="17dea-136">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17dea-137"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="17dea-137"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="17dea-138">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="17dea-138">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dea-139"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="17dea-139"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="17dea-140">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="17dea-140">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17dea-141"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="17dea-141"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="17dea-142">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="17dea-142">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17dea-143"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="17dea-143"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="17dea-144">Se implementa como <strong>JetDetachDatabaseW</strong> (Unicode) y <strong>JetDetachDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="17dea-144">Implemented as <strong>JetDetachDatabaseW</strong> (Unicode) and <strong>JetDetachDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="17dea-145">Consulte también</span><span class="sxs-lookup"><span data-stu-id="17dea-145">See Also</span></span>

[<span data-ttu-id="17dea-146">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="17dea-146">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="17dea-147">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="17dea-147">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="17dea-148">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="17dea-148">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="17dea-149">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="17dea-149">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="17dea-150">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="17dea-150">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="17dea-151">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="17dea-151">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="17dea-152">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="17dea-152">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="17dea-153">JetCreateDatabase2</span><span class="sxs-lookup"><span data-stu-id="17dea-153">JetCreateDatabase2</span></span>](./jetcreatedatabase2-function.md)  
[<span data-ttu-id="17dea-154">JetCloseDatabase</span><span class="sxs-lookup"><span data-stu-id="17dea-154">JetCloseDatabase</span></span>](./jetclosedatabase-function.md)  
[<span data-ttu-id="17dea-155">JetTerm</span><span class="sxs-lookup"><span data-stu-id="17dea-155">JetTerm</span></span>](./jetterm-function.md)
