---
description: 'Más información acerca de: JetAttachDatabase2 (función)'
title: Función JetAttachDatabase2
TOCTitle: JetAttachDatabase2 Function
ms:assetid: 8667f3fc-d178-49f1-9474-f09352614f92
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269322(v=EXCHG.10)
ms:contentKeyID: 32765612
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetAttachDatabase2A
- JetAttachDatabase2
- JetAttachDatabase2W
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a5839559751fe45ec18a55de14c565116a0f9a4c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716969"
---
# <a name="jetattachdatabase2-function"></a><span data-ttu-id="07c74-103">Función JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="07c74-103">JetAttachDatabase2 Function</span></span>


<span data-ttu-id="07c74-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="07c74-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetattachdatabase2-function"></a><span data-ttu-id="07c74-105">Función JetAttachDatabase2</span><span class="sxs-lookup"><span data-stu-id="07c74-105">JetAttachDatabase2 Function</span></span>

<span data-ttu-id="07c74-106">La función **JetAttachDatabase2** adjunta un archivo de base de datos para su uso con una instancia de base de datos y especifica un tamaño máximo para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-106">The **JetAttachDatabase2** function attaches a database file for use with a database instance and specifies a maximum size for that database.</span></span> <span data-ttu-id="07c74-107">Para poder usar la base de datos, deberá abrirse posteriormente con [JetOpenDatabase](./jetopendatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="07c74-107">In order to use the database, it will need to be subsequently opened with [JetOpenDatabase](./jetopendatabase-function.md).</span></span>

```cpp
    JET_ERR JET_API JetAttachDatabase2(
      __in          JET_SESID sesid,
      __in          const tchar* szFilename,
      __in          const unsigned long cpgDatabaseSizeMax,
      __in          JET_GRBIT grbit
    );
```

### <a name="parameters"></a><span data-ttu-id="07c74-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="07c74-108">Parameters</span></span>

<span data-ttu-id="07c74-109">*sesid*</span><span class="sxs-lookup"><span data-stu-id="07c74-109">*sesid*</span></span>

<span data-ttu-id="07c74-110">Contexto de sesión de base de datos que se usará para la llamada de API.</span><span class="sxs-lookup"><span data-stu-id="07c74-110">The database session context that will be used for the API call.</span></span>

<span data-ttu-id="07c74-111">*szFilename*</span><span class="sxs-lookup"><span data-stu-id="07c74-111">*szFilename*</span></span>

<span data-ttu-id="07c74-112">Nombre de la base de datos que se va a adjuntar.</span><span class="sxs-lookup"><span data-stu-id="07c74-112">The name of the database to attach.</span></span>

<span data-ttu-id="07c74-113">*cpgDatabaseSizeMax*</span><span class="sxs-lookup"><span data-stu-id="07c74-113">*cpgDatabaseSizeMax*</span></span>

<span data-ttu-id="07c74-114">Tamaño máximo, en páginas de base de datos, para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-114">The maximum size, in database pages, for database.</span></span> <span data-ttu-id="07c74-115">El tamaño de página predeterminado de la base de datos es de 4 kilobytes, que se puede cambiar mediante la función [JetSetSystemParameter](./jetsetsystemparameter-function.md) antes de crear una base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-115">The default database page size is 4 kilobytes, which can be changed using the [JetSetSystemParameter](./jetsetsystemparameter-function.md) function prior to creating a database.</span></span>

<span data-ttu-id="07c74-116">Pasar cero significa que no hay ningún máximo aplicado por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-116">Passing zero means that there is no maximum enforced by the database engine.</span></span>

<span data-ttu-id="07c74-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="07c74-117">*grbit*</span></span>

