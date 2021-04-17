---
description: Más información acerca de los parámetros de copia de seguridad y restauración
title: Parámetros de copia de seguridad y restauración
TOCTitle: Backup and Restore Parameters
ms:assetid: 432aff79-8766-428a-9a14-530f575308d0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269236(v=EXCHG.10)
ms:contentKeyID: 32765538
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
ms.openlocfilehash: 1940f3f93bdc018068868c5645409b22574c9fb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546846"
---
# <a name="backup-and-restore-parameters"></a><span data-ttu-id="b191f-103">Parámetros de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="b191f-103">Backup and Restore Parameters</span></span>


<span data-ttu-id="b191f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="b191f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="backup-and-restore-parameters"></a><span data-ttu-id="b191f-105">Parámetros de copia de seguridad y restauración</span><span class="sxs-lookup"><span data-stu-id="b191f-105">Backup and Restore Parameters</span></span>

<span data-ttu-id="b191f-106">Este tema contiene los parámetros que se usan para la copia de seguridad y la restauración.</span><span class="sxs-lookup"><span data-stu-id="b191f-106">This topic contains parameters that are used for backup and restore.</span></span>

<span data-ttu-id="b191f-107">*JET_paramAlternateDatabaseRecoveryPath*</span><span class="sxs-lookup"><span data-stu-id="b191f-107">*JET_paramAlternateDatabaseRecoveryPath*</span></span>  
<span data-ttu-id="b191f-108">113</span><span class="sxs-lookup"><span data-stu-id="b191f-108">113</span></span>  

<span data-ttu-id="b191f-109">La ruta de acceso completa a cada base de datos se conserva en los registros de transacciones en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="b191f-109">The full path to each database is persisted in the transaction logs at run time.</span></span> <span data-ttu-id="b191f-110">Normalmente, estas bases de datos deben permanecer en la ubicación original para que la reproducción de transacciones funcione correctamente.</span><span class="sxs-lookup"><span data-stu-id="b191f-110">Ordinarily, these databases must remain at the original location for transaction replay to function correctly.</span></span> <span data-ttu-id="b191f-111">Este parámetro se puede usar para forzar la recuperación tras bloqueo o una operación de restauración para buscar las bases de datos a las que se hace referencia en el registro de transacciones en la carpeta especificada.</span><span class="sxs-lookup"><span data-stu-id="b191f-111">This parameter can be used to force crash recovery or a restore operation to look for the databases referenced in the transaction log in the specified folder.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b191f-112">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b191f-112">Default Value:</span></span></p></td>
<td><p>&quot;&quot;</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b191f-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="b191f-114">Ruta de acceso de la carpeta (cadena)</span><span class="sxs-lookup"><span data-stu-id="b191f-114">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b191f-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b191f-116">de 0 a 246 caracteres</span><span class="sxs-lookup"><span data-stu-id="b191f-116">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-117">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b191f-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b191f-118">Instancia</span><span class="sxs-lookup"><span data-stu-id="b191f-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-119">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-120">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-121">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-122">No</span><span class="sxs-lookup"><span data-stu-id="b191f-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-123">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b191f-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b191f-124">No</span><span class="sxs-lookup"><span data-stu-id="b191f-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-125">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-126">No</span><span class="sxs-lookup"><span data-stu-id="b191f-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-127">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b191f-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b191f-128">No</span><span class="sxs-lookup"><span data-stu-id="b191f-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-129">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b191f-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b191f-130">No</span><span class="sxs-lookup"><span data-stu-id="b191f-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-131">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-132">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b191f-132">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b191f-133">*JET_paramCleanupMismatchedLogFiles*</span><span class="sxs-lookup"><span data-stu-id="b191f-133">*JET_paramCleanupMismatchedLogFiles*</span></span>  
<span data-ttu-id="b191f-134">77</span><span class="sxs-lookup"><span data-stu-id="b191f-134">77</span></span>  

<span data-ttu-id="b191f-135">Este parámetro controla el resultado de [JetInit](./jetinit-function.md) cuando el motor de base de datos está configurado para empezar a usar archivos de registro de transacciones en un disco con un tamaño diferente del configurado.</span><span class="sxs-lookup"><span data-stu-id="b191f-135">This parameter controls the outcome of [JetInit](./jetinit-function.md) when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="b191f-136">Normalmente, [JetInit](./jetinit-function.md) recuperará correctamente las bases de datos, pero producirá un error con JET_errLogFileSizeMismatchDatabasesConsistent para indicar que el tamaño del archivo de registro está mal configurado.</span><span class="sxs-lookup"><span data-stu-id="b191f-136">Normally, [JetInit](./jetinit-function.md) will successfully recover the databases but will fail with JET_errLogFileSizeMismatchDatabasesConsistent to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="b191f-137">Sin embargo, cuando este parámetro se establece en true, el motor de base de datos eliminará los archivos de registro antiguos de forma silenciosa, iniciará un nuevo conjunto de archivos de registro de transacciones con el tamaño de archivo de registro configurado y devolverá JET_errSuccess.</span><span class="sxs-lookup"><span data-stu-id="b191f-137">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size, and return JET_errSuccess.</span></span>

