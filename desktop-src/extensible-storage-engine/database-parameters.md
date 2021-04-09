---
description: 'Más información acerca de: parámetros de base de datos'
title: Parámetros de base de datos
TOCTitle: Database Parameters
ms:assetid: 8fb68748-8718-4393-9fd6-0d9adaa34844
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269337(v=EXCHG.10)
ms:contentKeyID: 32765626
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
ms.openlocfilehash: 8849096412fa77db107e3e866a20662bb2634665
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155045"
---
# <a name="database-parameters"></a><span data-ttu-id="09525-103">Parámetros de base de datos</span><span class="sxs-lookup"><span data-stu-id="09525-103">Database Parameters</span></span>


<span data-ttu-id="09525-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="09525-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-parameters"></a><span data-ttu-id="09525-105">Parámetros de base de datos</span><span class="sxs-lookup"><span data-stu-id="09525-105">Database Parameters</span></span>

<span data-ttu-id="09525-106">Este tema contiene los parámetros que se usan para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-106">This topic contains parameters that are used for the database.</span></span>

<span data-ttu-id="09525-107">*JET_paramCheckFormatWhenOpenFail*</span><span class="sxs-lookup"><span data-stu-id="09525-107">*JET_paramCheckFormatWhenOpenFail*</span></span>  
<span data-ttu-id="09525-108">44</span><span class="sxs-lookup"><span data-stu-id="09525-108">44</span></span>  

<span data-ttu-id="09525-109">Si se establece este parámetro, [JetInit](./jetinit-function.md) devolverá un error especial cuando se abra una base de datos o un registro de transacciones de una versión anterior del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-109">This parameter, when set, will cause [JetInit](./jetinit-function.md) to return a special error when a database or transaction log from a previous release of the database engine is opened.</span></span> <span data-ttu-id="09525-110">Estos errores son:</span><span class="sxs-lookup"><span data-stu-id="09525-110">These errors are:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09525-111">Error</span><span class="sxs-lookup"><span data-stu-id="09525-111">Error</span></span></p></th>
<th><p><span data-ttu-id="09525-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="09525-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-113">JET_errDatabase200Format</span><span class="sxs-lookup"><span data-stu-id="09525-113">JET_errDatabase200Format</span></span></p></td>
<td><p><span data-ttu-id="09525-114">Los archivos de base de datos o de registro de transacciones se crearon con el motor de base de datos en Windows NT 3,51.</span><span class="sxs-lookup"><span data-stu-id="09525-114">The database and/or transaction log files were created with the database engine in Windows NT 3.51.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-115">JET_errDatabase400Format</span><span class="sxs-lookup"><span data-stu-id="09525-115">JET_errDatabase400Format</span></span></p></td>
<td><p><span data-ttu-id="09525-116">Los archivos de base de datos o de registro de transacciones se crearon con el motor de base de datos en una versión de prueba anterior a Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="09525-116">The database and/or transaction log files were created with the database engine in a test release prior to Windows NT Server 4.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-117">JET_errDatabase500Format</span><span class="sxs-lookup"><span data-stu-id="09525-117">JET_errDatabase500Format</span></span></p></td>
<td><p><span data-ttu-id="09525-118">Los archivos de base de datos o de registro de transacciones se crearon con el motor de base de datos en Windows NT Server 4,0.</span><span class="sxs-lookup"><span data-stu-id="09525-118">The database and/or transaction log files were created with the database engine in Windows NT Server 4.0.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-119">**Windows Vista:**  En Windows Vista y versiones posteriores, este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-119">**Windows Vista:**  For Windows Vista and later, this parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-120">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-120">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-121">True</span><span class="sxs-lookup"><span data-stu-id="09525-121">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-122">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-122">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-123">Boolean</span><span class="sxs-lookup"><span data-stu-id="09525-123">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-124">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-124">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-125">False, True</span><span class="sxs-lookup"><span data-stu-id="09525-125">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-126">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-126">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-127">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-127">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-128">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-128">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-129">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-130">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-130">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-131">No</span><span class="sxs-lookup"><span data-stu-id="09525-131">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-132">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-132">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-133">No</span><span class="sxs-lookup"><span data-stu-id="09525-133">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-134">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-134">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-135">No</span><span class="sxs-lookup"><span data-stu-id="09525-135">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-136">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-136">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-137">No</span><span class="sxs-lookup"><span data-stu-id="09525-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-138">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-138">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-139">No</span><span class="sxs-lookup"><span data-stu-id="09525-139">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-140">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-140">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-141">All</span><span class="sxs-lookup"><span data-stu-id="09525-141">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-142">*JET_paramDatabasePageSize*</span><span class="sxs-lookup"><span data-stu-id="09525-142">*JET_paramDatabasePageSize*</span></span>  
<span data-ttu-id="09525-143">64</span><span class="sxs-lookup"><span data-stu-id="09525-143">64</span></span>  

