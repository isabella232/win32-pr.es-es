---
description: 'Más información acerca de: JetCloseFileInstance (función)'
title: JetCloseFileInstance función)
TOCTitle: JetCloseFileInstance Function
ms:assetid: 64a38655-b128-453b-9593-46032bd6c470
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269270(v=EXCHG.10)
ms:contentKeyID: 32765572
ms.date: 04/11/2016
ms.topic: reference
api_name:
- JetCloseFileInstance
topic_type:
- apiref
- kbArticle
api_type:
- COM
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d575e90d828159f310a27068ce8d88b29970f4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539982"
---
# <a name="jetclosefileinstance-function"></a><span data-ttu-id="98084-103">JetCloseFileInstance función)</span><span class="sxs-lookup"><span data-stu-id="98084-103">JetCloseFileInstance Function</span></span>


<span data-ttu-id="98084-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="98084-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jetclosefileinstance-function"></a><span data-ttu-id="98084-105">JetCloseFileInstance función)</span><span class="sxs-lookup"><span data-stu-id="98084-105">JetCloseFileInstance Function</span></span>

<span data-ttu-id="98084-106">La función **JetCloseFileInstance** cierra un archivo que se abrió con [JetOpenFileInstance](./jetopenfileinstance-function.md) después de que los datos de ese archivo se hayan extraído con [JetReadFileInstance](./jetreadfileinstance-function.md).</span><span class="sxs-lookup"><span data-stu-id="98084-106">The **JetCloseFileInstance** function closes a file that was opened with [JetOpenFileInstance](./jetopenfileinstance-function.md) after the data from that file has been extracted using [JetReadFileInstance](./jetreadfileinstance-function.md).</span></span>

<span data-ttu-id="98084-107">**Windows XP: JetCloseFileInstance** se presentó en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98084-107">**Windows XP:  JetCloseFileInstance** is introduced in Windows XP.</span></span>

```cpp
    JET_ERR JET_API JetCloseFileInstance(
      __in          JET_INSTANCE instance,
      __in          JET_HANDLE hfFile
    );
```

### <a name="parameters"></a><span data-ttu-id="98084-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="98084-108">Parameters</span></span>

<span data-ttu-id="98084-109">*repetición*</span><span class="sxs-lookup"><span data-stu-id="98084-109">*instance*</span></span>

<span data-ttu-id="98084-110">Instancia de que se va a usar para esta llamada.</span><span class="sxs-lookup"><span data-stu-id="98084-110">The instance to use for this call.</span></span>

<span data-ttu-id="98084-111">En Windows 2000, la variante de API que acepta este parámetro no está disponible porque solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="98084-111">For Windows 2000, the API variant that accepts this parameter is not available because only one instance is supported.</span></span> <span data-ttu-id="98084-112">En este caso, se implica el uso de esta instancia global.</span><span class="sxs-lookup"><span data-stu-id="98084-112">The use of this one global instance is implied in this case.</span></span>

<span data-ttu-id="98084-113">En Windows XP y versiones posteriores, solo se puede llamar a la variante de API que no acepta este parámetro cuando el motor está en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia.</span><span class="sxs-lookup"><span data-stu-id="98084-113">For Windows XP and later releases, the API variant that does not accept this parameter may only be called when the engine is in legacy mode (Windows 2000 compatibility mode) where only one instance is supported.</span></span> <span data-ttu-id="98084-114">De lo contrario, se producirá un error en la operación con JET_errRunningInMultiInstanceMode.</span><span class="sxs-lookup"><span data-stu-id="98084-114">Otherwise, the operation will fail with JET_errRunningInMultiInstanceMode.</span></span>

<span data-ttu-id="98084-115">*hfFile*</span><span class="sxs-lookup"><span data-stu-id="98084-115">*hfFile*</span></span>

<span data-ttu-id="98084-116">Identificador del archivo que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="98084-116">The handle of the file to be read.</span></span>

### <a name="return-value"></a><span data-ttu-id="98084-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="98084-117">Return Value</span></span>

