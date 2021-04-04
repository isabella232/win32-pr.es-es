---
description: Describe los formatos de fecha admitidos para su uso en la cláusula WQL WHERE.
ms.assetid: 24d70b7f-681b-4a36-bb67-beaf69f4919f
ms.tgt_platform: multiple
title: WQL-Supported formatos de fecha
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01e5741de24943defc4df0e59e7255bc1a37effd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910270"
---
# <a name="wql-supported-date-formats"></a><span data-ttu-id="b1551-103">WQL-Supported formatos de fecha</span><span class="sxs-lookup"><span data-stu-id="b1551-103">WQL-Supported Date Formats</span></span>

<span data-ttu-id="b1551-104">Además del formato **DateTime** de WMI, se admiten los siguientes formatos de fecha para su uso en la cláusula **Where** de WQL.</span><span class="sxs-lookup"><span data-stu-id="b1551-104">In addition to the WMI **DATETIME** format, the following date formats are supported for use in the WQL **WHERE** clause.</span></span>

<span data-ttu-id="b1551-105">El formato de hora mostrado es diferente para las distintas configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="b1551-105">The displayed time format is different for different locales.</span></span> <span data-ttu-id="b1551-106">Los scripts que se conectan a los equipos remotos deben especificar la hora con el formato adecuado para la configuración regional del equipo de destino.</span><span class="sxs-lookup"><span data-stu-id="b1551-106">Scripts that connect to remote computers must specify time in the format appropriate for the locale of the target computer.</span></span>

