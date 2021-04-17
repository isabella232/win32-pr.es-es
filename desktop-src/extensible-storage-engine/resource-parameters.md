---
description: 'Más información acerca de: parámetros de recursos'
title: Parámetros de recursos
TOCTitle: Resource Parameters
ms:assetid: 1f61845a-ffa5-4894-9fe0-a58737b3b54e
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269201(v=EXCHG.10)
ms:contentKeyID: 32765504
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
ms.openlocfilehash: 953488a273092413df78d4fe396899d284c7a01c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687676"
---
# <a name="resource-parameters"></a><span data-ttu-id="93bd8-103">Parámetros de recursos</span><span class="sxs-lookup"><span data-stu-id="93bd8-103">Resource Parameters</span></span>


<span data-ttu-id="93bd8-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="93bd8-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="resource-parameters"></a><span data-ttu-id="93bd8-105">Parámetros de recursos</span><span class="sxs-lookup"><span data-stu-id="93bd8-105">Resource Parameters</span></span>

<span data-ttu-id="93bd8-106">Este tema contiene los parámetros que se usan para los recursos.</span><span class="sxs-lookup"><span data-stu-id="93bd8-106">This topic contains parameters that are used for resources.</span></span>

<span data-ttu-id="93bd8-107">*JET_paramCachedClosedTables*</span><span class="sxs-lookup"><span data-stu-id="93bd8-107">*JET_paramCachedClosedTables*</span></span>  
<span data-ttu-id="93bd8-108">125</span><span class="sxs-lookup"><span data-stu-id="93bd8-108">125</span></span>  

<span data-ttu-id="93bd8-109">Este parámetro controla el número de recursos de árbol B + almacenados en memoria caché por la instancia de después de que la aplicación haya cerrado las tablas que representan.</span><span class="sxs-lookup"><span data-stu-id="93bd8-109">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span>

<span data-ttu-id="93bd8-110">Los valores grandes de este parámetro harán que el motor de base de datos use más memoria, pero aumentará la velocidad con la que la aplicación puede abrir aleatoriamente un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="93bd8-110">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="93bd8-111">Esto resulta útil para las aplicaciones que tienen un esquema con un gran número de tablas.</span><span class="sxs-lookup"><span data-stu-id="93bd8-111">This is useful for applications that have a schema with a very large number of tables.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-112">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-112">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-113">64</span><span class="sxs-lookup"><span data-stu-id="93bd8-113">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-114">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-114">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-115">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-115">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-116">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-116">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-117">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-117">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-118">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-118">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-119">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-119">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-120">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-120">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-121">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-121">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-122">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-122">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-123">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-123">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-124">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-124">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-125">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-126">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-126">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-127">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-127">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-128">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-128">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-129">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-129">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-130">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-130">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-131">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-131">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-132">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-132">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-133">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-133">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-134">*JET_paramDisablePerfmon*</span><span class="sxs-lookup"><span data-stu-id="93bd8-134">*JET_paramDisablePerfmon*</span></span>  
<span data-ttu-id="93bd8-135">107</span><span class="sxs-lookup"><span data-stu-id="93bd8-135">107</span></span>  

<span data-ttu-id="93bd8-136">Este parámetro se puede utilizar para evitar que el motor de base de datos publique datos sobre su rendimiento en Windows.</span><span class="sxs-lookup"><span data-stu-id="93bd8-136">This parameter can be used to prevent the database engine from publishing data about its performance to Windows.</span></span> <span data-ttu-id="93bd8-137">Esto se puede hacer para reducir la actividad de subprocesos de servicio del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="93bd8-137">This can be done to reduce the service thread activity of the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-138">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-138">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-139">False</span><span class="sxs-lookup"><span data-stu-id="93bd8-139">False</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-140">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-140">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-141">Boolean</span><span class="sxs-lookup"><span data-stu-id="93bd8-141">Boolean</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-142">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-142">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-143">False, True</span><span class="sxs-lookup"><span data-stu-id="93bd8-143">False, True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-144">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-144">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-145">Global</span><span class="sxs-lookup"><span data-stu-id="93bd8-145">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-146">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-146">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-147">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-147">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-148">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-148">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-149">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-149">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-150">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-150">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-151">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-151">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-152">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-152">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-153">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-153">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-154">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-154">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-155">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-155">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-156">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-156">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-157">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-157">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-158">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-158">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-159">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-159">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-160">*JET_paramGlobalMinVerPages*</span><span class="sxs-lookup"><span data-stu-id="93bd8-160">*JET_paramGlobalMinVerPages*</span></span>  
<span data-ttu-id="93bd8-161">81</span><span class="sxs-lookup"><span data-stu-id="93bd8-161">81</span></span>  

