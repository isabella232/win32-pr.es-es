---
description: 'Más información acerca de: parámetros de índice'
title: Parámetros de índice
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083410"
---
# <a name="index-parameters"></a><span data-ttu-id="89f8c-103">Parámetros de índice</span><span class="sxs-lookup"><span data-stu-id="89f8c-103">Index Parameters</span></span>


<span data-ttu-id="89f8c-104">_**Se aplica a:** Windows | Windows Server_</span><span class="sxs-lookup"><span data-stu-id="89f8c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="index-parameters"></a><span data-ttu-id="89f8c-105">Parámetros de índice</span><span class="sxs-lookup"><span data-stu-id="89f8c-105">Index Parameters</span></span>

<span data-ttu-id="89f8c-106">Este tema contiene los parámetros que se utilizan para el índice.</span><span class="sxs-lookup"><span data-stu-id="89f8c-106">This topic contains parameters that are used for the index.</span></span>

<span data-ttu-id="89f8c-107">*JET_paramIndexTupleIncrement*</span><span class="sxs-lookup"><span data-stu-id="89f8c-107">*JET_paramIndexTupleIncrement*</span></span>  
<span data-ttu-id="89f8c-108">132</span><span class="sxs-lookup"><span data-stu-id="89f8c-108">132</span></span>  

<span data-ttu-id="89f8c-109">Este parámetro especifica el valor predeterminado para el incremento de desplazamiento usado para recorrer el valor de la columna de origen mientras se genera cada tupla.</span><span class="sxs-lookup"><span data-stu-id="89f8c-109">This parameter specifies the default for the offset increment used to step through the source column value while generating each tuple.</span></span> <span data-ttu-id="89f8c-110">Para obtener más información, vea la estructura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89f8c-110">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-111">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="89f8c-111">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-112">1</span><span class="sxs-lookup"><span data-stu-id="89f8c-112">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-113">Escriba:</span><span class="sxs-lookup"><span data-stu-id="89f8c-113">Type:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-114">Entero</span><span class="sxs-lookup"><span data-stu-id="89f8c-114">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-115">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="89f8c-115">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-116">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="89f8c-116">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-117">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="89f8c-117">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-118">Instancia</span><span class="sxs-lookup"><span data-stu-id="89f8c-118">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-119">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-119">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-120">Sí</span><span class="sxs-lookup"><span data-stu-id="89f8c-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-121">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-121">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-122">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-122">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-123">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="89f8c-123">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-124">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-124">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-125">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-125">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-126">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-127">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="89f8c-127">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-128">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-128">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-129">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="89f8c-129">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-130">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-130">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-131">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-131">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-132">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="89f8c-132">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89f8c-133">*JET_paramIndexTupleStart*</span><span class="sxs-lookup"><span data-stu-id="89f8c-133">*JET_paramIndexTupleStart*</span></span>  
<span data-ttu-id="89f8c-134">133</span><span class="sxs-lookup"><span data-stu-id="89f8c-134">133</span></span>  

<span data-ttu-id="89f8c-135">Este parámetro especifica el valor predeterminado para el desplazamiento en el valor de la columna de origen en el que se iniciará la generación de tupla.</span><span class="sxs-lookup"><span data-stu-id="89f8c-135">This parameter specifies the default for the offset in the source column value at which tuple generation will start.</span></span> <span data-ttu-id="89f8c-136">Para obtener más información, vea la estructura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89f8c-136">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-137">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="89f8c-137">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-138">0</span><span class="sxs-lookup"><span data-stu-id="89f8c-138">0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-139">Escriba:</span><span class="sxs-lookup"><span data-stu-id="89f8c-139">Type:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-140">Entero</span><span class="sxs-lookup"><span data-stu-id="89f8c-140">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-141">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="89f8c-141">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-142">0 - 32767</span><span class="sxs-lookup"><span data-stu-id="89f8c-142">0 - 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-143">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="89f8c-143">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-144">Instancia</span><span class="sxs-lookup"><span data-stu-id="89f8c-144">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-145">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-145">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-146">Sí</span><span class="sxs-lookup"><span data-stu-id="89f8c-146">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-147">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-147">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-148">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-148">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-149">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="89f8c-149">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-150">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-150">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-151">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-151">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-152">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-152">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-153">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="89f8c-153">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-154">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-154">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-155">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="89f8c-155">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-156">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-156">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-157">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-157">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-158">Windows Vista y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="89f8c-158">Windows Vista and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89f8c-159">*JET_paramIndexTuplesLengthMax*</span><span class="sxs-lookup"><span data-stu-id="89f8c-159">*JET_paramIndexTuplesLengthMax*</span></span>  
<span data-ttu-id="89f8c-160">111</span><span class="sxs-lookup"><span data-stu-id="89f8c-160">111</span></span>  

