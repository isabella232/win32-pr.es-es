---
description: 'Más información acerca de: parámetros de caché de base de datos'
title: Parámetros de caché de base de datos
TOCTitle: Database Cache Parameters
ms:assetid: 715e5495-0cd8-430f-bf21-509cf03bfbfd
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269293(v=EXCHG.10)
ms:contentKeyID: 32765585
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
ms.openlocfilehash: 77d83ea8998da7c00fd294f81b94099d23d524e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715413"
---
# <a name="database-cache-parameters"></a><span data-ttu-id="cdf25-103">Parámetros de caché de base de datos</span><span class="sxs-lookup"><span data-stu-id="cdf25-103">Database Cache Parameters</span></span>


<span data-ttu-id="cdf25-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="cdf25-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="database-cache-parameters"></a><span data-ttu-id="cdf25-105">Parámetros de caché de base de datos</span><span class="sxs-lookup"><span data-stu-id="cdf25-105">Database Cache Parameters</span></span>

<span data-ttu-id="cdf25-106">Este tema contiene los parámetros que se utilizan para la caché de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-106">This topic contains parameters that are used for the database cache.</span></span>

<span data-ttu-id="cdf25-107">*JET_paramBatchIOBufferMax*</span><span class="sxs-lookup"><span data-stu-id="cdf25-107">*JET_paramBatchIOBufferMax*</span></span>  
<span data-ttu-id="cdf25-108">22</span><span class="sxs-lookup"><span data-stu-id="cdf25-108">22</span></span>  

<span data-ttu-id="cdf25-109">Este parámetro controla el tamaño de una parte auxiliar de la memoria caché de páginas de base de datos que se usa para simular la e/s de recopilación de dispersión cuando, de lo contrario, no está disponible.</span><span class="sxs-lookup"><span data-stu-id="cdf25-109">This parameter controls the size of an auxiliary part of the database page cache that is used to simulate scatter gather I/O when it is otherwise not available.</span></span> <span data-ttu-id="cdf25-110">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-110">The size is in database pages.</span></span>

<span data-ttu-id="cdf25-111">**Windows XP y versiones posteriores:**  Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-111">**Windows XP and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-112">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-113">256</span><span class="sxs-lookup"><span data-stu-id="cdf25-113">256</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-114">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-115">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-116">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-117">0,2:2147483647</span><span class="sxs-lookup"><span data-stu-id="cdf25-117">0, 2 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-118">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-119">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-119">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-120">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-121">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-121">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-122">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-123">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-124">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-125">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-126">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-127">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-128">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-129">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-130">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-131">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-132">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-133">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-133">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-134">*JET_paramCacheSize*</span><span class="sxs-lookup"><span data-stu-id="cdf25-134">*JET_paramCacheSize*</span></span>  
<span data-ttu-id="cdf25-135">41</span><span class="sxs-lookup"><span data-stu-id="cdf25-135">41</span></span>  

<span data-ttu-id="cdf25-136">Este parámetro se puede utilizar para controlar el tamaño de la memoria caché de páginas de base de datos en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="cdf25-136">This parameter can be used to control the size of the database page cache at run time.</span></span> <span data-ttu-id="cdf25-137">Normalmente, la memoria caché ajustará automáticamente su tamaño como una función de los niveles de actividad de la base de datos y del equipo.</span><span class="sxs-lookup"><span data-stu-id="cdf25-137">Ordinarily, the cache will automatically tune its size as a function of database and machine activity levels.</span></span> <span data-ttu-id="cdf25-138">Si la aplicación establece este parámetro en cero, la memoria caché ajustará su propio tamaño de esta manera.</span><span class="sxs-lookup"><span data-stu-id="cdf25-138">If the application sets this parameter to zero, then the cache will tune its own size in this manner.</span></span> <span data-ttu-id="cdf25-139">Sin embargo, si la aplicación establece este parámetro en un valor distinto de cero, la memoria caché se ajustará a ese tamaño de destino (en páginas de base de datos).</span><span class="sxs-lookup"><span data-stu-id="cdf25-139">However, if the application sets this parameter to a non-zero value then the cache will adjust itself to that target size (in database pages).</span></span> <span data-ttu-id="cdf25-140">La caché conservará su tamaño en ese umbral hasta que se le proporcione un nuevo tamaño o hasta que se libere para elegir su propio tamaño.</span><span class="sxs-lookup"><span data-stu-id="cdf25-140">The cache will then hold its size at that threshold until given a new size or until it is released to choose its own size.</span></span>

