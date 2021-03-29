---
description: Constantes de SMONTHNAME de configuración regional \_ \*
ms.assetid: 81269282-bea8-4a5d-929d-c68af34bd1ac
title: Constantes de LOCALE_SMONTHNAME *
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ef4b45a84ea31d7d8c3d5de6e2f3f3a452c7a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810753"
---
# <a name="locale_smonthname-constants"></a><span data-ttu-id="06694-103">Constantes de SMONTHNAME de configuración regional \_ \*</span><span class="sxs-lookup"><span data-stu-id="06694-103">LOCALE\_SMONTHNAME\* Constants</span></span>

<span data-ttu-id="06694-104">En este tema se definen las constantes de SMONTHNAME de configuración regional \_ \* utilizadas por NLS.</span><span class="sxs-lookup"><span data-stu-id="06694-104">This topic defines the LOCALE\_SMONTHNAME\* constants used by NLS.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="06694-105">Value</span><span class="sxs-lookup"><span data-stu-id="06694-105">Value</span></span></th>
<th><span data-ttu-id="06694-106">Significado</span><span class="sxs-lookup"><span data-stu-id="06694-106">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="06694-107">LOCALE_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="06694-107">LOCALE_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="06694-108">Nombre largo nativo de enero.</span><span class="sxs-lookup"><span data-stu-id="06694-108">Native long name for January.</span></span> <span data-ttu-id="06694-109">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-109">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="06694-110">La llamada a la función <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> o <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> con una constante LOCALE_SMONTHNAME \* devuelve la forma independiente, o nominativa, del nombre del mes.</span><span class="sxs-lookup"><span data-stu-id="06694-110">Calling the <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa"><strong>GetLocaleInfo</strong></a> or <a href="/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex"><strong>GetLocaleInfoEx</strong></a> function with a LOCALE_SMONTHNAME\* constant returns the standalone, or nominative, form of the month name.</span></span> <span data-ttu-id="06694-111">Para obtener el formulario genitivo del nombre del mes, la aplicación llama a <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> o <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> con una fecha de la imagen de ddMMMM y quita los dos dígitos del principio de la cadena recuperada.</span><span class="sxs-lookup"><span data-stu-id="06694-111">To get the genitive form of the month name, the application calls <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformata">GetDateFormat</a> or <a href="/windows/desktop/api/datetimeapi/nf-datetimeapi-getdateformatex">GetDateFormatEx</a> with a date picture of ddMMMM and removes the two digits from the beginning of the retrieved string.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06694-112">LOCALE_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="06694-112">LOCALE_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="06694-113">Nombre largo nativo para febrero.</span><span class="sxs-lookup"><span data-stu-id="06694-113">Native long name for February.</span></span> <span data-ttu-id="06694-114">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-114">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-115">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-115">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06694-116">LOCALE_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="06694-116">LOCALE_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="06694-117">Nombre largo nativo para marzo.</span><span class="sxs-lookup"><span data-stu-id="06694-117">Native long name for March.</span></span> <span data-ttu-id="06694-118">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-118">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-119">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-119">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06694-120">LOCALE_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="06694-120">LOCALE_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="06694-121">Nombre largo nativo de abril.</span><span class="sxs-lookup"><span data-stu-id="06694-121">Native long name for April.</span></span> <span data-ttu-id="06694-122">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-122">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-123">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-123">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06694-124">LOCALE_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="06694-124">LOCALE_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="06694-125">Nombre largo nativo para mayo.</span><span class="sxs-lookup"><span data-stu-id="06694-125">Native long name for May.</span></span> <span data-ttu-id="06694-126">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-126">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-127">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-127">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06694-128">LOCALE_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="06694-128">LOCALE_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="06694-129">Nombre largo nativo de junio.</span><span class="sxs-lookup"><span data-stu-id="06694-129">Native long name for June.</span></span> <span data-ttu-id="06694-130">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-130">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-131">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-131">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06694-132">LOCALE_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="06694-132">LOCALE_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="06694-133">Nombre largo nativo de julio.</span><span class="sxs-lookup"><span data-stu-id="06694-133">Native long name for July.</span></span> <span data-ttu-id="06694-134">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-134">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-135">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-135">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06694-136">LOCALE_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="06694-136">LOCALE_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="06694-137">Nombre largo nativo de agosto.</span><span class="sxs-lookup"><span data-stu-id="06694-137">Native long name for August.</span></span> <span data-ttu-id="06694-138">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-138">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-139">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-139">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06694-140">LOCALE_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="06694-140">LOCALE_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="06694-141">Nombre largo nativo de septiembre.</span><span class="sxs-lookup"><span data-stu-id="06694-141">Native long name for September.</span></span> <span data-ttu-id="06694-142">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-142">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-143">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-143">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06694-144">LOCALE_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="06694-144">LOCALE_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="06694-145">Nombre largo nativo para octubre.</span><span class="sxs-lookup"><span data-stu-id="06694-145">Native long name for October.</span></span> <span data-ttu-id="06694-146">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-146">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-147">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-147">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06694-148">LOCALE_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="06694-148">LOCALE_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="06694-149">Nombre largo nativo para noviembre.</span><span class="sxs-lookup"><span data-stu-id="06694-149">Native long name for November.</span></span> <span data-ttu-id="06694-150">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-150">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-151">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-151">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="06694-152">LOCALE_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="06694-152">LOCALE_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="06694-153">Nombre largo nativo de diciembre.</span><span class="sxs-lookup"><span data-stu-id="06694-153">Native long name for December.</span></span> <span data-ttu-id="06694-154">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-154">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-155">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-155">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="06694-156">LOCALE_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="06694-156">LOCALE_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="06694-157">Nombre nativo de un decimotercer mes, si existe.</span><span class="sxs-lookup"><span data-stu-id="06694-157">Native name for a 13th month, if it exists.</span></span> <span data-ttu-id="06694-158">El número máximo de caracteres permitido para esta cadena es 80, incluido un carácter nulo de terminación.</span><span class="sxs-lookup"><span data-stu-id="06694-158">The maximum number of characters allowed for this string is 80, including a terminating null character.</span></span> <span data-ttu-id="06694-159">Vea la nota para obtener LOCALE_SMONTHNAME1.</span><span class="sxs-lookup"><span data-stu-id="06694-159">See note for LOCALE_SMONTHNAME1.</span></span></td>
</tr>
</tbody>
</table>



 

 

 