<span data-ttu-id="b191f-138">Este parámetro es útil cuando la aplicación desea cambiar de forma transparente el tamaño del archivo de registro de transacciones todavía funciona de forma transparente en los escenarios de actualización y restauración.</span><span class="sxs-lookup"><span data-stu-id="b191f-138">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b191f-139">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b191f-139">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b191f-140">False</span><span class="sxs-lookup"><span data-stu-id="b191f-140">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-141">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b191f-141">Type:</span></span></p></td>
<td><p><span data-ttu-id="b191f-142">Boolean</span><span class="sxs-lookup"><span data-stu-id="b191f-142">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-143">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b191f-143">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b191f-144">False, True</span><span class="sxs-lookup"><span data-stu-id="b191f-144">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-145">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b191f-145">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b191f-146">Instancia</span><span class="sxs-lookup"><span data-stu-id="b191f-146">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-147">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-147">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-148">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-148">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-149">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-149">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-150">No</span><span class="sxs-lookup"><span data-stu-id="b191f-150">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-151">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b191f-151">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b191f-152">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-153">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-153">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-154">No</span><span class="sxs-lookup"><span data-stu-id="b191f-154">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-155">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b191f-155">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b191f-156">No</span><span class="sxs-lookup"><span data-stu-id="b191f-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-157">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b191f-157">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b191f-158">No</span><span class="sxs-lookup"><span data-stu-id="b191f-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-159">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-159">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-160">All</span><span class="sxs-lookup"><span data-stu-id="b191f-160">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b191f-161">*JET_paramDeleteOutOfRangeLogs*</span><span class="sxs-lookup"><span data-stu-id="b191f-161">*JET_paramDeleteOutOfRangeLogs*</span></span>  
<span data-ttu-id="b191f-162">52</span><span class="sxs-lookup"><span data-stu-id="b191f-162">52</span></span>  

