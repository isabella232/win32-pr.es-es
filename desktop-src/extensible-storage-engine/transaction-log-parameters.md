---
description: 'Más información acerca de: parámetros de registro de transacciones'
title: Parámetros de registro de transacciones
TOCTitle: Transaction Log Parameters
ms:assetid: 41ade693-2bae-4c84-9339-a68a1b7c23e6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269235(v=EXCHG.10)
ms:contentKeyID: 32765537
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
ms.openlocfilehash: 2d72cafc990d8526cadf7c5f6d149796ff846181
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697438"
---
# <a name="transaction-log-parameters"></a><span data-ttu-id="73391-103">Parámetros de registro de transacciones</span><span class="sxs-lookup"><span data-stu-id="73391-103">Transaction Log Parameters</span></span>


<span data-ttu-id="73391-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="73391-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="73391-105">**En este artículo**</span><span class="sxs-lookup"><span data-stu-id="73391-105">**In this article**</span></span>  
<span data-ttu-id="73391-106">Parámetros de registro de transacciones</span><span class="sxs-lookup"><span data-stu-id="73391-106">Transaction Log Parameters</span></span>  
<span data-ttu-id="73391-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73391-107">Requirements</span></span>  
<span data-ttu-id="73391-108">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73391-108">See Also</span></span>  

## <a name="transaction-log-parameters"></a><span data-ttu-id="73391-109">Parámetros de registro de transacciones</span><span class="sxs-lookup"><span data-stu-id="73391-109">Transaction Log Parameters</span></span>

<span data-ttu-id="73391-110">Este tema contiene los parámetros que se utilizan para los registros de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-110">This topic contains parameters that are used for transaction logs.</span></span>

<span data-ttu-id="73391-111">*JET_paramBaseName*</span><span class="sxs-lookup"><span data-stu-id="73391-111">*JET_paramBaseName*</span></span>  
<span data-ttu-id="73391-112">3</span><span class="sxs-lookup"><span data-stu-id="73391-112">3</span></span>  

<span data-ttu-id="73391-113">Este parámetro establece el prefijo de tres letras que se usa para muchos de los archivos utilizados por el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-113">This parameter sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="73391-114">Por ejemplo, el archivo de punto de comprobación se denomina EDB. CHK de forma predeterminada porque EDB es el nombre base predeterminado.</span><span class="sxs-lookup"><span data-stu-id="73391-114">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span> <span data-ttu-id="73391-115">El nombre base se puede usar para distinguir fácilmente entre los conjuntos de archivos que pertenecen a distintas instancias o a aplicaciones diferentes.</span><span class="sxs-lookup"><span data-stu-id="73391-115">The base name can be used to easily distinguish between sets of files that belong to different instances or to different applications.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-116">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-116">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-117">&quot;EDB&quot;</span><span class="sxs-lookup"><span data-stu-id="73391-117">&quot;edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-118">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-118">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-119">String</span><span class="sxs-lookup"><span data-stu-id="73391-119">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-120">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-120">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-121">3 caracteres</span><span class="sxs-lookup"><span data-stu-id="73391-121">3 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-122">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-122">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-123">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-123">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-124">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-124">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-125">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-125">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-126">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-126">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-127">No</span><span class="sxs-lookup"><span data-stu-id="73391-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-128">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-128">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-129">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-130">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-130">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-131">No</span><span class="sxs-lookup"><span data-stu-id="73391-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-132">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-132">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-133">No</span><span class="sxs-lookup"><span data-stu-id="73391-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-134">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-134">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-135">No</span><span class="sxs-lookup"><span data-stu-id="73391-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-136">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-136">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-137">All</span><span class="sxs-lookup"><span data-stu-id="73391-137">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-138">*JET_paramCircularLog*</span><span class="sxs-lookup"><span data-stu-id="73391-138">*JET_paramCircularLog*</span></span>  
<span data-ttu-id="73391-139">17</span><span class="sxs-lookup"><span data-stu-id="73391-139">17</span></span>  

<span data-ttu-id="73391-140">Este parámetro configura el modo en que el motor de base de datos administra los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-140">This parameter configures how transaction log files are managed by the database engine.</span></span>

<span data-ttu-id="73391-141">Cuando el registro circular está desactivado, todos los archivos de registro de transacciones que se generan se conservan en el disco hasta que ya no son necesarios porque se ha realizado una copia de seguridad completa de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-141">When circular logging is off, all transaction log files that are generated are retained on disk until they are no longer needed because a full backup of the database has been performed.</span></span> <span data-ttu-id="73391-142">En este modo, es posible realizar una restauración a partir de una copia de seguridad anterior y reproducir hacia delante a través de todos los archivos de registro de transacciones retenidos, de modo que no se pierdan datos como resultado del desastre que forzó la restauración.</span><span class="sxs-lookup"><span data-stu-id="73391-142">In this mode, it is possible to restore from an older backup and play forward through all the retained transaction log files such that no data is lost as a result of the disaster that forced the restore.</span></span> <span data-ttu-id="73391-143">Se requieren copias de seguridad completas normales para evitar que el disco se llene con los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-143">Regular full backups are required to prevent the disk from filling up with transaction log files.</span></span>