<span data-ttu-id="09525-144">Este parámetro configura el tamaño de página para la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-144">This parameter configures the page size for the database.</span></span> <span data-ttu-id="09525-145">El tamaño de página es la unidad más pequeña de asignación de espacio posible para un archivo de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-145">The page size is the smallest unit of space allocation possible for a database file.</span></span> <span data-ttu-id="09525-146">El tamaño de página de la base de datos también es muy importante, ya que establece el límite superior del tamaño de un registro individual en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-146">The database page size is also very important because it sets the upper limit on the size of an individual record in the database.</span></span>

<span data-ttu-id="09525-147">**Nota:** En este momento, solo se admite un tamaño de página de base de datos por proceso.</span><span class="sxs-lookup"><span data-stu-id="09525-147">**Note** Only one database page size is supported per process at this time.</span></span> <span data-ttu-id="09525-148">Esto significa que, si se encuentra en un único proceso que contiene diferentes aplicaciones que usan el motor de base de datos, todos deben aceptar un tamaño de página de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-148">This means that if you are in a single process that contains different applications that use the database engine then they must all agree on a database page size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-149">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-149">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-150">4096</span><span class="sxs-lookup"><span data-stu-id="09525-150">4096</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-151">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-151">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-152">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-152">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-153">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-153">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-154">2048, 4096, 8192</span><span class="sxs-lookup"><span data-stu-id="09525-154">2048, 4096, 8192</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-155">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-155">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-156">Global</span><span class="sxs-lookup"><span data-stu-id="09525-156">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-157">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-157">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-158">No</span><span class="sxs-lookup"><span data-stu-id="09525-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-159">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-159">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-160">No</span><span class="sxs-lookup"><span data-stu-id="09525-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-161">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-161">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-162">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-163">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-163">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-164">No</span><span class="sxs-lookup"><span data-stu-id="09525-164">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-165">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-165">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-166">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-166">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-167">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-167">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-168">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-168">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-169">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-169">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-170">All</span><span class="sxs-lookup"><span data-stu-id="09525-170">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-171">*JET_paramDbExtensionSize*</span><span class="sxs-lookup"><span data-stu-id="09525-171">*JET_paramDbExtensionSize*</span></span>  
<span data-ttu-id="09525-172">18</span><span class="sxs-lookup"><span data-stu-id="09525-172">18</span></span>  

<span data-ttu-id="09525-173">Este parámetro controla la cantidad de espacio que se agrega a un archivo de base de datos cada vez que necesita crecer para alojar más datos.</span><span class="sxs-lookup"><span data-stu-id="09525-173">This parameter controls the amount of space that is added to a database file each time it needs to grow to accommodate more data.</span></span> <span data-ttu-id="09525-174">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-174">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-175">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-176">256</span><span class="sxs-lookup"><span data-stu-id="09525-176">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-177">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-177">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-178">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-178">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-179">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-179">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-180">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="09525-180">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-181">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-181">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-182">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-182">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-183">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-183">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-184">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-184">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-185">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-185">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-186">No</span><span class="sxs-lookup"><span data-stu-id="09525-186">No</span></span></p>
<p><span data-ttu-id="09525-187"><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: sí</span><span class="sxs-lookup"><span data-stu-id="09525-187"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-188">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-188">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-189">No</span><span class="sxs-lookup"><span data-stu-id="09525-189">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-190">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-190">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-191">No</span><span class="sxs-lookup"><span data-stu-id="09525-191">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-192">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-192">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-193">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-193">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-194">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-194">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-195">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-195">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-196">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-196">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-197">All</span><span class="sxs-lookup"><span data-stu-id="09525-197">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-198">*JET_paramEnableIndexChecking*</span><span class="sxs-lookup"><span data-stu-id="09525-198">*JET_paramEnableIndexChecking*</span></span>  
<span data-ttu-id="09525-199">45</span><span class="sxs-lookup"><span data-stu-id="09525-199">45</span></span>  

<span data-ttu-id="09525-200">Cuando este parámetro es true, todas las bases de datos se comprueban en el momento de la [JetAttachDatabase](./jetattachdatabase-function.md) para los índices de las columnas de clave Unicode compiladas con una versión anterior de la biblioteca NLS en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="09525-200">When this parameter is true, every database is checked at [JetAttachDatabase](./jetattachdatabase-function.md) time for indexes over Unicode key columns that were built using an older version of the NLS library in the operating system.</span></span> <span data-ttu-id="09525-201">Esto debe hacerse porque el motor de base de datos conserva las claves de ordenación generadas por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) y el valor de estas claves de ordenación cambia de Release a Release.</span><span class="sxs-lookup"><span data-stu-id="09525-201">This must be done because the database engine persists the sort keys generated by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) and the value of these sort keys change from release to release.</span></span>