<span data-ttu-id="b191f-163">Cuando este parámetro es true, los archivos de registro de transacciones que se encuentran en el disco y que no forman parte de la secuencia actual de archivos de registro se eliminarán mediante [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="b191f-163">When this parameter is true, then any transaction log files found on disk that are not part of the current sequence of log files will be deleted by [JetInit](./jetinit-function.md).</span></span> <span data-ttu-id="b191f-164">Se puede usar para limpiar automáticamente los archivos de registro superfluos después de una operación de restauración.</span><span class="sxs-lookup"><span data-stu-id="b191f-164">This may be used to automatically clean up extraneous log files after a restore operation.</span></span>

<span data-ttu-id="b191f-165">**Windows XP:**  Introducido en Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b191f-165">**Windows XP:**  Introduced in Windows XP.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b191f-166">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b191f-166">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b191f-167">False</span><span class="sxs-lookup"><span data-stu-id="b191f-167">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-168">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b191f-168">Type:</span></span></p></td>
<td><p><span data-ttu-id="b191f-169">Boolean</span><span class="sxs-lookup"><span data-stu-id="b191f-169">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-170">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b191f-170">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b191f-171">False, True</span><span class="sxs-lookup"><span data-stu-id="b191f-171">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-172">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b191f-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b191f-173">Instancia</span><span class="sxs-lookup"><span data-stu-id="b191f-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-174">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-175">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-176">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-177">No</span><span class="sxs-lookup"><span data-stu-id="b191f-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-178">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b191f-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b191f-179">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-179">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-180">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-181">No</span><span class="sxs-lookup"><span data-stu-id="b191f-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-182">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b191f-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b191f-183">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-183">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-184">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b191f-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b191f-185">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-185">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-186">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-187">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b191f-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b191f-188">*JET_paramOSSnapshotTimeout*</span><span class="sxs-lookup"><span data-stu-id="b191f-188">*JET_paramOSSnapshotTimeout*</span></span>  
<span data-ttu-id="b191f-189">82</span><span class="sxs-lookup"><span data-stu-id="b191f-189">82</span></span>  

<span data-ttu-id="b191f-190">Este parámetro configura la cantidad de tiempo que se permite entre una llamada a [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) y [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) antes de que se agote el tiempo de espera.</span><span class="sxs-lookup"><span data-stu-id="b191f-190">This parameter configures the amount of time allowed between a call to [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) before a timeout occurs.</span></span> <span data-ttu-id="b191f-191">Consulte [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) y [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="b191f-191">Please see [JetOSSnapshotFreeze](./jetossnapshotfreeze-function.md) and [JetOSSnapshotThaw](./jetossnapshotthaw-function.md) for more information.</span></span> <span data-ttu-id="b191f-192">El tiempo de espera es en milisegundos.</span><span class="sxs-lookup"><span data-stu-id="b191f-192">The timeout is in milliseconds.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b191f-193">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b191f-193">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b191f-194">20000 (Windows XP y Windows Server 2003);</span><span class="sxs-lookup"><span data-stu-id="b191f-194">20000 (Windows XP and Windows Server 2003);</span></span></p>
<p><span data-ttu-id="b191f-195">70000 (Windows Server 2003 SP1)</span><span class="sxs-lookup"><span data-stu-id="b191f-195">70000 (Windows Server 2003 SP1)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-196">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b191f-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="b191f-197">Entero</span><span class="sxs-lookup"><span data-stu-id="b191f-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-198">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b191f-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b191f-199">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="b191f-199">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-200">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b191f-200">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b191f-201">Global</span><span class="sxs-lookup"><span data-stu-id="b191f-201">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-202">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-202">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-203">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-203">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-204">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-204">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-205">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-205">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-206">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b191f-206">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b191f-207">No</span><span class="sxs-lookup"><span data-stu-id="b191f-207">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-208">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-208">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-209">No</span><span class="sxs-lookup"><span data-stu-id="b191f-209">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-210">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b191f-210">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b191f-211">No</span><span class="sxs-lookup"><span data-stu-id="b191f-211">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-212">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b191f-212">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b191f-213">No</span><span class="sxs-lookup"><span data-stu-id="b191f-213">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-214">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-214">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-215">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b191f-215">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b191f-216">*JET_paramZeroDatabaseDuringBackup*</span><span class="sxs-lookup"><span data-stu-id="b191f-216">*JET_paramZeroDatabaseDuringBackup*</span></span>  
<span data-ttu-id="b191f-217">71</span><span class="sxs-lookup"><span data-stu-id="b191f-217">71</span></span>  

<span data-ttu-id="b191f-218">Cuando este parámetro es true, todas las páginas de una base de datos que se está sometiendo a una copia de seguridad de streaming se borrarán de los datos eliminados.</span><span class="sxs-lookup"><span data-stu-id="b191f-218">When this parameter is true then every page in a database that is undergoing a streaming backup will be scrubbed of deleted data.</span></span> <span data-ttu-id="b191f-219">Es importante tener en cuenta que las páginas de la base de datos que se van a limpiar están en el disco.</span><span class="sxs-lookup"><span data-stu-id="b191f-219">It is important to note that the database pages that are being scrubbed are on disk.</span></span> <span data-ttu-id="b191f-220">Se realiza una copia de seguridad del conjunto de datos completo antes del proceso de limpieza.</span><span class="sxs-lookup"><span data-stu-id="b191f-220">The full data set is backed up prior to the scrub process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b191f-221">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="b191f-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="b191f-222">False</span><span class="sxs-lookup"><span data-stu-id="b191f-222">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-223">Escriba:</span><span class="sxs-lookup"><span data-stu-id="b191f-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="b191f-224">Boolean</span><span class="sxs-lookup"><span data-stu-id="b191f-224">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-225">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="b191f-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="b191f-226">False, True</span><span class="sxs-lookup"><span data-stu-id="b191f-226">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-227">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="b191f-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="b191f-228">Instancia</span><span class="sxs-lookup"><span data-stu-id="b191f-228">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-229">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-230">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-230">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-231">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="b191f-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="b191f-232">No</span><span class="sxs-lookup"><span data-stu-id="b191f-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-233">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="b191f-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="b191f-234">No</span><span class="sxs-lookup"><span data-stu-id="b191f-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-235">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-236">No</span><span class="sxs-lookup"><span data-stu-id="b191f-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-237">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="b191f-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="b191f-238">Sí</span><span class="sxs-lookup"><span data-stu-id="b191f-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-239">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="b191f-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="b191f-240">No</span><span class="sxs-lookup"><span data-stu-id="b191f-240">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-241">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="b191f-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="b191f-242">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="b191f-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="b191f-243">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b191f-243">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b191f-244"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="b191f-244"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="b191f-245">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="b191f-245">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b191f-246"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="b191f-246"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="b191f-247">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="b191f-247">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b191f-248"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="b191f-248"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="b191f-249">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="b191f-249">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="b191f-250">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b191f-250">See Also</span></span>

[<span data-ttu-id="b191f-251">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="b191f-251">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="b191f-252">JetInit</span><span class="sxs-lookup"><span data-stu-id="b191f-252">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="b191f-253">JetOSSnapshotFreeze</span><span class="sxs-lookup"><span data-stu-id="b191f-253">JetOSSnapshotFreeze</span></span>](./jetossnapshotfreeze-function.md)  
[<span data-ttu-id="b191f-254">JetOSSnapshotThaw</span><span class="sxs-lookup"><span data-stu-id="b191f-254">JetOSSnapshotThaw</span></span>](./jetossnapshotthaw-function.md)