<span data-ttu-id="73391-144">Cuando el registro circular está activado, solo se conservan en el disco los archivos de registro de transacciones que son más jóvenes que el punto de control actual.</span><span class="sxs-lookup"><span data-stu-id="73391-144">When circular logging is on, only transaction log files that are younger than the current checkpoint are retained on disk.</span></span> <span data-ttu-id="73391-145">La ventaja de este modo es que las copias de seguridad no son necesarias para retirar los archivos de registro de transacciones antiguos.</span><span class="sxs-lookup"><span data-stu-id="73391-145">The benefit of this mode is that backups are not required to retire old transaction log files.</span></span> <span data-ttu-id="73391-146">La contrapartida es que ya no es posible la restauración de una pérdida de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-146">The tradeoff is that a zero data loss restore is no longer possible.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-147">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-147">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-148">False</span><span class="sxs-lookup"><span data-stu-id="73391-148">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-149">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-149">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-150">Boolean</span><span class="sxs-lookup"><span data-stu-id="73391-150">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-151">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-151">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-152">False, True</span><span class="sxs-lookup"><span data-stu-id="73391-152">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-153">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-153">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-154">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-154">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-155">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-155">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-156">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-156">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-157">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-157">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-158">No</span><span class="sxs-lookup"><span data-stu-id="73391-158">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-159">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-159">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-160">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-160">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-161">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-161">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-162">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-162">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-163">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-163">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-164">No</span><span class="sxs-lookup"><span data-stu-id="73391-164">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-165">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-165">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-166">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-166">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-167">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-167">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-168">All</span><span class="sxs-lookup"><span data-stu-id="73391-168">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-169">*JET_paramCommitDefault*</span><span class="sxs-lookup"><span data-stu-id="73391-169">*JET_paramCommitDefault*</span></span>  
<span data-ttu-id="73391-170">16</span><span class="sxs-lookup"><span data-stu-id="73391-170">16</span></span>  

<span data-ttu-id="73391-171">Este parámetro controla la acción predeterminada realizada cuando se confirma la transacción más externa en una sesión.</span><span class="sxs-lookup"><span data-stu-id="73391-171">This parameter controls the default action taken when the outermost transaction is committed on a session.</span></span> <span data-ttu-id="73391-172">Cualquier opción válida que se pueda pasar a [JetCommitTransaction](./jetcommittransaction-function.md) también puede ser la predeterminada para todas las sesiones de una instancia de o para una sesión específica.</span><span class="sxs-lookup"><span data-stu-id="73391-172">Any valid option that can be passed to [JetCommitTransaction](./jetcommittransaction-function.md) can also be made to be the default for all sessions in an instance and/or for a specific session.</span></span> <span data-ttu-id="73391-173">Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obtener más información sobre estas opciones.</span><span class="sxs-lookup"><span data-stu-id="73391-173">See [JetCommitTransaction](./jetcommittransaction-function.md) for more details on these options.</span></span>

<span data-ttu-id="73391-174">Este parámetro afecta a la confiabilidad y el rendimiento de las transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-174">This parameter has an impact on the reliability and performance of transactions.</span></span> <span data-ttu-id="73391-175">Consulte [JetCommitTransaction](./jetcommittransaction-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="73391-175">Please see [JetCommitTransaction](./jetcommittransaction-function.md) for more details.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-176">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-176">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-177">0</span><span class="sxs-lookup"><span data-stu-id="73391-177">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-178">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-179">JET_GRBIT (entero)</span><span class="sxs-lookup"><span data-stu-id="73391-179">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-180">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-181">Una opción válida para JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="73391-181">A valid option for JetCommitTransaction</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-182">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-182">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-183">Instancia o sesión</span><span class="sxs-lookup"><span data-stu-id="73391-183">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-184">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-184">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-185">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-185">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-186">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-186">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-187">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-187">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-188">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-189">No</span><span class="sxs-lookup"><span data-stu-id="73391-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-190">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-191">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-191">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-192">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-193">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-194">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-195">No</span><span class="sxs-lookup"><span data-stu-id="73391-195">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-196">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-197">All</span><span class="sxs-lookup"><span data-stu-id="73391-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-198">*JET_paramDeleteOldLogs*</span><span class="sxs-lookup"><span data-stu-id="73391-198">*JET_paramDeleteOldLogs*</span></span>  
<span data-ttu-id="73391-199">48</span><span class="sxs-lookup"><span data-stu-id="73391-199">48</span></span>  

<span data-ttu-id="73391-200">Cuando este parámetro es true y los archivos de registro de transacciones a los que apunta la ruta de acceso del archivo de registro (**JET_paramLogFilePath**) son una versión obsoleta, esos archivos de registro de transacciones se eliminarán automáticamente.</span><span class="sxs-lookup"><span data-stu-id="73391-200">When this parameter is true and the transaction log files pointed to by the log file path (**JET_paramLogFilePath**) are all of an obsolete version then those transaction log files will be automatically deleted.</span></span>

<span data-ttu-id="73391-201">**Windows 2000:**  Se debe tener cuidado con el uso de este parámetro al actualizar una base de datos de Windows NT a Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="73391-201">**Windows 2000:**  Care must be taken with the use of this parameter when upgrading a database from Windows NT to Windows 2000.</span></span> <span data-ttu-id="73391-202">Si la base de datos no tiene un estado coherente y se eliminan los archivos de registro antiguos, se perderá el contenido de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-202">If the database is not in a consistent state and the old log files are deleted then the contents of the database will be lost.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-203">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-203">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-204"><strong>Windows 2000:</strong>  Es</span><span class="sxs-lookup"><span data-stu-id="73391-204"><strong>Windows 2000:</strong>  False</span></span></p>
<p><span data-ttu-id="73391-205"><strong>Windows XP:</strong>  Reales</span><span class="sxs-lookup"><span data-stu-id="73391-205"><strong>Windows XP:</strong>  True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-206">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-206">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-207">Boolean</span><span class="sxs-lookup"><span data-stu-id="73391-207">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-208">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-208">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-209">False, True</span><span class="sxs-lookup"><span data-stu-id="73391-209">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-210">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-210">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-211">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-211">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-212">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-212">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-213">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-213">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-214">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-214">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-215">No</span><span class="sxs-lookup"><span data-stu-id="73391-215">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-216">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-216">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-217">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-217">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-218">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-218">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-219">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-219">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-220">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-220">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-221">No</span><span class="sxs-lookup"><span data-stu-id="73391-221">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-222">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-222">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-223">No</span><span class="sxs-lookup"><span data-stu-id="73391-223">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-224">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-224">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-225">All</span><span class="sxs-lookup"><span data-stu-id="73391-225">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-226">*JET_paramIgnoreLogVersion*</span><span class="sxs-lookup"><span data-stu-id="73391-226">*JET_paramIgnoreLogVersion*</span></span>  
<span data-ttu-id="73391-227">47</span><span class="sxs-lookup"><span data-stu-id="73391-227">47</span></span>  