<span data-ttu-id="93bd8-162">Este parámetro permite que las aplicaciones que operan en modo de varias instancias realicen previamente la asignación de memoria para las páginas de versión de un grupo global con el fin de emular el comportamiento anterior.</span><span class="sxs-lookup"><span data-stu-id="93bd8-162">This parameter allows applications that operate in multi-instance mode to pre-allocate memory for version pages in a global pool to emulate the older behavior.</span></span> <span data-ttu-id="93bd8-163">Esto resulta útil en caso de que la aplicación quiera garantizar que las transacciones de un determinado tamaño puedan tener éxito más adelante aunque la memoria se vuelva insuficiente.</span><span class="sxs-lookup"><span data-stu-id="93bd8-163">This is useful in case the application wishes to guarantee that transactions of a certain size can succeed later on even if memory becomes scarce.</span></span>

<span data-ttu-id="93bd8-164">**Windows 2000:**  La memoria suficiente para volver a todas las páginas de la versión siempre se reserva en el momento de [JetInit](./jetinit-function.md) .</span><span class="sxs-lookup"><span data-stu-id="93bd8-164">**Windows 2000:**  Enough memory to back all version pages is always reserved at [JetInit](./jetinit-function.md) time.</span></span>

<span data-ttu-id="93bd8-165">**Windows XP:**  A partir de Windows XP, esto sigue siendo true cuando se encuentra en modo de instancia única.</span><span class="sxs-lookup"><span data-stu-id="93bd8-165">**Windows XP:**  As of Windows XP, this is still true when in single instance mode.</span></span> <span data-ttu-id="93bd8-166">Sin embargo, la memoria de la página de la versión se asigna dinámicamente cuando se está en modo de varias instancias.</span><span class="sxs-lookup"><span data-stu-id="93bd8-166">However, version page memory is dynamically allocated when in multi-instance mode.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-167">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-167">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-168">64</span><span class="sxs-lookup"><span data-stu-id="93bd8-168">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-169">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-170">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-171">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-172">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-172">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-173">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-173">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-174">Global</span><span class="sxs-lookup"><span data-stu-id="93bd8-174">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-175">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-175">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-176">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-176">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-177">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-177">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-178">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-178">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-179">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-179">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-180">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-180">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-181">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-181">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-182">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-182">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-183">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-183">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-184">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-184">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-185">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-185">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-186">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-186">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-187">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-187">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-188">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-188">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-189">*JET_paramMaxCursors*</span><span class="sxs-lookup"><span data-stu-id="93bd8-189">*JET_paramMaxCursors*</span></span>  
<span data-ttu-id="93bd8-190">8</span><span class="sxs-lookup"><span data-stu-id="93bd8-190">8</span></span>  

<span data-ttu-id="93bd8-191">Este parámetro reserva el número solicitado de recursos de cursor para su uso por parte de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="93bd8-191">This parameter reserves the requested number of cursor resources for use by an instance.</span></span> <span data-ttu-id="93bd8-192">Un recurso cursor se corresponde directamente con un tipo de datos [JET_TABLEID](./jet-tableid.md) .</span><span class="sxs-lookup"><span data-stu-id="93bd8-192">A cursor resource directly corresponds to a [JET_TABLEID](./jet-tableid.md) data type.</span></span> <span data-ttu-id="93bd8-193">Este valor afectará al número de cursores que se pueden usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="93bd8-193">This setting will affect how many cursors can be used at the same time.</span></span> <span data-ttu-id="93bd8-194">Un recurso de cursor no puede compartirse por sesiones diferentes, por lo que este parámetro debe establecerse en un valor suficientemente grande para que cada sesión pueda usar tantos cursores como sean necesarios.</span><span class="sxs-lookup"><span data-stu-id="93bd8-194">A cursor resource cannot be shared by different sessions so this parameter must be set to a large enough value so that each session can use as many cursors as are required.</span></span>