<span data-ttu-id="07c74-118">Grupo de bits que contiene las opciones que se van a usar para esta llamada, que incluyen cero o más de los siguientes elementos:</span><span class="sxs-lookup"><span data-stu-id="07c74-118">A group of bits that contain the options to be used for this call, which include zero or more of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07c74-119">Value</span><span class="sxs-lookup"><span data-stu-id="07c74-119">Value</span></span></p></th>
<th><p><span data-ttu-id="07c74-120">Significado</span><span class="sxs-lookup"><span data-stu-id="07c74-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07c74-121">JET_bitDbDeleteCorruptIndexes</span><span class="sxs-lookup"><span data-stu-id="07c74-121">JET_bitDbDeleteCorruptIndexes</span></span></p></td>
<td><p><span data-ttu-id="07c74-122">Si se ha establecido <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> , se eliminarán todos los índices sobre los datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="07c74-122">If <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a> has been set, all indexes over Unicode data will be deleted.</span></span> <span data-ttu-id="07c74-123">Para obtener información más detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="07c74-123">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-124">JET_bitDbDeleteUnicodeIndexes</span><span class="sxs-lookup"><span data-stu-id="07c74-124">JET_bitDbDeleteUnicodeIndexes</span></span></p></td>
<td><p><span data-ttu-id="07c74-125">Se eliminarán todos los índices sobre datos Unicode, independientemente del valor de <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span><span class="sxs-lookup"><span data-stu-id="07c74-125">All indexes over Unicode data will be deleted, regardless of the setting of <a href="gg269337(v=exchg.10).md">JET_paramEnableIndexChecking</a>.</span></span> <span data-ttu-id="07c74-126">Para obtener información más detallada, consulte la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="07c74-126">See the Remarks section for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-127">JET_bitDbReadOnly</span><span class="sxs-lookup"><span data-stu-id="07c74-127">JET_bitDbReadOnly</span></span></p></td>
<td><p><span data-ttu-id="07c74-128">Impide las modificaciones en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-128">Prevents modifications to the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-129">JET_bitDbUpgrade</span><span class="sxs-lookup"><span data-stu-id="07c74-129">JET_bitDbUpgrade</span></span></p></td>
<td><p><span data-ttu-id="07c74-130">Reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="07c74-130">Reserved for future use.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="07c74-131">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="07c74-131">Return Value</span></span>