<span data-ttu-id="73391-228">Si este parámetro es true, el motor de base de datos no validará el número de versión del archivo de registro de transacciones durante [JetInit](./jetinit-function.md).</span><span class="sxs-lookup"><span data-stu-id="73391-228">If this parameter is true then the database engine will not validate the transaction log file version number during [JetInit](./jetinit-function.md).</span></span>

<span data-ttu-id="73391-229">**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-229">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-230">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-230">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-231">False</span><span class="sxs-lookup"><span data-stu-id="73391-231">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-232">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-232">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-233">Boolean</span><span class="sxs-lookup"><span data-stu-id="73391-233">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-234">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-234">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-235">False, True</span><span class="sxs-lookup"><span data-stu-id="73391-235">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-236">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-236">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-237">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-237">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-238">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-238">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-239">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-239">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-240">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-240">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-241">No</span><span class="sxs-lookup"><span data-stu-id="73391-241">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-242">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-242">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-243">No</span><span class="sxs-lookup"><span data-stu-id="73391-243">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-244">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-244">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-245">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-245">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-246">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-246">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-247">No</span><span class="sxs-lookup"><span data-stu-id="73391-247">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-248">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-248">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-249">No</span><span class="sxs-lookup"><span data-stu-id="73391-249">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-250">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-250">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-251">All</span><span class="sxs-lookup"><span data-stu-id="73391-251">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-252">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="73391-252">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="73391-253">136</span><span class="sxs-lookup"><span data-stu-id="73391-253">136</span></span>  

<span data-ttu-id="73391-254">Este parámetro proporciona compatibilidad con versiones anteriores de las convenciones de nomenclatura de los archivos de las versiones anteriores del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-254">This parameter provides backwards compatibility with the file naming conventions of earlier releases of the database engine.</span></span>

<span data-ttu-id="73391-255">Actualmente se admiten las siguientes opciones:</span><span class="sxs-lookup"><span data-stu-id="73391-255">The following options are currently supported:</span></span>

<span data-ttu-id="73391-256">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="73391-256">JET_bitESE98FileNames</span></span>

<span data-ttu-id="73391-257">Cuando esta opción está presente, el motor de base de datos usará las siguientes convenciones de nomenclatura para sus archivos:</span><span class="sxs-lookup"><span data-stu-id="73391-257">When this option is present then the database engine will use the following naming conventions for its files:</span></span>

  - <span data-ttu-id="73391-258">Los archivos de registro de transacciones utilizarán. LOG para la extensión de archivo</span><span class="sxs-lookup"><span data-stu-id="73391-258">Transaction Log files will use .LOG for their file extension</span></span>

  - <span data-ttu-id="73391-259">Los archivos de punto de comprobación usarán. CHK para la extensión de archivo</span><span class="sxs-lookup"><span data-stu-id="73391-259">Checkpoint files will use .CHK for their file extension</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-260">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-261">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="73391-261">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-262">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-263">JET_GRBIT (entero)</span><span class="sxs-lookup"><span data-stu-id="73391-263">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-264">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-265">0, JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="73391-265">0, JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-266">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-267">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-268">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-269">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-270">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-271">No</span><span class="sxs-lookup"><span data-stu-id="73391-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-272">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-273">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-273">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-274">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-275">No</span><span class="sxs-lookup"><span data-stu-id="73391-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-276">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-277">No</span><span class="sxs-lookup"><span data-stu-id="73391-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-278">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-279">No</span><span class="sxs-lookup"><span data-stu-id="73391-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-280">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-281">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="73391-281">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-282">*JET_paramLogBuffers*</span><span class="sxs-lookup"><span data-stu-id="73391-282">*JET_paramLogBuffers*</span></span>  
<span data-ttu-id="73391-283">12</span><span class="sxs-lookup"><span data-stu-id="73391-283">12</span></span>  

<span data-ttu-id="73391-284">Este parámetro configurará la cantidad de memoria que se usa para almacenar en caché las entradas de registro antes de que se escriban en el archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-284">This parameter will configure the amount of memory used to cache log records before they are written to the transaction log file.</span></span> <span data-ttu-id="73391-285">La unidad para este parámetro es el tamaño de sector del volumen que contiene los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-285">The unit for this parameter is the sector size of the volume that holds the transaction log files.</span></span> <span data-ttu-id="73391-286">El tamaño del sector es casi siempre de 512 bytes, por lo que es seguro suponer ese tamaño para la unidad.</span><span class="sxs-lookup"><span data-stu-id="73391-286">The sector size is almost always 512 bytes, so it is safe to assume that size for the unit.</span></span>