<span data-ttu-id="89f8c-161">Este parámetro especifica el valor predeterminado para la longitud máxima de tupla en un índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="89f8c-161">This parameter specifies the default for the maximum tuple length in a tuple index.</span></span> <span data-ttu-id="89f8c-162">Para obtener más información, vea la estructura [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) .</span><span class="sxs-lookup"><span data-stu-id="89f8c-162">For more information, see the [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) structure.</span></span>

<span data-ttu-id="89f8c-163">**Windows Vista:**  Antes de Windows Vista, si se establece este parámetro en cero, se volverá a establecer en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="89f8c-163">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="89f8c-164">Para Windows Vista, ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="89f8c-164">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-165">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="89f8c-165">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-166">10</span><span class="sxs-lookup"><span data-stu-id="89f8c-166">10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-167">Escriba:</span><span class="sxs-lookup"><span data-stu-id="89f8c-167">Type:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-168">Entero</span><span class="sxs-lookup"><span data-stu-id="89f8c-168">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-169">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="89f8c-169">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-170"><strong>Windows 2000, Windows XP y Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="89f8c-170"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="89f8c-171"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="89f8c-171"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-172">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="89f8c-172">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-173">Instancia</span><span class="sxs-lookup"><span data-stu-id="89f8c-173">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-174">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-174">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-175">Sí</span><span class="sxs-lookup"><span data-stu-id="89f8c-175">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-176">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-176">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-177">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-177">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-178">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="89f8c-178">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-179">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-179">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-180">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-180">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-181">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-181">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-182">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="89f8c-182">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-183">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-183">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-184">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="89f8c-184">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-185">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-185">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-186">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-186">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-187">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="89f8c-187">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89f8c-188">*JET_paramIndexTuplesLengthMin*</span><span class="sxs-lookup"><span data-stu-id="89f8c-188">*JET_paramIndexTuplesLengthMin*</span></span>  
<span data-ttu-id="89f8c-189">110</span><span class="sxs-lookup"><span data-stu-id="89f8c-189">110</span></span>  

<span data-ttu-id="89f8c-190">Este parámetro especifica el valor predeterminado para la longitud de tupla mínima en un índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="89f8c-190">This parameter specifies the default for the minimum tuple length in a tuple index.</span></span> <span data-ttu-id="89f8c-191">Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="89f8c-191">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="89f8c-192">**Windows Vista:**  Antes de Windows Vista, si se establece este parámetro en cero, se volverá a establecer en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="89f8c-192">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="89f8c-193">Para Windows Vista, ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="89f8c-193">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-194">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="89f8c-194">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-195">3</span><span class="sxs-lookup"><span data-stu-id="89f8c-195">3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-196">Escriba:</span><span class="sxs-lookup"><span data-stu-id="89f8c-196">Type:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-197">Entero</span><span class="sxs-lookup"><span data-stu-id="89f8c-197">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-198">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="89f8c-198">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-199"><strong>Windows 2000, Windows XP y Windows Server 2003: </strong>  0, 2-255</span><span class="sxs-lookup"><span data-stu-id="89f8c-199"><strong>Windows 2000, Windows XP and Windows Server 2003: </strong>  0, 2-255</span></span></p>
<p><span data-ttu-id="89f8c-200"><strong>Windows Vista:</strong>  2-255</span><span class="sxs-lookup"><span data-stu-id="89f8c-200"><strong>Windows Vista:</strong>  2-255</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-201">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="89f8c-201">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-202">Instancia</span><span class="sxs-lookup"><span data-stu-id="89f8c-202">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-203">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-203">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-204">Sí</span><span class="sxs-lookup"><span data-stu-id="89f8c-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-205">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-205">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-206">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-206">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-207">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="89f8c-207">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-208">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-208">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-209">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-209">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-210">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-210">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-211">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="89f8c-211">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-212">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-212">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-213">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="89f8c-213">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-214">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-214">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-215">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-215">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-216">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="89f8c-216">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89f8c-217">*JET_paramIndexTuplesToIndexMax*</span><span class="sxs-lookup"><span data-stu-id="89f8c-217">*JET_paramIndexTuplesToIndexMax*</span></span>  
<span data-ttu-id="89f8c-218">112</span><span class="sxs-lookup"><span data-stu-id="89f8c-218">112</span></span>  