<span data-ttu-id="07c74-132">La función devuelve uno de los códigos de error de [JET_ERR](./jet-err.md) .</span><span class="sxs-lookup"><span data-stu-id="07c74-132">The function returns one of the [JET_ERR](./jet-err.md) error codes.</span></span> <span data-ttu-id="07c74-133">A continuación se muestran los elementos que se devuelven con más frecuencia.</span><span class="sxs-lookup"><span data-stu-id="07c74-133">The following are the most commonly returned.</span></span> <span data-ttu-id="07c74-134">(Para obtener una lista completa de los errores de esta API, consulte [códigos de error del motor de almacenamiento extensible](./extensible-storage-engine-error-codes.md)).</span><span class="sxs-lookup"><span data-stu-id="07c74-134">(For a complete list of errors for this API, see [Extensible Storage Engine Error Codes](./extensible-storage-engine-error-codes.md).)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="07c74-135">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="07c74-135">Return code</span></span></p></th>
<th><p><span data-ttu-id="07c74-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="07c74-136">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07c74-137">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="07c74-137">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="07c74-138">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="07c74-138">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-139">JET_errBackupInProgress</span><span class="sxs-lookup"><span data-stu-id="07c74-139">JET_errBackupInProgress</span></span></p></td>
<td><p><span data-ttu-id="07c74-140">No se permite adjuntar una base de datos durante una copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="07c74-140">Attaching a database is not allowed during a backup.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-141">JET_errDatabaseFileReadOnly</span><span class="sxs-lookup"><span data-stu-id="07c74-141">JET_errDatabaseFileReadOnly</span></span></p></td>
<td><p><span data-ttu-id="07c74-142">El archivo de base de datos especificado por <em>szFilename</em> debe ser grabable.</span><span class="sxs-lookup"><span data-stu-id="07c74-142">The database file specified by <em>szFilename</em> must be writable.</span></span> <span data-ttu-id="07c74-143">No se debe establecer el atributo Read-Only y el proceso en ejecución debe tener privilegios suficientes para escribir en el archivo.</span><span class="sxs-lookup"><span data-stu-id="07c74-143">The Read-Only attribute must not be set, and the running process must have sufficient privileges to write to the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-144">JET_errDatabaseInUse</span><span class="sxs-lookup"><span data-stu-id="07c74-144">JET_errDatabaseInUse</span></span></p></td>
<td><p><span data-ttu-id="07c74-145">Otro proceso está abriendo el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-145">The database file is already opened by another process.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-146">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="07c74-146">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="07c74-147">Se proporcionó una ruta de acceso no válida en <em>szFilename</em>.</span><span class="sxs-lookup"><span data-stu-id="07c74-147">An invalid path was given in <em>szFilename</em>.</span></span> <span data-ttu-id="07c74-148"><em>szFilename</em> debe ser distinto de NULL y hacer referencia a una ruta de acceso válida.</span><span class="sxs-lookup"><span data-stu-id="07c74-148"><em>szFilename</em> must be non-NULL and refer to a valid path.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-149">JET_errDatabaseSharingViolation</span><span class="sxs-lookup"><span data-stu-id="07c74-149">JET_errDatabaseSharingViolation</span></span></p></td>
<td><p><span data-ttu-id="07c74-150">Una sesión diferente ya ha adjuntado el archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="07c74-150">The database file has already been attached by a different session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-151">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="07c74-151">JET_errFileNotFound</span></span></p></td>
<td><p><span data-ttu-id="07c74-152">El archivo proporcionado en <em>szFilename</em> no existe.</span><span class="sxs-lookup"><span data-stu-id="07c74-152">The file given in <em>szFilename</em> does not exist.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-153">JET_errPrimaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="07c74-153">JET_errPrimaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="07c74-154">Hay un error con el índice principal.</span><span class="sxs-lookup"><span data-stu-id="07c74-154">There is an error with the primary index.</span></span> <span data-ttu-id="07c74-155">Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria).</span><span class="sxs-lookup"><span data-stu-id="07c74-155">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="07c74-156">También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y el índice principal está sobre una columna con datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="07c74-156">It may also be returned when attaching a database last modified on an older operating system and the primary index is over a column with Unicode data.</span></span> <span data-ttu-id="07c74-157">Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="07c74-157">See the remarks for more information on indexes over Unicode data.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-158">JET_errSecondaryIndexCorrupted</span><span class="sxs-lookup"><span data-stu-id="07c74-158">JET_errSecondaryIndexCorrupted</span></span></p></td>
<td><p><span data-ttu-id="07c74-159">Hay un error con un índice secundario.</span><span class="sxs-lookup"><span data-stu-id="07c74-159">There is an error with a secondary index.</span></span> <span data-ttu-id="07c74-160">Esto puede deberse a daños físicos (por ejemplo, daños en disco o memoria).</span><span class="sxs-lookup"><span data-stu-id="07c74-160">This may be from physical corruption (such as disk or memory corruption).</span></span> <span data-ttu-id="07c74-161">También se puede devolver al adjuntar una base de datos que se modificó por última vez en un sistema operativo anterior y un índice secundario se encuentra sobre una columna con datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="07c74-161">It may also be returned when attaching a database last modified on an older operating system and a secondary index is over a column with Unicode data.</span></span> <span data-ttu-id="07c74-162">Vea la sección Comentarios para obtener más información sobre los índices sobre datos Unicode.</span><span class="sxs-lookup"><span data-stu-id="07c74-162">See the remarks for more information on indexes over Unicode data.</span></span> <span data-ttu-id="07c74-163">Los índices secundarios se recompilan completamente cuando una base de datos se desfragmenta con una utilidad sin conexión mediante el siguiente comando: <strong>esentutl-d</strong>.</span><span class="sxs-lookup"><span data-stu-id="07c74-163">Secondary indexes are completely rebuilt when a database is defragmented with an offline utility using the following command: <strong>esentutl -d</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-164">JET_errTooManyAttachedDatabases</span><span class="sxs-lookup"><span data-stu-id="07c74-164">JET_errTooManyAttachedDatabases</span></span></p></td>
<td><p><span data-ttu-id="07c74-165">Solo se puede asociar un número finito de bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="07c74-165">Only a finite number of databases can be attached per instance.</span></span> <span data-ttu-id="07c74-166">Actualmente, el límite es de siete bases de datos por instancia.</span><span class="sxs-lookup"><span data-stu-id="07c74-166">The limit is currently seven databases per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-167">JET_wrnDatabaseAttached</span><span class="sxs-lookup"><span data-stu-id="07c74-167">JET_wrnDatabaseAttached</span></span></p></td>
<td><p><span data-ttu-id="07c74-168">Una advertencia no fatal que indica que el archivo de base de datos ya se ha adjuntado a esta sesión.</span><span class="sxs-lookup"><span data-stu-id="07c74-168">A nonfatal warning indicating that the database file has already been attached by this session.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="07c74-169">Observaciones</span><span class="sxs-lookup"><span data-stu-id="07c74-169">Remarks</span></span>