<span data-ttu-id="09525-202">Si se detecta que un índice principal está en este estado, [JetAttachDatabase](./jetattachdatabase-function.md) siempre producirá un error con JET_errPrimaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="09525-202">If a primary index is detected to be in this state then [JetAttachDatabase](./jetattachdatabase-function.md) will always fail with JET_errPrimaryIndexCorrupted.</span></span>

<span data-ttu-id="09525-203">Si se detecta que algún índice secundario está en este estado, hay dos resultados posibles.</span><span class="sxs-lookup"><span data-stu-id="09525-203">If any secondary indexes are detected to be in this state then there are two possible outcomes.</span></span> <span data-ttu-id="09525-204">Si JET_bitDbDeleteCorruptIndexes se pasó a [JetAttachDatabase](./jetattachdatabase-function.md) , estos índices se eliminarán y JET_wrnCorruptIndexDeleted se devolverán desde [JetAttachDatabase](./jetattachdatabase-function.md).</span><span class="sxs-lookup"><span data-stu-id="09525-204">If JET_bitDbDeleteCorruptIndexes was passed to [JetAttachDatabase](./jetattachdatabase-function.md) then these indexes will be deleted and JET_wrnCorruptIndexDeleted will be returned from [JetAttachDatabase](./jetattachdatabase-function.md).</span></span> <span data-ttu-id="09525-205">Estos índices deberán volver a crearse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09525-205">These indexes will need to be recreated by your application.</span></span> <span data-ttu-id="09525-206">Si JET_bitDbDeleteCorruptIndexes no se pasó a [JetAttachDatabase](./jetattachdatabase-function.md) , se producirá un error en la llamada con JET_errSecondaryIndexCorrupted.</span><span class="sxs-lookup"><span data-stu-id="09525-206">If JET_bitDbDeleteCorruptIndexes was not passed to [JetAttachDatabase](./jetattachdatabase-function.md) then the call will fail with JET_errSecondaryIndexCorrupted.</span></span>

<span data-ttu-id="09525-207">**Nota:** Se recomienda encarecidamente que la aplicación establezca este parámetro en true.</span><span class="sxs-lookup"><span data-stu-id="09525-207">**Note** It is strongly recommended that this parameter be set to True by your application.</span></span>

<span data-ttu-id="09525-208">**Nota:** Se recomienda encarecidamente que las aplicaciones eviten el uso de columnas de clave Unicode en sus índices de clave principal (clúster).</span><span class="sxs-lookup"><span data-stu-id="09525-208">**Note** It is very strongly recommended that applications avoid the use of Unicode key columns in their primary key (clustered) indexes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-209">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-209">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-210">False</span><span class="sxs-lookup"><span data-stu-id="09525-210">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-211">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-212">Boolean</span><span class="sxs-lookup"><span data-stu-id="09525-212">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-213">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-214">False, True</span><span class="sxs-lookup"><span data-stu-id="09525-214">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-215">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-215">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-216">Global</span><span class="sxs-lookup"><span data-stu-id="09525-216">Global</span></span></p>
<p><span data-ttu-id="09525-217"><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: instancia</span><span class="sxs-lookup"><span data-stu-id="09525-217"><strong>Windows Vista:</strong>  For Windows Vista and later: Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-218">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-219">No</span><span class="sxs-lookup"><span data-stu-id="09525-219">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-220">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-220">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-221">No</span><span class="sxs-lookup"><span data-stu-id="09525-221">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-222">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-222">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-223">No</span><span class="sxs-lookup"><span data-stu-id="09525-223">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-224">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-224">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-225">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-225">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-226">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-226">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-227">No</span><span class="sxs-lookup"><span data-stu-id="09525-227">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-228">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-228">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-229">No</span><span class="sxs-lookup"><span data-stu-id="09525-229">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-230">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-230">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-231">All</span><span class="sxs-lookup"><span data-stu-id="09525-231">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-232">*JET_paramEnableIndexCleanup*</span><span class="sxs-lookup"><span data-stu-id="09525-232">*JET_paramEnableIndexCleanup*</span></span>  
<span data-ttu-id="09525-233">54</span><span class="sxs-lookup"><span data-stu-id="09525-233">54</span></span>  