<span data-ttu-id="93bd8-195">**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="93bd8-195">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-196">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-196">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-197">1024</span><span class="sxs-lookup"><span data-stu-id="93bd8-197">1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-198">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-198">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-199">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-199">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-200">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-200">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-201">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-201">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-202">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-202">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-203">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-203">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-204">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-204">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-205">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-205">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-206">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-206">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-207">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-207">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-208">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-208">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-209">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-209">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-210">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-210">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-211">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-211">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-212">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-212">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-213">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-213">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-214">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-214">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-215">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-215">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-216">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-216">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-217">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-217">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-218">*JET_paramMaxInstances*</span><span class="sxs-lookup"><span data-stu-id="93bd8-218">*JET_paramMaxInstances*</span></span>  
<span data-ttu-id="93bd8-219">104</span><span class="sxs-lookup"><span data-stu-id="93bd8-219">104</span></span>  

<span data-ttu-id="93bd8-220">Este parámetro controla el número máximo de instancias que se pueden crear en un único proceso.</span><span class="sxs-lookup"><span data-stu-id="93bd8-220">This parameter controls the maximum number of instances that can be created in a single process.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-221">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-221">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-222">16</span><span class="sxs-lookup"><span data-stu-id="93bd8-222">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-223">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-223">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-224">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-224">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-225">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-225">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-226">1-1024</span><span class="sxs-lookup"><span data-stu-id="93bd8-226">1-1024</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-227">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-227">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-228">Global</span><span class="sxs-lookup"><span data-stu-id="93bd8-228">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-229">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-229">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-230">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-230">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-231">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-231">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-232">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-232">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-233">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-233">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-234">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-234">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-235">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-235">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-236">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-236">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-237">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-237">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-238">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-238">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-239">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-239">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-240">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-240">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-241">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-241">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-242">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-242">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-243">*JET_paramMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="93bd8-243">*JET_paramMaxOpenTables*</span></span>  
<span data-ttu-id="93bd8-244">6</span><span class="sxs-lookup"><span data-stu-id="93bd8-244">6</span></span>  

<span data-ttu-id="93bd8-245">Este parámetro reserva el número solicitado de recursos de árbol B + para su uso por parte de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="93bd8-245">This parameter reserves the requested number of B+ Tree resources for use by an instance.</span></span> <span data-ttu-id="93bd8-246">Este valor afectará al número de tablas que se pueden usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="93bd8-246">This setting will affect how many tables can be used at the same time.</span></span> <span data-ttu-id="93bd8-247">Este parámetro debe establecerse en relación con el esquema físico de las bases de datos que usa el motor de base de datos, por lo que esta configuración no es tan sencilla como podría ser.</span><span class="sxs-lookup"><span data-stu-id="93bd8-247">This parameter needs to be set relative to the physical schema of the databases in use by the database engine, so this setting is not as straightforward as it could be.</span></span>

<span data-ttu-id="93bd8-248">En general, necesitará dos recursos más un recurso por cada índice secundario por tabla en uso simultáneo por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="93bd8-248">In general, you will need two resources plus one resource per secondary index per table in concurrent use by the application.</span></span>

<span data-ttu-id="93bd8-249">**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="93bd8-249">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-250">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-250">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-251">300</span><span class="sxs-lookup"><span data-stu-id="93bd8-251">300</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-252">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-252">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-253">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-253">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-254">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-254">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-255">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-255">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-256">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-256">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-257">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-257">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-258">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-258">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-259">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-259">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-260">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-260">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-261">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-261">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-262">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-262">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-263">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-263">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-264">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-264">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-265">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-265">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-266">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-266">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-267">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-267">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-268">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-268">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-269">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-269">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-270">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-270">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-271">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-271">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-272">*JET_paramMaxSessions*</span><span class="sxs-lookup"><span data-stu-id="93bd8-272">*JET_paramMaxSessions*</span></span>  
<span data-ttu-id="93bd8-273">5</span><span class="sxs-lookup"><span data-stu-id="93bd8-273">5</span></span>  

<span data-ttu-id="93bd8-274">Este parámetro reserva el número solicitado de recursos de sesión para su uso por parte de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="93bd8-274">This parameter reserves the requested number of session resources for use by an instance.</span></span> <span data-ttu-id="93bd8-275">Un recurso de sesión se corresponde directamente con un tipo de datos [JET_SESID](./jet-sesid.md) .</span><span class="sxs-lookup"><span data-stu-id="93bd8-275">A session resource directly corresponds to a [JET_SESID](./jet-sesid.md) data type.</span></span> <span data-ttu-id="93bd8-276">Esta configuración afectará a la cantidad de sesiones que se pueden usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="93bd8-276">This setting will affect how many sessions can be used at the same time.</span></span>