<span data-ttu-id="89f8c-219">Este parámetro especifica el valor predeterminado para la longitud máxima de una cadena de origen que se va a dividir en tuplas para un índice de tupla.</span><span class="sxs-lookup"><span data-stu-id="89f8c-219">This parameter specifies the default for the maximum length of a source string to break into tuples for a tuple index.</span></span> <span data-ttu-id="89f8c-220">Consulte [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="89f8c-220">See [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) for more information.</span></span>

<span data-ttu-id="89f8c-221">**Windows Vista:**  Antes de Windows Vista, si se establece este parámetro en cero, se volverá a establecer en su valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="89f8c-221">**Windows Vista:**  Prior to Windows Vista, setting this parameter to zero would set it back to its default value.</span></span> <span data-ttu-id="89f8c-222">Para Windows Vista, ya no se admite.</span><span class="sxs-lookup"><span data-stu-id="89f8c-222">For Windows Vista, this is no longer supported.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-223">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="89f8c-223">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-224">32767</span><span class="sxs-lookup"><span data-stu-id="89f8c-224">32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-225">Escriba:</span><span class="sxs-lookup"><span data-stu-id="89f8c-225">Type:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-226">Entero</span><span class="sxs-lookup"><span data-stu-id="89f8c-226">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-227">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="89f8c-227">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-228"><strong>Windows 2000, Windows XP y Windows Server 2003:</strong>  0 – 32767</span><span class="sxs-lookup"><span data-stu-id="89f8c-228"><strong>Windows 2000, Windows XP and Windows Server 2003:</strong>  0 – 32767</span></span></p>
<p><span data-ttu-id="89f8c-229"><strong>Windows Vista:</strong>  1 – 32767</span><span class="sxs-lookup"><span data-stu-id="89f8c-229"><strong>Windows Vista:</strong>  1 – 32767</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-230">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="89f8c-230">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-231">Instancia</span><span class="sxs-lookup"><span data-stu-id="89f8c-231">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-232">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-232">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-233">Sí</span><span class="sxs-lookup"><span data-stu-id="89f8c-233">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-234">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-234">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-235">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-235">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-236">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="89f8c-236">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-237">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-237">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-238">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-238">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-239">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-239">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-240">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="89f8c-240">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-241">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-241">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-242">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="89f8c-242">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-243">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-243">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-244">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-244">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-245">Windows XP y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="89f8c-245">Windows XP and later releases</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="89f8c-246">*JET_paramUnicodeIndexDefault*</span><span class="sxs-lookup"><span data-stu-id="89f8c-246">*JET_paramUnicodeIndexDefault*</span></span>  
<span data-ttu-id="89f8c-247">72</span><span class="sxs-lookup"><span data-stu-id="89f8c-247">72</span></span>  

<span data-ttu-id="89f8c-248">Este parámetro controla los parámetros Unicode predeterminados usados por cualquier índice en una columna de clave Unicode.</span><span class="sxs-lookup"><span data-stu-id="89f8c-248">This parameter controls the default Unicode parameters used by any index over a Unicode key column.</span></span> <span data-ttu-id="89f8c-249">El tipo de este parámetro es [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) y, en realidad, se pasa mediante un puntero de búfer almacenado en el parámetro de entero de [JetGetSystemParameter](./jetgetsystemparameter-function.md) y [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span><span class="sxs-lookup"><span data-stu-id="89f8c-249">The type of this parameter is [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and is actually passed using a buffer pointer stored in the integer parameter of [JetGetSystemParameter](./jetgetsystemparameter-function.md) and [JetSetSystemParameter](./jetsetsystemparameter-function.md).</span></span> <span data-ttu-id="89f8c-250">El tamaño del búfer debe ser igual al tamaño de [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) y se debe pasar a [JetGetSystemParameter](./jetgetsystemparameter-function.md) mediante el parámetro de tamaño de búfer de cadena.</span><span class="sxs-lookup"><span data-stu-id="89f8c-250">The size of the buffer must equal the size of [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) and must be passed to [JetGetSystemParameter](./jetgetsystemparameter-function.md) using the string buffer size parameter.</span></span> <span data-ttu-id="89f8c-251">Esto es claramente incoherente, pero es el comportamiento de este parámetro.</span><span class="sxs-lookup"><span data-stu-id="89f8c-251">This is clearly inconsistent but that is the behavior of this parameter.</span></span>

<span data-ttu-id="89f8c-252">El valor predeterminado de este parámetro contiene un LCID para la configuración regional de Inglés de EE. UU. y las siguientes marcas de [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa): LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="89f8c-252">The default value of this parameter contains an LCID for the U.S. English locale and the following [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span>

<span data-ttu-id="89f8c-253">**Windows 2000:**  Se omite SORTID en el LCID.</span><span class="sxs-lookup"><span data-stu-id="89f8c-253">**Windows 2000:**  The SORTID in the LCID is ignored.</span></span> <span data-ttu-id="89f8c-254">Siempre se usa un SORTID de SORT_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="89f8c-254">A SORTID of SORT_DEFAULT is always used.</span></span>

<span data-ttu-id="89f8c-255">**Windows 2000:**  Las marcas [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) deben contener las marcas siguientes: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE y NORM_IGNOREWIDTH.</span><span class="sxs-lookup"><span data-stu-id="89f8c-255">**Windows 2000:**  The [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) flags must contain the following flags: LCMAP_SORTKEY, NORM_IGNORECASE, NORM_IGNOREKANATYPE, and NORM_IGNOREWIDTH.</span></span> <span data-ttu-id="89f8c-256">Además, las marcas de [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)pueden contener las marcas siguientes: NORM_IGNORENONSPACE.</span><span class="sxs-lookup"><span data-stu-id="89f8c-256">In addition, the [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags may contain the following flags: NORM_IGNORENONSPACE.</span></span>

<span data-ttu-id="89f8c-257">**Nota:**  Si su aplicación desea almacenar datos Unicode, se recomienda encarecidamente que no se base en los parámetros Unicode predeterminados para los índices.</span><span class="sxs-lookup"><span data-stu-id="89f8c-257">**Note**  If your application wishes to store Unicode data, then it is strongly recommended that you do not rely on the default Unicode parameters for your indexes.</span></span> <span data-ttu-id="89f8c-258">El uso del Inglés de EE. UU. es equivalente al uso de la configuración regional de todos los idiomas y se sabe que las marcas [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)predeterminadas interfieren seriamente con algunos lenguajes.</span><span class="sxs-lookup"><span data-stu-id="89f8c-258">The use of U.S. English is tantamount to using the invariant locale and the default [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)flags are known to seriously interfere with some languages.</span></span> <span data-ttu-id="89f8c-259">Siempre debe especificar su propia configuración para los parámetros Unicode a JetCreateIndex2 con [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span><span class="sxs-lookup"><span data-stu-id="89f8c-259">You should always specify your own settings for the Unicode parameters to JetCreateIndex2 using [JET_INDEXCREATE](./jet-indexcreate-structure.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-260">Valor predeterminado:</span><span class="sxs-lookup"><span data-stu-id="89f8c-260">Default Value:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-261">Especial</span><span class="sxs-lookup"><span data-stu-id="89f8c-261">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-262">Escriba:</span><span class="sxs-lookup"><span data-stu-id="89f8c-262">Type:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-263">JET_UNICODEINDEX \* (JET_UNICODEINDEX)</span><span class="sxs-lookup"><span data-stu-id="89f8c-263">JET_UNICODEINDEX\* (JET_UNICODEINDEX)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-264">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="89f8c-264">Valid Range:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-265">Especial</span><span class="sxs-lookup"><span data-stu-id="89f8c-265">Special</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-266">Ámbito:</span><span class="sxs-lookup"><span data-stu-id="89f8c-266">Scope:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-267">Instancia</span><span class="sxs-lookup"><span data-stu-id="89f8c-267">Instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-268">Establecer después de <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-268">Set After <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-269">Sí</span><span class="sxs-lookup"><span data-stu-id="89f8c-269">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-270">Establecer después de <a href="gg294068(v=exchg.10).md">JetInit</a>:</span><span class="sxs-lookup"><span data-stu-id="89f8c-270">Set after <a href="gg294068(v=exchg.10).md">JetInit</a>:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-271">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-271">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-272">Afecta al diseño físico:</span><span class="sxs-lookup"><span data-stu-id="89f8c-272">Affects Physical Layout:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-273">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-273">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-274">Afecta a la confiabilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-274">Affects Reliability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-275">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-275">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-276">Afecta al rendimiento:</span><span class="sxs-lookup"><span data-stu-id="89f8c-276">Affects Performance:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-277">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-277">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-278">Afecta a los recursos:</span><span class="sxs-lookup"><span data-stu-id="89f8c-278">Affects Resources:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-279">No</span><span class="sxs-lookup"><span data-stu-id="89f8c-279">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-280">Disponibilidad:</span><span class="sxs-lookup"><span data-stu-id="89f8c-280">Availability:</span></span></p></td>
<td><p><span data-ttu-id="89f8c-281">All</span><span class="sxs-lookup"><span data-stu-id="89f8c-281">All</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a><span data-ttu-id="89f8c-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="89f8c-282">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-283"><strong>Cliente</strong></span><span class="sxs-lookup"><span data-stu-id="89f8c-283"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="89f8c-284">Requiere Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="89f8c-284">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="89f8c-285"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="89f8c-285"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="89f8c-286">Requiere Windows Server 2008, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="89f8c-286">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="89f8c-287"><strong>Header</strong></span><span class="sxs-lookup"><span data-stu-id="89f8c-287"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="89f8c-288">Declarado en esent. h.</span><span class="sxs-lookup"><span data-stu-id="89f8c-288">Declared in Esent.h.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="89f8c-289">Consulte también</span><span class="sxs-lookup"><span data-stu-id="89f8c-289">See Also</span></span>

[<span data-ttu-id="89f8c-290">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="89f8c-290">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)  
[<span data-ttu-id="89f8c-291">JET_TUPLELIMITS</span><span class="sxs-lookup"><span data-stu-id="89f8c-291">JET_TUPLELIMITS</span></span>](./jet-tuplelimits-structure.md)  
[<span data-ttu-id="89f8c-292">JET_UNICODEINDEX</span><span class="sxs-lookup"><span data-stu-id="89f8c-292">JET_UNICODEINDEX</span></span>](./jet-unicodeindex-structure.md)  
[<span data-ttu-id="89f8c-293">JetCreateInstance</span><span class="sxs-lookup"><span data-stu-id="89f8c-293">JetCreateInstance</span></span>](./jetcreateinstance-function.md)  
[<span data-ttu-id="89f8c-294">JetGetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="89f8c-294">JetGetSystemParameter</span></span>](./jetgetsystemparameter-function.md)  
[<span data-ttu-id="89f8c-295">JetInit</span><span class="sxs-lookup"><span data-stu-id="89f8c-295">JetInit</span></span>](./jetinit-function.md)  
[<span data-ttu-id="89f8c-296">JetSetSystemParameter</span><span class="sxs-lookup"><span data-stu-id="89f8c-296">JetSetSystemParameter</span></span>](./jetsetsystemparameter-function.md)