<span data-ttu-id="73391-287">Este parámetro afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73391-287">This parameter has an impact on performance.</span></span> <span data-ttu-id="73391-288">Cuando el motor de base de datos está sometido a una carga de actualización pesada, este búfer puede llenarse con mucha rapidez.</span><span class="sxs-lookup"><span data-stu-id="73391-288">When the database engine is under heavy update load, this buffer can become full very rapidly.</span></span> <span data-ttu-id="73391-289">Un tamaño de caché mayor para el archivo de registro de transacciones es fundamental para un buen rendimiento de actualización en una condición de carga elevada.</span><span class="sxs-lookup"><span data-stu-id="73391-289">A larger cache size for the transaction log file is critical for good update performance under such a high load condition.</span></span> <span data-ttu-id="73391-290">Se sabe que el valor predeterminado es demasiado pequeño para este caso.</span><span class="sxs-lookup"><span data-stu-id="73391-290">The default is known to be too small for this case.</span></span>

<span data-ttu-id="73391-291">**Windows XP y windows 2000:**  En Windows XP y versiones anteriores, no se recomienda establecer este parámetro en un número de búferes mayor (en bytes) de la mitad del tamaño de un archivo de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-291">**Windows XP and Windows 2000:**  On Windows XP and previous releases, it is not recommended to set this parameter to a number of buffers that is larger (in bytes) than half the size of a transaction log file.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-292">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-292">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-293"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  80</span><span class="sxs-lookup"><span data-stu-id="73391-293"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80</span></span></p>
<p><span data-ttu-id="73391-294"><strong>Windows Vista:</strong>  126</span><span class="sxs-lookup"><span data-stu-id="73391-294"><strong>Windows Vista:</strong>  126</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-295">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-295">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-296">Entero</span><span class="sxs-lookup"><span data-stu-id="73391-296">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-297">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-297">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-298"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  80 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="73391-298"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  80 – 2147483647</span></span></p>
<p><span data-ttu-id="73391-299"><strong>Windows Vista:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="73391-299"><strong>Windows Vista:</strong>  1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-300">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-300">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-301">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-301">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-302">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-302">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-303">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-303">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-304">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-304">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-305">No</span><span class="sxs-lookup"><span data-stu-id="73391-305">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-306">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-306">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-307">No</span><span class="sxs-lookup"><span data-stu-id="73391-307">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-308">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-308">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-309">No</span><span class="sxs-lookup"><span data-stu-id="73391-309">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-310">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-310">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-311">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-311">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-312">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-312">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-313">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-313">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-314">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-314">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-315">All</span><span class="sxs-lookup"><span data-stu-id="73391-315">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-316">*JET_paramLogCheckpointPeriod*</span><span class="sxs-lookup"><span data-stu-id="73391-316">*JET_paramLogCheckpointPeriod*</span></span>  
<span data-ttu-id="73391-317">14</span><span class="sxs-lookup"><span data-stu-id="73391-317">14</span></span>  

<span data-ttu-id="73391-318">Este parámetro configura el motor de base de datos para tomar un punto de control cuando se ha generado el número especificado de sectores del archivo de registro.</span><span class="sxs-lookup"><span data-stu-id="73391-318">This parameter configures the database engine to take a checkpoint when the specified number of log file sectors has been generated.</span></span>

<span data-ttu-id="73391-319">**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-319">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-320">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-320">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-321">1024</span><span class="sxs-lookup"><span data-stu-id="73391-321">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-322">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-322">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-323">Entero</span><span class="sxs-lookup"><span data-stu-id="73391-323">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-324">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-324">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-325">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="73391-325">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-326">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-327">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-328">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-329">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-330">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-331">No</span><span class="sxs-lookup"><span data-stu-id="73391-331">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-332">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-333">No</span><span class="sxs-lookup"><span data-stu-id="73391-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-334">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-335">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-336">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-337">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-338">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-339">No</span><span class="sxs-lookup"><span data-stu-id="73391-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-340">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-341">All</span><span class="sxs-lookup"><span data-stu-id="73391-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-342">*JET_paramLogFileCreateAsynch*</span><span class="sxs-lookup"><span data-stu-id="73391-342">*JET_paramLogFileCreateAsynch*</span></span>  
<span data-ttu-id="73391-343">69</span><span class="sxs-lookup"><span data-stu-id="73391-343">69</span></span>  

<span data-ttu-id="73391-344">Cuando este parámetro se establece en true, el motor de base de datos creará el siguiente archivo de registro de transacciones a medida que se consuma el archivo de registro de transacciones actual.</span><span class="sxs-lookup"><span data-stu-id="73391-344">When this parameter is set to true, the database engine will create the next transaction log file as the current transaction log file is consumed.</span></span> <span data-ttu-id="73391-345">La intención es minimizar el tiempo invertido en cambiar de un archivo de registro de transacciones a la siguiente bajo una carga de actualización pesada.</span><span class="sxs-lookup"><span data-stu-id="73391-345">The intent is to minimize the time spent switching from one transaction log file to the next under a heavy update load.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-346">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-347">True</span><span class="sxs-lookup"><span data-stu-id="73391-347">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-348">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-349">Boolean</span><span class="sxs-lookup"><span data-stu-id="73391-349">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-350">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-351">False, True</span><span class="sxs-lookup"><span data-stu-id="73391-351">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-352">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-353">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-354">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-355">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-356">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-357">No</span><span class="sxs-lookup"><span data-stu-id="73391-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-358">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-359">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-359">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-360">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-361">No</span><span class="sxs-lookup"><span data-stu-id="73391-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-362">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-363">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-364">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-365">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-366">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-367">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="73391-367">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-368">*JET_paramLogFilePath*</span><span class="sxs-lookup"><span data-stu-id="73391-368">*JET_paramLogFilePath*</span></span>  
<span data-ttu-id="73391-369">2</span><span class="sxs-lookup"><span data-stu-id="73391-369">2</span></span> 