<span data-ttu-id="93bd8-277">**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="93bd8-277">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-278">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-278">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-279">16</span><span class="sxs-lookup"><span data-stu-id="93bd8-279">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-280">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-280">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-281">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-281">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-282">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-282">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-283">de 0 a 30000</span><span class="sxs-lookup"><span data-stu-id="93bd8-283">0 – 30000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-284">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-284">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-285">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-285">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-286">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-286">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-287">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-287">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-288">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-288">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-289">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-289">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-290">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-290">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-291">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-291">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-292">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-292">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-293">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-293">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-294">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-294">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-295">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-295">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-296">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-296">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-297">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-297">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-298">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-298">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-299">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-299">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-300">*JET_paramMaxTemporaryTables*</span><span class="sxs-lookup"><span data-stu-id="93bd8-300">*JET_paramMaxTemporaryTables*</span></span>  
<span data-ttu-id="93bd8-301">10</span><span class="sxs-lookup"><span data-stu-id="93bd8-301">10</span></span>  

<span data-ttu-id="93bd8-302">Este parámetro reserva el número solicitado de recursos de tabla temporal para su uso por parte de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="93bd8-302">This parameter reserves the requested number of temporary table resources for use by an instance.</span></span> <span data-ttu-id="93bd8-303">Esta configuración afectará al número de tablas temporales que se pueden usar al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="93bd8-303">This setting will affect how many temporary tables can be used at the same time.</span></span>

<span data-ttu-id="93bd8-304">**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="93bd8-304">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="93bd8-305">**Windows XP y versiones posteriores:**  Si este parámetro del sistema se establece en cero, no se creará ninguna base de datos temporal y se producirá un error en cualquier actividad que requiera el uso de la base de datos temporal.</span><span class="sxs-lookup"><span data-stu-id="93bd8-305">**Windows XP and later:**  If this system parameter is set to zero then no temporary database will be created and any activity that requires use of the temporary database will fail.</span></span> <span data-ttu-id="93bd8-306">Esta configuración puede ser útil para evitar la e/s necesaria para crear la base de datos temporal si se sabe que no se va a usar.</span><span class="sxs-lookup"><span data-stu-id="93bd8-306">This setting can be useful to avoid the I/O required to create the temporary database if it is known that it will not be used.</span></span>

<span data-ttu-id="93bd8-307">**Nota:**  El uso de una tabla temporal también requiere un recurso de cursor.</span><span class="sxs-lookup"><span data-stu-id="93bd8-307">**Note**  The use of a temporary table also requires a cursor resource.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-308">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-308">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-309">20</span><span class="sxs-lookup"><span data-stu-id="93bd8-309">20</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-310">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-310">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-311">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-311">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-312">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-312">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-313">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-313">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-314">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-314">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-315">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-315">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-316">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-316">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-317">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-317">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-318">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-318">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-319">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-319">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-320">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-320">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-321">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-321">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-322">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-322">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-323">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-323">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-324">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-324">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-325">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-325">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-326">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-326">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-327">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-327">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-328">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-328">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-329">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-329">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-330">*JET_paramMaxVerPages*</span><span class="sxs-lookup"><span data-stu-id="93bd8-330">*JET_paramMaxVerPages*</span></span>  
<span data-ttu-id="93bd8-331">9</span><span class="sxs-lookup"><span data-stu-id="93bd8-331">9</span></span>  

