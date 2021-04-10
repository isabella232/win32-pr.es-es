---
description: 'Más información acerca de: JetSetDatabaseSize (función)'
title: JetSetDatabaseSize función)
TOCTitle: JetSetDatabaseSize Function
ms:assetid: 4a87bf43-c8f7-4966-9f1f-68c16d1cb558
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269242(v=EXCHG.10)
ms:contentKeyID: 32765544
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetSetDatabaseSizeW
- JetSetDatabaseSize
- JetSetDatabaseSizeA
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cd450a0afed0256b0b80d97a278dccf99418a900
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153763"
---
# <a name="jetsetdatabasesize-function"></a><span data-ttu-id="c401e-103">JetSetDatabaseSize función)</span><span class="sxs-lookup"><span data-stu-id="c401e-103">JetSetDatabaseSize Function</span></span>


<span data-ttu-id="c401e-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="c401e-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetsetdatabasesize-function"></a><span data-ttu-id="c401e-105">JetSetDatabaseSize función)</span><span class="sxs-lookup"><span data-stu-id="c401e-105">JetSetDatabaseSize Function</span></span>

<span data-ttu-id="c401e-106">La función **JetSetDatabaseSize** establece el tamaño de un archivo de base de datos no abierto.</span><span class="sxs-lookup"><span data-stu-id="c401e-106">The **JetSetDatabaseSize** function sets the size of an unopened database file.</span></span>