<span data-ttu-id="73391-370">Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá los registros de transacciones de la instancia.</span><span class="sxs-lookup"><span data-stu-id="73391-370">This parameter indicates the relative or absolute file system path of the folder that will contain the transaction logs for the instance.</span></span> <span data-ttu-id="73391-371">La ruta de acceso debe terminar con un carácter de barra diagonal inversa, lo que indica que la ruta de acceso de destino es una carpeta.</span><span class="sxs-lookup"><span data-stu-id="73391-371">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="73391-372">Los archivos de registro de transacciones contienen la información necesaria para poner los archivos de base de datos en un estado coherente después de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="73391-372">The transaction log files contain the information required to bring the database files to a consistent state after a crash.</span></span> <span data-ttu-id="73391-373">Normalmente se denominan EDB \* . Inicia.</span><span class="sxs-lookup"><span data-stu-id="73391-373">They are typically named EDB\*.LOG.</span></span> <span data-ttu-id="73391-374">El contenido de los archivos de registro de transacciones es tan importante (si no más) que los propios archivos de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-374">The contents of the transaction log files are just as important (if not more so) than the database files themselves.</span></span> <span data-ttu-id="73391-375">Se debe hacer todo lo posible para protegerlos.</span><span class="sxs-lookup"><span data-stu-id="73391-375">Every effort should be made to protect them.</span></span>

<span data-ttu-id="73391-376">También habrá archivos de registro de reserva adicionales denominados RES1. LOG y RES2. REGISTRO almacenado junto con los archivos de registro normales.</span><span class="sxs-lookup"><span data-stu-id="73391-376">There will also be additional reserve log files named RES1.LOG and RES2.LOG stored along with the ordinary log files.</span></span> <span data-ttu-id="73391-377">El contenido de estos archivos no es importante porque su único propósito es reservar espacio en disco para permitir que el motor se cierre correctamente en un escenario de disco insuficiente.</span><span class="sxs-lookup"><span data-stu-id="73391-377">The contents of these files are not important as their only purpose is to reserve disk space to allow the engine to shut down gracefully in a low disk scenario.</span></span> <span data-ttu-id="73391-378">También serán un archivo de registro temporal denominado EDBTMP. Inicie sesión en esta misma carpeta.</span><span class="sxs-lookup"><span data-stu-id="73391-378">These will also be a temporary log file typically named EDBTMP.LOG in this same folder.</span></span> <span data-ttu-id="73391-379">El contenido de este archivo no es importante.</span><span class="sxs-lookup"><span data-stu-id="73391-379">The contents of this file are not important either.</span></span> <span data-ttu-id="73391-380">Este archivo es un nuevo archivo de registro que se está preparando para su uso.</span><span class="sxs-lookup"><span data-stu-id="73391-380">This file is a new log file being prepared for use.</span></span>

<span data-ttu-id="73391-381">Las propiedades del volumen de host de los archivos de registro de transacciones y su ubicación en relación con los otros archivos utilizados por el motor de base de datos pueden afectar drásticamente al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73391-381">The properties of the host volume of the transaction log files and their placement relative to the other files used by the database engine can dramatically impact performance.</span></span>

<span data-ttu-id="73391-382">**Nota:**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-382">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-383">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-384">&quot;.\& entrecomillados</span><span class="sxs-lookup"><span data-stu-id="73391-384">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-385">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-386">Ruta de acceso de la carpeta (cadena)</span><span class="sxs-lookup"><span data-stu-id="73391-386">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-387">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-388">de 0 a 246 caracteres</span><span class="sxs-lookup"><span data-stu-id="73391-388">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-389">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-390">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-390">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-391">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-392">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-392">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-393">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-394">No</span><span class="sxs-lookup"><span data-stu-id="73391-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-395">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-396">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-396">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-397">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-398">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-398">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-399">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-400">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-401">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-402">No</span><span class="sxs-lookup"><span data-stu-id="73391-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-403">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-404">All</span><span class="sxs-lookup"><span data-stu-id="73391-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-405">*JET_paramLogFileSize*</span><span class="sxs-lookup"><span data-stu-id="73391-405">*JET_paramLogFileSize*</span></span>  
<span data-ttu-id="73391-406">11</span><span class="sxs-lookup"><span data-stu-id="73391-406">11</span></span>  

<span data-ttu-id="73391-407">Este parámetro configurará el tamaño de los archivos de registro de transacciones.</span><span class="sxs-lookup"><span data-stu-id="73391-407">This parameter will configure the size of the transaction log files.</span></span> <span data-ttu-id="73391-408">Cada archivo de registro de transacciones tiene un tamaño fijo.</span><span class="sxs-lookup"><span data-stu-id="73391-408">Each transaction log file is a fixed size.</span></span> <span data-ttu-id="73391-409">El tamaño es igual al valor de este parámetro del sistema en unidades de 1024 bytes.</span><span class="sxs-lookup"><span data-stu-id="73391-409">The size is equal to the setting of this system parameter in units of 1024 bytes.</span></span>

<span data-ttu-id="73391-410">Este parámetro afecta a la confiabilidad.</span><span class="sxs-lookup"><span data-stu-id="73391-410">This parameter has an impact on reliability.</span></span> <span data-ttu-id="73391-411">Si el valor es demasiado pequeño, el número máximo de archivos de registro (1048575) se alcanzará mucho más rápido.</span><span class="sxs-lookup"><span data-stu-id="73391-411">If the setting is too small then the maximum number of log files (1048575) will be reached much faster.</span></span> <span data-ttu-id="73391-412">Cuando esto sucede, la instancia debe cerrarse correctamente, se deben eliminar los archivos de registro existentes y se debe reiniciar la instancia.</span><span class="sxs-lookup"><span data-stu-id="73391-412">When this happens, the instance must be shutdown cleanly, the existing log files must be deleted, and the instance must be restarted.</span></span> <span data-ttu-id="73391-413">Esta acción no solo reducirá la disponibilidad de la aplicación, sino que también invalidará las copias de seguridad anteriores de la base de datos de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="73391-413">This action will not only reduce the availability of the application but it will also invalidate any previous backups of the application's database.</span></span>