<span data-ttu-id="09525-234">Cuando este parámetro se establece en true, el motor de base de datos puede limpiar automáticamente los índices de las columnas de clave Unicode en el tiempo de [JetInit](./jetinit-function.md) , según sea necesario, para evitar cambios en el formato de la base de datos causados por cambios en la biblioteca NLS de Windows.</span><span class="sxs-lookup"><span data-stu-id="09525-234">When this parameter is set to true, then the database engine may automatically clean up indexes over Unicode key columns at [JetInit](./jetinit-function.md) time as necessary to avoid database format changes caused by changes to the NLS library in Windows.</span></span> <span data-ttu-id="09525-235">Estos cambios se realizan habitualmente en la biblioteca NLS para agregar compatibilidad con nuevos idiomas, agregar caracteres que faltan a un idioma, agregar un orden de intercalación a un idioma o corregir errores en el orden de intercalación de un idioma.</span><span class="sxs-lookup"><span data-stu-id="09525-235">Such changes are made routinely to the NLS library to add support for new languages, to add missing characters to a language, to add a collation order to a language, or to fix bugs in the collation order of a language.</span></span> <span data-ttu-id="09525-236">Estos cambios afectan a los criterios de ordenación generados por [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) que el motor de base de datos conserva como componentes de las claves de índice.</span><span class="sxs-lookup"><span data-stu-id="09525-236">These changes affect the sort keys produced by [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) which are persisted by the database engine as components of index keys.</span></span>

<span data-ttu-id="09525-237">Es importante saber que es posible que los cambios en el índice sean tan grandes que no sea posible realizar una limpieza incremental.</span><span class="sxs-lookup"><span data-stu-id="09525-237">It is important to realize that it is possible for the changes to the index to be so great that an incremental cleanup is not possible.</span></span> <span data-ttu-id="09525-238">En este caso, el índice se administrará como se indica en **JET_paramEnableIndexChecking**.</span><span class="sxs-lookup"><span data-stu-id="09525-238">In this case, the index will be handled as prescribed by **JET_paramEnableIndexChecking**.</span></span>

<span data-ttu-id="09525-239">**Nota:** Se recomienda encarecidamente que la aplicación establezca este parámetro y **JET_paramEnableIndexChecking** en **true** .</span><span class="sxs-lookup"><span data-stu-id="09525-239">**Note** It is strongly recommended that this parameter and **JET_paramEnableIndexChecking** be set to **True** by your application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-240">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-240">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-241">True</span><span class="sxs-lookup"><span data-stu-id="09525-241">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-242">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-242">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-243">Boolean</span><span class="sxs-lookup"><span data-stu-id="09525-243">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-244">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-244">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-245">False, True</span><span class="sxs-lookup"><span data-stu-id="09525-245">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-246">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-246">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-247">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-247">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-248">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-248">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-249">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-249">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-250">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-250">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-251">No</span><span class="sxs-lookup"><span data-stu-id="09525-251">No</span></span></p>
<p><span data-ttu-id="09525-252"><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: sí</span><span class="sxs-lookup"><span data-stu-id="09525-252"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-253">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-253">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-254">No</span><span class="sxs-lookup"><span data-stu-id="09525-254">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-255">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-255">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-256">No</span><span class="sxs-lookup"><span data-stu-id="09525-256">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-257">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-257">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-258">No</span><span class="sxs-lookup"><span data-stu-id="09525-258">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-259">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-259">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-260">No</span><span class="sxs-lookup"><span data-stu-id="09525-260">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-261">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-261">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-262">Windows Server 2003 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="09525-262">Windows Server 2003 and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-263">*JET_paramOneDatabasePerSession*</span><span class="sxs-lookup"><span data-stu-id="09525-263">*JET_paramOneDatabasePerSession*</span></span>  
<span data-ttu-id="09525-264">102</span><span class="sxs-lookup"><span data-stu-id="09525-264">102</span></span>  

<span data-ttu-id="09525-265">Cuando este parámetro es true, solo se permite abrir una base de datos mediante [JetOpenDatabase](./jetopendatabase-function.md) por una sesión determinada al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="09525-265">When this parameter is true then only one database is allowed to be opened using [JetOpenDatabase](./jetopendatabase-function.md) by a given session at one time.</span></span> <span data-ttu-id="09525-266">La base de datos temporal se excluye de esta restricción.</span><span class="sxs-lookup"><span data-stu-id="09525-266">The temporary database is excluded from this restriction.</span></span>

<span data-ttu-id="09525-267">**Windows XP y Windows Server 2003:**  Este parámetro solo se escribe en Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="09525-267">**Windows XP and Windows Server 2003:**  This parameter is write only on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="09525-268">**Windows Vista:**  Este parámetro se comporta normalmente a partir de Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09525-268">**Windows Vista:**  This parameter behaves normally as of Windows Vista.</span></span>