<span data-ttu-id="93bd8-332">Este parámetro reserva el número solicitado de páginas del almacén de versiones para su uso por parte de una instancia de.</span><span class="sxs-lookup"><span data-stu-id="93bd8-332">This parameter reserves the requested number of version store pages for use by an instance.</span></span> <span data-ttu-id="93bd8-333">El almacén de versiones contiene un registro en directo de todas las versiones de cada entrada de registro o índice de la base de datos que pueden verse en todas las transacciones activas.</span><span class="sxs-lookup"><span data-stu-id="93bd8-333">The version store holds a live record of all the different versions of each record or index entry in the database that can be seen by all active transactions.</span></span> <span data-ttu-id="93bd8-334">Estas versiones se utilizan para admitir el control de simultaneidad con varias versiones que usa el motor de base de datos para admitir transacciones que usan el aislamiento de instantánea.</span><span class="sxs-lookup"><span data-stu-id="93bd8-334">These versions are used to support the multi-versioned concurrency control in use by the database engine to support transactions using snapshot isolation.</span></span> <span data-ttu-id="93bd8-335">Este valor afectará al número de actualizaciones que se pueden conservar en la memoria a la vez.</span><span class="sxs-lookup"><span data-stu-id="93bd8-335">This setting will affect how many updates can be held in memory at a time.</span></span> <span data-ttu-id="93bd8-336">Esto, a su vez, afecta al número máximo de actualizaciones que puede realizar una única transacción, la duración máxima de una transacción abierta, la carga máxima simultánea de transacciones de actualización en el sistema o una combinación de estas.</span><span class="sxs-lookup"><span data-stu-id="93bd8-336">This in turn will affect either the maximum number of updates a single transaction can perform, the maximum duration a transaction can be held open, the maximum concurrent load of updating transactions on the system, or a combination of these.</span></span>

<span data-ttu-id="93bd8-337">Cada página del almacén de versiones tal como la configura este parámetro tiene 16 KB de tamaño en los equipos de 32 bits y 32 KB en los equipos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="93bd8-337">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="93bd8-338">**Windows Vista y versiones posteriores:**  El tamaño de la página del almacén de versiones se puede leer y cambiar mediante JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="93bd8-338">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="93bd8-339">**Windows 2000, Windows XP y Windows Server 2003:**  Los valores grandes de este parámetro utilizarán el espacio de direcciones y pueden aumentar el uso de memoria.</span><span class="sxs-lookup"><span data-stu-id="93bd8-339">**Windows 2000, Windows XP and Windows Server 2003:**  Large values for this parameter will consume address space and may increase memory usage.</span></span>

<span data-ttu-id="93bd8-340">**Nota:**  Este es el recurso más común que el motor de base de datos debe agotar.</span><span class="sxs-lookup"><span data-stu-id="93bd8-340">**Note**  This is by far the most common resource to be exhausted by the database engine.</span></span> <span data-ttu-id="93bd8-341">Se debe prestar especial atención a la configuración del parámetro del sistema y a la carga transaccional de la aplicación para evitar agotar este recurso en el funcionamiento normal.</span><span class="sxs-lookup"><span data-stu-id="93bd8-341">Careful attention must be paid to the setting of the system parameter and to the transactional load of the application to avoid exhausting this resource under normal operation.</span></span> <span data-ttu-id="93bd8-342">Cuando se agote este recurso, las actualizaciones de la base de datos se rechazarán con JET_errVersionStoreOutOfMemory.</span><span class="sxs-lookup"><span data-stu-id="93bd8-342">When this resource is exhausted, updates to the database will be rejected with JET_errVersionStoreOutOfMemory.</span></span> <span data-ttu-id="93bd8-343">Para liberar algunos de estos recursos, se debe anular la transacción pendiente más antigua.</span><span class="sxs-lookup"><span data-stu-id="93bd8-343">To release some of these resources, the oldest outstanding transaction must be aborted.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-344">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-344">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-345">64</span><span class="sxs-lookup"><span data-stu-id="93bd8-345">64</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-346">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-346">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-347">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-347">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-348">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-348">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-349">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-349">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-350">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-350">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-351">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-351">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-352">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-352">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-353">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-353">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-354">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-354">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-355">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-355">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-356">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-356">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-357">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-357">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-358">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-358">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-359">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-359">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-360">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-360">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-361">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-361">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-362">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-362">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-363">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-363">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-364">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-364">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-365">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-365">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-366">*JET_paramPageHintCacheSize*</span><span class="sxs-lookup"><span data-stu-id="93bd8-366">*JET_paramPageHintCacheSize*</span></span>  
<span data-ttu-id="93bd8-367">101</span><span class="sxs-lookup"><span data-stu-id="93bd8-367">101</span></span>  