<span data-ttu-id="73391-414">Este parámetro afecta al rendimiento.</span><span class="sxs-lookup"><span data-stu-id="73391-414">This parameter has an impact on performance.</span></span> <span data-ttu-id="73391-415">Si el valor es muy grande, [JetInit](./jetinit-function.md) será lento, ya que el motor de base de datos debe leer el archivo de registro más reciente (como mínimo) cuando se inicializa.</span><span class="sxs-lookup"><span data-stu-id="73391-415">If the setting is very large then [JetInit](./jetinit-function.md) will be slow because the database engine must read the youngest log file (at a minimum) when it initializes.</span></span> <span data-ttu-id="73391-416">Si el valor es muy grande, también tardará más tiempo en cambiar entre los archivos de registro.</span><span class="sxs-lookup"><span data-stu-id="73391-416">If the setting is very large then it will also take longer to switch between log files.</span></span> <span data-ttu-id="73391-417">Si el valor es muy pequeño, se deberán crear más archivos de registro para un número determinado de actualizaciones que agregarán más sobrecarga.</span><span class="sxs-lookup"><span data-stu-id="73391-417">If the setting is very small then more log files will need to be created for a given number of updates which will add more overhead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-418">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-418">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-419">5120</span><span class="sxs-lookup"><span data-stu-id="73391-419">5120</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-420">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-420">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-421">Entero</span><span class="sxs-lookup"><span data-stu-id="73391-421">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-422">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-422">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-423"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  128 – 32768</span><span class="sxs-lookup"><span data-stu-id="73391-423"><strong>Windows 2000, Windows XP, and Windows Server 2003:</strong>  128 – 32768</span></span></p>
<p><span data-ttu-id="73391-424"><strong>Windows Vista:</strong>  64 – 32768</span><span class="sxs-lookup"><span data-stu-id="73391-424"><strong>Windows Vista:</strong>  64 – 32768</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-425">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-425">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-426">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-426">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-427">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-427">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-428">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-428">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-429">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-429">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-430">No</span><span class="sxs-lookup"><span data-stu-id="73391-430">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-431">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-431">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-432">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-432">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-433">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-433">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-434">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-434">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-435">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-435">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-436">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-436">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-437">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-437">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-438">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-438">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-439">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-439">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-440">All</span><span class="sxs-lookup"><span data-stu-id="73391-440">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-441">*JET_paramLogWaitingUserMax*</span><span class="sxs-lookup"><span data-stu-id="73391-441">*JET_paramLogWaitingUserMax*</span></span>  
<span data-ttu-id="73391-442">15</span><span class="sxs-lookup"><span data-stu-id="73391-442">15</span></span>  

<span data-ttu-id="73391-443">Este parámetro intenta optimizar el vaciado del búfer de registro causado por una confirmación duradera al esperar a que un número especificado de sesiones espere una confirmación duradera antes de forzar que se produzca una operación de vaciado en la espera de que otra transacción comparta el vaciado.</span><span class="sxs-lookup"><span data-stu-id="73391-443">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified number of sessions to wait for a durable commit prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="73391-444">**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-444">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-445">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-445">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-446">3</span><span class="sxs-lookup"><span data-stu-id="73391-446">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-447">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-447">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-448">Entero</span><span class="sxs-lookup"><span data-stu-id="73391-448">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-449">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-449">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-450">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="73391-450">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-451">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-451">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-452">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-452">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-453">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-453">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-454">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-454">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-455">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-455">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-456">No</span><span class="sxs-lookup"><span data-stu-id="73391-456">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-457">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-457">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-458">No</span><span class="sxs-lookup"><span data-stu-id="73391-458">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-459">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-459">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-460">No</span><span class="sxs-lookup"><span data-stu-id="73391-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-461">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-461">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-462">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-463">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-463">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-464">No</span><span class="sxs-lookup"><span data-stu-id="73391-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-465">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-465">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-466">All</span><span class="sxs-lookup"><span data-stu-id="73391-466">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-467">*JET_paramRecovery*</span><span class="sxs-lookup"><span data-stu-id="73391-467">*JET_paramRecovery*</span></span>  
<span data-ttu-id="73391-468">34</span><span class="sxs-lookup"><span data-stu-id="73391-468">34</span></span>  

<span data-ttu-id="73391-469">Este parámetro es el modificador principal que controla la recuperación tras bloqueo de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="73391-469">This parameter is the master switch that controls crash recovery for an instance.</span></span> <span data-ttu-id="73391-470">Si este parámetro se establece en "ON", se usará la recuperación de estilo ARIES para que todas las bases de datos de la instancia tengan un estado coherente en caso de que se produzca un bloqueo del proceso o del equipo.</span><span class="sxs-lookup"><span data-stu-id="73391-470">If this parameter is set to "On" then ARIES style recovery will be used to bring all databases in the instance to a consistent state in the event of a process or machine crash.</span></span> <span data-ttu-id="73391-471">Si este parámetro se establece en "OFF", todas las bases de datos de la instancia se administrarán sin la ventaja de la recuperación tras bloqueo.</span><span class="sxs-lookup"><span data-stu-id="73391-471">If this parameter is set to "Off" then all databases in the instance will be managed without the benefit of crash recovery.</span></span> <span data-ttu-id="73391-472">Es decir, que si la instancia no se cierra correctamente con [JetTerm](./jetterm-function.md) antes de que el proceso salga o cierre el equipo, el contenido de todas las bases de datos de esa instancia estará dañado.</span><span class="sxs-lookup"><span data-stu-id="73391-472">That is to say, that if the instance is not shut down cleanly using [JetTerm](./jetterm-function.md) prior to the process exiting or machine shutdown then the contents of all databases in that instance will be corrupted.</span></span>

