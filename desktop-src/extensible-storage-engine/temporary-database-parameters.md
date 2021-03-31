---
description: 'Más información acerca de: parámetros temporales de base de datos'
title: Parámetros temporales de base de datos
TOCTitle: Temporary Database Parameters
ms:assetid: fa1cd867-6ce4-4de5-b31d-5b886f7c1e77
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294140(v=EXCHG.10)
ms:contentKeyID: 32765754
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
ms.openlocfilehash: c137472d03f1088da061c20b52050ae1a1f6629e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278654"
---
# <a name="temporary-database-parameters"></a><span data-ttu-id="82536-103">Parámetros temporales de base de datos</span><span class="sxs-lookup"><span data-stu-id="82536-103">Temporary Database Parameters</span></span>


<span data-ttu-id="82536-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="82536-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="temporary-database-parameters"></a><span data-ttu-id="82536-105">Parámetros temporales de base de datos</span><span class="sxs-lookup"><span data-stu-id="82536-105">Temporary Database Parameters</span></span>

<span data-ttu-id="82536-106">Este tema contiene los parámetros que se utilizan para la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="82536-106">This topic contains parameters that are used for the temporary database.</span></span>

<span data-ttu-id="82536-107">*JET_paramEnableTempTableVersioning*</span><span class="sxs-lookup"><span data-stu-id="82536-107">*JET_paramEnableTempTableVersioning*</span></span>  
<span data-ttu-id="82536-108">46</span><span class="sxs-lookup"><span data-stu-id="82536-108">46</span></span>  

<span data-ttu-id="82536-109">Este parámetro controla el uso de transacciones en tablas temporales.</span><span class="sxs-lookup"><span data-stu-id="82536-109">This parameter controls the use of transactions in temporary tables.</span></span> <span data-ttu-id="82536-110">Cuando este parámetro es false, las tablas temporales serán más rápidas, pero no será posible revertir las actualizaciones realizadas en una transacción.</span><span class="sxs-lookup"><span data-stu-id="82536-110">When this parameter is false, temporary tables will be faster but it will not be possible to rollback any updates made in a transaction.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82536-111">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="82536-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="82536-112">True</span><span class="sxs-lookup"><span data-stu-id="82536-112">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="82536-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="82536-114">Boolean</span><span class="sxs-lookup"><span data-stu-id="82536-114">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="82536-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="82536-116">False, True</span><span class="sxs-lookup"><span data-stu-id="82536-116">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-117">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="82536-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="82536-118">Instancia</span><span class="sxs-lookup"><span data-stu-id="82536-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-119">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="82536-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="82536-120">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-121">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="82536-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="82536-122">No</span><span class="sxs-lookup"><span data-stu-id="82536-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-123">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="82536-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="82536-124">No</span><span class="sxs-lookup"><span data-stu-id="82536-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-125">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="82536-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="82536-126">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-126">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-127">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="82536-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="82536-128">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-128">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-129">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="82536-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="82536-130">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-130">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-131">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="82536-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="82536-132">All</span><span class="sxs-lookup"><span data-stu-id="82536-132">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82536-133">*JET_paramPageTempDBMin*</span><span class="sxs-lookup"><span data-stu-id="82536-133">*JET_paramPageTempDBMin*</span></span>  
<span data-ttu-id="82536-134">19</span><span class="sxs-lookup"><span data-stu-id="82536-134">19</span></span>  

<span data-ttu-id="82536-135">Este parámetro controla el tamaño inicial de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="82536-135">This parameter controls the initial size of the temporary database.</span></span> <span data-ttu-id="82536-136">El tamaño está en páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="82536-136">The size is in database pages.</span></span> <span data-ttu-id="82536-137">Un tamaño de cero indica que se debe usar el tamaño predeterminado de una base de datos normal.</span><span class="sxs-lookup"><span data-stu-id="82536-137">A size of zero indicates that the default size of an ordinary database should be used.</span></span>

