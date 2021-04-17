---
description: 'Más información acerca de: JET_ERRCAT'
title: JET_ERRCAT
TOCTitle: JET_ERRCAT
ms:assetid: 96551dc8-8df5-417c-850f-278b5231b0b6
ms:mtpsurl: https://msdn.microsoft.com/library/Hh475860(v=EXCHG.10)
ms:contentKeyID: 37033566
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: fe3f5ebad9f0838d089beb83b20b818b7faa4001
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706452"
---
# <a name="jet_errcat"></a><span data-ttu-id="f1ac0-103">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="f1ac0-103">JET_ERRCAT</span></span>


<span data-ttu-id="f1ac0-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="f1ac0-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_errcat"></a><span data-ttu-id="f1ac0-105">JET_ERRCAT</span><span class="sxs-lookup"><span data-stu-id="f1ac0-105">JET_ERRCAT</span></span>

<span data-ttu-id="f1ac0-106">El **JET_ERRCAT** grupo de constantes describe las clasificaciones de nivel superior o las categorías de errores.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-106">The **JET_ERRCAT** group of constants describes higher-level classifications or categories of errors.</span></span> <span data-ttu-id="f1ac0-107">Este grupo de constantes permite a las aplicaciones definir el tratamiento predeterminado para una clasificación de errores, en lugar de controlar cada caso de error de forma individual.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-107">This group of constants enables applications to define default treatment for a classification of errors, rather than handling each error case individually.</span></span> <span data-ttu-id="f1ac0-108">También garantiza que la aplicación no tiene que controlar las nuevas condiciones de error que se incluyen en las clasificaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-108">It also ensures that the application does not have to handle new error conditions that are included in existing classifications.</span></span>

<span data-ttu-id="f1ac0-109">Nota: esta documentación se basa en una versión preliminar del motor de almacenamiento extensible.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-109">Note: This documentation is based on a preliminary release of the Extensible Storage Engine.</span></span> <span data-ttu-id="f1ac0-110">Esta información está sujeta a cambios.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-110">This information is subject to change.</span></span>

<span data-ttu-id="f1ac0-111">Las constantes de **JET_ERRCAT** se organizan en una jerarquía específica de condiciones y subcondiciones, como se indica a continuación:</span><span class="sxs-lookup"><span data-stu-id="f1ac0-111">The **JET_ERRCAT** constants are arranged in a specific hierarchy of conditions and subconditions, as follows:</span></span>

<span data-ttu-id="f1ac0-112">|---Error |---operación (al) | |---fatal | |---e/s | |---recurso | |---memoria | |---quota | |---el disco | |---datos | |---daños | |---incoherente | |---fragmentación | |---la API |---uso |---</span><span class="sxs-lookup"><span data-stu-id="f1ac0-112">|--- Error |--- Operation(al) | |--- Fatal | |--- IO | |--- Resource | |--- Memory | |--- Quota | |--- Disk | |--- Data | |--- Corruption | |--- Inconsistent | |--- Fragmentation | |--- Api |--- Usage |--- State</span></span>