<span data-ttu-id="09525-269">**Nota:**  Este parámetro es de solo escritura.</span><span class="sxs-lookup"><span data-stu-id="09525-269">**Note**  This parameter is write only.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-270">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-270">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-271">False</span><span class="sxs-lookup"><span data-stu-id="09525-271">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-272">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-272">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-273">Boolean</span><span class="sxs-lookup"><span data-stu-id="09525-273">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-274">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-274">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-275">False, True</span><span class="sxs-lookup"><span data-stu-id="09525-275">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-276">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-276">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-277">Global</span><span class="sxs-lookup"><span data-stu-id="09525-277">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-278">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-278">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-279">No</span><span class="sxs-lookup"><span data-stu-id="09525-279">No</span></span></p>
<p><span data-ttu-id="09525-280"><strong>Windows Vista:</strong>  En Windows Vista y versiones posteriores: sí</span><span class="sxs-lookup"><span data-stu-id="09525-280"><strong>Windows Vista:</strong>  For Windows Vista and later: Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-281">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-281">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-282">No</span><span class="sxs-lookup"><span data-stu-id="09525-282">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-283">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-283">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-284">No</span><span class="sxs-lookup"><span data-stu-id="09525-284">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-285">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-285">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-286">No</span><span class="sxs-lookup"><span data-stu-id="09525-286">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-287">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-287">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-288">No</span><span class="sxs-lookup"><span data-stu-id="09525-288">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-289">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-289">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-290">No</span><span class="sxs-lookup"><span data-stu-id="09525-290">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-291">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-291">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-292">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="09525-292">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-293">*JET_paramEnableOnlineDefrag*</span><span class="sxs-lookup"><span data-stu-id="09525-293">*JET_paramEnableOnlineDefrag*</span></span>  
<span data-ttu-id="09525-294">35</span><span class="sxs-lookup"><span data-stu-id="09525-294">35</span></span>  