<span data-ttu-id="93bd8-368">Este parámetro controla el tamaño de una memoria caché especial que se usa para acelerar la búsqueda de punteros de página secundaria de B + árbol en la caché de páginas de base de datos.</span><span class="sxs-lookup"><span data-stu-id="93bd8-368">This parameter controls the size of a special cache used to accelerate the lookup of B+ Tree child page pointers in the database page cache.</span></span> <span data-ttu-id="93bd8-369">El tamaño de la memoria caché está en bytes.</span><span class="sxs-lookup"><span data-stu-id="93bd8-369">The size of the cache is in bytes.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-370">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-370">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-371">262 144</span><span class="sxs-lookup"><span data-stu-id="93bd8-371">262144</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-372">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-372">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-373">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-373">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-374">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-374">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-375">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-375">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-376">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-376">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-377">Global</span><span class="sxs-lookup"><span data-stu-id="93bd8-377">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-378">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-378">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-379">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-379">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-380">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-380">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-381">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-381">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-382">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-382">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-383">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-383">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-384">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-384">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-385">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-385">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-386">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-386">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-387">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-387">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-388">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-388">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-389">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-389">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-390">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-390">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-391">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-391">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-392">*JET_paramPreferredMaxOpenTables*</span><span class="sxs-lookup"><span data-stu-id="93bd8-392">*JET_paramPreferredMaxOpenTables*</span></span>  
<span data-ttu-id="93bd8-393">7</span><span class="sxs-lookup"><span data-stu-id="93bd8-393">7</span></span>  

<span data-ttu-id="93bd8-394">Este parámetro intenta mantener el número de recursos de árbol B + en uso por debajo del umbral especificado.</span><span class="sxs-lookup"><span data-stu-id="93bd8-394">This parameter attempts to keep the number of B+ Tree resources in use below the specified threshold.</span></span>

<span data-ttu-id="93bd8-395">Si este parámetro se establece en cero, el valor predeterminado será 100% de **JET_paramMaxOpenTables**.</span><span class="sxs-lookup"><span data-stu-id="93bd8-395">If this parameter is set to zero then it will default to 100% of **JET_paramMaxOpenTables**.</span></span>

<span data-ttu-id="93bd8-396">**Windows Vista y versiones posteriores:**  Este parámetro está obsoleto y no afecta al funcionamiento del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="93bd8-396">**Windows Vista and later:**  This parameter is obsolete and does not affect the operation of the database engine.</span></span> <span data-ttu-id="93bd8-397">Las aplicaciones deben usar JET_paramMaxCachedClosedTables en su lugar.</span><span class="sxs-lookup"><span data-stu-id="93bd8-397">Applications should use JET_paramMaxCachedClosedTables instead.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-398">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-398">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-399">0 (100% de <strong>JET_paramMaxOpenTables</strong>)</span><span class="sxs-lookup"><span data-stu-id="93bd8-399">0 (100% of <strong>JET_paramMaxOpenTables</strong>)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-400">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-400">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-401">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-401">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-402">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-402">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-403">de 0 a 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-403">0 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-404">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-404">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-405">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-405">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-406">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-406">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-407">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-407">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-408">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-408">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-409">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-409">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-410">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-410">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-411">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-411">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-412">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-412">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-413">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-413">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-414">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-414">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-415">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-415">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-416">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-416">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-417">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-417">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-418">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-418">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-419">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-419">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-420">*JET_paramPreferredVerPages*</span><span class="sxs-lookup"><span data-stu-id="93bd8-420">*JET_paramPreferredVerPages*</span></span>  
<span data-ttu-id="93bd8-421">63</span><span class="sxs-lookup"><span data-stu-id="93bd8-421">63</span></span>  

<span data-ttu-id="93bd8-422">Este parámetro representa un umbral relativo a **JET_paramMaxVerPages** que controla el uso discrecional de páginas de versión por parte del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="93bd8-422">This parameter represents a threshold relative to **JET_paramMaxVerPages** that controls the discretionary use of version pages by the database engine.</span></span> <span data-ttu-id="93bd8-423">Si el tamaño del almacén de versiones supera este umbral, cualquier información que solo se use para tareas en segundo plano opcionales, como la recuperación del espacio eliminado en la base de datos, se sacrifica en su lugar para conservar el espacio para la información transaccional.</span><span class="sxs-lookup"><span data-stu-id="93bd8-423">If the size of the version store exceeds this threshold then any information that is only used for optional background tasks, such as reclaiming deleted space in the database, is instead sacrificed to preserve room for transactional information.</span></span>