<span data-ttu-id="f1ac0-113">En la tabla siguiente se enumeran las constantes de **JET_ERRCAT** y se proporciona una descripción e información de recuperación, según corresponda.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-113">The following table lists the **JET_ERRCAT** constants and provides a description and recovery information, as applicable.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f1ac0-114">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="f1ac0-114">Constant/value</span></span></p></th>
<th><p><span data-ttu-id="f1ac0-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="f1ac0-115">Description</span></span></p></th>
<th><p><span data-ttu-id="f1ac0-116">Recuperación</span><span class="sxs-lookup"><span data-stu-id="f1ac0-116">Recovery</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-117">JET_errcatUnknown 0</span><span class="sxs-lookup"><span data-stu-id="f1ac0-117">JET_errcatUnknown 0</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-118">Una categoría de error no válida.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-118">An invalid error category.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-119">N/D</span><span class="sxs-lookup"><span data-stu-id="f1ac0-119">N/A.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-120">JET_errcatError 1</span><span class="sxs-lookup"><span data-stu-id="f1ac0-120">JET_errcatError 1</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-121">La categoría de nivel superior (no hay errores de esta clase).</span><span class="sxs-lookup"><span data-stu-id="f1ac0-121">The top level category (no errors should be of this class).</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-122">Vea las constantes de error específicas.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-122">See the specific error constants.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-123">JET_errcatOperation 2</span><span class="sxs-lookup"><span data-stu-id="f1ac0-123">JET_errcatOperation 2</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-124">Representa los errores que pueden producirse en cualquier momento debido a condiciones no controlables y que suelen ser temporales.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-124">Represents errors that can happen at any time due to uncontrollable conditions and are often temporary.</span></span> <span data-ttu-id="f1ac0-125">Vea subcategorías si se especifica.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-125">See subcategories if specified.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-126">Vuelva a intentarlo y, si el error continúa, informe al operador.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-126">Retry and if the error continues, inform the operator.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-127">JET_errcatFatal 3</span><span class="sxs-lookup"><span data-stu-id="f1ac0-127">JET_errcatFatal 3</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-128">Representa los errores irrecuperables que, cuando se producen, crean un riesgo de que ESE no pueda continuar de forma segura (a menudo transaccional) y los datos pueden resultar dañados.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-128">Represents fatal errors that, when they occur, create a risk that ESE cannot continue in a safe (often transactional) way, and data may become corrupted.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-129">Reinicie la instancia o el proceso.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-129">Restart the instance or process.</span></span> <span data-ttu-id="f1ac0-130">Si el problema persiste, informe al operador.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-130">If the problem persists, inform the operator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-131">JET_errcatIO 4</span><span class="sxs-lookup"><span data-stu-id="f1ac0-131">JET_errcatIO 4</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-132">Representa los errores de e/s, que proceden del sistema operativo, y están fuera del control de ESE.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-132">Represents IO errors, which come from the operating system, and are out of ESE's control.</span></span> <span data-ttu-id="f1ac0-133">Este tipo de error puede ser temporal.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-133">This type of error may be temporary.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-134">Vuelva a intentarlo y, si el error continúa, pida al operador que compruebe el disco.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-134">Retry, and if the error continues, ask the operator to check the disk.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-135">JET_errcatResource 5</span><span class="sxs-lookup"><span data-stu-id="f1ac0-135">JET_errcatResource 5</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-136">Representa una categoría de errores relacionados con la falta de condiciones de recursos.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-136">Represents a category of errors related to lack of resource conditions.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-137">Vea subcategorías.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-137">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-138">JET_errcatMemory 6</span><span class="sxs-lookup"><span data-stu-id="f1ac0-138">JET_errcatMemory 6</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-139">Representa un error causado por la falta de memoria.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-139">Represents an error caused by lack of memory.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-140">Vuelva a intentarlo después de un período de tiempo, libere memoria o salga.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-140">Retry after a period of time, free up memory, or quit.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-141">JET_errcatQuota 7</span><span class="sxs-lookup"><span data-stu-id="f1ac0-141">JET_errcatQuota 7</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-142">Determinados &quot; &quot; recursos especializados se encuentran en grupos de cierto tamaño, lo que facilita la detección de pérdidas de estos recursos.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-142">Certain &quot;specialty&quot; resources are in pools of a certain size, making it easier to detect leaks of these resources.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-143">La aplicación debe <strong>validar ()</strong> para detectar estos problemas durante el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-143">The application should <strong>Assert()</strong> to detect these issues during development .</span></span> <span data-ttu-id="f1ac0-144">Sin embargo, en el código comercial, la aplicación debe tratar esto como un error de memoria.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-144">However, in retail code, the application should treat this as a memory error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-145">JET_errcatDisk 8</span><span class="sxs-lookup"><span data-stu-id="f1ac0-145">JET_errcatDisk 8</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-146">Representa un error causado por la falta de espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-146">Represents an error caused by lack of disk space.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-147">Vuelva a intentarlo más tarde para determinar si hay más espacio en disco disponible o pida al operador que libere espacio en disco.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-147">Retry later to determine whether more disk space is available, or ask the operator to free some disk space.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-148">JET_errcatData 9</span><span class="sxs-lookup"><span data-stu-id="f1ac0-148">JET_errcatData 9</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-149">Representa una categoría de nivel superior para los errores relacionados con los datos.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-149">Represents a top-level category for errors related to data.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-150">Vea subcategorías.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-150">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-151">JET_errcatCorruption 10</span><span class="sxs-lookup"><span data-stu-id="f1ac0-151">JET_errcatCorruption 10</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-152">Representa un problema de daños, que suele ser permanente sin ninguna acción correctiva.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-152">Represents a corruption issue, which is often permanent without corrective action.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-153">Restaurar desde la copia de seguridad mediante la operación de reparación de utilidades de ESE (esta operación restaura solo los datos que se han dejado/perdidos).</span><span class="sxs-lookup"><span data-stu-id="f1ac0-153">Restore from backup by using the ESE utilities repair operation (this operation restores only the data that is left/lossy).</span></span> <span data-ttu-id="f1ac0-154">Además, cuando se usa el método de recuperación (JetInit), se puede realizar la recuperación mediante la posibilidad de pérdida de datos (para obtener más información, vea <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-154">Also when the recovery(JetInit) method is used, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-155">JET_errcatInconsistent 11</span><span class="sxs-lookup"><span data-stu-id="f1ac0-155">JET_errcatInconsistent 11</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-156">Representa un error en el que los archivos de base de datos o de registro se encuentran en un estado incoherente y no se pueden reconciliar.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-156">Represents an error in which the database and/or log files are in a state that is inconsistent and cannot be reconciled.</span></span> <span data-ttu-id="f1ac0-157">Este error puede deberse a un error de control de la aplicación o administrador.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-157">This error might be caused by application/administrator mishandling.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-158">Restaure desde una copia de seguridad mediante la operación de reparación de utilidades de ESE (que solo restaura los datos que se han dejado/perdidos).</span><span class="sxs-lookup"><span data-stu-id="f1ac0-158">Restore from backup by using the ESE utilities repair operation (which only restores the data that is left/lossy).</span></span> <span data-ttu-id="f1ac0-159">Además, en el caso de la operación de <strong>recuperación (JetInit)</strong> , se puede realizar la recuperación mediante la posibilidad de pérdida de datos (para obtener más información, vea <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-159">Also in the case of the <strong>recovery(JetInit)</strong> operation, recovery can be performed by allowing data loss (for more information, see <a href="gg269296(v=exchg.10).md">JET_bitReplayIgnoreLostLogs</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-160">JET_errcatFragmentation 12</span><span class="sxs-lookup"><span data-stu-id="f1ac0-160">JET_errcatFragmentation 12</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-161">Representa una clase de errores en los que se ha agotado algún recurso interno persistente.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-161">Represents a class of errors in which some persisted internal resource ran out.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-162">En el caso de los errores de base de datos, la desfragmentación sin conexión corregirá el problema.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-162">For database errors, offline defragmentation will fix the problem.</span></span> <span data-ttu-id="f1ac0-163">En el caso de los archivos de registro, recupere primero todas las bases de datos adjuntas en un cierre correcto y, a continuación, elimine todos los archivos de registro y el punto de control.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-163">For the log files, first recover all attached databases to a clean shutdown, and then delete all the log files and the checkpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-164">JET_errcatApi 13</span><span class="sxs-lookup"><span data-stu-id="f1ac0-164">JET_errcatApi 13</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-165">Vea subcategorías.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-165">See subcategories.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-166">Vea subcategorías.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-166">See subcategories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-167">JET_errcatUsage 14</span><span class="sxs-lookup"><span data-stu-id="f1ac0-167">JET_errcatUsage 14</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-168">Representa un error de uso.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-168">Represents a usage error.</span></span> <span data-ttu-id="f1ac0-169">El código de cliente no ha pasado los argumentos correctos a la API de <strong>jet</strong> .</span><span class="sxs-lookup"><span data-stu-id="f1ac0-169">The client code did not pass the correct arguments to the <strong>JET</strong> API.</span></span> <span data-ttu-id="f1ac0-170">Este error se conservará con el reintento.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-170">This error will persist with retry.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-171">El código de cliente debe utilizar el método <strong>Assert ()</strong> para asegurarse de que no se devuelve esta clase de errores, por lo que se pueden detectar problemas durante el desarrollo.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-171">Client code should use the <strong>Assert()</strong> method to ensure that this class of errors is not returned, so issues can be caught during development.</span></span> <span data-ttu-id="f1ac0-172">En el comercio minorista, la aplicación debe notificar al operador el error.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-172">In retail, the application should notify the operator about the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-173">JET_errcatState 15</span><span class="sxs-lookup"><span data-stu-id="f1ac0-173">JET_errcatState 15</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-174">Representa una clase de mensajes que la API puede devolver para describir el estado de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-174">Represents a class of messages that the API can return to describe the state of the database.</span></span> <span data-ttu-id="f1ac0-175">Por ejemplo, el método <a href="gg294103(v=exchg.10).md">JetSeek ()</a> puede devolver <strong>JET_errRecordNotFound</strong> cuando no se encontró el registro solicitado.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-175">For example, the <a href="gg294103(v=exchg.10).md">JetSeek()</a> method might return <strong>JET_errRecordNotFound</strong> when the requested record was not found.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-176">Varía en función de la API.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-176">Varies based on the API.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-177">JET_errcatObsolete 16</span><span class="sxs-lookup"><span data-stu-id="f1ac0-177">JET_errcatObsolete 16</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-178">Representa los errores que proceden de una versión anterior del motor.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-178">Represents errors that are from a previous version of the engine.</span></span> <span data-ttu-id="f1ac0-179">El motor actual no debe devolver estos errores.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-179">These errors should not be returned by the current engine.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-180">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-180">Unknown.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-181">JET_errcatMax 17</span><span class="sxs-lookup"><span data-stu-id="f1ac0-181">JET_errcatMax 17</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-182">Constante que indica el final de la enumeración.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-182">A constant that indicates the end of the enumeration.</span></span></p></td>
<td><p><span data-ttu-id="f1ac0-183">N/D</span><span class="sxs-lookup"><span data-stu-id="f1ac0-183">N/A.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="f1ac0-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ac0-184">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-185"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="f1ac0-185"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ac0-186">Requiere Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-186">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f1ac0-187"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="f1ac0-187"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ac0-188">Requiere Windows 8 Server.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-188">Requires Windows 8 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f1ac0-189"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="f1ac0-189"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="f1ac0-190">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-190">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>

