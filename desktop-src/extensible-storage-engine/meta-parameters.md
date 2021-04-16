---
description: 'Más información acerca de: parámetros meta'
title: Metaparámetros
TOCTitle: Meta Parameters
ms:assetid: 947e9342-7916-4e62-85e5-2d18805000c0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269346(v=EXCHG.10)
ms:contentKeyID: 32765634
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
ms.openlocfilehash: 82b5fac0cc59e9a0511344e72b3f316af9013965
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652381"
---
# <a name="meta-parameters"></a><span data-ttu-id="7eb6c-103">Metaparámetros</span><span class="sxs-lookup"><span data-stu-id="7eb6c-103">Meta Parameters</span></span>


<span data-ttu-id="7eb6c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="7eb6c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="meta-parameters"></a><span data-ttu-id="7eb6c-105">Metaparámetros</span><span class="sxs-lookup"><span data-stu-id="7eb6c-105">Meta Parameters</span></span>

<span data-ttu-id="7eb6c-106">Este tema contiene los parámetros que se usan para controlar otros parámetros.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-106">This topic contains parameters that are used to control other parameters.</span></span>

<span data-ttu-id="7eb6c-107">JET_paramConfiguration</span><span class="sxs-lookup"><span data-stu-id="7eb6c-107">JET_paramConfiguration</span></span>  
<span data-ttu-id="7eb6c-108">129</span><span class="sxs-lookup"><span data-stu-id="7eb6c-108">129</span></span>  
<span data-ttu-id="7eb6c-109">Este parámetro expone varios conjuntos de valores predeterminados para todo el conjunto de parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-109">This parameter exposes multiple sets of default values for the entire set of system parameters.</span></span> <span data-ttu-id="7eb6c-110">Cuando este parámetro se establece en una configuración específica, se restablecen los valores predeterminados de todos los valores de los parámetros del sistema para esa configuración.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-110">When this parameter is set to a specific configuration, all system parameter values are reset to their default values for that configuration.</span></span> <span data-ttu-id="7eb6c-111">Si se establece la configuración para una instancia específica de, los parámetros globales del sistema no se restablecerán a sus valores predeterminados.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-111">If the configuration is set for a specific instance then global system parameters will not be reset to their default values.</span></span>

<span data-ttu-id="7eb6c-112">Además, el propio parámetro puede tener otros efectos en el comportamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-112">In addition, the parameter itself can have other effects on the behavior of the database engine.</span></span>

<span data-ttu-id="7eb6c-113">En este momento, hay dos configuraciones admitidas:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-113">At this time, there are two supported configurations:</span></span>

  - <span data-ttu-id="7eb6c-114">Configuración pequeña (0): el motor de base de datos está optimizado para el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-114">Small Configuration (0): The database engine is optimized for memory use.</span></span>

  - <span data-ttu-id="7eb6c-115">Configuración heredada (1): el motor de base de datos tiene sus valores predeterminados tradicionales.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-115">Legacy Configuration (1): The database engine has its traditional defaults.</span></span>

