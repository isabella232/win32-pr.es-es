---
description: 'Más información acerca de: JetOpenDatabase (función)'
title: Función JetOpenDatabase
TOCTitle: JetOpenDatabase Function
ms:assetid: 7764f0c2-6795-4b93-be3d-f6830cdce369
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269299(v=EXCHG.10)
ms:contentKeyID: 32765591
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetOpenDatabase
- JetOpenDatabaseW
- JetOpenDatabaseA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3492a037ac0c52a78bbe3265bd629969c301771c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819075"
---
# <a name="jetopendatabase-function"></a><span data-ttu-id="8ee98-103">Función JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="8ee98-103">JetOpenDatabase Function</span></span>


<span data-ttu-id="8ee98-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="8ee98-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetopendatabase-function"></a><span data-ttu-id="8ee98-105">Función JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="8ee98-105">JetOpenDatabase Function</span></span>

<span data-ttu-id="8ee98-106">La función **JetOpenDatabase** abre una base de datos adjuntada previamente, con las funciones [JetAttachDatabase](./jetattachdatabase-function.md) o [JetAttachDatabase2](./jetattachdatabase2-function.md) , para su uso con una sesión de base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee98-106">The **JetOpenDatabase** function opens a previously attached database, using the [JetAttachDatabase](./jetattachdatabase-function.md) or [JetAttachDatabase2](./jetattachdatabase2-function.md) functions, for use with a database session.</span></span> <span data-ttu-id="8ee98-107">Se puede llamar a esta función varias veces para la misma base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee98-107">This function can be called multiple times for the same database.</span></span>