<span data-ttu-id="cdf25-141">**Nota:**  El tamaño de la caché sigue sujeto a los límites impuestos por **JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-141">**Note**  The cache size is still subject to the limits imposed by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="cdf25-142">Cuando se lee este parámetro, se devuelve el tamaño real de la memoria caché en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-142">When this parameter is read, the actual size of the cache in database pages is returned.</span></span> <span data-ttu-id="cdf25-143">La aplicación puede usar este tamaño como entrada para impulsar su ajuste manual del tamaño de la memoria caché.</span><span class="sxs-lookup"><span data-stu-id="cdf25-143">This size can be used by the application as an input to drive its manual adjustment of the cache size.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-144">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-144">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-145">Especial</span><span class="sxs-lookup"><span data-stu-id="cdf25-145">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-146">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-146">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-147">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-147">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-148">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-148">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-149"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="cdf25-149"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="cdf25-150"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="cdf25-150"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-151">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-151">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-152">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-152">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-153">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-153">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-154">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-155">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-155">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-156">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-156">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-157">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-157">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-158">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-158">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-159">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-159">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-160">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-160">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-161">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-161">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-162">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-162">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-163">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-163">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-164">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-164">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-165">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-165">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-166">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-166">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-167">*JET_paramCacheSizeMin*</span><span class="sxs-lookup"><span data-stu-id="cdf25-167">*JET_paramCacheSizeMin*</span></span>  
<span data-ttu-id="cdf25-168">60</span><span class="sxs-lookup"><span data-stu-id="cdf25-168">60</span></span>  

<span data-ttu-id="cdf25-169">Este parámetro configura el tamaño mínimo de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-169">This parameter configures the minimum size of the database page cache.</span></span> <span data-ttu-id="cdf25-170">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-170">The size is in database pages.</span></span>

<span data-ttu-id="cdf25-171">De forma predeterminada, la memoria caché de base de datos ajustará automáticamente su tamaño entre los límites establecidos por **JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-171">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="cdf25-172">**Windows 2000:**  En Windows 2000, este parámetro debe establecerse en un valor que sea aproximadamente igual a cuatro veces el número de subprocesos que estarán dentro de la API de ESE al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="cdf25-172">**Windows 2000:**  On Windows 2000, this parameter should be set to a value roughly equal to four times the number of threads that will be inside the ESE API at the same time.</span></span> <span data-ttu-id="cdf25-173">Esto es necesario para evitar interbloqueos causados por un número insuficiente de búferes de caché de páginas de base de datos para realizar operaciones complejas como divisiones de árbol B +.</span><span class="sxs-lookup"><span data-stu-id="cdf25-173">This is required to avoid deadlocks caused by an insufficient number of database page cache buffers to perform complex operations like B+ Tree splits.</span></span>

<span data-ttu-id="cdf25-174">**Windows XP y versiones posteriores:**  El administrador de caché establecerá automáticamente su propio tamaño de caché mínimo para evitar los interbloqueos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-174">**Windows XP and later:**  The cache manager will automatically set its own minimum cache size to avoid deadlocks.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-175">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-175">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-176"><strong>Windows 2000:</strong>  64</span><span class="sxs-lookup"><span data-stu-id="cdf25-176"><strong>Windows 2000:</strong>  64</span></span></p>
<p><span data-ttu-id="cdf25-177"><strong>Windows XP:</strong>  1</span><span class="sxs-lookup"><span data-stu-id="cdf25-177"><strong>Windows XP:</strong>  1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-178">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-178">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-179">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-179">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-180">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-180">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-181"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="cdf25-181"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="cdf25-182"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="cdf25-182"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-183">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-183">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-184">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-184">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-185">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-185">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-186"><strong>Windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="cdf25-186"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="cdf25-187"><strong>Windows XP:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="cdf25-187"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-188">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-188">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-189"><strong>Windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="cdf25-189"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="cdf25-190"><strong>Windows XP:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="cdf25-190"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-191">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-191">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-192">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-192">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-193">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-193">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-194">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-194">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-195">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-195">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-196">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-196">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-197">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-197">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-198">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-198">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-199">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-199">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-200">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-200">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-201">*JET_paramCacheSizeMax*</span><span class="sxs-lookup"><span data-stu-id="cdf25-201">*JET_paramCacheSizeMax*</span></span>  
<span data-ttu-id="cdf25-202">23</span><span class="sxs-lookup"><span data-stu-id="cdf25-202">23</span></span>  