<span data-ttu-id="07c74-170">El archivo de base de datos se separa mediante [JetDetachDatabase](./jetdetachdatabase-function.md) o [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span><span class="sxs-lookup"><span data-stu-id="07c74-170">The database file is detached using [JetDetachDatabase](./jetdetachdatabase-function.md) or [JetDetachDatabase2](./jetdetachdatabase2-function.md).</span></span>

<span data-ttu-id="07c74-171">Consulte [JetAttachDatabase](./jetattachdatabase-function.md) para obtener comentarios.</span><span class="sxs-lookup"><span data-stu-id="07c74-171">See [JetAttachDatabase](./jetattachdatabase-function.md) for remarks.</span></span>

#### <a name="requirements"></a><span data-ttu-id="07c74-172">Requisitos</span><span class="sxs-lookup"><span data-stu-id="07c74-172">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="07c74-173"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="07c74-173"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="07c74-174">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="07c74-174">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-175"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="07c74-175"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="07c74-176">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="07c74-176">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-177"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="07c74-177"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="07c74-178">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="07c74-178">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-179"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="07c74-179"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="07c74-180">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="07c74-180">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="07c74-181"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="07c74-181"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="07c74-182">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="07c74-182">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="07c74-183"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="07c74-183"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="07c74-184">Se implementa como <strong>JetAttachDatabase2W</strong> (Unicode) y <strong>JetAttachDatabase2A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="07c74-184">Implemented as <strong>JetAttachDatabase2W</strong> (Unicode) and <strong>JetAttachDatabase2A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="07c74-185">Consulte también</span><span class="sxs-lookup"><span data-stu-id="07c74-185">See Also</span></span>

[<span data-ttu-id="07c74-186">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="07c74-186">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="07c74-187">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="07c74-187">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="07c74-188">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="07c74-188">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="07c74-189">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="07c74-189">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="07c74-190">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="07c74-190">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="07c74-191">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="07c74-191">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="07c74-192">JetCreateDatabase</span><span class="sxs-lookup"><span data-stu-id="07c74-192">JetCreateDatabase</span></span>](./jetcreatedatabase-function.md)  
[<span data-ttu-id="07c74-193">JetOpenDatabase</span><span class="sxs-lookup"><span data-stu-id="07c74-193">JetOpenDatabase</span></span>](./jetopendatabase-function.md)  
[<span data-ttu-id="07c74-194">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="07c74-194">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