```cpp
    JET_ERR JET_API JetSetDatabaseSize(
      __in          JET_SESID sesid,
      __in          JET_PCSTR szDatabaseName,
      __in          unsigned long cpg,
      __out         unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="c401e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c401e-107">Parameters</span></span>

<span data-ttu-id="c401e-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="c401e-108">*sesid*</span></span>

<span data-ttu-id="c401e-109">Identifica el contexto de la sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="c401e-109">Identifies the database session context to use for the API call.</span></span>

<span data-ttu-id="c401e-110">*szDatabaseName*</span><span class="sxs-lookup"><span data-stu-id="c401e-110">*szDatabaseName*</span></span>

<span data-ttu-id="c401e-111">Identifica el nombre del archivo de base de datos cuyo tamaño se va a modificar.</span><span class="sxs-lookup"><span data-stu-id="c401e-111">Identifies the name of the database file whose size is to be altered.</span></span>

<span data-ttu-id="c401e-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="c401e-112">*cpg*</span></span>

<span data-ttu-id="c401e-113">Especifica el tamaño deseado de la base de datos, en páginas.</span><span class="sxs-lookup"><span data-stu-id="c401e-113">Specifies the desired size of the database, in pages.</span></span>

<span data-ttu-id="c401e-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="c401e-114">*pcpgReal*</span></span>

<span data-ttu-id="c401e-115">Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada a la API.</span><span class="sxs-lookup"><span data-stu-id="c401e-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="c401e-116">Si la llamada a la API no se ha realizado correctamente, el contenido de *pcpgReal* no está definido.</span><span class="sxs-lookup"><span data-stu-id="c401e-116">If the API call was unsuccessful, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="c401e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c401e-117">Return Value</span></span>

<span data-ttu-id="c401e-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="c401e-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="c401e-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="c401e-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c401e-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="c401e-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="c401e-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="c401e-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c401e-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="c401e-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="c401e-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="c401e-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c401e-124">JET_errDatabaseInconsistent</span><span class="sxs-lookup"><span data-stu-id="c401e-124">JET_errDatabaseInconsistent</span></span><br />
<span data-ttu-id="c401e-125">JET_errDatabaseDirtyShutdown</span><span class="sxs-lookup"><span data-stu-id="c401e-125">JET_errDatabaseDirtyShutdown</span></span></p></td>
<td><p><span data-ttu-id="c401e-126">JET_errDatabaseInconsistent y JET_errDatabaseDirtyShutdown son el mismo valor numérico.</span><span class="sxs-lookup"><span data-stu-id="c401e-126">JET_errDatabaseInconsistent and JET_errDatabaseDirtyShutdown are the same numeric value.</span></span> <span data-ttu-id="c401e-127">La base de datos cuyo tamaño se va a ajustar debe estar en un cierre correcto, conocido como estado coherente.</span><span class="sxs-lookup"><span data-stu-id="c401e-127">The database whose size is to be adjusted must be in a clean shutdown, known as a consistent state.</span></span> <span data-ttu-id="c401e-128">Una base de datos incoherente no está dañada, pero requiere que se reproduzcan los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="c401e-128">An inconsistent database is not corrupted, but it requires log files to be replayed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c401e-129">JET_errDatabaseInvalidPath</span><span class="sxs-lookup"><span data-stu-id="c401e-129">JET_errDatabaseInvalidPath</span></span></p></td>
<td><p><span data-ttu-id="c401e-130"><em>szDatabaseName</em> no debe ser una cadena vacía, que no sea NULL.</span><span class="sxs-lookup"><span data-stu-id="c401e-130"><em>szDatabaseName</em> must not be an empty, non-NULL string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c401e-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="c401e-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="c401e-132">No hay suficiente espacio disponible en el volumen para realizar la operación de crecimiento.</span><span class="sxs-lookup"><span data-stu-id="c401e-132">There is insufficient free space on the volume to perform the grow operation.</span></span> <span data-ttu-id="c401e-133"><strong>JetSetDatabaseSize</strong> también puede devolver muchos errores relacionados con archivos, incluidos, entre otros, los siguientes:</span><span class="sxs-lookup"><span data-stu-id="c401e-133"><strong>JetSetDatabaseSize</strong> may also return many file-related errors, including, but not limited to:</span></span></p>
<ul>
<li><p><span data-ttu-id="c401e-134">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="c401e-134">JET_errDiskIO</span></span></p></li>
<li><p><span data-ttu-id="c401e-135">JET_errFileNotFound</span><span class="sxs-lookup"><span data-stu-id="c401e-135">JET_errFileNotFound</span></span></p></li>
<li><p><span data-ttu-id="c401e-136">JET_errInvalidPath</span><span class="sxs-lookup"><span data-stu-id="c401e-136">JET_errInvalidPath</span></span></p></li>
<li><p><span data-ttu-id="c401e-137">JET_errFileAccessDenied</span><span class="sxs-lookup"><span data-stu-id="c401e-137">JET_errFileAccessDenied</span></span></p></li>
<li><p><span data-ttu-id="c401e-138">JET_errOutOfFileHandles</span><span class="sxs-lookup"><span data-stu-id="c401e-138">JET_errOutOfFileHandles</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c401e-139">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="c401e-139">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="c401e-140">Uno de los motivos por los que se puede devolver este error es si <em>CPG</em> cumple el tamaño mínimo de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="c401e-140">One of the reasons this error may be returned is if <em>cpg</em> does meet the minimum database size.</span></span> <span data-ttu-id="c401e-141">El tamaño mínimo de la base de datos actual es 256 páginas.</span><span class="sxs-lookup"><span data-stu-id="c401e-141">The current minimum database size is 256 pages.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c401e-142">JET_errOutOfMemory</span><span class="sxs-lookup"><span data-stu-id="c401e-142">JET_errOutOfMemory</span></span></p></td>
<td><p><span data-ttu-id="c401e-143">El sistema tiene pocos recursos de memoria.</span><span class="sxs-lookup"><span data-stu-id="c401e-143">The system is low on memory resources.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="c401e-144">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c401e-144">Remarks</span></span>

<span data-ttu-id="c401e-145">Si se llama a **JetSetDatabaseSize** antes de insertar grandes cantidades de datos, el archivo de base de datos se incrementará en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="c401e-145">If **JetSetDatabaseSize** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="c401e-146">Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reduce el número de veces que el archivo de base de datos tiene que crecer.</span><span class="sxs-lookup"><span data-stu-id="c401e-146">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="c401e-147">El crecimiento del archivo de base de datos una vez puede ser más rápido que crecer varias veces.</span><span class="sxs-lookup"><span data-stu-id="c401e-147">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="c401e-148">Actualmente solo se admite el crecimiento del archivo.</span><span class="sxs-lookup"><span data-stu-id="c401e-148">Only growing the file is currently supported.</span></span> <span data-ttu-id="c401e-149">Para reducir un archivo, use la característica de desfragmentación del programa esentutl.exe Utility.</span><span class="sxs-lookup"><span data-stu-id="c401e-149">To shrink a file, use the defragmentation feature of the esentutl.exe utility program.</span></span>

<span data-ttu-id="c401e-150">Si *CPG* es menor que el tamaño actual de la base de datos, se omitirá la operación.</span><span class="sxs-lookup"><span data-stu-id="c401e-150">If *cpg* is smaller than the current size of the database, the operation will be ignored.</span></span> <span data-ttu-id="c401e-151">Si *CPG* es menor que el tamaño mínimo de la base de datos (actualmente 256 páginas), devolverá JET_errInvalidParameter.</span><span class="sxs-lookup"><span data-stu-id="c401e-151">If *cpg* is less than the minimum database size (currently 256 pages), it will return JET_errInvalidParameter.</span></span>

<span data-ttu-id="c401e-152">Para establecer el tamaño de una base de datos que se abre, vea [JetGrowDatabase](./jetgrowdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="c401e-152">To set the size of a database that is opened, see [JetGrowDatabase](./jetgrowdatabase-function.md).</span></span>

<span data-ttu-id="c401e-153">Es posible que el tamaño del archivo no coincida con el número de páginas devueltas en *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="c401e-153">The file size may not match the number of pages returned in *pcpgReal*.</span></span> <span data-ttu-id="c401e-154">Hay dos páginas reservadas adicionales que pueden no contarse en *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="c401e-154">There are two additional reserved pages that may not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="c401e-155">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c401e-155">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c401e-156"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="c401e-156"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="c401e-157">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="c401e-157">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c401e-158"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="c401e-158"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="c401e-159">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="c401e-159">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c401e-160"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="c401e-160"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="c401e-161">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="c401e-161">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c401e-162"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="c401e-162"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="c401e-163">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="c401e-163">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c401e-164"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="c401e-164"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="c401e-165">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="c401e-165">Requires ESENT.dll.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c401e-166"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="c401e-166"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="c401e-167">Se implementa como <strong>JetSetDatabaseSizeW</strong> (Unicode) y <strong>JetSetDatabaseSizeA</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="c401e-167">Implemented as <strong>JetSetDatabaseSizeW</strong> (Unicode) and <strong>JetSetDatabaseSizeA</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="c401e-168">Consulte también</span><span class="sxs-lookup"><span data-stu-id="c401e-168">See Also</span></span>

[<span data-ttu-id="c401e-169">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="c401e-169">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="c401e-170">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="c401e-170">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="c401e-171">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="c401e-171">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="c401e-172">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="c401e-172">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="c401e-173">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="c401e-173">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="c401e-174">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="c401e-174">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="c401e-175">JetGrowDatabase</span><span class="sxs-lookup"><span data-stu-id="c401e-175">JetGrowDatabase</span></span>](./jetgrowdatabase-function.md)
