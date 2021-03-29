---
description: 'Más información acerca de: parámetros informativos'
title: Parámetros informativos
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: a8923b544726e474775684f54fed47d8b4ba281e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811138"
---
# <a name="informational-parameters"></a><span data-ttu-id="22c5f-103">Parámetros informativos</span><span class="sxs-lookup"><span data-stu-id="22c5f-103">Informational Parameters</span></span>


<span data-ttu-id="22c5f-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="22c5f-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="informational-parameters"></a><span data-ttu-id="22c5f-105">Parámetros informativos</span><span class="sxs-lookup"><span data-stu-id="22c5f-105">Informational Parameters</span></span>

<span data-ttu-id="22c5f-106">Este tema contiene los parámetros que se utilizan para exponer información sobre el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="22c5f-106">This topic contains parameters that are used to expose information about the database engine.</span></span>

<span data-ttu-id="22c5f-107">*JET_paramKeyMost*</span><span class="sxs-lookup"><span data-stu-id="22c5f-107">*JET_paramKeyMost*</span></span>  
<span data-ttu-id="22c5f-108">134</span><span class="sxs-lookup"><span data-stu-id="22c5f-108">134</span></span>  

<span data-ttu-id="22c5f-109">Este parámetro de solo lectura indica la longitud máxima permitida de la clave de índice que se puede seleccionar para el tamaño de página de la base de datos actual (tal y como se configura mediante JET_paramDatabasePageSize).</span><span class="sxs-lookup"><span data-stu-id="22c5f-109">This read-only parameter indicates the maximum allowable index key length that can be selected for the current database page size (as configured by JET_paramDatabasePageSize).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-110">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="22c5f-110">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-111">JET_cbKeyMost4KBytePage</span><span class="sxs-lookup"><span data-stu-id="22c5f-111">JET_cbKeyMost4KBytePage</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-112">Escriba:</span><span class="sxs-lookup"><span data-stu-id="22c5f-112">Type:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-113">Entero</span><span class="sxs-lookup"><span data-stu-id="22c5f-113">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-114">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="22c5f-114">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-115">255 – 65535</span><span class="sxs-lookup"><span data-stu-id="22c5f-115">255 – 65535</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-116">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="22c5f-116">Scope:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-117">Global</span><span class="sxs-lookup"><span data-stu-id="22c5f-117">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-118">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="22c5f-118">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-119">N/D</span><span class="sxs-lookup"><span data-stu-id="22c5f-119">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-120">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="22c5f-120">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-121">N/D</span><span class="sxs-lookup"><span data-stu-id="22c5f-121">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-122">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="22c5f-122">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-123">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-123">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-124">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="22c5f-124">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-125">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-125">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-126">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="22c5f-126">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-127">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-127">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-128">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="22c5f-128">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-129">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-129">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-130">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="22c5f-130">Availability:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-131">A partir de Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c5f-131">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22c5f-132">*JET_paramMaxColtyp*</span><span class="sxs-lookup"><span data-stu-id="22c5f-132">*JET_paramMaxColtyp*</span></span>  
<span data-ttu-id="22c5f-133">131</span><span class="sxs-lookup"><span data-stu-id="22c5f-133">131</span></span>  

<span data-ttu-id="22c5f-134">Este parámetro de solo lectura devuelve el [JET_COLTYP](./jet-coltyp.md) máximo (JET_coltypMax) de la versión del motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="22c5f-134">This read only parameter returns the maximum [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) for that version of the database engine.</span></span> <span data-ttu-id="22c5f-135">Este valor se puede usar para comprobar la compatibilidad de un [JET_COLTYP](./jet-coltyp.md)específico.</span><span class="sxs-lookup"><span data-stu-id="22c5f-135">This value can be used to test for support of a specific [JET_COLTYP](./jet-coltyp.md).</span></span> <span data-ttu-id="22c5f-136">Si una [JET_COLTYP](./jet-coltyp.md) determinada es menor que el valor de este parámetro, es compatible con el motor de base de datos.</span><span class="sxs-lookup"><span data-stu-id="22c5f-136">If a given [JET_COLTYP](./jet-coltyp.md) is less than the value of this parameter then it is supported by the database engine.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-137">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="22c5f-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-138">JET_coltypUnsignedShort + 1</span><span class="sxs-lookup"><span data-stu-id="22c5f-138">JET_coltypUnsignedShort + 1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-139">Escriba:</span><span class="sxs-lookup"><span data-stu-id="22c5f-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-140">Entero</span><span class="sxs-lookup"><span data-stu-id="22c5f-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-141">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="22c5f-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-142">de 0 a 255</span><span class="sxs-lookup"><span data-stu-id="22c5f-142">0 – 255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-143">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="22c5f-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-144">Global</span><span class="sxs-lookup"><span data-stu-id="22c5f-144">Global</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-145">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="22c5f-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-146">N/D</span><span class="sxs-lookup"><span data-stu-id="22c5f-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-147">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="22c5f-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-148">N/D</span><span class="sxs-lookup"><span data-stu-id="22c5f-148">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-149">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="22c5f-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-150">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-151">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="22c5f-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-152">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-153">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="22c5f-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-154">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-155">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="22c5f-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-156">No</span><span class="sxs-lookup"><span data-stu-id="22c5f-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-157">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="22c5f-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-158">A partir de Windows Server 2008 y Windows Vista</span><span class="sxs-lookup"><span data-stu-id="22c5f-158">Starting with Windows Server 2008 and Windows Vista</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="22c5f-159">*JET_paramLVChunkSizeMost*</span><span class="sxs-lookup"><span data-stu-id="22c5f-159">*JET_paramLVChunkSizeMost*</span></span>  
<span data-ttu-id="22c5f-160">163</span><span class="sxs-lookup"><span data-stu-id="22c5f-160">163</span></span>  