<span data-ttu-id="98084-118">Esta función devuelve el tipo de valor de [JET_ERR](./jet-err.md) con uno de los siguientes códigos de retorno.</span><span class="sxs-lookup"><span data-stu-id="98084-118">This function returns the [JET_ERR](./jet-err.md) datatype with one of the following return codes.</span></span> <span data-ttu-id="98084-119">Para obtener más información sobre los posibles errores de ESE, vea [errores del motor de almacenamiento extensible](./extensible-storage-engine-errors.md) y [parámetros de control de errores](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="98084-119">For more information about the possible ESE errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="98084-120">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="98084-120">Return code</span></span></p></th>
<th><p><span data-ttu-id="98084-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="98084-121">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98084-122">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="98084-122">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="98084-123">La operación se ha completado correctamente.</span><span class="sxs-lookup"><span data-stu-id="98084-123">The operation completed successfully.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98084-124">JET_errClientRequestToStopJetService</span><span class="sxs-lookup"><span data-stu-id="98084-124">JET_errClientRequestToStopJetService</span></span></p></td>
<td><p><span data-ttu-id="98084-125">No es posible completar la operación porque se ha interrumpido toda la actividad en la instancia asociada a la sesión como resultado de una llamada a <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span><span class="sxs-lookup"><span data-stu-id="98084-125">It is not possible to complete the operation because all activity on the instance associated with the session has ceased as a result of a call to <a href="gg294108(v=exchg.10).md">JetStopServiceInstance</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98084-126">JET_errInstanceUnavailable</span><span class="sxs-lookup"><span data-stu-id="98084-126">JET_errInstanceUnavailable</span></span></p></td>
<td><p><span data-ttu-id="98084-127">No es posible completar la operación porque la instancia asociada a la sesión ha encontrado un error irrecuperable que requiere que se revoque el acceso a todos los datos para proteger la integridad de los datos.</span><span class="sxs-lookup"><span data-stu-id="98084-127">It is not possible to complete the operation because the instance associated with the session has encountered a fatal error that requires that access to all data be revoked to protect the integrity of that data.</span></span></p>
<p><span data-ttu-id="98084-128">Este error solo se devolverá en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="98084-128">This error will only be returned by Windows XP and later releases.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98084-129">JET_errInvalidParameter</span><span class="sxs-lookup"><span data-stu-id="98084-129">JET_errInvalidParameter</span></span></p></td>
<td><p><span data-ttu-id="98084-130">Uno de los parámetros que se proporcionó contenía un valor inesperado o la combinación de varios valores de parámetro produjo un resultado inesperado.</span><span class="sxs-lookup"><span data-stu-id="98084-130">One of the parameters that was provided contained an unexpected value, or the combination of several parameter values yielded an unexpected result.</span></span> <span data-ttu-id="98084-131">Esto puede ocurrir para <strong>JetCloseFileInstance</strong> cuando:</span><span class="sxs-lookup"><span data-stu-id="98084-131">This can happen for <strong>JetCloseFileInstance</strong> when:</span></span></p>
<ul>
<li><p><span data-ttu-id="98084-132">El identificador de instancia especificado no es válido (Windows XP y versiones posteriores)</span><span class="sxs-lookup"><span data-stu-id="98084-132">The specified instance handle is invalid (Windows XP and later releases)</span></span></p></li>
<li><p><span data-ttu-id="98084-133">El identificador de archivo especificado no es válido</span><span class="sxs-lookup"><span data-stu-id="98084-133">The specified file handle is invalid</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98084-134">JET_errNoBackup</span><span class="sxs-lookup"><span data-stu-id="98084-134">JET_errNoBackup</span></span></p></td>
<td><p><span data-ttu-id="98084-135">No se pudo realizar la operación porque no hay ninguna copia de seguridad externa en curso.</span><span class="sxs-lookup"><span data-stu-id="98084-135">The operation failed because no external backup is in progress.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98084-136">JET_errNotInitialized</span><span class="sxs-lookup"><span data-stu-id="98084-136">JET_errNotInitialized</span></span></p></td>
<td><p><span data-ttu-id="98084-137">No es posible completar la operación porque todavía no se ha inicializado la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98084-137">It is not possible to complete the operation because the instance associated with the session has not been initialized yet.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98084-138">JET_errRestoreInProgress</span><span class="sxs-lookup"><span data-stu-id="98084-138">JET_errRestoreInProgress</span></span></p></td>
<td><p><span data-ttu-id="98084-139">No es posible completar la operación porque hay una operación de restauración en curso en la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98084-139">It is not possible to complete the operation because a restore operation is in progress on the instance associated with the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98084-140">JET_errRunningInMultiInstanceMode</span><span class="sxs-lookup"><span data-stu-id="98084-140">JET_errRunningInMultiInstanceMode</span></span></p></td>
<td><p><span data-ttu-id="98084-141">No se pudo realizar la operación porque se intentó usar el motor en modo heredado (modo de compatibilidad de Windows 2000), donde solo se admite una instancia cuando en realidad existen varias instancias.</span><span class="sxs-lookup"><span data-stu-id="98084-141">The operation failed because an attempt was made to use the engine in legacy mode (Windows 2000 compatibility mode) where only one instance is supported when in fact multiple instances already exist.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98084-142">JET_errTermInProgress</span><span class="sxs-lookup"><span data-stu-id="98084-142">JET_errTermInProgress</span></span></p></td>
<td><p><span data-ttu-id="98084-143">No es posible completar la operación porque se está cerrando la instancia asociada a la sesión.</span><span class="sxs-lookup"><span data-stu-id="98084-143">It is not possible to complete the operation because the instance associated with the session is being shut down.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="98084-144">Si se ejecuta correctamente, se cierra el identificador de archivo.</span><span class="sxs-lookup"><span data-stu-id="98084-144">On success, the file handle is closed.</span></span> <span data-ttu-id="98084-145">Si se ha cerrado un archivo de base de datos, se destruye el archivo de revisión de la base de datos asociado (si existe).</span><span class="sxs-lookup"><span data-stu-id="98084-145">If a database file was closed then the associated database patch file (if any) is destroyed.</span></span>

<span data-ttu-id="98084-146">En caso de error, no se produce ningún cambio.</span><span class="sxs-lookup"><span data-stu-id="98084-146">On failure, no change occurs.</span></span>

#### <a name="remarks"></a><span data-ttu-id="98084-147">Observaciones</span><span class="sxs-lookup"><span data-stu-id="98084-147">Remarks</span></span>

<span data-ttu-id="98084-148">Actualmente, el motor de base de datos solo admite un archivo abierto a través de [JetOpenFileInstance](./jetopenfileinstance-function.md) a la vez.</span><span class="sxs-lookup"><span data-stu-id="98084-148">The database engine currently only supports one open file through [JetOpenFileInstance](./jetopenfileinstance-function.md) at a time.</span></span> <span data-ttu-id="98084-149">Si se abre un identificador de archivo con [JetOpenFileInstance](./jetopenfileinstance-function.md) , se debe cerrar con **JetCloseFileInstance** antes de que se pueda abrir otro archivo.</span><span class="sxs-lookup"><span data-stu-id="98084-149">If a file handle is opened using [JetOpenFileInstance](./jetopenfileinstance-function.md) then it must be closed using **JetCloseFileInstance** before another file can be opened.</span></span>

#### <a name="requirements"></a><span data-ttu-id="98084-150">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98084-150">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98084-151"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="98084-151"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="98084-152">Requiere Windows Vista o Windows XP.</span><span class="sxs-lookup"><span data-stu-id="98084-152">Requires Windows Vista or Windows XP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98084-153"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="98084-153"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="98084-154">Requiere Windows Server 2008 o Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="98084-154">Requires Windows Server 2008 or Windows Server 2003.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98084-155"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="98084-155"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="98084-156">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="98084-156">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98084-157"><strong>Library</strong></span><span class="sxs-lookup"><span data-stu-id="98084-157"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="98084-158">Use ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="98084-158">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98084-159"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="98084-159"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="98084-160">Requiere ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="98084-160">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="98084-161">Consulte también</span><span class="sxs-lookup"><span data-stu-id="98084-161">See Also</span></span>

[<span data-ttu-id="98084-162">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="98084-162">JET_ERR</span></span>](./jet-err.md)  
[<span data-ttu-id="98084-163">JET_HANDLE</span><span class="sxs-lookup"><span data-stu-id="98084-163">JET_HANDLE</span></span>](./jet-handle.md)  
[<span data-ttu-id="98084-164">JET_INSTANCE</span><span class="sxs-lookup"><span data-stu-id="98084-164">JET_INSTANCE</span></span>](./jet-instance.md)  
[<span data-ttu-id="98084-165">JetOpenFileInstance</span><span class="sxs-lookup"><span data-stu-id="98084-165">JetOpenFileInstance</span></span>](./jetopenfileinstance-function.md)  
[<span data-ttu-id="98084-166">JetReadFileInstance</span><span class="sxs-lookup"><span data-stu-id="98084-166">JetReadFileInstance</span></span>](./jetreadfileinstance-function.md)  
[<span data-ttu-id="98084-167">JetStopServiceInstance</span><span class="sxs-lookup"><span data-stu-id="98084-167">JetStopServiceInstance</span></span>](./jetstopserviceinstance-function.md)