<span data-ttu-id="73391-473">La deshabilitación de la recuperación resulta útil en circunstancias especiales en las que se sabe que el contenido de una base de datos no es útil en caso de bloqueo.</span><span class="sxs-lookup"><span data-stu-id="73391-473">Disabling recovery is useful in special circumstances where it is known that the contents of a database are not useful in the event of a crash.</span></span> <span data-ttu-id="73391-474">La recuperación debe estar habilitada para todos los demás casos.</span><span class="sxs-lookup"><span data-stu-id="73391-474">Recovery should be enabled for all other cases.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-475">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-475">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-476">&quot;Activado&quot;</span><span class="sxs-lookup"><span data-stu-id="73391-476">&quot;On&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-477">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-477">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-478">String</span><span class="sxs-lookup"><span data-stu-id="73391-478">String</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-479">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-479">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-480">de 0 a 259 caracteres</span><span class="sxs-lookup"><span data-stu-id="73391-480">0 – 259 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-481">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-481">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-482">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-482">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-483">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-483">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-484">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-484">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-485">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-485">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-486">No</span><span class="sxs-lookup"><span data-stu-id="73391-486">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-487">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-487">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-488">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-488">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-489">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-489">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-490">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-490">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-491">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-491">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-492">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-492">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-493">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-493">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-494">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-494">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-495">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-495">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-496">All</span><span class="sxs-lookup"><span data-stu-id="73391-496">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-497">*JET_paramSystemPath*</span><span class="sxs-lookup"><span data-stu-id="73391-497">*JET_paramSystemPath*</span></span>  
<span data-ttu-id="73391-498">0</span><span class="sxs-lookup"><span data-stu-id="73391-498">0</span></span>  

<span data-ttu-id="73391-499">Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta que contendrá el archivo de punto de comprobación de la instancia.</span><span class="sxs-lookup"><span data-stu-id="73391-499">This parameter indicates the relative or absolute file system path of the folder that will contain the checkpoint file for the instance.</span></span> <span data-ttu-id="73391-500">La ruta de acceso debe terminar con un carácter de barra diagonal inversa, lo que indica que la ruta de acceso de destino es una carpeta.</span><span class="sxs-lookup"><span data-stu-id="73391-500">The path must be terminated with a backslash character, which indicates that the target path is a folder.</span></span> <span data-ttu-id="73391-501">El archivo de punto de comprobación es un archivo simple mantenido por instancia que recuerda el archivo de registro de transacciones más antiguo que debe reproducirse para que todas las bases de datos de esa instancia tengan un estado coherente después de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="73391-501">The checkpoint file is a simple file maintained per instance that remembers the oldest transaction log file that must be replayed to bring all databases in that instance to a consistent state after a crash.</span></span> <span data-ttu-id="73391-502">El archivo de punto de comprobación se denomina normalmente EDB. CHK.</span><span class="sxs-lookup"><span data-stu-id="73391-502">The checkpoint file is typically named EDB.CHK.</span></span>

<span data-ttu-id="73391-503">**Nota:**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-503">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-504">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-504">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-505">&quot;.\& entrecomillados</span><span class="sxs-lookup"><span data-stu-id="73391-505">&quot;.\&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-506">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-506">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-507">Ruta de acceso de la carpeta (cadena)</span><span class="sxs-lookup"><span data-stu-id="73391-507">Folder Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-508">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-508">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-509">de 0 a 246 caracteres</span><span class="sxs-lookup"><span data-stu-id="73391-509">0 – 246 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-510">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-510">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-511">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-511">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-512">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-512">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-513">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-513">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-514">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-514">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-515">No</span><span class="sxs-lookup"><span data-stu-id="73391-515">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-516">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-516">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-517">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-517">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-518">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-518">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-519">No</span><span class="sxs-lookup"><span data-stu-id="73391-519">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-520">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-520">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-521">No</span><span class="sxs-lookup"><span data-stu-id="73391-521">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-522">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-522">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-523">No</span><span class="sxs-lookup"><span data-stu-id="73391-523">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-524">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-524">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-525">All</span><span class="sxs-lookup"><span data-stu-id="73391-525">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-526">*JET_paramWaitLogFlush*</span><span class="sxs-lookup"><span data-stu-id="73391-526">*JET_paramWaitLogFlush*</span></span>  
<span data-ttu-id="73391-527">13</span><span class="sxs-lookup"><span data-stu-id="73391-527">13</span></span> 

<span data-ttu-id="73391-528">Este parámetro intenta optimizar el vaciado del búfer de registro causado por una confirmación duradera esperando un período de tiempo especificado antes de forzar que se produzca una operación de vaciado, por lo que otra transacción compartirá el vaciado.</span><span class="sxs-lookup"><span data-stu-id="73391-528">This parameter attempts to optimize the flush of the log buffer caused by a durable commit by waiting for a specified time period prior to forcing a flush to occur in the hope that another transaction will share the flush.</span></span>