<span data-ttu-id="cdf25-203">Este parámetro configura el tamaño máximo de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-203">This parameter configures the maximum size of the database page cache.</span></span> <span data-ttu-id="cdf25-204">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-204">The size is in database pages.</span></span>

<span data-ttu-id="cdf25-205">De forma predeterminada, la memoria caché de base de datos ajustará automáticamente su tamaño entre los límites establecidos por **JET_paramCacheSizeMin** y **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-205">By default, the database cache will automatically adjust its size between the limits set by **JET_paramCacheSizeMin** and **JET_paramCacheSizeMax**.</span></span>

<span data-ttu-id="cdf25-206">**Nota:**   Si este parámetro se deja en su valor predeterminado, el tamaño máximo de la memoria caché se establecerá en el tamaño de la memoria física cuando se llame a [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="cdf25-206">**Note**   If this parameter is left to its default value, then the maximum size of the cache will be set to the size of physical memory when [JetInit](./jetinit-function.md) is called.</span></span>

<span data-ttu-id="cdf25-207">**Windows Vista:**  A partir de Windows Vista, el valor predeterminado de este parámetro se ha cambiado para aclarar este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="cdf25-207">**Windows Vista:**  As of Windows Vista, the default value of this parameter was changed to clarify this behavior.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-208">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-208">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-209"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  512</span><span class="sxs-lookup"><span data-stu-id="cdf25-209"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  512</span></span></p>
<p><span data-ttu-id="cdf25-210"><strong>Windows Vista:</strong>  2 mil millones</span><span class="sxs-lookup"><span data-stu-id="cdf25-210"><strong>Windows Vista:</strong>  2000000000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-211">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-211">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-212">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-212">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-213">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-213">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-214"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="cdf25-214"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="cdf25-215"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="cdf25-215"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-216">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-216">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-217">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-217">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-218">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-218">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-219"><strong>Windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="cdf25-219"><strong>Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="cdf25-220"><strong>Windows XP:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="cdf25-220"><strong>Windows XP:</strong>  Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-221">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-221">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-222"><strong>Windows XP y windows 2000:</strong>  No</span><span class="sxs-lookup"><span data-stu-id="cdf25-222"><strong>Windows XP and Windows 2000:</strong>  No</span></span></p>
<p><span data-ttu-id="cdf25-223"><strong>Windows Vista y Windows Server 2003:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="cdf25-223"><strong>Windows Vista and Windows Server 2003:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-224">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-224">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-225">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-225">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-226">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-226">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-227">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-227">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-228">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-228">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-229">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-229">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-230">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-230">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-231">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-231">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-232">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-232">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-233">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-233">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-234">*JET_paramCheckpointDepthMax*</span><span class="sxs-lookup"><span data-stu-id="cdf25-234">*JET_paramCheckpointDepthMax*</span></span>  
<span data-ttu-id="cdf25-235">24</span><span class="sxs-lookup"><span data-stu-id="cdf25-235">24</span></span> 

<span data-ttu-id="cdf25-236">Este parámetro controla el modo en que se vacían las páginas de base de datos de forma agresiva desde la memoria caché de páginas de base de datos para minimizar la cantidad de tiempo que se tarda en recuperarse de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="cdf25-236">This parameter controls how aggressively database pages are flushed from the database page cache to minimize the amount of time it will take to recover from a crash.</span></span> <span data-ttu-id="cdf25-237">El parámetro es un umbral en bytes para el número de archivos de registro de transacciones que se deben reproducir después de un bloqueo.</span><span class="sxs-lookup"><span data-stu-id="cdf25-237">The parameter is a threshold in bytes for about how many transaction log files will need to be replayed after a crash.</span></span>

<span data-ttu-id="cdf25-238">Si el registro circular está habilitado mediante [JET_paramCircularLog](./transaction-log-parameters.md) , este parámetro también controlará la cantidad aproximada de archivos de registro de transacciones que se conservarán en el disco.</span><span class="sxs-lookup"><span data-stu-id="cdf25-238">If circular logging is enabled using [JET_paramCircularLog](./transaction-log-parameters.md) then this parameter will also control the approximate amount of transaction log files that will be retained on disk.</span></span>

<span data-ttu-id="cdf25-239">Es importante que este parámetro no se establezca demasiado bajo.</span><span class="sxs-lookup"><span data-stu-id="cdf25-239">It is important that this parameter not be set too low.</span></span> <span data-ttu-id="cdf25-240">Como el valor de este parámetro se aproxima a cero, la memoria caché se vuelve más agresiva al vaciar páginas de base de datos en el disco.</span><span class="sxs-lookup"><span data-stu-id="cdf25-240">As the value of this parameter approaches zero, the cache will become more and more aggressive when flushing database pages to disk.</span></span> <span data-ttu-id="cdf25-241">Esto no solo da como resultado un mayor número de operaciones de escritura en los archivos de base de datos, pero también provoca indirectamente un mayor número de lecturas en esos archivos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-241">This not only results in an increased number of writes to the database files but it also indirectly causes an increased number of reads to those files as well.</span></span> <span data-ttu-id="cdf25-242">Esto puede producir problemas de rendimiento muy significativos en algunos casos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-242">This can cause very significant performance problems in some cases.</span></span> <span data-ttu-id="cdf25-243">Desafortunadamente, el establecimiento del valor óptimo más pequeño para este parámetro solo se puede realizar mediante experimentación con la aplicación de destino.</span><span class="sxs-lookup"><span data-stu-id="cdf25-243">Unfortunately, setting the smallest optimal value for this parameter can only be done using experimentation with the target application.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-244">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-244">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-245">20971520</span><span class="sxs-lookup"><span data-stu-id="cdf25-245">20971520</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-246">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-246">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-247">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-247">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-248">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-248">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-249"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cdf25-249"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 2147483647</span></span></p>
<p><span data-ttu-id="cdf25-250"><strong>Windows Vista:</strong>  Todos los valores</span><span class="sxs-lookup"><span data-stu-id="cdf25-250"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-251">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-251">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-252"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong> Este parámetro es global.</span><span class="sxs-lookup"><span data-stu-id="cdf25-252"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong> This parameter is global.</span></span></p>
<p><span data-ttu-id="cdf25-253"><strong>Windows Vista:</strong>  Este parámetro es por instancia.</span><span class="sxs-lookup"><span data-stu-id="cdf25-253"><strong>Windows Vista:</strong>  This parameter is per instance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-254">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-254">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-255">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-255">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-256">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-256">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-257">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-257">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-258">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-258">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-259">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-259">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-260">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-260">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-261">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-261">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-262">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-262">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-263">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-263">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-264">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-264">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-265">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-265">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-266">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-266">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-267">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-267">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-268">*JET_paramCheckpointIOMax*</span><span class="sxs-lookup"><span data-stu-id="cdf25-268">*JET_paramCheckpointIOMax*</span></span>  
<span data-ttu-id="cdf25-269">135</span><span class="sxs-lookup"><span data-stu-id="cdf25-269">135</span></span>  

<span data-ttu-id="cdf25-270">Este parámetro controla el número máximo de escrituras simultáneas que utilizará el motor de base de datos para vaciar las páginas de base de datos modificadas con el fin de avanzar el punto de control.</span><span class="sxs-lookup"><span data-stu-id="cdf25-270">This parameter controls the maximum number of concurrent writes that the database engine will use to flush modified database pages for the purpose of advancing the checkpoint.</span></span> <span data-ttu-id="cdf25-271">El valor de este parámetro puede usarse para equilibrar la velocidad con la que el punto de control puede ser avanzado frente al impacto negativo que este proceso tendrá en el tiempo de respuesta para otras operaciones de e/s en los discos que contienen la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-271">The value of this parameter can be used to balance the speed with which the checkpoint can be advanced versus the negative impact this process will have on the response time for other I/O operations to the disks holding the database.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-272">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-272">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-273">96</span><span class="sxs-lookup"><span data-stu-id="cdf25-273">96</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-274">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-274">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-275">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-275">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-276">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-276">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-277">8:1024</span><span class="sxs-lookup"><span data-stu-id="cdf25-277">8 – 1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-278">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-278">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-279">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-279">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-280">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-280">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-281">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-281">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-282">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-282">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-283">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-283">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-284">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-284">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-285">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-285">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-286">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-286">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-287">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-287">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-288">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-288">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-289">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-289">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-290">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-290">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-291">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-291">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-292">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-292">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-293">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="cdf25-293">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-294">*JET_paramEnableViewCache*</span><span class="sxs-lookup"><span data-stu-id="cdf25-294">*JET_paramEnableViewCache*</span></span>  
<span data-ttu-id="cdf25-295">127</span><span class="sxs-lookup"><span data-stu-id="cdf25-295">127</span></span>  

<span data-ttu-id="cdf25-296">Cuando este parámetro es **true**, el motor de base de datos usará los datos de la base de datos directamente desde la memoria caché de archivos de Windows en lugar de copiar los datos almacenados en caché en su propia memoria privada.</span><span class="sxs-lookup"><span data-stu-id="cdf25-296">When this parameter is **True**, the database engine will use database data directly from the Windows file cache rather than copying the cached data into its own private memory.</span></span> <span data-ttu-id="cdf25-297">Cualquier dato de base de datos que se modifique se almacenará en la memoria caché privada.</span><span class="sxs-lookup"><span data-stu-id="cdf25-297">Any database data that is modified will still be cached in private memory.</span></span>

<span data-ttu-id="cdf25-298">La intención de este modo es reducir aún más la cantidad de memoria privada que usa el motor de base de datos para almacenar en caché los datos de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-298">The intent of this mode is to further reduce the amount of private memory used by the database engine to cache database data.</span></span>

<span data-ttu-id="cdf25-299">La memoria caché de vista solo se puede usar si el uso de la memoria caché de archivos de Windows está habilitado estableciendo JET_paramEnableFileCache en **true**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-299">The view cache may only be used if the use of the Windows file cache is enabled by setting JET_paramEnableFileCache to **True**.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-300">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-300">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-301">False</span><span class="sxs-lookup"><span data-stu-id="cdf25-301">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-302">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-302">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-303">Boolean</span><span class="sxs-lookup"><span data-stu-id="cdf25-303">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-304">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-304">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-305">False, True</span><span class="sxs-lookup"><span data-stu-id="cdf25-305">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-306">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-306">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-307">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-307">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-308">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-308">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-309">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-309">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-310">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-310">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-311">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-311">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-312">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-312">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-313">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-313">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-314">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-314">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-315">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-315">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-316">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-316">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-317">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-318">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-318">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-319">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-319">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-320">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-320">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-321">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="cdf25-321">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-322">*JET_paramLRUKCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="cdf25-322">*JET_paramLRUKCorrInterval*</span></span>  
<span data-ttu-id="cdf25-323">25</span><span class="sxs-lookup"><span data-stu-id="cdf25-323">25</span></span>  

<span data-ttu-id="cdf25-324">Este parámetro establece el intervalo de tiempo en microsegundos en el que se considera que dos accesos a las páginas de base de datos están correlacionados.</span><span class="sxs-lookup"><span data-stu-id="cdf25-324">This parameter sets the time interval in microseconds over which two database page accesses are considered to be correlated.</span></span> <span data-ttu-id="cdf25-325">Este intervalo de correlación controla la sensibilidad del algoritmo de sustitución de páginas (LRU-K) de la memoria caché en los accesos de página sucesivos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-325">This correlation interval controls the sensitivity of the cache's page replacement algorithm (LRU-K) to successive page accesses.</span></span> <span data-ttu-id="cdf25-326">Esto, a su vez, afectará a las páginas que decida mantener almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="cdf25-326">This in turn will affect which pages it chooses to keep cached.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-327">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-327">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-328">128000</span><span class="sxs-lookup"><span data-stu-id="cdf25-328">128000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-329">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-329">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-330">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-330">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-331">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-331">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-332"><strong>Windows 2000, Windows XP y Windows Server 2003: </strong>    0 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cdf25-332"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>    0 – 2147483647</span></span></p>
<p><span data-ttu-id="cdf25-333"><strong>Windows Vista:</strong>  Todos los valores</span><span class="sxs-lookup"><span data-stu-id="cdf25-333"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-334">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-334">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-335">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-335">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-336">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-336">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-337">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-337">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-338">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-338">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-339">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-339">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-340">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-340">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-341">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-341">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-342">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-342">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-343">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-343">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-344">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-344">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-345">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-345">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-346">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-346">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-347">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-347">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-348">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-348">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-349">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-349">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-350">*JET_paramLRUKHistoryMax*</span><span class="sxs-lookup"><span data-stu-id="cdf25-350">*JET_paramLRUKHistoryMax*</span></span>  
<span data-ttu-id="cdf25-351">26</span><span class="sxs-lookup"><span data-stu-id="cdf25-351">26</span></span>  

<span data-ttu-id="cdf25-352">Este parámetro establece el número máximo de páginas de base de datos no almacenadas en caché para las que se conservarán los tiempos de acceso a las páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-352">This parameter sets the maximum number of non cached database pages for which database page access times will be retained.</span></span> <span data-ttu-id="cdf25-353">Estos registros de historial permiten que el algoritmo de sustitución de páginas de la memoria caché (LRU-K) detecte con más precisión las páginas populares que se expulsaron erróneamente de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-353">These history records allow the cache's page replacement algorithm (LRU-K) to more accurately detect popular pages that were wrongly evicted from the database page cache.</span></span>

<span data-ttu-id="cdf25-354">**Windows XP y Windows Server 2003:**  Este parámetro se omite en Windows XP y Windows Server 2003 y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-354">**Windows XP and Windows Server 2003:**  This parameter is ignored on Windows XP and Windows Server 2003 and does not affect the operation of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-355">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-355">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-356"><strong>Windows 2000:</strong>  1024</span><span class="sxs-lookup"><span data-stu-id="cdf25-356"><strong>Windows 2000:</strong>  1024</span></span></p>
<p><span data-ttu-id="cdf25-357"><strong>Windows Vista:</strong>  100000</span><span class="sxs-lookup"><span data-stu-id="cdf25-357"><strong>Windows Vista:</strong>  100000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-358">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-358">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-359">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-359">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-360">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-360">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-361"><strong>Windows 2000:</strong>  0 – 4194303</span><span class="sxs-lookup"><span data-stu-id="cdf25-361"><strong>Windows 2000:</strong>  0 – 4194303</span></span></p>
<p><span data-ttu-id="cdf25-362"><strong>Windows Vista:</strong>  Todos los valores</span><span class="sxs-lookup"><span data-stu-id="cdf25-362"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-363">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-363">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-364">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-364">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-365">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-365">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-366">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-366">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-367">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-367">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-368">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-368">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-369">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-369">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-370">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-370">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-371">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-371">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-372">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-372">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-373">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-373">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-374">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-374">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-375">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-375">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-376">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-376">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-377">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-377">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-378">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-378">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-379">*JET_paramLRUKPolicy*</span><span class="sxs-lookup"><span data-stu-id="cdf25-379">*JET_paramLRUKPolicy*</span></span>  
<span data-ttu-id="cdf25-380">27</span><span class="sxs-lookup"><span data-stu-id="cdf25-380">27</span></span>  

<span data-ttu-id="cdf25-381">Este parámetro configura el número de accesos a páginas de base de datos que se tienen en cuenta para determinar la utilidad de la página.</span><span class="sxs-lookup"><span data-stu-id="cdf25-381">This parameter configures the number of database page accesses that are considered for determining the usefulness of the page.</span></span> <span data-ttu-id="cdf25-382">Este parámetro es esencialmente el K de LRU-K, el algoritmo de reemplazo de páginas de la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-382">This parameter is essentially the K in LRU-K, the database page cache's page replacement algorithm.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-383">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-383">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-384">2</span><span class="sxs-lookup"><span data-stu-id="cdf25-384">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-385">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-385">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-386">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-386">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-387">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-387">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-388">1-2</span><span class="sxs-lookup"><span data-stu-id="cdf25-388">1-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-389">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-389">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-390">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-390">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-391">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-391">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-392">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-392">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-393">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-393">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-394">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-394">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-395">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-395">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-396">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-396">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-397">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-397">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-398">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-398">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-399">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-399">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-400">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-400">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-401">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-401">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-402">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-402">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-403">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-403">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-404">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-404">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-405">*JET_paramLRUKTimeout*</span><span class="sxs-lookup"><span data-stu-id="cdf25-405">*JET_paramLRUKTimeout*</span></span>  
<span data-ttu-id="cdf25-406">28</span><span class="sxs-lookup"><span data-stu-id="cdf25-406">28</span></span>

<span data-ttu-id="cdf25-407">Este parámetro indica el período de tiempo, en segundos, tras el cual se considera que una página de la memoria caché de páginas de base de datos ha perdido el acceso a la página con el fin de considerar la utilidad de la página.</span><span class="sxs-lookup"><span data-stu-id="cdf25-407">This parameter indicates the period of time in seconds after which a page in the database page cache is considered to have lost a page access for the purpose of considering the usefulness of the page.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-408">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-408">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-409">100</span><span class="sxs-lookup"><span data-stu-id="cdf25-409">100</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-410">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-410">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-411">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-411">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-412">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-412">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-413"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="cdf25-413"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  1 – 2147483647</span></span></p>
<p><span data-ttu-id="cdf25-414"><strong>Windows Vista:</strong>   1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="cdf25-414"><strong>Windows Vista:</strong>   1 – 4294967295</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-415">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-415">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-416">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-416">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-417">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-417">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-418">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-418">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-419">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-419">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-420">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-420">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-421">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-421">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-422">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-422">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-423">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-423">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-424">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-424">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-425">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-425">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-426">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-426">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-427">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-427">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-428">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-428">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-429">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-429">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-430">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-430">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-431">*JET_paramLRUKTrxCorrInterval*</span><span class="sxs-lookup"><span data-stu-id="cdf25-431">*JET_paramLRUKTrxCorrInterval*</span></span>  
<span data-ttu-id="cdf25-432">29</span><span class="sxs-lookup"><span data-stu-id="cdf25-432">29</span></span>  

<span data-ttu-id="cdf25-433">Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-433">This parameter is obsolete and does not affect the operation of the database engine.</span></span>

<span data-ttu-id="cdf25-434">*JET_paramStartFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="cdf25-434">*JET_paramStartFlushThreshold*</span></span>  
<span data-ttu-id="cdf25-435">31</span><span class="sxs-lookup"><span data-stu-id="cdf25-435">31</span></span>  

<span data-ttu-id="cdf25-436">Este parámetro controla si la memoria caché de páginas de base de datos empieza a expulsar páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="cdf25-436">This parameter controls when the database page cache begins evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="cdf25-437">Cuando el número de búferes de página en la memoria caché cae por debajo de este umbral, se iniciará un proceso en segundo plano para reponer ese grupo de búferes disponibles.</span><span class="sxs-lookup"><span data-stu-id="cdf25-437">When the number of page buffers in the cache drops below this threshold then a background process will be started to replenish that pool of available buffers.</span></span> <span data-ttu-id="cdf25-438">Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-438">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="cdf25-439">Este umbral también debe ser siempre inferior al umbral de detención establecido por **JET_paramStopFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-439">This threshold must also always be less than the stop threshold as set by **JET_paramStopFlushThreshold**.</span></span>

<span data-ttu-id="cdf25-440">El alto de distancia del umbral de inicio determinará el tiempo de respuesta que debe tener la caché de páginas de base de datos para generar los búferes disponibles antes de que la aplicación los necesite.</span><span class="sxs-lookup"><span data-stu-id="cdf25-440">The distance height of the start threshold will determine the response time that the database page cache must have to produce available buffers before the application needs them.</span></span> <span data-ttu-id="cdf25-441">Un umbral de inicio alto proporcionará al proceso en segundo plano más tiempo para reaccionar.</span><span class="sxs-lookup"><span data-stu-id="cdf25-441">A high start threshold will give the background process more time to react.</span></span> <span data-ttu-id="cdf25-442">Sin embargo, un umbral de inicio alto implica un umbral de detención mayor y reduce el tamaño efectivo de la caché de páginas de base de datos para las páginas modificadas (Windows 2000) o para todas las páginas (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="cdf25-442">However, a high start threshold implies a higher stop threshold and that will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-443">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-443">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-444"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  5 (1%)</span><span class="sxs-lookup"><span data-stu-id="cdf25-444"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  5 (1%)</span></span></p>
<p><span data-ttu-id="cdf25-445"><strong>Windows Vista:</strong>  20 millones (1%)</span><span class="sxs-lookup"><span data-stu-id="cdf25-445"><strong>Windows Vista:</strong>  20000000 (1%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-446">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-446">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-447">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-447">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-448">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-448">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-449"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="cdf25-449"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="cdf25-450"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="cdf25-450"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="cdf25-451"><strong>Windows Vista:</strong>  Todos los valores</span><span class="sxs-lookup"><span data-stu-id="cdf25-451"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-452">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-452">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-453">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-453">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-454">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-454">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-455">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-455">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-456">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-456">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-457">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-457">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-458">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-458">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-459">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-459">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-460">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-460">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-461">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-461">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-462">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-462">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-463">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-463">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-464">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-464">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-465">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-465">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-466">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-466">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-467">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-467">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cdf25-468">*JET_paramStopFlushThreshold*</span><span class="sxs-lookup"><span data-stu-id="cdf25-468">*JET_paramStopFlushThreshold*</span></span>  
<span data-ttu-id="cdf25-469">32</span><span class="sxs-lookup"><span data-stu-id="cdf25-469">32</span></span>  

<span data-ttu-id="cdf25-470">Este parámetro controla cuándo la memoria caché de páginas de base de datos termina la expulsando páginas de la memoria caché para dejar espacio a las páginas que no están almacenadas en caché.</span><span class="sxs-lookup"><span data-stu-id="cdf25-470">This parameter controls when the database page cache ends evicting pages from the cache to make room for pages that are not cached.</span></span> <span data-ttu-id="cdf25-471">Cuando el número de búferes de página de la memoria caché supera este umbral, se detiene el proceso en segundo plano que se inició para reponer el grupo de búferes disponibles.</span><span class="sxs-lookup"><span data-stu-id="cdf25-471">When the number of page buffers in the cache rises above this threshold then the background process that was started to replenish that pool of available buffers is stopped.</span></span> <span data-ttu-id="cdf25-472">Este umbral siempre es relativo al tamaño máximo de la memoria caché establecido por **JET_paramCacheSizeMax**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-472">This threshold is always relative to the maximum cache size as set by **JET_paramCacheSizeMax**.</span></span> <span data-ttu-id="cdf25-473">Este umbral también debe ser siempre mayor que el umbral de inicio establecido por **JET_paramStartFlushThreshold**.</span><span class="sxs-lookup"><span data-stu-id="cdf25-473">This threshold must also always be greater than the start threshold as set by **JET_paramStartFlushThreshold**.</span></span>

<span data-ttu-id="cdf25-474">La distancia entre el umbral de inicio y el umbral de detención afecta a la eficacia con la que el proceso en segundo plano vacía las páginas de la base de datos.</span><span class="sxs-lookup"><span data-stu-id="cdf25-474">The distance between the start threshold and the stop threshold affects the efficiency with which database pages are flushed by the background process.</span></span> <span data-ttu-id="cdf25-475">Una brecha más grande hará que sea más probable que se combinen las escrituras en páginas vecinas.</span><span class="sxs-lookup"><span data-stu-id="cdf25-475">A larger gap will make it more likely that writes to neighboring pages may be combined.</span></span> <span data-ttu-id="cdf25-476">Sin embargo, un umbral de detención alta reducirá el tamaño efectivo de la caché de páginas de base de datos para las páginas modificadas (Windows 2000) o para todas las páginas (Windows XP y versiones posteriores).</span><span class="sxs-lookup"><span data-stu-id="cdf25-476">However, a high stop threshold will reduce the effective size of the database page cache for modified pages (Windows 2000) or for all pages (Windows XP and later).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-477">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="cdf25-477">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-478"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  10 (2%)</span><span class="sxs-lookup"><span data-stu-id="cdf25-478"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  10 (2%)</span></span></p>
<p><span data-ttu-id="cdf25-479"><strong>Windows Vista:</strong>  40 millones (2%)</span><span class="sxs-lookup"><span data-stu-id="cdf25-479"><strong>Windows Vista:</strong>  40000000 (2%)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-480">Escriba:</span><span class="sxs-lookup"><span data-stu-id="cdf25-480">Type:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-481">Entero</span><span class="sxs-lookup"><span data-stu-id="cdf25-481">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-482">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cdf25-482">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-483"><strong>Windows 2000:</strong>  1 – 1048575</span><span class="sxs-lookup"><span data-stu-id="cdf25-483"><strong>Windows 2000:</strong>  1 – 1048575</span></span></p>
<p><span data-ttu-id="cdf25-484"><strong>Windows XP:</strong>  1 – 4294967295</span><span class="sxs-lookup"><span data-stu-id="cdf25-484"><strong>Windows XP:</strong>  1 – 4294967295</span></span></p>
<p><span data-ttu-id="cdf25-485"><strong>Windows Vista:</strong>  Todos los valores</span><span class="sxs-lookup"><span data-stu-id="cdf25-485"><strong>Windows Vista:</strong>  All Values</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-486">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="cdf25-486">Scope:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-487">Global</span><span class="sxs-lookup"><span data-stu-id="cdf25-487">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-488">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-488">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-489">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-489">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-490">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="cdf25-490">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-491">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-491">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-492">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="cdf25-492">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-493">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-493">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-494">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-494">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-495">No</span><span class="sxs-lookup"><span data-stu-id="cdf25-495">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-496">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="cdf25-496">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-497">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-497">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-498">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="cdf25-498">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-499">Sí</span><span class="sxs-lookup"><span data-stu-id="cdf25-499">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-500">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="cdf25-500">Availability:</span></span></p></td>
<td><p><span data-ttu-id="cdf25-501">All</span><span class="sxs-lookup"><span data-stu-id="cdf25-501">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="cdf25-502">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cdf25-502">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-503"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="cdf25-503"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf25-504">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="cdf25-504">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdf25-505"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="cdf25-505"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf25-506">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="cdf25-506">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cdf25-507"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="cdf25-507"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="cdf25-508">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="cdf25-508">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="cdf25-509">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cdf25-509">See Also</span></span>

[<span data-ttu-id="cdf25-510">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="cdf25-510">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="cdf25-511">JetInit</span><span class="sxs-lookup"><span data-stu-id="cdf25-511">JetInit</span></span>](./jetinit-function.md)