<span data-ttu-id="93bd8-424">**Windows 2000, Windows XP y Windows Server 2003:**  Si se establece este parámetro en cero, el umbral se establecerá en el 90% de **JET_paramMaxVerPages**.</span><span class="sxs-lookup"><span data-stu-id="93bd8-424">**Windows 2000, Windows XP and Windows Server 2003:**  Setting this parameter to zero would set the threshold to be 90% of **JET_paramMaxVerPages**.</span></span>

<span data-ttu-id="93bd8-425">**Windows Vista y versiones posteriores:**  Ya no se admite y el valor predeterminado de este parámetro se ha cambiado para aclarar su comportamiento.</span><span class="sxs-lookup"><span data-stu-id="93bd8-425">**Windows Vista and later:**  This is no longer supported and the default value of this parameter was changed to clarify its behavior.</span></span>

<span data-ttu-id="93bd8-426">Cada página del almacén de versiones tal como la configura este parámetro tiene 16 KB de tamaño en los equipos de 32 bits y 32 KB en los equipos de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="93bd8-426">Each version store page as configured by this parameter is 16KB in size on 32-bit machines, and 32KB on 64-bit machines.</span></span>

<span data-ttu-id="93bd8-427">**Windows Vista y versiones posteriores:**  El tamaño de la página del almacén de versiones se puede leer y cambiar mediante JET_paramVerPageSize.</span><span class="sxs-lookup"><span data-stu-id="93bd8-427">**Windows Vista and later:**  The version store page size can be read and changed via JET_paramVerPageSize.</span></span>

<span data-ttu-id="93bd8-428">**Nota:**  Si el motor de base de datos funciona por encima de este umbral con demasiada frecuencia, es posible que la base de datos se reduzca el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="93bd8-428">**Note**  If the database engine operates above this threshold too often then it is possible for the database to degrade in performance.</span></span> <span data-ttu-id="93bd8-429">Esto sucede porque los procesos en segundo plano que limpian la base de datos no pueden funcionar sin la información opcional que se produce en este escenario.</span><span class="sxs-lookup"><span data-stu-id="93bd8-429">This happens because the background processes that clean up the database cannot function without the optional information that is thrown away in this scenario.</span></span> <span data-ttu-id="93bd8-430">La desfragmentación en línea o sin conexión contrarresta este efecto.</span><span class="sxs-lookup"><span data-stu-id="93bd8-430">Online or offline defragmentation will counteract this effect.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-431">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-431">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-432"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  0 (90% de JET_paramMaxVerPages)</span><span class="sxs-lookup"><span data-stu-id="93bd8-432"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 (90% of JET_paramMaxVerPages)</span></span></p>
<p><span data-ttu-id="93bd8-433"><strong>Windows Vista:</strong>  58</span><span class="sxs-lookup"><span data-stu-id="93bd8-433"><strong>Windows Vista:</strong>  58</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-434">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-434">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-435">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-435">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-436">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-436">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-437">1 – 2147483647</span><span class="sxs-lookup"><span data-stu-id="93bd8-437">1 – 2147483647</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-438">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-438">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-439">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-439">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-440">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-440">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-441">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-441">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-442">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-442">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-443">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-443">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-444">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-444">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-445">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-445">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-446">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-446">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-447">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-447">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-448">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-448">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-449">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-449">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-450">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-450">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-451">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-451">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-452">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-452">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-453">All</span><span class="sxs-lookup"><span data-stu-id="93bd8-453">All</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-454">*JET_paramVerPageSize*</span><span class="sxs-lookup"><span data-stu-id="93bd8-454">*JET_paramVerPageSize*</span></span>  
<span data-ttu-id="93bd8-455">128</span><span class="sxs-lookup"><span data-stu-id="93bd8-455">128</span></span>  

<span data-ttu-id="93bd8-456">Este parámetro controla el tamaño de las páginas del almacén de versiones utilizadas por el motor de base de datos para contener información transaccional.</span><span class="sxs-lookup"><span data-stu-id="93bd8-456">This parameter controls the size of the version store pages used by the database engine to hold transactional information.</span></span> <span data-ttu-id="93bd8-457">El valor de este parámetro es el tamaño de la unidad para todos los demás parámetros del sistema que se encuentran en términos de páginas de versión (por ejemplo, JET_paramMaxVerPages).</span><span class="sxs-lookup"><span data-stu-id="93bd8-457">The value of this parameter is the unit size for all the other system parameters that are in terms of version pages (e.g. JET_paramMaxVerPages).</span></span>