<span data-ttu-id="73391-529">**Windows XP:**  A partir de Windows XP, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="73391-529">**Windows XP:**  As of Windows XP, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-530">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-530">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-531">0</span><span class="sxs-lookup"><span data-stu-id="73391-531">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-532">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-532">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-533">Entero</span><span class="sxs-lookup"><span data-stu-id="73391-533">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-534">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-534">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-535">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="73391-535">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-536">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-536">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-537">Instancia o sesión</span><span class="sxs-lookup"><span data-stu-id="73391-537">Instance or Session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-538">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-538">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-539">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-539">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-540">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-540">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-541">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-541">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-542">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-542">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-543">No</span><span class="sxs-lookup"><span data-stu-id="73391-543">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-544">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-544">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-545">No</span><span class="sxs-lookup"><span data-stu-id="73391-545">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-546">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-546">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-547">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-547">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-548">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-548">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-549">No</span><span class="sxs-lookup"><span data-stu-id="73391-549">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-550">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-550">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-551">All</span><span class="sxs-lookup"><span data-stu-id="73391-551">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73391-552">*JET_paramLegacyFileNames*</span><span class="sxs-lookup"><span data-stu-id="73391-552">*JET_paramLegacyFileNames*</span></span>  
<span data-ttu-id="73391-553">136</span><span class="sxs-lookup"><span data-stu-id="73391-553">136</span></span>  

<span data-ttu-id="73391-554">Este parámetro se usa para especificar las características de compatibilidad de nombres de archivo que se deben mantener con Windows Server 2003 y el esquema de nombres de archivo anterior.</span><span class="sxs-lookup"><span data-stu-id="73391-554">This parameter is used to specify the file naming compatibility features to maintain with the Windows Server 2003 and previous file naming scheme.</span></span> <span data-ttu-id="73391-555">Para obtener más información sobre los distintos archivos y su nombre, consulte [archivos del motor de almacenamiento extensible](./extensible-storage-engine-files.md).</span><span class="sxs-lookup"><span data-stu-id="73391-555">For more information about the different files and their naming see [Extensible Storage Engine Files](./extensible-storage-engine-files.md).</span></span>

<span data-ttu-id="73391-556">El JET_bitESE98FileNames garantiza la extensión de archivo que se usa en los archivos de registro de transacciones y el archivo de punto de comprobación son los mismos que se usan en Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="73391-556">The JET_bitESE98FileNames ensures the file extension used on the transaction log files and the checkpoint file are the same as that used in Windows Server 2003.</span></span> <span data-ttu-id="73391-557">Nota: si se actualiza desde Windows Server 2003, no es necesario especificar este bit, ya que el motor actualizará automáticamente las extensiones de archivo si JET_paramCircularLog está establecido en **true** o mantiene la extensión de registro anterior si JET_paramCircularLog es **false**.</span><span class="sxs-lookup"><span data-stu-id="73391-557">Note if upgrading from Windows Server 2003, this bit still need not be specified, as the engine will automatically upgrade the file extensions if JET_paramCircularLog is set to **true**, or maintain the older log extension if JET_paramCircularLog is **false**.</span></span>

<span data-ttu-id="73391-558">**Nota:**  Para establecer un bit, primero se debe recuperar el valor y, después, "or" en el bit de compatibilidad deseado.</span><span class="sxs-lookup"><span data-stu-id="73391-558">**Note**  To set a bit, the value should first be retrieved, and then "or" in the desired compatibility bit.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-559">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="73391-559">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="73391-560">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="73391-560">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-561">Escriba:</span><span class="sxs-lookup"><span data-stu-id="73391-561">Type:</span></span></p></td>
<td><p><span data-ttu-id="73391-562">JET_GRBIT (entero)</span><span class="sxs-lookup"><span data-stu-id="73391-562">JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-563">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="73391-563">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="73391-564">JET_bitESE98FileNames</span><span class="sxs-lookup"><span data-stu-id="73391-564">JET_bitESE98FileNames</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-565">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="73391-565">Scope:</span></span></p></td>
<td><p><span data-ttu-id="73391-566">Instancia</span><span class="sxs-lookup"><span data-stu-id="73391-566">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-567">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-567">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-568">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-568">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-569">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="73391-569">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="73391-570">No</span><span class="sxs-lookup"><span data-stu-id="73391-570">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-571">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="73391-571">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="73391-572">Sí</span><span class="sxs-lookup"><span data-stu-id="73391-572">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-573">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-573">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="73391-574">No</span><span class="sxs-lookup"><span data-stu-id="73391-574">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-575">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="73391-575">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="73391-576">No</span><span class="sxs-lookup"><span data-stu-id="73391-576">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-577">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="73391-577">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="73391-578">No</span><span class="sxs-lookup"><span data-stu-id="73391-578">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-579">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="73391-579">Availability:</span></span></p></td>
<td><p><span data-ttu-id="73391-580">A partir de Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73391-580">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="requirements"></a><span data-ttu-id="73391-581">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73391-581">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73391-582"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="73391-582"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="73391-583">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="73391-583">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73391-584"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="73391-584"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="73391-585">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="73391-585">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73391-586"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="73391-586"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="73391-587">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="73391-587">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="73391-588">Consulte también</span><span class="sxs-lookup"><span data-stu-id="73391-588">See Also</span></span>

[<span data-ttu-id="73391-589">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="73391-589">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="73391-590">JetCommitTransaction</span><span class="sxs-lookup"><span data-stu-id="73391-590">JetCommitTransaction</span></span>](./jetcommittransaction-function.md)  
[<span data-ttu-id="73391-591">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="73391-591">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="73391-592">JetInit</span><span class="sxs-lookup"><span data-stu-id="73391-592">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="73391-593">JetTerm</span><span class="sxs-lookup"><span data-stu-id="73391-593">JetTerm</span></span>](./jetterm-function.md)
