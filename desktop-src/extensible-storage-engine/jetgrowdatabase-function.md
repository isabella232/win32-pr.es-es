---
description: 'Más información acerca de: JetGrowDatabase (función)'
title: JetGrowDatabase función)
TOCTitle: JetGrowDatabase Function
ms:assetid: d9719991-6c80-4dcb-a1d6-f0c7de61f459
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294109(v=EXCHG.10)
ms:contentKeyID: 32765724
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetGrowDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 9ed8ee9888a2e4ab7908b72cc071f7b8143ca6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648423"
---
# <a name="jetgrowdatabase-function"></a><span data-ttu-id="d11cc-103">JetGrowDatabase función)</span><span class="sxs-lookup"><span data-stu-id="d11cc-103">JetGrowDatabase Function</span></span>


<span data-ttu-id="d11cc-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="d11cc-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetgrowdatabase-function"></a><span data-ttu-id="d11cc-105">JetGrowDatabase función)</span><span class="sxs-lookup"><span data-stu-id="d11cc-105">JetGrowDatabase Function</span></span>

<span data-ttu-id="d11cc-106">La función **JetGrowDatabase** extiende el tamaño de una base de datos que está abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="d11cc-106">The **JetGrowDatabase** function extends the size of a database that is currently open.</span></span>

```cpp
    JET_ERR JET_API JetGrowDatabase(
      __in          JET_SESID sesid,
      __in          JET_DBID dbid,
      __in          unsigned long cpg,
      __in          unsigned long* pcpgReal
    );
```

### <a name="parameters"></a><span data-ttu-id="d11cc-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d11cc-107">Parameters</span></span>

<span data-ttu-id="d11cc-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="d11cc-108">*sesid*</span></span>

<span data-ttu-id="d11cc-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="d11cc-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="d11cc-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="d11cc-110">*dbid*</span></span>

<span data-ttu-id="d11cc-111">La base de datos que se extenderá.</span><span class="sxs-lookup"><span data-stu-id="d11cc-111">The database that will be extended.</span></span>

<span data-ttu-id="d11cc-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="d11cc-112">*cpg*</span></span>

<span data-ttu-id="d11cc-113">Tamaño deseado de la base de datos, en páginas.</span><span class="sxs-lookup"><span data-stu-id="d11cc-113">The desired size of the database, in pages.</span></span>

<span data-ttu-id="d11cc-114">*pcpgReal*</span><span class="sxs-lookup"><span data-stu-id="d11cc-114">*pcpgReal*</span></span>

<span data-ttu-id="d11cc-115">Puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada a la API.</span><span class="sxs-lookup"><span data-stu-id="d11cc-115">Pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="d11cc-116">Si se produce un error en la llamada API, el contenido de *pcpgReal* no está definido.</span><span class="sxs-lookup"><span data-stu-id="d11cc-116">If the API call fails, the contents of *pcpgReal* are undefined.</span></span>

### <a name="return-value"></a><span data-ttu-id="d11cc-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d11cc-117">Return Value</span></span>

<span data-ttu-id="d11cc-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="d11cc-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="d11cc-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="d11cc-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d11cc-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="d11cc-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="d11cc-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="d11cc-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d11cc-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="d11cc-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="d11cc-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="d11cc-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d11cc-124">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="d11cc-124">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="d11cc-125">No hay suficiente espacio disponible en el volumen para realizar la operación de crecimiento.</span><span class="sxs-lookup"><span data-stu-id="d11cc-125">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d11cc-126">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="d11cc-126">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="d11cc-127"><a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>devolvió un error relacionado con el archivo.</span><span class="sxs-lookup"><span data-stu-id="d11cc-127">A file-related error was returned by <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span> <span data-ttu-id="d11cc-128">Para obtener más información sobre otros errores relacionados con archivos que podrían devolverse, vea <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="d11cc-128">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="d11cc-129">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d11cc-129">Remarks</span></span>

<span data-ttu-id="d11cc-130">Si se llama a **JetGrowDatabase** antes de insertar grandes cantidades de datos, el archivo de base de datos se incrementará en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="d11cc-130">If **JetGrowDatabase** is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="d11cc-131">Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reduce el número de veces que el archivo de base de datos tiene que crecer.</span><span class="sxs-lookup"><span data-stu-id="d11cc-131">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="d11cc-132">El crecimiento del archivo de base de datos una vez puede ser más rápido que crecer varias veces.</span><span class="sxs-lookup"><span data-stu-id="d11cc-132">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="d11cc-133">Actualmente solo se admite el crecimiento del archivo.</span><span class="sxs-lookup"><span data-stu-id="d11cc-133">Only growing the file is currently supported.</span></span> <span data-ttu-id="d11cc-134">Para reducir un archivo, use la característica de desfragmentación del programa **esentutl.exe** Utility.</span><span class="sxs-lookup"><span data-stu-id="d11cc-134">To shrink a file, use the defragmentation feature of the **esentutl.exe** utility program.</span></span>

<span data-ttu-id="d11cc-135">Para establecer el tamaño de una base de datos que no está abierta, vea [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="d11cc-135">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="d11cc-136">El tamaño del archivo podría no coincidir con el número de páginas que se devuelven en *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="d11cc-136">The file size might not match the number of pages that are returned in *pcpgReal*.</span></span> <span data-ttu-id="d11cc-137">Hay dos páginas reservadas adicionales que podrían no contarse en *pcpgReal*.</span><span class="sxs-lookup"><span data-stu-id="d11cc-137">There are two additional reserved pages that might not be counted in *pcpgReal*.</span></span>

#### <a name="requirements"></a><span data-ttu-id="d11cc-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d11cc-138">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d11cc-139"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="d11cc-139"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d11cc-140">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="d11cc-140">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d11cc-141"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d11cc-141"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d11cc-142">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d11cc-142">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d11cc-143"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="d11cc-143"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d11cc-144">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="d11cc-144">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d11cc-145"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="d11cc-145"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="d11cc-146">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="d11cc-146">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d11cc-147"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="d11cc-147"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="d11cc-148">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="d11cc-148">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="d11cc-149">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d11cc-149">See Also</span></span>

[<span data-ttu-id="d11cc-150">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="d11cc-150">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="d11cc-151">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d11cc-151">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d11cc-152">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="d11cc-152">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="d11cc-153">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="d11cc-153">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="d11cc-154">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="d11cc-154">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="d11cc-155">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="d11cc-155">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="d11cc-156">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="d11cc-156">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