<span data-ttu-id="7eb6c-116">La configuración pequeña cambia los valores predeterminados de los siguientes parámetros del sistema a los valores especificados:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-116">Small Configuration changes the defaults of the following system parameters to the specified values:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7eb6c-117">Parámetro del sistema</span><span class="sxs-lookup"><span data-stu-id="7eb6c-117">System Parameter</span></span></p></th>
<th><p><span data-ttu-id="7eb6c-118">Nuevo valor predeterminado</span><span class="sxs-lookup"><span data-stu-id="7eb6c-118">New Default Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-119">JET_paramMaxSessions</span><span class="sxs-lookup"><span data-stu-id="7eb6c-119">JET_paramMaxSessions</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-120">30000</span><span class="sxs-lookup"><span data-stu-id="7eb6c-120">30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-121">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="7eb6c-121">JET_paramMaxOpenTables</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-122">2147483647</span><span class="sxs-lookup"><span data-stu-id="7eb6c-122">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-123">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="7eb6c-123">JET_paramMaxCursors</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-124">2147483647</span><span class="sxs-lookup"><span data-stu-id="7eb6c-124">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-125">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="7eb6c-125">JET_paramMaxVerPages</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-126">2147483647</span><span class="sxs-lookup"><span data-stu-id="7eb6c-126">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-127">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="7eb6c-127">JET_paramMaxTemporaryTables</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-128">2147483647</span><span class="sxs-lookup"><span data-stu-id="7eb6c-128">2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-129">JET_paramLogFileSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-129">JET_paramLogFileSize</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-130">64</span><span class="sxs-lookup"><span data-stu-id="7eb6c-130">64</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-131">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="7eb6c-131">JET_paramLogBuffers</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-132">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-132">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-133">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-133">JET_paramDbExtensionSize</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-134">16</span><span class="sxs-lookup"><span data-stu-id="7eb6c-134">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-135">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="7eb6c-135">JET_paramPageTempDBMin</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-136">14</span><span class="sxs-lookup"><span data-stu-id="7eb6c-136">14</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-137">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-137">JET_paramCacheSizeMax</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-138">16</span><span class="sxs-lookup"><span data-stu-id="7eb6c-138">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-139">JET_paramCheckpointDepthMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-139">JET_paramCheckpointDepthMax</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-140">65536</span><span class="sxs-lookup"><span data-stu-id="7eb6c-140">65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-141">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-141">JET_paramLRUKHistoryMax</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-142">10</span><span class="sxs-lookup"><span data-stu-id="7eb6c-142">10</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-143">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-143">JET_paramOutstandingIOMax</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-144">16</span><span class="sxs-lookup"><span data-stu-id="7eb6c-144">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-145">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="7eb6c-145">JET_paramStartFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-146">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-146">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-147">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="7eb6c-147">JET_paramStopFlushThreshold</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-148">2</span><span class="sxs-lookup"><span data-stu-id="7eb6c-148">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-149">JET_paramNoInformationEvent</span><span class="sxs-lookup"><span data-stu-id="7eb6c-149">JET_paramNoInformationEvent</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-150">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-150">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-151">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="7eb6c-151">JET_paramCacheSizeMin</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-152">16</span><span class="sxs-lookup"><span data-stu-id="7eb6c-152">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-153">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="7eb6c-153">JET_paramPreferredVerPages</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-154">2147483647</span><span class="sxs-lookup"><span data-stu-id="7eb6c-154">2147483647</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-155">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="7eb6c-155">JET_paramLogFileCreateAsynch</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-156">0</span><span class="sxs-lookup"><span data-stu-id="7eb6c-156">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-157">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="7eb6c-157">JET_paramGlobalMinVerPages</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-158">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-158">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-159">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-159">JET_paramPageHintCacheSize</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-160">32</span><span class="sxs-lookup"><span data-stu-id="7eb6c-160">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-161">JET_paramDisablePerfmon</span><span class="sxs-lookup"><span data-stu-id="7eb6c-161">JET_paramDisablePerfmon</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-162">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-162">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-163">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="7eb6c-163">JET_paramEnableFileCache</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-164">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-164">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-165">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="7eb6c-165">JET_paramEnableViewCache</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-166">1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-166">1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-167">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-167">JET_paramVerPageSize</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-168">1024</span><span class="sxs-lookup"><span data-stu-id="7eb6c-168">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-169">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="7eb6c-169">JET_paramEnableAdvanced</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-170">0</span><span class="sxs-lookup"><span data-stu-id="7eb6c-170">0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-171">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-171">JET_paramCheckpointIOMax</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-172">8</span><span class="sxs-lookup"><span data-stu-id="7eb6c-172">8</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eb6c-173">La configuración pequeña también tiene varios efectos en el motor de base de datos, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-173">Small Configuration also has several other effects on the database engine, including:</span></span>

  - <span data-ttu-id="7eb6c-174">Todos los recursos administrados por parámetros del sistema se asignan desde el montón según sea necesario.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-174">All resources managed by system parameters are allocated from the heap as needed</span></span>

  - <span data-ttu-id="7eb6c-175">Otros recursos internos utilizados por el motor de base de datos se escalan verticalmente en tamaño</span><span class="sxs-lookup"><span data-stu-id="7eb6c-175">Other internal resources used by the database engine are scaled down in size</span></span>

  - <span data-ttu-id="7eb6c-176">Varias actividades de mantenimiento se escalan de vuelta para evitar la actividad del subproceso en segundo plano</span><span class="sxs-lookup"><span data-stu-id="7eb6c-176">Various maintenance activities are scaled back to avoid background thread activity</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-177">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-177">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-178">1 (heredado)</span><span class="sxs-lookup"><span data-stu-id="7eb6c-178">1 (Legacy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-179">Escriba:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-179">Type:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-180">Entero</span><span class="sxs-lookup"><span data-stu-id="7eb6c-180">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-181">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-181">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-182">0 – 1</span><span class="sxs-lookup"><span data-stu-id="7eb6c-182">0 – 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-183">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-184">Instancia</span><span class="sxs-lookup"><span data-stu-id="7eb6c-184">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-185">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-186">Sí</span><span class="sxs-lookup"><span data-stu-id="7eb6c-186">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-187">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-187">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-188">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-189">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-189">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-190">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-190">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-191">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-191">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-192">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-192">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-193">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-193">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-194">Sí</span><span class="sxs-lookup"><span data-stu-id="7eb6c-194">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-195">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-195">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-196">Sí</span><span class="sxs-lookup"><span data-stu-id="7eb6c-196">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-197">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-197">Availability:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-198">A partir de Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eb6c-198">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eb6c-199">JET_paramEnableAdvanced</span><span class="sxs-lookup"><span data-stu-id="7eb6c-199">JET_paramEnableAdvanced</span></span>  