<span data-ttu-id="b1551-107">Por ejemplo, el formato de fecha y hora Estados Unidos es MM-DD-YYYY.</span><span class="sxs-lookup"><span data-stu-id="b1551-107">For example, the United States date and time format is MM-DD-YYYY.</span></span> <span data-ttu-id="b1551-108">Si un script de un equipo de EE. UU. se conecta a un equipo de destino en una configuración regional en la que el formato es DD-MM-AAAA, las consultas se procesan en el equipo de destino como DD-MM-AAAA.</span><span class="sxs-lookup"><span data-stu-id="b1551-108">If a script on a US computer connects to a target computer in a locale where the format is DD-MM-YYYY, then queries are processed on the target computer as DD-MM-YYYY.</span></span> <span data-ttu-id="b1551-109">Para evitar distintos resultados entre configuraciones regionales, use el formato de [**fecha y hora**](datetime.md) .</span><span class="sxs-lookup"><span data-stu-id="b1551-109">To avoid different results between locales, use the [**DATETIME**](datetime.md) format.</span></span> <span data-ttu-id="b1551-110">Para obtener más información, vea [formato de fecha y hora](date-and-time-format.md).</span><span class="sxs-lookup"><span data-stu-id="b1551-110">For more information, see [Date and Time Format](date-and-time-format.md).</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b1551-111">Formato</span><span class="sxs-lookup"><span data-stu-id="b1551-111">Format</span></span></th>
<th><span data-ttu-id="b1551-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="b1551-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b1551-113">Mon [th] DD [,] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="b1551-113">Mon[th] dd[,] [yy]yy</span></span></td>
<td><span data-ttu-id="b1551-114">Mes (deletreado o abreviado en tres letras), día, coma opcional y dos o cuatro dígitos de año.</span><span class="sxs-lookup"><span data-stu-id="b1551-114">Month (either spelled-out or abbreviated in three letters), day, optional comma, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="b1551-115">21 de enero de 1932</span><span class="sxs-lookup"><span data-stu-id="b1551-115">January 21, 1932</span></span><br />
<span data-ttu-id="b1551-116">21 de enero de 32</span><span class="sxs-lookup"><span data-stu-id="b1551-116">January 21, 32</span></span><br />
<span data-ttu-id="b1551-117">21 1932 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-117">Jan 21 1932</span></span><br />
<span data-ttu-id="b1551-118">21 32 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-118">Jan 21 32</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-119">Mon [th] [,] AAAA</span><span class="sxs-lookup"><span data-stu-id="b1551-119">Mon[th][,] yyyy</span></span></td>
<td><span data-ttu-id="b1551-120">Mes (deletreado o abreviado en tres letras), una coma opcional y un año de cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="b1551-120">Month (either spelled-out or abbreviated in three letters), optional comma, and four-digit year.</span></span><br/> <dl> <span data-ttu-id="b1551-121">1932 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-121">January 1932</span></span><br />
<span data-ttu-id="b1551-122">1932 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-122">Jan 1932</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-123">Mon [th] [yy] yy DD</span><span class="sxs-lookup"><span data-stu-id="b1551-123">Mon[th] [yy]yy dd</span></span></td>
<td><span data-ttu-id="b1551-124">Mes (deletreado o abreviado en tres letras), dos o cuatro dígitos de año y día.</span><span class="sxs-lookup"><span data-stu-id="b1551-124">Month (either spelled-out or abbreviated in three letters), two or four digit year, and day.</span></span><br/> <dl> <span data-ttu-id="b1551-125">1932 21 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-125">January 1932 21</span></span><br />
<span data-ttu-id="b1551-126">32 21 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-126">Jan 32 21</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-127">DD mes [th] [,] [] [AA] AA</span><span class="sxs-lookup"><span data-stu-id="b1551-127">dd Mon[th][,][ ][yy]yy</span></span></td>
<td><span data-ttu-id="b1551-128">Día del mes, mes (deletreado o abreviado en tres letras), coma opcional, espacio opcional y dos o cuatro dígitos de año.</span><span class="sxs-lookup"><span data-stu-id="b1551-128">Day of the month, month (either spelled-out or abbreviated in three letters), optional comma, optional space, and two or four-digit year.</span></span><br/> <dl> <span data-ttu-id="b1551-129">21 de enero de 1932</span><span class="sxs-lookup"><span data-stu-id="b1551-129">21 January, 1932</span></span><br />
<span data-ttu-id="b1551-130">21 Jan32</span><span class="sxs-lookup"><span data-stu-id="b1551-130">21 Jan32</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-131">DD [AA] AA Mon [th]</span><span class="sxs-lookup"><span data-stu-id="b1551-131">dd [yy]yy Mon[th]</span></span></td>
<td><span data-ttu-id="b1551-132">Día del mes, dos o cuatro dígitos año y mes (deletreado o abreviado en tres letras).</span><span class="sxs-lookup"><span data-stu-id="b1551-132">Day of the month, two or four-digit year, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="b1551-133">21 1932 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-133">21 1932 January</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-134">[yy] yy mes [th] DD</span><span class="sxs-lookup"><span data-stu-id="b1551-134">[yy]yy Mon[th] dd</span></span></td>
<td><span data-ttu-id="b1551-135">Año de dos o cuatro dígitos, mes (deletreado o abreviado en tres letras) y día.</span><span class="sxs-lookup"><span data-stu-id="b1551-135">Two or four-digit year, month (either spelled-out or abbreviated in three letters), and day.</span></span><br/> <dl> <span data-ttu-id="b1551-136">21 de enero de 1932</span><span class="sxs-lookup"><span data-stu-id="b1551-136">1932 January 21</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-137">yyyy Mon [th]</span><span class="sxs-lookup"><span data-stu-id="b1551-137">yyyy Mon[th]</span></span></td>
<td><span data-ttu-id="b1551-138">Año y mes de dos o cuatro dígitos (deletreado o abreviado en tres letras).</span><span class="sxs-lookup"><span data-stu-id="b1551-138">Two or four-digit year and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="b1551-139">1932 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-139">1932 Jan</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-140">AAAA DD mes [th]</span><span class="sxs-lookup"><span data-stu-id="b1551-140">yyyy dd Mon[th]</span></span></td>
<td><span data-ttu-id="b1551-141">Año, día y mes de dos o cuatro dígitos (deletreado o abreviado en tres letras).</span><span class="sxs-lookup"><span data-stu-id="b1551-141">Two or four-digit year, day, and month (either spelled-out or abbreviated in three letters).</span></span><br/> <dl> <span data-ttu-id="b1551-142">1932 21 de enero</span><span class="sxs-lookup"><span data-stu-id="b1551-142">1932 21 January</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-143">F M {/-.} DD {/-.} [yy] AA</span><span class="sxs-lookup"><span data-stu-id="b1551-143">[M]M{/-.}dd{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="b1551-144">Mes, día y dos o cuatro dígitos de año.</span><span class="sxs-lookup"><span data-stu-id="b1551-144">Month, day, and two or four-digit year.</span></span> <span data-ttu-id="b1551-145">Tenga en cuenta que los separadores deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="b1551-145">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-146">DD {/-.} F M {/-.} [yy] AA</span><span class="sxs-lookup"><span data-stu-id="b1551-146">dd{/-.}[M]M{/-.}[yy]yy</span></span></td>
<td><span data-ttu-id="b1551-147">Día del mes, mes y año de dos o cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="b1551-147">Day of the month, month, and two or four-digit year.</span></span> <span data-ttu-id="b1551-148">Tenga en cuenta que los separadores deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="b1551-148">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-149">F M {/-.} [yy] yy {/-.} DD</span><span class="sxs-lookup"><span data-stu-id="b1551-149">[M]M{/-.}[yy]yy{/-.}dd</span></span></td>
<td><span data-ttu-id="b1551-150">Mes, dos o cuatro dígitos de año y día.</span><span class="sxs-lookup"><span data-stu-id="b1551-150">Month, two or four-digit year, and day.</span></span> <span data-ttu-id="b1551-151">Tenga en cuenta que los separadores deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="b1551-151">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-152">DD {/-.} [yy] yy {/-.} F F</span><span class="sxs-lookup"><span data-stu-id="b1551-152">dd{/-.}[yy]yy{/-.}[M]M</span></span></td>
<td><span data-ttu-id="b1551-153">Día del mes, dos o cuatro dígitos de año y mes.</span><span class="sxs-lookup"><span data-stu-id="b1551-153">Day of the month, two or four-digit year, and month.</span></span> <span data-ttu-id="b1551-154">Tenga en cuenta que los separadores deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="b1551-154">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-155">[yy] yy {/-.} DD {/-.} F F</span><span class="sxs-lookup"><span data-stu-id="b1551-155">[yy]yy{/-.}dd{/-.}[M]M</span></span></td>
<td><span data-ttu-id="b1551-156">Año, día y mes de dos o cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="b1551-156">Two or four digit year, day, and month.</span></span> <span data-ttu-id="b1551-157">Tenga en cuenta que los separadores deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="b1551-157">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-158">[yy] yy {/-.} F M {/-.} DD</span><span class="sxs-lookup"><span data-stu-id="b1551-158">[yy]yy{/-.}[M]M{/-.}dd</span></span></td>
<td><span data-ttu-id="b1551-159">Año, mes y día de dos o cuatro dígitos.</span><span class="sxs-lookup"><span data-stu-id="b1551-159">Two or four digit year, month, and day.</span></span> <span data-ttu-id="b1551-160">Tenga en cuenta que los separadores deben ser iguales.</span><span class="sxs-lookup"><span data-stu-id="b1551-160">Note that the separators must be the same.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b1551-161">[yy] AAMMDD</span><span class="sxs-lookup"><span data-stu-id="b1551-161">[yy]yyMMdd</span></span></td>
<td><span data-ttu-id="b1551-162">Dos o cuatro dígitos de año, mes y día, sin espacios.</span><span class="sxs-lookup"><span data-stu-id="b1551-162">Two or four digit year, month, and day, without spaces.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b1551-163">aaaa [MM [DD]]</span><span class="sxs-lookup"><span data-stu-id="b1551-163">yyyy[MM[dd]]</span></span></td>
<td><span data-ttu-id="b1551-164">Año de dos o cuatro dígitos, un mes opcional y un día opcional, sin espacios.</span><span class="sxs-lookup"><span data-stu-id="b1551-164">Two or four digit year, optional month, and optional day, without spaces.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b1551-165">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b1551-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1551-166">Cláusula WHERE</span><span class="sxs-lookup"><span data-stu-id="b1551-166">WHERE Clause</span></span>](where-clause.md)
</dt> </dl>

 

 




