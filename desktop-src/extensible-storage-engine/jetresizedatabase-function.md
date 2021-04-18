---
description: 'Más información acerca de: JetResizeDatabase (función)'
title: JetResizeDatabase función)
TOCTitle: JetResizeDatabase Function
ms:assetid: b6420de7-acff-480e-838b-f0e5acc29c65
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835047(v=EXCHG.10)
ms:contentKeyID: 49894669
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetResizeDatabase
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dadaa7eaa310c5b3a6a2730d316218bc2607d100
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707373"
---
# <a name="jetresizedatabase-function"></a><span data-ttu-id="21e30-103">JetResizeDatabase función)</span><span class="sxs-lookup"><span data-stu-id="21e30-103">JetResizeDatabase Function</span></span>


<span data-ttu-id="21e30-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="21e30-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="21e30-105">La función **JetResizeDatabase** extiende o reduce el tamaño de una base de datos que está abierta actualmente.</span><span class="sxs-lookup"><span data-stu-id="21e30-105">The **JetResizeDatabase** function extends or shrinks the size of a database that is currently open.</span></span>

<span data-ttu-id="21e30-106">La función **JetResizeDatabase** se presentó en el sistema operativo Windows 8.</span><span class="sxs-lookup"><span data-stu-id="21e30-106">The **JetResizeDatabase** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetResizeDatabase(
  __in          JET_SESID sesid,
  __in          JET_DBID dbid,
  __in          unsigned long cpg,
  __out         unsigned long* pcpgActual,
  __in          const JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="21e30-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="21e30-107">Parameters</span></span>

<span data-ttu-id="21e30-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="21e30-108">*sesid*</span></span>

<span data-ttu-id="21e30-109">Contexto de sesión de base de datos que se va a usar para la llamada API.</span><span class="sxs-lookup"><span data-stu-id="21e30-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="21e30-110">*DBID*</span><span class="sxs-lookup"><span data-stu-id="21e30-110">*dbid*</span></span>

<span data-ttu-id="21e30-111">La base de datos que se extenderá.</span><span class="sxs-lookup"><span data-stu-id="21e30-111">The database that will be extended.</span></span>

<span data-ttu-id="21e30-112">*CPG*</span><span class="sxs-lookup"><span data-stu-id="21e30-112">*cpg*</span></span>

<span data-ttu-id="21e30-113">Tamaño solicitado de la base de datos, en páginas.</span><span class="sxs-lookup"><span data-stu-id="21e30-113">The requested size of the database, in pages.</span></span>

<span data-ttu-id="21e30-114">*pcpgActual*</span><span class="sxs-lookup"><span data-stu-id="21e30-114">*pcpgActual*</span></span>

<span data-ttu-id="21e30-115">Un puntero a un número que recibe el tamaño de la base de datos, en páginas, después de la llamada a la API.</span><span class="sxs-lookup"><span data-stu-id="21e30-115">A pointer to a number that receives the size of the database, in pages, after the API call.</span></span> <span data-ttu-id="21e30-116">Si se produce un error en la llamada API, el contenido del parámetro *pcpgActual* no está definido.</span><span class="sxs-lookup"><span data-stu-id="21e30-116">If the API call fails, the contents of *pcpgActual* parameter are undefined.</span></span>

<span data-ttu-id="21e30-117">*grbit*</span><span class="sxs-lookup"><span data-stu-id="21e30-117">*grbit*</span></span>

<span data-ttu-id="21e30-118">Grupo de bits que especifica cero o más de los valores enumerados en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="21e30-118">A group of bits that specifies zero or more of the values listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21e30-119">Value</span><span class="sxs-lookup"><span data-stu-id="21e30-119">Value</span></span></p></th>
<th><p><span data-ttu-id="21e30-120">Significado</span><span class="sxs-lookup"><span data-stu-id="21e30-120">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e30-121">JET_bitResizeDatabaseOnlyGrow</span><span class="sxs-lookup"><span data-stu-id="21e30-121">JET_bitResizeDatabaseOnlyGrow</span></span></p></td>
<td><p><span data-ttu-id="21e30-122">Crezca solo la base de datos.</span><span class="sxs-lookup"><span data-stu-id="21e30-122">Only grow the database.</span></span> <span data-ttu-id="21e30-123">Si la llamada de cambiar tamaño reduciría la base de datos, no haga nada.</span><span class="sxs-lookup"><span data-stu-id="21e30-123">If the resize call would shrink the database, do nothing.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="21e30-124">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="21e30-124">Return value</span></span>

<span data-ttu-id="21e30-125">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los códigos de retorno que se enumeran en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="21e30-125">This function returns the [JET_ERR](./jet-err.md) datatype with one of the return codes listed in the following table.</span></span> <span data-ttu-id="21e30-126">Para obtener más información sobre los posibles errores del motor de almacenamiento extensible (ESE), vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="21e30-126">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="21e30-127">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="21e30-127">Return code</span></span></p></th>
<th><p><span data-ttu-id="21e30-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="21e30-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e30-129">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="21e30-129">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="21e30-130">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="21e30-130">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e30-131">JET_errDiskFull</span><span class="sxs-lookup"><span data-stu-id="21e30-131">JET_errDiskFull</span></span></p></td>
<td><p><span data-ttu-id="21e30-132">No hay suficiente espacio disponible en el volumen para realizar la operación de crecimiento.</span><span class="sxs-lookup"><span data-stu-id="21e30-132">There is insufficient free space on the volume to perform the grow operation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e30-133">JET_errDiskIO</span><span class="sxs-lookup"><span data-stu-id="21e30-133">JET_errDiskIO</span></span></p></td>
<td><p><span data-ttu-id="21e30-134">La función <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> devolvió un error relacionado con el archivo.</span><span class="sxs-lookup"><span data-stu-id="21e30-134">A file-related error was returned by the <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a> function.</span></span> <span data-ttu-id="21e30-135">Para obtener más información sobre otros errores relacionados con archivos que podrían devolverse, vea <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span><span class="sxs-lookup"><span data-stu-id="21e30-135">For more information about other file-related errors that might be returned, see <a href="gg269242(v=exchg.10).md">JetSetDatabaseSize</a>.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="remarks"></a><span data-ttu-id="21e30-136">Observaciones</span><span class="sxs-lookup"><span data-stu-id="21e30-136">Remarks</span></span>

<span data-ttu-id="21e30-137">Si se llama a la función **JetResizeDatabase** antes de insertar grandes cantidades de datos, el archivo de base de datos se incrementará en una sola operación.</span><span class="sxs-lookup"><span data-stu-id="21e30-137">If the **JetResizeDatabase** function is called prior to inserting large amounts of data, the database file will be grown in one operation.</span></span> <span data-ttu-id="21e30-138">Esto reducirá la probabilidad de que el archivo de base de datos se fragmente en el nivel del sistema de archivos y también reduce el número de veces que el archivo de base de datos tiene que crecer.</span><span class="sxs-lookup"><span data-stu-id="21e30-138">This will reduce the likelihood of the database file becoming fragmented at the file system level, and also reduce the number of times the database file has to be grown.</span></span> <span data-ttu-id="21e30-139">El crecimiento del archivo de base de datos una vez puede ser más rápido que crecer varias veces.</span><span class="sxs-lookup"><span data-stu-id="21e30-139">Growing the database file once can be faster than growing it several times.</span></span>

<span data-ttu-id="21e30-140">Para establecer el tamaño de una base de datos que no está abierta, vea [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span><span class="sxs-lookup"><span data-stu-id="21e30-140">To set the size of a database that is not opened, see [JetSetDatabaseSize](./jetsetdatabasesize-function.md).</span></span>

<span data-ttu-id="21e30-141">El tamaño del archivo podría no coincidir con el número de páginas que se devuelven en el parámetro *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="21e30-141">The file size might not match the number of pages that are returned in the *pcpgReal* parameter.</span></span> <span data-ttu-id="21e30-142">Es posible que no se cuenten dos páginas reservadas adicionales en el parámetro *pcpgReal* .</span><span class="sxs-lookup"><span data-stu-id="21e30-142">Two additional reserved pages might not be counted in the *pcpgReal* parameter.</span></span>

#### <a name="requirements"></a><span data-ttu-id="21e30-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21e30-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="21e30-144"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="21e30-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="21e30-145">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="21e30-145">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e30-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="21e30-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="21e30-147">Requiere Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="21e30-147">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e30-148"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="21e30-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="21e30-149">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="21e30-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="21e30-150"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="21e30-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="21e30-151">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="21e30-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="21e30-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="21e30-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="21e30-153">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="21e30-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="21e30-154">Vea también</span><span class="sxs-lookup"><span data-stu-id="21e30-154">See also</span></span>

[<span data-ttu-id="21e30-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="21e30-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="21e30-156">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="21e30-156">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="21e30-157">JET_SESID</span><span class="sxs-lookup"><span data-stu-id="21e30-157">JET_SESID</span></span>](./jet-sesid.md)  
[<span data-ttu-id="21e30-158">JET_TABLEID</span><span class="sxs-lookup"><span data-stu-id="21e30-158">JET_TABLEID</span></span>](./jet-tableid.md)  
[<span data-ttu-id="21e30-159">JET_OBJECTINFO</span><span class="sxs-lookup"><span data-stu-id="21e30-159">JET_OBJECTINFO</span></span>](./jet-objectinfo-structure.md)  
[<span data-ttu-id="21e30-160">JET_OBJECTLIST</span><span class="sxs-lookup"><span data-stu-id="21e30-160">JET_OBJECTLIST</span></span>](./jet-objectlist-structure.md)  
[<span data-ttu-id="21e30-161">JetSetDatabaseSize</span><span class="sxs-lookup"><span data-stu-id="21e30-161">JetSetDatabaseSize</span></span>](./jetsetdatabasesize-function.md)