```cpp
    JET_ERR JET_API JetOpenDatabase(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in_opt      const tchar* szConnect,
      __out         JET_DBID* pdbid,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="8ee98-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8ee98-108">Parameters</span></span>

<span data-ttu-id="8ee98-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="8ee98-109">*sesid*</span></span>

<span data-ttu-id="8ee98-110">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="8ee98-110">The database session context to use for the API call.</span></span>

<span data-ttu-id="8ee98-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="8ee98-111">*szFilename*</span></span>

<span data-ttu-id="8ee98-112">Nombre de la base de datos que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="8ee98-112">The name of the database to open.</span></span>

<span data-ttu-id="8ee98-113">*szConnect*</span><span class="sxs-lookup"><span data-stu-id="8ee98-113">*szConnect*</span></span>

<span data-ttu-id="8ee98-114">Reservado.</span><span class="sxs-lookup"><span data-stu-id="8ee98-114">Reserved.</span></span> <span data-ttu-id="8ee98-115">Definición en NULL</span><span class="sxs-lookup"><span data-stu-id="8ee98-115">Set to NULL.</span></span>

<span data-ttu-id="8ee98-116">*pdbid*</span><span class="sxs-lookup"><span data-stu-id="8ee98-116">*pdbid*</span></span>

<span data-ttu-id="8ee98-117">Puntero a un búfer que, en una llamada correcta, contiene el identificador de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee98-117">Pointer to a buffer that, on a successful call, contains the identifier of the database.</span></span> <span data-ttu-id="8ee98-118">Si se produce un error en la llamada, el valor es indefinido.</span><span class="sxs-lookup"><span data-stu-id="8ee98-118">If the call fails, the value is undefined.</span></span>

<span data-ttu-id="8ee98-119">*grbit*</span><span class="sxs-lookup"><span data-stu-id="8ee98-119">*grbit*</span></span>

<span data-ttu-id="8ee98-120">Grupo de bits que especifica cero o más de las opciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="8ee98-120">A group of bits that specify zero or more of the following options.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ee98-121">Value</span><span class="sxs-lookup"><span data-stu-id="8ee98-121">Value</span></span></p></th>
<th><p><span data-ttu-id="8ee98-122">Significado</span><span class="sxs-lookup"><span data-stu-id="8ee98-122">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-123">JET_bitDbExclusive</span><span class="sxs-lookup"><span data-stu-id="8ee98-123">JET_bitDbExclusive</span></span></p></td>
<td><p><span data-ttu-id="8ee98-124">Permite que una sola sesión adjunte una base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee98-124">Allows only a single session to attach a database.</span></span> <span data-ttu-id="8ee98-125">Normalmente, varias sesiones pueden abrir una base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee98-125">Normally, several sessions can open a database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-126">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="8ee98-126">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="8ee98-127">Impide las modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="8ee98-127">Prevents modifications to the database.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="8ee98-128">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8ee98-128">Return Value</span></span>

<span data-ttu-id="8ee98-129">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="8ee98-129">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="8ee98-130">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="8ee98-130">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8ee98-131">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="8ee98-131">Return code</span></span></p></th>
<th><p><span data-ttu-id="8ee98-132">Descripción</span><span class="sxs-lookup"><span data-stu-id="8ee98-132">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-133">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="8ee98-133">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="8ee98-134">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="8ee98-134">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-135">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="8ee98-135">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="8ee98-136">Se solicitó acceso exclusivo, pero no se pudo conceder.</span><span class="sxs-lookup"><span data-stu-id="8ee98-136">Exclusive access was requested, but could not be granted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-137">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="8ee98-137">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="8ee98-138">Se proporcionó una ruta de acceso no válida en <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="8ee98-138">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="8ee98-139"><em>szFilename</em> debe ser distinto de NULL y hacer referencia a un archivo válido.</span><span class="sxs-lookup"><span data-stu-id="8ee98-139"><em>szFilename</em> must be non-NULL and refer to a valid file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-140">JET_errDatabaseLocked</span><span class="sxs-lookup"><span data-stu-id="8ee98-140">JET_errDatabaseLocked</span></span></p></td>
<td><p><span data-ttu-id="8ee98-141">Otra sesión ya ha abierto la base de datos de forma exclusiva (mediante JET_bitDbExclusive).</span><span class="sxs-lookup"><span data-stu-id="8ee98-141">Another session has already opened the database exclusively (using JET_bitDbExclusive).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-142">JET_errDatabaseNotFound</span><span class="sxs-lookup"><span data-stu-id="8ee98-142">JET_errDatabaseNotFound</span></span></p></td>
<td><p><span data-ttu-id="8ee98-143">La base de datos no se adjuntó previamente (vea <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span><span class="sxs-lookup"><span data-stu-id="8ee98-143">The database was not previously attached (See <a href="gg294074(v=exchg.10).md">JetAttachDatabase</a>).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-144">JET_errInvalidDatabase</span><span class="sxs-lookup"><span data-stu-id="8ee98-144">JET_errInvalidDatabase</span></span></p></td>
<td><p><span data-ttu-id="8ee98-145">Se intentó abrir un archivo que no es un archivo de base de datos válido.</span><span class="sxs-lookup"><span data-stu-id="8ee98-145">An attempt was made to open a file that is not a valid database file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-146">JET_errOneDatabasePerSession</span><span class="sxs-lookup"><span data-stu-id="8ee98-146">JET_errOneDatabasePerSession</span></span></p></td>
<td><p><span data-ttu-id="8ee98-147">Se intentó abrir más de una base de datos y se estableció <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> .</span><span class="sxs-lookup"><span data-stu-id="8ee98-147">An attempt was made to open more than one database, and <a href="gg269337(v=exchg.10).md">JET_paramOneDatabasePerSession</a> was set.</span></span> <span data-ttu-id="8ee98-148">Para obtener más información, vea <a href="gg294139(v=exchg.10).md">parámetros del sistema</a>.</span><span class="sxs-lookup"><span data-stu-id="8ee98-148">For more information, see <a href="gg294139(v=exchg.10).md">System Parameters</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-149">JET_wrnFileOpenReadOnly</span><span class="sxs-lookup"><span data-stu-id="8ee98-149">JET_wrnFileOpenReadOnly</span></span></p></td>
<td><p><span data-ttu-id="8ee98-150">El archivo se adjuntó como de solo lectura, pero <strong>JetOpenDatabase</strong> no pasó JET_bitDbReadOnly.</span><span class="sxs-lookup"><span data-stu-id="8ee98-150">The file was attached as read-only, but <strong>JetOpenDatabase</strong> did not pass JET_bitDbReadOnly.</span></span> <span data-ttu-id="8ee98-151">La base de datos todavía está abierta con acceso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8ee98-151">The database is still opened with read-only access.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="8ee98-152">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ee98-152">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-153"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="8ee98-153"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="8ee98-154">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="8ee98-154">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-155"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="8ee98-155"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="8ee98-156">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="8ee98-156">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-157"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="8ee98-157"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="8ee98-158">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="8ee98-158">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-159"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="8ee98-159"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="8ee98-160">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="8ee98-160">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8ee98-161"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="8ee98-161"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="8ee98-162">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="8ee98-162">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8ee98-163"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="8ee98-163"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="8ee98-164">Se implementa como <strong>JetOpenDatabaseW</strong> (Unicode) y <strong>JetOpenDatabaseA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="8ee98-164">Implemented as <strong>JetOpenDatabaseW</strong> (Unicode) and <strong>JetOpenDatabaseA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="8ee98-165">Consulte también</span><span class="sxs-lookup"><span data-stu-id="8ee98-165">See Also</span></span>

[<span data-ttu-id="8ee98-166">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="8ee98-166">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="8ee98-167">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="8ee98-167">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="8ee98-168">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="8ee98-168">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="8ee98-169">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="8ee98-169">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="8ee98-170">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="8ee98-170">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="8ee98-171">JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="8ee98-171">JetAttachDatabase2</span></span>](./jetattachdatabase2-function.md)  
[<span data-ttu-id="8ee98-172">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="8ee98-172">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)  
[<span data-ttu-id="8ee98-173">Parámetros del sistema</span><span class="sxs-lookup"><span data-stu-id="8ee98-173">System Parameters</span></span>](./extensible-storage-engine-system-parameters.md)