<span data-ttu-id="09525-295">Este parámetro controla el comportamiento de la desfragmentación con conexión cuando se inicia mediante [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="09525-295">This parameter controls the behavior of online defragmentation when initiated using [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="09525-296">Consulte [JetDefragment](./jetdefragment-function.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="09525-296">Please see [JetDefragment](./jetdefragment-function.md) for more information.</span></span>

<span data-ttu-id="09525-297">Windows 2000: en Windows 2000, este parámetro era un valor booleano simple que canalizaría la desfragmentación en línea cuando lo inició [JetDefragment](./jetdefragment-function.md).</span><span class="sxs-lookup"><span data-stu-id="09525-297">Windows 2000:  On Windows 2000, this parameter was a simple Boolean that would gate online defragmentation when initiated by [JetDefragment](./jetdefragment-function.md).</span></span> <span data-ttu-id="09525-298">Cuando se establece en **true**, la desfragmentación con conexión se realizará en los registros de cada tabla de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-298">When set to **TRUE**, online defragmentation will be performed on the records of each table in the database.</span></span>

<span data-ttu-id="09525-299">**Windows XP:**  En Windows XP y versiones posteriores, este parámetro se puede establecer en una o varias de las opciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="09525-299">**Windows XP:**  On Windows XP and later releases, this parameter can be set to one or more of the following options:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09525-300">Opción</span><span class="sxs-lookup"><span data-stu-id="09525-300">Option</span></span></p></th>
<th><p><span data-ttu-id="09525-301">Descripción</span><span class="sxs-lookup"><span data-stu-id="09525-301">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-302">JET_OnlineDefragDisable</span><span class="sxs-lookup"><span data-stu-id="09525-302">JET_OnlineDefragDisable</span></span></p></td>
<td><p><span data-ttu-id="09525-303">No lleve a cabo la desfragmentación en línea.</span><span class="sxs-lookup"><span data-stu-id="09525-303">Do not perform online defragmentation.</span></span> <span data-ttu-id="09525-304">Es el binario equivalente a la configuración de Windows 2000 de false para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="09525-304">This is the binary equivalent to the Windows 2000 setting of False for this parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-305">JET_OnlineDefragAllOBSOLETE</span><span class="sxs-lookup"><span data-stu-id="09525-305">JET_OnlineDefragAllOBSOLETE</span></span></p></td>
<td><p><span data-ttu-id="09525-306">Realice una desfragmentación en línea completa.</span><span class="sxs-lookup"><span data-stu-id="09525-306">Perform full online defragmentation.</span></span> <span data-ttu-id="09525-307">Es el binario equivalente a la configuración de Windows 2000 de true para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="09525-307">This is the binary equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-308">JET_OnlineDefragDatabases</span><span class="sxs-lookup"><span data-stu-id="09525-308">JET_OnlineDefragDatabases</span></span></p></td>
<td><p><span data-ttu-id="09525-309">Realice una desfragmentación en línea de los registros de cada tabla en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-309">Perform online defragmentation of the records of each table in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-310">JET_OnlineDefragSpaceTrees</span><span class="sxs-lookup"><span data-stu-id="09525-310">JET_OnlineDefragSpaceTrees</span></span></p></td>
<td><p><span data-ttu-id="09525-311">Realice una desfragmentación en línea de los árboles de espacio de cada tabla en la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-311">Perform online defragmentation of the space trees of each table in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-312">JET_OnlineDefragStreamingFiles</span><span class="sxs-lookup"><span data-stu-id="09525-312">JET_OnlineDefragStreamingFiles</span></span></p></td>
<td><p><span data-ttu-id="09525-313">Este parámetro se usa para admitir la infraestructura de Microsoft Exchange y no está diseñado para usarse en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="09525-313">This parameter is used to support the Microsoft Exchange infrastructure and is not intended to be used in your application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-314">JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="09525-314">JET_OnlineDefragAll</span></span></p></td>
<td><p><span data-ttu-id="09525-315">Realice una desfragmentación en línea completa.</span><span class="sxs-lookup"><span data-stu-id="09525-315">Perform full online defragmentation.</span></span> <span data-ttu-id="09525-316">Este es el equivalente conceptual del valor de Windows 2000 de true para este parámetro.</span><span class="sxs-lookup"><span data-stu-id="09525-316">This is the conceptual equivalent to the Windows 2000 setting of True for this parameter.</span></span></p></td>
</tr>
</tbody>
</table>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-317">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-317">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-318"><strong>Windows 2000:</strong>  Reales</span><span class="sxs-lookup"><span data-stu-id="09525-318"><strong>Windows 2000:</strong>  True</span></span></p>
<p><span data-ttu-id="09525-319"><strong>Windows XP: para Windows XP y versiones posteriores:</strong> JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="09525-319"><strong>Windows XP:  For Windows XP and later:</strong> JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-320">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-320">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-321"><strong>Windows 2000:</strong>  Booleano</span><span class="sxs-lookup"><span data-stu-id="09525-321"><strong>Windows 2000:</strong>  Boolean</span></span></p>
<p><span data-ttu-id="09525-322"><strong>Windows XP y versiones posteriores:</strong>  JET_GRBIT (entero)</span><span class="sxs-lookup"><span data-stu-id="09525-322"><strong>Windows XP and later:</strong>  JET_GRBIT (integer)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-323">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-323">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-324"><strong>Windows 2000:</strong>  False, true</span><span class="sxs-lookup"><span data-stu-id="09525-324"><strong>Windows 2000:</strong>  False, True</span></span></p>
<p><span data-ttu-id="09525-325"><strong>Windows XP y versiones posteriores:</strong>  0: JET_OnlineDefragAll</span><span class="sxs-lookup"><span data-stu-id="09525-325"><strong>Windows XP and later:</strong>  0 – JET_OnlineDefragAll</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-326">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-326">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-327">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-327">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-328">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-328">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-329">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-329">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-330">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-330">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-331">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-331">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-332">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-332">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-333">No</span><span class="sxs-lookup"><span data-stu-id="09525-333">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-334">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-334">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-335">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-335">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-336">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-336">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-337">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-337">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-338">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-338">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-339">No</span><span class="sxs-lookup"><span data-stu-id="09525-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-340">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-340">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-341">All</span><span class="sxs-lookup"><span data-stu-id="09525-341">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-342">*JET_paramPageFragment*</span><span class="sxs-lookup"><span data-stu-id="09525-342">*JET_paramPageFragment*</span></span>  
<span data-ttu-id="09525-343">20</span><span class="sxs-lookup"><span data-stu-id="09525-343">20</span></span>  

<span data-ttu-id="09525-344">Este parámetro es el umbral que usa el motor de base de datos para controlar la fragmentación del espacio libre.</span><span class="sxs-lookup"><span data-stu-id="09525-344">This parameter is the threshold that the database engine uses to control free space fragmentation.</span></span> <span data-ttu-id="09525-345">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-345">The size is in database pages.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-346">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-346">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-347">8</span><span class="sxs-lookup"><span data-stu-id="09525-347">8</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-348">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-348">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-349">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-349">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-350">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-350">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-351">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="09525-351">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-352">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-352">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-353">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-353">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-354">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-354">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-355">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-355">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-356">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-356">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-357">No</span><span class="sxs-lookup"><span data-stu-id="09525-357">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-358">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-358">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-359">No</span><span class="sxs-lookup"><span data-stu-id="09525-359">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-360">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-360">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-361">No</span><span class="sxs-lookup"><span data-stu-id="09525-361">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-362">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-362">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-363">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-363">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-364">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-364">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-365">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-365">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-366">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-366">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-367">All</span><span class="sxs-lookup"><span data-stu-id="09525-367">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-368">*JET_paramRecordUpgradeDirtyLevel*</span><span class="sxs-lookup"><span data-stu-id="09525-368">*JET_paramRecordUpgradeDirtyLevel*</span></span>  
<span data-ttu-id="09525-369">78</span><span class="sxs-lookup"><span data-stu-id="09525-369">78</span></span>

<span data-ttu-id="09525-370">Este parámetro controla el modo en que el administrador de caché de páginas de base de datos escribirá una página de base de datos que se haya sometido a una conversión de formato en contexto.</span><span class="sxs-lookup"><span data-stu-id="09525-370">This parameter controls how aggressively the database page cache manager will write a database page that has undergone an in place format conversion.</span></span> <span data-ttu-id="09525-371">Estas conversiones de formato se producen sobre la marcha a medida que las páginas se cargan desde una base de datos que se creó con el motor de base de datos de Windows 2000, pero que usa Windows XP o una versión posterior del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-371">These format conversions occur on the fly as pages are loaded from a database that was created with the Windows 2000 database engine but used by a Windows XP or later release of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-372">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-372">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-373">1</span><span class="sxs-lookup"><span data-stu-id="09525-373">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-374">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-374">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-375">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-375">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-376">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-376">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-377">0-3</span><span class="sxs-lookup"><span data-stu-id="09525-377">0-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-378">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-378">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-379">Global</span><span class="sxs-lookup"><span data-stu-id="09525-379">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-380">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-380">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-381">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-381">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-382">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-382">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-383">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-383">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-384">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-384">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-385">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-385">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-386">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-386">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-387">No</span><span class="sxs-lookup"><span data-stu-id="09525-387">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-388">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-388">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-389">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-389">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-390">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-390">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-391">No</span><span class="sxs-lookup"><span data-stu-id="09525-391">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-392">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-392">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-393">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="09525-393">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-394">*JET_paramWaypointLatency*</span><span class="sxs-lookup"><span data-stu-id="09525-394">*JET_paramWaypointLatency*</span></span>  
<span data-ttu-id="09525-395">153</span><span class="sxs-lookup"><span data-stu-id="09525-395">153</span></span>  

<span data-ttu-id="09525-396">La latencia (en registros) detrás del registro de propinas más alto para aplazar los vaciados de las páginas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="09525-396">The latency (in logs) behind the tip / highest committed log to defer database page flushes.</span></span> <span data-ttu-id="09525-397">La habilitación de esta latencia puede permitir la recuperación de bases de datos en caso de una pérdida catastrófica del archivo de registro más reciente.</span><span class="sxs-lookup"><span data-stu-id="09525-397">Enabling this latency can allow database recovery in the case of catastrophic loss of the most recent logfile.</span></span> <span data-ttu-id="09525-398">Vea JET_bitReplayIgnoreLostLogs.</span><span class="sxs-lookup"><span data-stu-id="09525-398">See JET_bitReplayIgnoreLostLogs.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-399">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-399">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-400">0</span><span class="sxs-lookup"><span data-stu-id="09525-400">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-401">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-401">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-402">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-402">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-403">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-403">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-404">0-1023</span><span class="sxs-lookup"><span data-stu-id="09525-404">0-1023</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-405">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-405">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-406">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-406">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-407">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-407">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-408">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-408">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-409">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-409">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-410">No</span><span class="sxs-lookup"><span data-stu-id="09525-410">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-411">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-411">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-412">No</span><span class="sxs-lookup"><span data-stu-id="09525-412">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-413">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-413">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-414">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-414">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-415">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-415">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-416">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-416">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-417">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-417">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-418">No</span><span class="sxs-lookup"><span data-stu-id="09525-418">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-419">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-419">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-420">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09525-420">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-421">*JET_paramDefragmentSequentialBTrees*</span><span class="sxs-lookup"><span data-stu-id="09525-421">*JET_paramDefragmentSequentialBTrees*</span></span>  
<span data-ttu-id="09525-422">160</span><span class="sxs-lookup"><span data-stu-id="09525-422">160</span></span>  

<span data-ttu-id="09525-423">Active o desactive la desfragmentación de árbol B secuencial automática.</span><span class="sxs-lookup"><span data-stu-id="09525-423">Turn on/off automatic sequential B-tree defragmentation.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-424">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-424">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-425">1</span><span class="sxs-lookup"><span data-stu-id="09525-425">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-426">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-426">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-427">Boolean</span><span class="sxs-lookup"><span data-stu-id="09525-427">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-428">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-428">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-429">0-1</span><span class="sxs-lookup"><span data-stu-id="09525-429">0-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-430">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-430">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-431">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-431">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-432">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-432">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-433">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-433">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-434">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-434">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-435">No</span><span class="sxs-lookup"><span data-stu-id="09525-435">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-436">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-436">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-437">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-437">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-438">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-438">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-439">No</span><span class="sxs-lookup"><span data-stu-id="09525-439">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-440">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-440">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-441">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-442">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-442">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-443">No</span><span class="sxs-lookup"><span data-stu-id="09525-443">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-444">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-444">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-445">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09525-445">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span><span class="sxs-lookup"><span data-stu-id="09525-446">*JET_paramDefragmentSequentialBTreesDensityCheckFrequency*</span></span>  
<span data-ttu-id="09525-447">161</span><span class="sxs-lookup"><span data-stu-id="09525-447">161</span></span>  

<span data-ttu-id="09525-448">Determina la frecuencia con la que se comprueba la densidad del árbol B.</span><span class="sxs-lookup"><span data-stu-id="09525-448">Determines how frequently B-tree density is checked.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-449">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-449">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-450">10</span><span class="sxs-lookup"><span data-stu-id="09525-450">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-451">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-451">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-452">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-452">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-453">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-453">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-454">0: entero máximo</span><span class="sxs-lookup"><span data-stu-id="09525-454">0-Max Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-455">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-455">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-456">Instancia</span><span class="sxs-lookup"><span data-stu-id="09525-456">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-457">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-457">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-458">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-458">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-459">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-459">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-460">No</span><span class="sxs-lookup"><span data-stu-id="09525-460">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-461">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-461">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-462">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-462">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-463">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-463">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-464">No</span><span class="sxs-lookup"><span data-stu-id="09525-464">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-465">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-465">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-466">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-466">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-467">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-467">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-468">No</span><span class="sxs-lookup"><span data-stu-id="09525-468">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-469">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-469">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-470">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09525-470">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="09525-471">*JET_paramIOThrottlingTimeQuanta*</span><span class="sxs-lookup"><span data-stu-id="09525-471">*JET_paramIOThrottlingTimeQuanta*</span></span>  
<span data-ttu-id="09525-472">162</span><span class="sxs-lookup"><span data-stu-id="09525-472">162</span></span>  

<span data-ttu-id="09525-473">Tiempo máximo, en milisegundos, que el mecanismo de limitación de e/s permite que una tarea se ejecute para que se considere "completada".</span><span class="sxs-lookup"><span data-stu-id="09525-473">Max time, in milliseconds, that the I/O throttling mechanism gives a task to run for it to be considered 'completed'.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-474">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="09525-474">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="09525-475">125</span><span class="sxs-lookup"><span data-stu-id="09525-475">125</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-476">Escriba:</span><span class="sxs-lookup"><span data-stu-id="09525-476">Type:</span></span></p></td>
<td><p><span data-ttu-id="09525-477">Entero</span><span class="sxs-lookup"><span data-stu-id="09525-477">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-478">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="09525-478">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="09525-479">0-10000</span><span class="sxs-lookup"><span data-stu-id="09525-479">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-480">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="09525-480">Scope:</span></span></p></td>
<td><p><span data-ttu-id="09525-481">Global</span><span class="sxs-lookup"><span data-stu-id="09525-481">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-482">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-482">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-483">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-483">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-484">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="09525-484">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="09525-485">No</span><span class="sxs-lookup"><span data-stu-id="09525-485">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-486">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="09525-486">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="09525-487">No</span><span class="sxs-lookup"><span data-stu-id="09525-487">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-488">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-488">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="09525-489">No</span><span class="sxs-lookup"><span data-stu-id="09525-489">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-490">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="09525-490">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="09525-491">Sí</span><span class="sxs-lookup"><span data-stu-id="09525-491">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-492">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="09525-492">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="09525-493">No</span><span class="sxs-lookup"><span data-stu-id="09525-493">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-494">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="09525-494">Availability:</span></span></p></td>
<td><p><span data-ttu-id="09525-495">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09525-495">Windows 7</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="09525-496">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09525-496">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09525-497"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="09525-497"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="09525-498">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="09525-498">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09525-499"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="09525-499"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="09525-500">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="09525-500">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09525-501"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="09525-501"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="09525-502">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="09525-502">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="09525-503">Consulte también</span><span class="sxs-lookup"><span data-stu-id="09525-503">See Also</span></span>

[<span data-ttu-id="09525-504">JetAttachDatabase</span><span class="sxs-lookup"><span data-stu-id="09525-504">JetAttachDatabase</span></span>](./jetattachdatabase-function.md)  
[<span data-ttu-id="09525-505">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="09525-505">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="09525-506">JetDefragment</span><span class="sxs-lookup"><span data-stu-id="09525-506">JetDefragment</span></span>](./jetdefragment-function.md)  
[<span data-ttu-id="09525-507">JetInit</span><span class="sxs-lookup"><span data-stu-id="09525-507">JetInit</span></span>](./jetinit-function.md)