<span data-ttu-id="7eb6c-200">130</span><span class="sxs-lookup"><span data-stu-id="7eb6c-200">130</span></span>  
<span data-ttu-id="7eb6c-201">Este parámetro se usa para controlar el momento en que el motor de base de datos acepta o rechaza los cambios en un subconjunto de los parámetros del sistema.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-201">This parameter is used to control when the database engine accepts or rejects changes to a subset of the system parameters.</span></span> <span data-ttu-id="7eb6c-202">Este parámetro se usa junto con JET_paramConfiguration para evitar que algunos parámetros del sistema se establezcan fuera de los valores predeterminados de la configuración seleccionada.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-202">This parameter is used in conjunction with JET_paramConfiguration to prevent some system parameters from being set away from the selected configuration's defaults.</span></span>

<span data-ttu-id="7eb6c-203">Los siguientes parámetros del sistema se protegerán de su establecimiento cuando este parámetro se establezca en false:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-203">The following system parameters will be protected from being set when this parameter is set to False:</span></span>

  - <span data-ttu-id="7eb6c-204">JET_paramMaxSessionsfon</span><span class="sxs-lookup"><span data-stu-id="7eb6c-204">JET_paramMaxSessionsfon</span></span>

  - <span data-ttu-id="7eb6c-205">JET_paramMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="7eb6c-205">JET_paramMaxOpenTables</span></span>

  - <span data-ttu-id="7eb6c-206">JET_paramPreferredMaxOpenTables</span><span class="sxs-lookup"><span data-stu-id="7eb6c-206">JET_paramPreferredMaxOpenTables</span></span>

  - <span data-ttu-id="7eb6c-207">JET_paramMaxCursors</span><span class="sxs-lookup"><span data-stu-id="7eb6c-207">JET_paramMaxCursors</span></span>

  - <span data-ttu-id="7eb6c-208">JET_paramMaxVerPages</span><span class="sxs-lookup"><span data-stu-id="7eb6c-208">JET_paramMaxVerPages</span></span>

  - <span data-ttu-id="7eb6c-209">JET_paramMaxTemporaryTables</span><span class="sxs-lookup"><span data-stu-id="7eb6c-209">JET_paramMaxTemporaryTables</span></span>

  - <span data-ttu-id="7eb6c-210">JET_paramLogBuffers</span><span class="sxs-lookup"><span data-stu-id="7eb6c-210">JET_paramLogBuffers</span></span>

  - <span data-ttu-id="7eb6c-211">JET_paramWaitLogFlush</span><span class="sxs-lookup"><span data-stu-id="7eb6c-211">JET_paramWaitLogFlush</span></span>

  - <span data-ttu-id="7eb6c-212">JET_paramLogCheckpointPeriod</span><span class="sxs-lookup"><span data-stu-id="7eb6c-212">JET_paramLogCheckpointPeriod</span></span>

  - <span data-ttu-id="7eb6c-213">JET_paramLogWaitingUserMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-213">JET_paramLogWaitingUserMax</span></span>

  - <span data-ttu-id="7eb6c-214">JET_paramDbExtensionSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-214">JET_paramDbExtensionSize</span></span>

  - <span data-ttu-id="7eb6c-215">JET_paramPageTempDBMin</span><span class="sxs-lookup"><span data-stu-id="7eb6c-215">JET_paramPageTempDBMin</span></span>

  - <span data-ttu-id="7eb6c-216">JET_paramPageFragment</span><span class="sxs-lookup"><span data-stu-id="7eb6c-216">JET_paramPageFragment</span></span>

  - <span data-ttu-id="7eb6c-217">JET_paramBatchIOBufferMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-217">JET_paramBatchIOBufferMax</span></span>

  - <span data-ttu-id="7eb6c-218">JET_paramCacheSizeMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-218">JET_paramCacheSizeMax</span></span>

  - <span data-ttu-id="7eb6c-219">JET_paramLRUKCorrInterval</span><span class="sxs-lookup"><span data-stu-id="7eb6c-219">JET_paramLRUKCorrInterval</span></span>

  - <span data-ttu-id="7eb6c-220">JET_paramLRUKHistoryMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-220">JET_paramLRUKHistoryMax</span></span>

  - <span data-ttu-id="7eb6c-221">JET_paramLRUKPolicy</span><span class="sxs-lookup"><span data-stu-id="7eb6c-221">JET_paramLRUKPolicy</span></span>

  - <span data-ttu-id="7eb6c-222">JET_paramLRUKTimeout</span><span class="sxs-lookup"><span data-stu-id="7eb6c-222">JET_paramLRUKTimeout</span></span>

  - <span data-ttu-id="7eb6c-223">JET_paramLRUKTrxCorrInterval</span><span class="sxs-lookup"><span data-stu-id="7eb6c-223">JET_paramLRUKTrxCorrInterval</span></span>

  - <span data-ttu-id="7eb6c-224">JET_paramOutstandingIOMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-224">JET_paramOutstandingIOMax</span></span>

  - <span data-ttu-id="7eb6c-225">JET_paramStartFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="7eb6c-225">JET_paramStartFlushThreshold</span></span>

  - <span data-ttu-id="7eb6c-226">JET_paramStopFlushThreshold</span><span class="sxs-lookup"><span data-stu-id="7eb6c-226">JET_paramStopFlushThreshold</span></span>

  - <span data-ttu-id="7eb6c-227">JET_paramCacheSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-227">JET_paramCacheSize</span></span>

  - <span data-ttu-id="7eb6c-228">JET_paramCacheSizeMin</span><span class="sxs-lookup"><span data-stu-id="7eb6c-228">JET_paramCacheSizeMin</span></span>

  - <span data-ttu-id="7eb6c-229">JET_paramPreferredVerPages</span><span class="sxs-lookup"><span data-stu-id="7eb6c-229">JET_paramPreferredVerPages</span></span>

  - <span data-ttu-id="7eb6c-230">JET_paramBackupChunkSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-230">JET_paramBackupChunkSize</span></span>

  - <span data-ttu-id="7eb6c-231">JET_paramBackupOutstandingReads</span><span class="sxs-lookup"><span data-stu-id="7eb6c-231">JET_paramBackupOutstandingReads</span></span>

  - <span data-ttu-id="7eb6c-232">JET_paramLogFileCreateAsynch</span><span class="sxs-lookup"><span data-stu-id="7eb6c-232">JET_paramLogFileCreateAsynch</span></span>

  - <span data-ttu-id="7eb6c-233">JET_paramRecordUpgradeDirtyLevel</span><span class="sxs-lookup"><span data-stu-id="7eb6c-233">JET_paramRecordUpgradeDirtyLevel</span></span>

  - <span data-ttu-id="7eb6c-234">JET_paramGlobalMinVerPages</span><span class="sxs-lookup"><span data-stu-id="7eb6c-234">JET_paramGlobalMinVerPages</span></span>

  - <span data-ttu-id="7eb6c-235">JET_paramPageHintCacheSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-235">JET_paramPageHintCacheSize</span></span>

  - <span data-ttu-id="7eb6c-236">JET_paramVersionStoreTaskQueueMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-236">JET_paramVersionStoreTaskQueueMax</span></span>

  - <span data-ttu-id="7eb6c-237">JET_paramDBAPageAvailMin</span><span class="sxs-lookup"><span data-stu-id="7eb6c-237">JET_paramDBAPageAvailMin</span></span>

  - <span data-ttu-id="7eb6c-238">JET_paramMaxRandomIOSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-238">JET_paramMaxRandomIOSize</span></span>

  - <span data-ttu-id="7eb6c-239">JET_paramCachedClosedTables</span><span class="sxs-lookup"><span data-stu-id="7eb6c-239">JET_paramCachedClosedTables</span></span>

  - <span data-ttu-id="7eb6c-240">JET_paramEnableFileCache</span><span class="sxs-lookup"><span data-stu-id="7eb6c-240">JET_paramEnableFileCache</span></span>

  - <span data-ttu-id="7eb6c-241">JET_paramEnableViewCache</span><span class="sxs-lookup"><span data-stu-id="7eb6c-241">JET_paramEnableViewCache</span></span>

  - <span data-ttu-id="7eb6c-242">JET_paramVerPageSize</span><span class="sxs-lookup"><span data-stu-id="7eb6c-242">JET_paramVerPageSize</span></span>

  - <span data-ttu-id="7eb6c-243">JET_paramCheckpointIOMax</span><span class="sxs-lookup"><span data-stu-id="7eb6c-243">JET_paramCheckpointIOMax</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-244">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-245">True</span><span class="sxs-lookup"><span data-stu-id="7eb6c-245">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-246">Escriba:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-247">Boolean</span><span class="sxs-lookup"><span data-stu-id="7eb6c-247">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-248">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-249">False, True</span><span class="sxs-lookup"><span data-stu-id="7eb6c-249">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-250">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-250">Scope:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-251">Instancia</span><span class="sxs-lookup"><span data-stu-id="7eb6c-251">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-252">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-252">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-253">Sí</span><span class="sxs-lookup"><span data-stu-id="7eb6c-253">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-254">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-254">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-255">Sí</span><span class="sxs-lookup"><span data-stu-id="7eb6c-255">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-256">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-256">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-257">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-257">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-258">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-258">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-259">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-259">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-260">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-260">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-261">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-261">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-262">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-262">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-263">No</span><span class="sxs-lookup"><span data-stu-id="7eb6c-263">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-264">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="7eb6c-264">Availability:</span></span></p></td>
<td><p><span data-ttu-id="7eb6c-265">A partir de Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7eb6c-265">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="7eb6c-266">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7eb6c-266">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-267"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="7eb6c-267"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="7eb6c-268">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-268">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb6c-269"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="7eb6c-269"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="7eb6c-270">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-270">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb6c-271"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="7eb6c-271"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="7eb6c-272">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="7eb6c-272">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="7eb6c-273">Consulte también</span><span class="sxs-lookup"><span data-stu-id="7eb6c-273">See Also</span></span>

[<span data-ttu-id="7eb6c-274">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="7eb6c-274">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="7eb6c-275">JetInit</span><span class="sxs-lookup"><span data-stu-id="7eb6c-275">JetInit</span></span>](./jetinit-function.md)