<span data-ttu-id="22c5f-161">Parámetro de solo lectura que devuelve el tamaño de fragmento de valor largo basado en el tamaño de página configurado.</span><span class="sxs-lookup"><span data-stu-id="22c5f-161">Read only parameter that returns the long-value chunk size based on configured page size.</span></span> <span data-ttu-id="22c5f-162">Si un valor largo se va a leer o escribir con varias llamadas a la columna jet {set, Retrieve}, el uso de un búfer cuyo tamaño sea un múltiplo del tamaño del fragmento es más eficaz.</span><span class="sxs-lookup"><span data-stu-id="22c5f-162">If a long-value is to be read or written with multiple Jet{Set,Retrieve}Column calls then using a buffer whose size is a multiple of the chunk size is more efficient.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-163">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="22c5f-163">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-164">Página de 2 KB = 1966 bytes</span><span class="sxs-lookup"><span data-stu-id="22c5f-164">2kb page = 1966 bytes</span></span><br />
<span data-ttu-id="22c5f-165">Página de 4 KB = 4014 bytes</span><span class="sxs-lookup"><span data-stu-id="22c5f-165">4kb page = 4014 bytes</span></span><br />
<span data-ttu-id="22c5f-166">8 KB página = 8110 bytes</span><span class="sxs-lookup"><span data-stu-id="22c5f-166">8kb page = 8110 bytes</span></span><br />
<span data-ttu-id="22c5f-167">Página de 16kb = 4050 bytes</span><span class="sxs-lookup"><span data-stu-id="22c5f-167">16kb page = 4050 bytes</span></span><br />
<span data-ttu-id="22c5f-168">Página de 32 KB = 8150 bytes</span><span class="sxs-lookup"><span data-stu-id="22c5f-168">32kb page = 8150 bytes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-169">Escriba:</span><span class="sxs-lookup"><span data-stu-id="22c5f-169">Type:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-170">Entero</span><span class="sxs-lookup"><span data-stu-id="22c5f-170">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-171">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="22c5f-171">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="22c5f-172">0-10000</span><span class="sxs-lookup"><span data-stu-id="22c5f-172">0-10000</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-173">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="22c5f-173">Scope:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-174">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="22c5f-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-175">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="22c5f-175">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-176">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="22c5f-176">Affects Physical Layout:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-177">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="22c5f-177">Affects Reliability:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-178">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="22c5f-178">Affects Performance:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-179">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="22c5f-179">Affects Resources:</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-180">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="22c5f-180">Availability:</span></span></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="22c5f-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="22c5f-181">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-182"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="22c5f-182"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="22c5f-183">Requiere Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="22c5f-183">Requires Windows Vista.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22c5f-184"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="22c5f-184"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="22c5f-185">Requiere Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="22c5f-185">Requires Windows Server 2008.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22c5f-186"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="22c5f-186"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="22c5f-187">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="22c5f-187">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="22c5f-188">Consulte también</span><span class="sxs-lookup"><span data-stu-id="22c5f-188">See Also</span></span>

[<span data-ttu-id="22c5f-189">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="22c5f-189">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="22c5f-190">JetInit</span><span class="sxs-lookup"><span data-stu-id="22c5f-190">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="22c5f-191">JET_COLTYP</span><span class="sxs-lookup"><span data-stu-id="22c5f-191">JET_COLTYP</span></span>](./jet-coltyp.md)
