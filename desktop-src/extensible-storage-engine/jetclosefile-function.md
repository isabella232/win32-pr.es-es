---
description: 'Más información acerca de: JetCloseFile (función)'
title: JetCloseFile función)
TOCTitle: JetCloseFile Function
ms:assetid: e8930915-8102-44b0-ae42-abedbd3e0512
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294127(v=EXCHG.10)
ms:contentKeyID: 32765741
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFile
topic_type:
- kbArticle
- apiref
api_type:
- DLLExport
- COM
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 29fc2c76bf8528956d3e3331b3c2f23bf52f929f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423648"
---
# <a name="jetclosefile-function"></a><span data-ttu-id="2a3a5-103">JetCloseFile función)</span><span class="sxs-lookup"><span data-stu-id="2a3a5-103">JetCloseFile Function</span></span>


<span data-ttu-id="2a3a5-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="2a3a5-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefile-function"></a><span data-ttu-id="2a3a5-105">JetCloseFile función)</span><span class="sxs-lookup"><span data-stu-id="2a3a5-105">JetCloseFile Function</span></span>

<span data-ttu-id="2a3a5-106">La función **JetCloseFile** cierra un archivo que se abrió con [JetOpenFile](./jetopenfile-function.md) después de que los datos de ese archivo se hayan extraído con [JetReadFile](./jetreadfile-function.md).</span><span class="sxs-lookup"><span data-stu-id="2a3a5-106">The **JetCloseFile** function closes a file that was opened with [JetOpenFile](./jetopenfile-function.md) after the data from that file has been extracted using [JetReadFile](./jetreadfile-function.md).</span></span>

```cpp
    JET_ERR JET_API JetCloseFile(
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="2a3a5-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2a3a5-107">Parameters</span></span>

<span data-ttu-id="2a3a5-108">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="2a3a5-108">*hfFile*</span></span>

<span data-ttu-id="2a3a5-109">Identificador del archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-109">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="2a3a5-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2a3a5-110">Return Value</span></span>

<span data-ttu-id="2a3a5-111">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-111">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="2a3a5-112">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="2a3a5-112">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2a3a5-113">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="2a3a5-113">Return code</span></span></p></th>
<th><p><span data-ttu-id="2a3a5-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="2a3a5-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-115">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="2a3a5-115">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-116">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-116">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a3a5-117">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="2a3a5-117">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-118">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-118">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg269240(v=exchg.10).md">JetStopService</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-119">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="2a3a5-119">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-120">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-120">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="2a3a5-121">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-121">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a3a5-122">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="2a3a5-122">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-123">Uno de los parámetros proporcionados contenía un valor inesperado o contenía un valor que no tenía sentido cuando se combinó con el valor de otro parámetro.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-123">One of the parameters provided contained an unexpected value or contained a value that did not make sense when combined with the value of another parameter.</span></span> <span data-ttu-id="2a3a5-124">Esto puede ocurrir para <strong>JetCloseFile</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="2a3a5-124">This can happen for <strong>JetCloseFile</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="2a3a5-125">El identificador de instancia especificado no es válido (Windows XP y versiones posteriores),</span><span class="sxs-lookup"><span data-stu-id="2a3a5-125">The specified instance handle is invalid (Windows XP and later releases),</span></span></p></li>
<li><p><span data-ttu-id="2a3a5-126">El identificador de archivo especificado no es válido.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-126">The specified file handle is invalid.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-127">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="2a3a5-127">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-128">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-128">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a3a5-129">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="2a3a5-129">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-130">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-130">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-131">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="2a3a5-131">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-132">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-132">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a3a5-133">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="2a3a5-133">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-134">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-134">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-135">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="2a3a5-135">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="2a3a5-136">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-136">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2a3a5-137">Si se ejecuta correctamente, se cierra el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-137">On success, the file handle is closed.</span></span> <span data-ttu-id="2a3a5-138">Si se ha cerrado un archivo de base de datos, se destruye el archivo de revisión de la base de datos asociado (si existe).</span><span class="sxs-lookup"><span data-stu-id="2a3a5-138">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="2a3a5-139">En caso de error, no se produce ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-139">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="2a3a5-140">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2a3a5-140">Remarks</span></span>

<span data-ttu-id="2a3a5-141">Actualmente, el motor de base de datos solo admite un archivo abierto a través de [JetOpenFile](./jetopenfile-function.md) a la vez.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-141">The database engine currently only supports one open file through [JetOpenFile](./jetopenfile-function.md) at a time.</span></span> <span data-ttu-id="2a3a5-142">Si se abre un identificador de archivo con [JetOpenFile](./jetopenfile-function.md) , se debe cerrar con **JetCloseFile** antes de que se pueda abrir otro archivo.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-142">If a file handle is opened using [JetOpenFile](./jetopenfile-function.md) then it must be closed using **JetCloseFile** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="2a3a5-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a3a5-143">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-144"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="2a3a5-144"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="2a3a5-145">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-145">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a3a5-146"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="2a3a5-146"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="2a3a5-147">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-147">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-148"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="2a3a5-148"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="2a3a5-149">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-149">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2a3a5-150"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="2a3a5-150"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="2a3a5-151">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-151">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2a3a5-152"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="2a3a5-152"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="2a3a5-153">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="2a3a5-153">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="2a3a5-154">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2a3a5-154">See Also</span></span>

[<span data-ttu-id="2a3a5-155">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="2a3a5-155">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="2a3a5-156">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="2a3a5-156">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="2a3a5-157">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="2a3a5-157">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="2a3a5-158">JetOpenFile</span><span class="sxs-lookup"><span data-stu-id="2a3a5-158">JetOpenFile</span></span>](./jetopenfile-function.md)  
[<span data-ttu-id="2a3a5-159">JetReadFile</span><span class="sxs-lookup"><span data-stu-id="2a3a5-159">JetReadFile</span></span>](./jetreadfile-function.md)  
[<span data-ttu-id="2a3a5-160">JetStopService</span><span class="sxs-lookup"><span data-stu-id="2a3a5-160">JetStopService</span></span>](./jetstopservice-function.md)