<span data-ttu-id="82536-138">A menudo, es deseable que las aplicaciones pequeñas configuren la base de datos temporal para que sea lo más pequeña posible.</span><span class="sxs-lookup"><span data-stu-id="82536-138">It is often desirable for small applications to configure the temporary database to be as small as possible.</span></span> <span data-ttu-id="82536-139">Si se establece este parámetro en 14, se obtiene la base de datos temporal más pequeña posible.</span><span class="sxs-lookup"><span data-stu-id="82536-139">Setting this parameter to 14 will achieve the smallest temporary database possible.</span></span> <span data-ttu-id="82536-140">Tenga en cuenta que también puede eliminar por completo la base de datos temporal estableciendo **JET_paramMaxTemporaryTables** en cero.</span><span class="sxs-lookup"><span data-stu-id="82536-140">Note that one can also entirely eliminate the temporary database by setting **JET_paramMaxTemporaryTables** to zero.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82536-141">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="82536-141">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="82536-142">0</span><span class="sxs-lookup"><span data-stu-id="82536-142">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-143">Escriba:</span><span class="sxs-lookup"><span data-stu-id="82536-143">Type:</span></span></p></td>
<td><p><span data-ttu-id="82536-144">Entero</span><span class="sxs-lookup"><span data-stu-id="82536-144">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-145">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="82536-145">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="82536-146">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="82536-146">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-147">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="82536-147">Scope:</span></span></p></td>
<td><p><span data-ttu-id="82536-148">Instancia</span><span class="sxs-lookup"><span data-stu-id="82536-148">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-149">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="82536-149">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="82536-150">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-150">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-151">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="82536-151">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="82536-152">No</span><span class="sxs-lookup"><span data-stu-id="82536-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-153">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="82536-153">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="82536-154">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-154">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-155">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="82536-155">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="82536-156">No</span><span class="sxs-lookup"><span data-stu-id="82536-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-157">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="82536-157">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="82536-158">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-158">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-159">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="82536-159">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="82536-160">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-160">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-161">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="82536-161">Availability:</span></span></p></td>
<td><p><span data-ttu-id="82536-162">All</span><span class="sxs-lookup"><span data-stu-id="82536-162">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="82536-163">*JET_paramTempPath*</span><span class="sxs-lookup"><span data-stu-id="82536-163">*JET_paramTempPath*</span></span>  
<span data-ttu-id="82536-164">1</span><span class="sxs-lookup"><span data-stu-id="82536-164">1</span></span>  

<span data-ttu-id="82536-165">Este parámetro indica la ruta de acceso del sistema de archivos relativa o absoluta de la carpeta o el archivo que contendrá la base de datos temporal de la instancia.</span><span class="sxs-lookup"><span data-stu-id="82536-165">This parameter indicates the relative or absolute file system path of the folder or file that will contain the temporary database for the instance.</span></span> <span data-ttu-id="82536-166">Si la ruta de acceso es a una carpeta que contendrá la base de datos temporal, debe terminar con un carácter de barra diagonal inversa.</span><span class="sxs-lookup"><span data-stu-id="82536-166">If the path is to a folder that will contain the temporary database then it must be terminated with a backslash character.</span></span> <span data-ttu-id="82536-167">La base de datos temporal se usa para contener datos volátiles que se generan en el proceso de control de llamadas de información de la API de ESE, creación de índices o almacenamiento del contenido de una tabla temporal.</span><span class="sxs-lookup"><span data-stu-id="82536-167">The temporary database is used to hold volatile data that is generated in the process of handling ESE API info calls, creating indexes, or storing the contents of a temporary table.</span></span>

<span data-ttu-id="82536-168">**Nota:**  Si se especifica una ruta de acceso relativa, será relativa al directorio de trabajo actual del proceso que hospeda la aplicación que usa el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="82536-168">**Note**  If a relative path is specified then it will be relative to the current working directory of the process that hosts the application that is using the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82536-169">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="82536-169">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="82536-170">&quot;tmp. edb&quot;</span><span class="sxs-lookup"><span data-stu-id="82536-170">&quot;tmp.edb&quot;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-171">Escriba:</span><span class="sxs-lookup"><span data-stu-id="82536-171">Type:</span></span></p></td>
<td><p><span data-ttu-id="82536-172">Path (cadena)</span><span class="sxs-lookup"><span data-stu-id="82536-172">Path (string)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-173">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="82536-173">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="82536-174">de 0 a 247 caracteres</span><span class="sxs-lookup"><span data-stu-id="82536-174">0 – 247 characters</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-175">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="82536-175">Scope:</span></span></p></td>
<td><p><span data-ttu-id="82536-176">Instancia</span><span class="sxs-lookup"><span data-stu-id="82536-176">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-177">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="82536-177">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="82536-178">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-178">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-179">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="82536-179">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="82536-180">No</span><span class="sxs-lookup"><span data-stu-id="82536-180">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-181">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="82536-181">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="82536-182">Sí</span><span class="sxs-lookup"><span data-stu-id="82536-182">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-183">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="82536-183">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="82536-184">No</span><span class="sxs-lookup"><span data-stu-id="82536-184">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-185">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="82536-185">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="82536-186">No</span><span class="sxs-lookup"><span data-stu-id="82536-186">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-187">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="82536-187">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="82536-188">No</span><span class="sxs-lookup"><span data-stu-id="82536-188">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-189">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="82536-189">Availability:</span></span></p></td>
<td><p><span data-ttu-id="82536-190">All</span><span class="sxs-lookup"><span data-stu-id="82536-190">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="82536-191">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82536-191">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="82536-192"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="82536-192"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="82536-193">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="82536-193">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="82536-194"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="82536-194"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="82536-195">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="82536-195">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="82536-196"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="82536-196"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="82536-197">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="82536-197">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="82536-198">Consulte también</span><span class="sxs-lookup"><span data-stu-id="82536-198">See Also</span></span>

[<span data-ttu-id="82536-199">Archivos del motor de almacenamiento extensible</span><span class="sxs-lookup"><span data-stu-id="82536-199">Extensible Storage Engine Files</span></span>](./extensible-storage-engine-files.md)  
[<span data-ttu-id="82536-200">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="82536-200">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="82536-201">JetInit</span><span class="sxs-lookup"><span data-stu-id="82536-201">JetInit</span></span>](./jetinit-function.md)