<span data-ttu-id="93bd8-458">El motor de base de datos puede optar por usar un tamaño de página del almacén de versiones mayor que el solicitado.</span><span class="sxs-lookup"><span data-stu-id="93bd8-458">The database engine may choose to use a larger version store page size than requested.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-459">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-459">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-460">16384</span><span class="sxs-lookup"><span data-stu-id="93bd8-460">16384</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-461">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-461">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-462">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-462">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-463">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-463">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span><span class="sxs-lookup"><span data-stu-id="93bd8-464">1024, 2048, 4096, 8192, 16384, 32768, 65536</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-465">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-465">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-466">Global</span><span class="sxs-lookup"><span data-stu-id="93bd8-466">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-467">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-467">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-468">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-468">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-469">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-469">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-470">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-470">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-471">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-471">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-472">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-472">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-473">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-473">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-474">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-474">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-475">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-475">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-476">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-476">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-477">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-477">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-478">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-478">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-479">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-479">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-480">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-480">Windows Vista and later</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="93bd8-481">*JET_paramVersionStoreTaskQueueMax*</span><span class="sxs-lookup"><span data-stu-id="93bd8-481">*JET_paramVersionStoreTaskQueueMax*</span></span>  
<span data-ttu-id="93bd8-482">105</span><span class="sxs-lookup"><span data-stu-id="93bd8-482">105</span></span>  

<span data-ttu-id="93bd8-483">Este parámetro controla el número de elementos de trabajo de limpieza en segundo plano que se pueden poner en cola en el grupo de subprocesos del motor de base de datos al mismo tiempo.</span><span class="sxs-lookup"><span data-stu-id="93bd8-483">This parameter controls the number of background cleanup work items that can be queued to the database engine thread pool at any one time.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-484">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="93bd8-484">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-485">32</span><span class="sxs-lookup"><span data-stu-id="93bd8-485">32</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-486">Escriba:</span><span class="sxs-lookup"><span data-stu-id="93bd8-486">Type:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-487">Entero</span><span class="sxs-lookup"><span data-stu-id="93bd8-487">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-488">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="93bd8-488">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-489"><strong>Windows XP y Windows Server 2003:  </strong>  1 – 63</span><span class="sxs-lookup"><span data-stu-id="93bd8-489"><strong>Windows XP and Windows Server 2003:  </strong>  1 – 63</span></span></p>
<p><span data-ttu-id="93bd8-490"><strong>Windows Vista:</strong>  1 – 127</span><span class="sxs-lookup"><span data-stu-id="93bd8-490"><strong>Windows Vista:</strong>  1 – 127</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-491">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="93bd8-491">Scope:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-492">Instancia</span><span class="sxs-lookup"><span data-stu-id="93bd8-492">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-493">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-493">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-494">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-494">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-495">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="93bd8-495">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-496"><strong>Windows XP y Windows Server 2003:  </strong>  No</span><span class="sxs-lookup"><span data-stu-id="93bd8-496"><strong>Windows XP and Windows Server 2003:  </strong>  No</span></span></p>
<p><span data-ttu-id="93bd8-497"><strong>Windows Vista:</strong>  ?</span><span class="sxs-lookup"><span data-stu-id="93bd8-497"><strong>Windows Vista:</strong>  Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-498">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="93bd8-498">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-499">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-499">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-500">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-500">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-501">No</span><span class="sxs-lookup"><span data-stu-id="93bd8-501">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-502">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="93bd8-502">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-503">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-503">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-504">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="93bd8-504">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-505">Sí</span><span class="sxs-lookup"><span data-stu-id="93bd8-505">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-506">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="93bd8-506">Availability:</span></span></p></td>
<td><p><span data-ttu-id="93bd8-507">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="93bd8-507">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="93bd8-508">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93bd8-508">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-509"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="93bd8-509"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="93bd8-510">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="93bd8-510">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93bd8-511"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="93bd8-511"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="93bd8-512">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="93bd8-512">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93bd8-513"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="93bd8-513"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="93bd8-514">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="93bd8-514">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="93bd8-515">Consulte también</span><span class="sxs-lookup"><span data-stu-id="93bd8-515">See Also</span></span>

[<span data-ttu-id="93bd8-516">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="93bd8-516">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="93bd8-517">JetInit</span><span class="sxs-lookup"><span data-stu-id="93bd8-517">JetInit</span></span>](./jetinit-function.md)
