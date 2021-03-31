---
description: En este tema se describe la información de tipo de calendario (tipo de datos CALTYPE) utilizada en las funciones EnumCalendarInfo, EnumCalendarInfoEx, EnumCalendarInfoExEx, GetCalendarInfo y GetCalendarInfoEx.
ms.assetid: 33361a97-0f27-477a-a0ee-3d4d3aaeaacf
title: Información de tipo de calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a8e334a1b05f372f51c81ab8158294d46eebfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912565"
---
# <a name="calendar-type-information"></a><span data-ttu-id="ba3fe-103">Información de tipo de calendario</span><span class="sxs-lookup"><span data-stu-id="ba3fe-103">Calendar Type Information</span></span>

<span data-ttu-id="ba3fe-104">En este tema se describe la información de tipo de calendario (tipo de datos CALTYPE) utilizada en las funciones [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)y [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) .</span><span class="sxs-lookup"><span data-stu-id="ba3fe-104">This topic describes the calendar type information (CALTYPE data type) used in the [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa), [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa), [**EnumCalendarInfoExEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex), [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa), and [**GetCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex) functions.</span></span> <span data-ttu-id="ba3fe-105">Algunos de estos valores también se usan en la función [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) .</span><span class="sxs-lookup"><span data-stu-id="ba3fe-105">Some of these values are also used by the [**SetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa) function.</span></span>

<span data-ttu-id="ba3fe-106">Las constantes CALTYPE siguientes se pueden usar en combinación con cualquier otra constante CALTYPE.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-106">The following CALTYPE constants can be used in combination with any other CALTYPE constants.</span></span>



| <span data-ttu-id="ba3fe-107">Constante</span><span class="sxs-lookup"><span data-stu-id="ba3fe-107">Constant</span></span>                     | <span data-ttu-id="ba3fe-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba3fe-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba3fe-109">CAL \_ NOUSEROVERRIDE</span><span class="sxs-lookup"><span data-stu-id="ba3fe-109">CAL\_NOUSEROVERRIDE</span></span>          | <span data-ttu-id="ba3fe-110">**Windows Me/98, windows 2000:** Use el valor predeterminado del sistema en lugar de la elección del usuario.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-110">**Windows Me/98, Windows 2000:** Use the system default instead of the user's choice.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="ba3fe-111">la \_ cal \_ devuelve \_ nombres genitivo</span><span class="sxs-lookup"><span data-stu-id="ba3fe-111">CAL\_RETURN\_GENITIVE\_NAMES</span></span> | <span data-ttu-id="ba3fe-112">**Windows 7 y versiones posteriores:** Recupere el resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) en forma de nombres genitivo de meses, que son los nombres que se usan cuando los nombres de los meses se combinan con otros elementos.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-112">**Windows 7 and later:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) in the form of genitive names of months, which are the names used when the month names are combined with other items.</span></span> <span data-ttu-id="ba3fe-113">Por ejemplo, en ucraniano, el equivalente de enero se escribe "Січень" cuando el mes se denomina solo.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-113">For example, in Ukrainian the equivalent of January is written "Січень" when the month is named alone.</span></span> <span data-ttu-id="ba3fe-114">Sin embargo, cuando el nombre del mes se usa en combinación, por ejemplo, en una fecha como el 5 de enero de 2003, se usa la forma genitivo del nombre.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-114">However, when the month name is used in combination, for example, in a date such as January 5th, 2003, the genitive form of the name is used.</span></span> <span data-ttu-id="ba3fe-115">En el ejemplo ucraniano, el nombre del mes en genitivo se muestra como "5 січня 2003".</span><span class="sxs-lookup"><span data-stu-id="ba3fe-115">For the Ukrainian example, the genitive month name is displayed as "5 січня 2003".</span></span> <span data-ttu-id="ba3fe-116">Para obtener más información, vea [configuración \_ regional \_ devolver \_ nombres genitivo](locale-return-constants.md).</span><span class="sxs-lookup"><span data-stu-id="ba3fe-116">For more information, see [LOCALE\_RETURN\_GENITIVE\_NAMES](locale-return-constants.md).</span></span> |
| <span data-ttu-id="ba3fe-117">\_número de devolución de cal \_</span><span class="sxs-lookup"><span data-stu-id="ba3fe-117">CAL\_RETURN\_NUMBER</span></span>          | <span data-ttu-id="ba3fe-118">**Windows Me/98, windows 2000:** Recupere el resultado de [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) como un número en lugar de una cadena.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-118">**Windows Me/98, Windows 2000:** Retrieve the result from [**GetCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa) as a number instead of a string.</span></span> <span data-ttu-id="ba3fe-119">Esto solo es válido para los valores que comienzan con CAL \_ I.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-119">This is only valid for values beginning with CAL\_I.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="ba3fe-120">CAL- \_ usar \_ CP \_ ACP</span><span class="sxs-lookup"><span data-stu-id="ba3fe-120">CAL\_USE\_CP\_ACP</span></span>            | <span data-ttu-id="ba3fe-121">**Windows Me/98, windows 2000:** Use la página de códigos ANSI (ACP) del sistema en lugar de la página de códigos de configuración regional para la traducción de cadenas.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-121">**Windows Me/98, Windows 2000:** Use the system ANSI code page (ACP) instead of the locale code page for string translation.</span></span> <span data-ttu-id="ba3fe-122">Esto solo es relevante para las versiones ANSI de funciones, por ejemplo, **EnumCalendarInfoA**.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-122">This is only relevant for ANSI versions of functions, for example, **EnumCalendarInfoA**.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

<span data-ttu-id="ba3fe-123">Las constantes CALTYPE siguientes se excluyen mutuamente y no se pueden usar en combinación entre sí en una llamada de función.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-123">The following CALTYPE constants are mutually exclusive and cannot be used in combination with each other in a function call.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ba3fe-124">Constante</span><span class="sxs-lookup"><span data-stu-id="ba3fe-124">Constant</span></span></th>
<th><span data-ttu-id="ba3fe-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="ba3fe-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ba3fe-126">CAL_ICALINTVALUE</span><span class="sxs-lookup"><span data-stu-id="ba3fe-126">CAL_ICALINTVALUE</span></span></td>
<td><span data-ttu-id="ba3fe-127">Un valor entero que indica el tipo de calendario del calendario alternativo.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-127">An integer value indicating the calendar type of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-128">CAL_ITWODIGITYEARMAX</span><span class="sxs-lookup"><span data-stu-id="ba3fe-128">CAL_ITWODIGITYEARMAX</span></span></td>
<td><span data-ttu-id="ba3fe-129"><strong>Windows Me/98, windows 2000:</strong> Un valor entero que indica el límite superior del intervalo de año de dos dígitos.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-129"><strong>Windows Me/98, Windows 2000:</strong> An integer value indicating the upper boundary of the two-digit year range.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-130">CAL_IYEAROFFSETRANGE</span><span class="sxs-lookup"><span data-stu-id="ba3fe-130">CAL_IYEAROFFSETRANGE</span></span></td>
<td><span data-ttu-id="ba3fe-131">Una o más cadenas terminadas en null que especifican los desplazamientos de año para cada uno de los intervalos de la era.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-131">One or more null-terminated strings that specify the year offsets for each of the era ranges.</span></span> <span data-ttu-id="ba3fe-132">La última cadena tiene un carácter nulo de terminación adicional.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-132">The last string has an extra terminating null character.</span></span> <span data-ttu-id="ba3fe-133">Este valor varía en función del tipo de calendario opcional.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-133">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-134">CAL_SABBREVDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="ba3fe-134">CAL_SABBREVDAYNAME1</span></span></td>
<td><span data-ttu-id="ba3fe-135">Nombre nativo abreviado del primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-135">Abbreviated native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-136">CAL_SABBREVDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="ba3fe-136">CAL_SABBREVDAYNAME2</span></span></td>
<td><span data-ttu-id="ba3fe-137">Nombre nativo abreviado del segundo día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-137">Abbreviated native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-138">CAL_SABBREVDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="ba3fe-138">CAL_SABBREVDAYNAME3</span></span></td>
<td><span data-ttu-id="ba3fe-139">Nombre nativo abreviado del tercer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-139">Abbreviated native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-140">CAL_SABBREVDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="ba3fe-140">CAL_SABBREVDAYNAME4</span></span></td>
<td><span data-ttu-id="ba3fe-141">Nombre nativo abreviado del cuarto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-141">Abbreviated native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-142">CAL_SABBREVDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="ba3fe-142">CAL_SABBREVDAYNAME5</span></span></td>
<td><span data-ttu-id="ba3fe-143">Nombre nativo abreviado del quinto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-143">Abbreviated native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-144">CAL_SABBREVDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="ba3fe-144">CAL_SABBREVDAYNAME6</span></span></td>
<td><span data-ttu-id="ba3fe-145">Nombre nativo abreviado del sexto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-145">Abbreviated native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-146">CAL_SABBREVDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="ba3fe-146">CAL_SABBREVDAYNAME7</span></span></td>
<td><span data-ttu-id="ba3fe-147">Nombre nativo abreviado del séptimo día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-147">Abbreviated native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-148">CAL_SABBREVERASTRING</span><span class="sxs-lookup"><span data-stu-id="ba3fe-148">CAL_SABBREVERASTRING</span></span></td>
<td><span data-ttu-id="ba3fe-149"><strong>Windows 7 y versiones posteriores:</strong> Nombre nativo abreviado de una era.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-149"><strong>Windows 7 and later:</strong> Abbreviated native name of an era.</span></span> <span data-ttu-id="ba3fe-150">La era completa se representa mediante la constante CAL_SERASTRING.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-150">The full era is represented by the CAL_SERASTRING constant.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-151">CAL_SABBREVMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="ba3fe-151">CAL_SABBREVMONTHNAME1</span></span></td>
<td><span data-ttu-id="ba3fe-152">Nombre nativo abreviado del primer mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-152">Abbreviated native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-153">CAL_SABBREVMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="ba3fe-153">CAL_SABBREVMONTHNAME2</span></span></td>
<td><span data-ttu-id="ba3fe-154">Nombre nativo abreviado del segundo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-154">Abbreviated native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-155">CAL_SABBREVMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="ba3fe-155">CAL_SABBREVMONTHNAME3</span></span></td>
<td><span data-ttu-id="ba3fe-156">Nombre nativo abreviado del tercer mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-156">Abbreviated native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-157">CAL_SABBREVMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="ba3fe-157">CAL_SABBREVMONTHNAME4</span></span></td>
<td><span data-ttu-id="ba3fe-158">Nombre nativo abreviado del cuarto mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-158">Abbreviated native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-159">CAL_SABBREVMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="ba3fe-159">CAL_SABBREVMONTHNAME5</span></span></td>
<td><span data-ttu-id="ba3fe-160">Nombre nativo abreviado del quinto mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-160">Abbreviated native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-161">CAL_SABBREVMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="ba3fe-161">CAL_SABBREVMONTHNAME6</span></span></td>
<td><span data-ttu-id="ba3fe-162">Nombre nativo abreviado del sexto mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-162">Abbreviated native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-163">CAL_SABBREVMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="ba3fe-163">CAL_SABBREVMONTHNAME7</span></span></td>
<td><span data-ttu-id="ba3fe-164">Nombre nativo abreviado del séptimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-164">Abbreviated native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-165">CAL_SABBREVMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="ba3fe-165">CAL_SABBREVMONTHNAME8</span></span></td>
<td><span data-ttu-id="ba3fe-166">Nombre nativo abreviado del octavo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-166">Abbreviated native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-167">CAL_SABBREVMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="ba3fe-167">CAL_SABBREVMONTHNAME9</span></span></td>
<td><span data-ttu-id="ba3fe-168">Nombre nativo abreviado del noveno mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-168">Abbreviated native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-169">CAL_SABBREVMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="ba3fe-169">CAL_SABBREVMONTHNAME10</span></span></td>
<td><span data-ttu-id="ba3fe-170">Nombre nativo abreviado del décimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-170">Abbreviated native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-171">CAL_SABBREVMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="ba3fe-171">CAL_SABBREVMONTHNAME11</span></span></td>
<td><span data-ttu-id="ba3fe-172">Nombre nativo abreviado del undécimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-172">Abbreviated native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-173">CAL_SABBREVMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="ba3fe-173">CAL_SABBREVMONTHNAME12</span></span></td>
<td><span data-ttu-id="ba3fe-174">Nombre nativo abreviado del duodécimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-174">Abbreviated native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-175">CAL_SABBREVMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="ba3fe-175">CAL_SABBREVMONTHNAME13</span></span></td>
<td><span data-ttu-id="ba3fe-176">Nombre nativo abreviado del decimotercer mes del año, si existe.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-176">Abbreviated native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-177">CAL_SCALNAME</span><span class="sxs-lookup"><span data-stu-id="ba3fe-177">CAL_SCALNAME</span></span></td>
<td><span data-ttu-id="ba3fe-178">Nombre nativo del calendario alternativo.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-178">Native name of the alternate calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-179">CAL_SDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="ba3fe-179">CAL_SDAYNAME1</span></span></td>
<td><span data-ttu-id="ba3fe-180">Nombre nativo del primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-180">Native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-181">CAL_SDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="ba3fe-181">CAL_SDAYNAME2</span></span></td>
<td><span data-ttu-id="ba3fe-182">Nombre nativo del segundo día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-182">Native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-183">CAL_SDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="ba3fe-183">CAL_SDAYNAME3</span></span></td>
<td><span data-ttu-id="ba3fe-184">Nombre nativo del tercer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-184">Native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-185">CAL_SDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="ba3fe-185">CAL_SDAYNAME4</span></span></td>
<td><span data-ttu-id="ba3fe-186">Nombre nativo del cuarto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-186">Native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-187">CAL_SDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="ba3fe-187">CAL_SDAYNAME5</span></span></td>
<td><span data-ttu-id="ba3fe-188">Nombre nativo del quinto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-188">Native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-189">CAL_SDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="ba3fe-189">CAL_SDAYNAME6</span></span></td>
<td><span data-ttu-id="ba3fe-190">Nombre nativo del sexto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-190">Native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-191">CAL_SDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="ba3fe-191">CAL_SDAYNAME7</span></span></td>
<td><span data-ttu-id="ba3fe-192">Nombre nativo del séptimo día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-192">Native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-193">CAL_SERASTRING</span><span class="sxs-lookup"><span data-stu-id="ba3fe-193">CAL_SERASTRING</span></span></td>
<td><span data-ttu-id="ba3fe-194">Una o más cadenas terminadas en null que especifican cada uno de los puntos de código Unicode que especifican la era asociada a CAL_IYEAROFFSETRANGE.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-194">One or more null-terminated strings that specify each of the Unicode code points specifying the era associated with CAL_IYEAROFFSETRANGE.</span></span> <span data-ttu-id="ba3fe-195">La última cadena tiene un carácter nulo de terminación adicional.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-195">The last string has an extra terminating null character.</span></span> <span data-ttu-id="ba3fe-196">Este valor varía en función del tipo de calendario opcional.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-196">This value varies in format depending on the type of optional calendar.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-197">CAL_SLONGDATE</span><span class="sxs-lookup"><span data-stu-id="ba3fe-197">CAL_SLONGDATE</span></span></td>
<td><span data-ttu-id="ba3fe-198">Formatos de fecha larga para el tipo de calendario.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-198">Long date formats for the calendar type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-199">CAL_SMONTHDAY</span><span class="sxs-lookup"><span data-stu-id="ba3fe-199">CAL_SMONTHDAY</span></span></td>
<td><span data-ttu-id="ba3fe-200"><strong>Windows 7 y versiones posteriores:</strong> Formato del mes y día para el tipo de calendario.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-200"><strong>Windows 7 and later:</strong> Format of the month and day for the calendar type.</span></span> <span data-ttu-id="ba3fe-201">El formato es similar al de CAL_SLONGDATE.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-201">The formatting is similar to that for CAL_SLONGDATE.</span></span> <span data-ttu-id="ba3fe-202">Por ejemplo, si el patrón de mes/día es el nombre completo del mes seguido del número de día con ceros a la izquierda, por ejemplo, &quot; el 03 de septiembre &quot; , el formato es &quot; mmmm DD &quot; .</span><span class="sxs-lookup"><span data-stu-id="ba3fe-202">For example, if the Month/Day pattern is the full month name followed by the day number with leading zeros, for example, &quot;September 03&quot;, the format is &quot;MMMM dd&quot;.</span></span> <span data-ttu-id="ba3fe-203">Las comillas simples se pueden usar para insertar caracteres sin formato, por ejemplo, ' de ' en español.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-203">Single quotation marks can be used to insert non-format characters, for example, 'de' in Spanish.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="ba3fe-204">Este tipo de calendario solo admite un formato.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-204">This calendar type supports only one format.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-205">CAL_SMONTHNAME1</span><span class="sxs-lookup"><span data-stu-id="ba3fe-205">CAL_SMONTHNAME1</span></span></td>
<td><span data-ttu-id="ba3fe-206">Nombre nativo del primer mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-206">Native name of the first month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-207">CAL_SMONTHNAME2</span><span class="sxs-lookup"><span data-stu-id="ba3fe-207">CAL_SMONTHNAME2</span></span></td>
<td><span data-ttu-id="ba3fe-208">Nombre nativo del segundo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-208">Native name of the second month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-209">CAL_SMONTHNAME3</span><span class="sxs-lookup"><span data-stu-id="ba3fe-209">CAL_SMONTHNAME3</span></span></td>
<td><span data-ttu-id="ba3fe-210">Nombre nativo del tercer mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-210">Native name of the third month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-211">CAL_SMONTHNAME4</span><span class="sxs-lookup"><span data-stu-id="ba3fe-211">CAL_SMONTHNAME4</span></span></td>
<td><span data-ttu-id="ba3fe-212">Nombre nativo del cuarto mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-212">Native name of the fourth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-213">CAL_SMONTHNAME5</span><span class="sxs-lookup"><span data-stu-id="ba3fe-213">CAL_SMONTHNAME5</span></span></td>
<td><span data-ttu-id="ba3fe-214">Nombre nativo del quinto mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-214">Native name of the fifth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-215">CAL_SMONTHNAME6</span><span class="sxs-lookup"><span data-stu-id="ba3fe-215">CAL_SMONTHNAME6</span></span></td>
<td><span data-ttu-id="ba3fe-216">Nombre nativo del sexto mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-216">Native name of the sixth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-217">CAL_SMONTHNAME7</span><span class="sxs-lookup"><span data-stu-id="ba3fe-217">CAL_SMONTHNAME7</span></span></td>
<td><span data-ttu-id="ba3fe-218">Nombre nativo del séptimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-218">Native name of the seventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-219">CAL_SMONTHNAME8</span><span class="sxs-lookup"><span data-stu-id="ba3fe-219">CAL_SMONTHNAME8</span></span></td>
<td><span data-ttu-id="ba3fe-220">Nombre nativo del octavo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-220">Native name of the eighth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-221">CAL_SMONTHNAME9</span><span class="sxs-lookup"><span data-stu-id="ba3fe-221">CAL_SMONTHNAME9</span></span></td>
<td><span data-ttu-id="ba3fe-222">Nombre nativo del noveno mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-222">Native name of the ninth month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-223">CAL_SMONTHNAME10</span><span class="sxs-lookup"><span data-stu-id="ba3fe-223">CAL_SMONTHNAME10</span></span></td>
<td><span data-ttu-id="ba3fe-224">Nombre nativo del décimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-224">Native name of the tenth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-225">CAL_SMONTHNAME11</span><span class="sxs-lookup"><span data-stu-id="ba3fe-225">CAL_SMONTHNAME11</span></span></td>
<td><span data-ttu-id="ba3fe-226">Nombre nativo del undécimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-226">Native name of the eleventh month of the year.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-227">CAL_SMONTHNAME12</span><span class="sxs-lookup"><span data-stu-id="ba3fe-227">CAL_SMONTHNAME12</span></span></td>
<td><span data-ttu-id="ba3fe-228">Nombre nativo del duodécimo mes del año.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-228">Native name of the twelfth month of the year.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-229">CAL_SMONTHNAME13</span><span class="sxs-lookup"><span data-stu-id="ba3fe-229">CAL_SMONTHNAME13</span></span></td>
<td><span data-ttu-id="ba3fe-230">Nombre nativo del decimotercer mes del año, si existe.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-230">Native name of the thirteenth month of the year, if it exists.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-231">CAL_SSHORTDATE</span><span class="sxs-lookup"><span data-stu-id="ba3fe-231">CAL_SSHORTDATE</span></span></td>
<td><span data-ttu-id="ba3fe-232">Formatos de fecha corta para el tipo de calendario.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-232">Short date formats for the calendar type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-233">CAL_SSHORTESTDAYNAME1</span><span class="sxs-lookup"><span data-stu-id="ba3fe-233">CAL_SSHORTESTDAYNAME1</span></span></td>
<td><span data-ttu-id="ba3fe-234"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del primer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-234"><strong>Windows Vista and later:</strong> Short native name of the first day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-235">CAL_SSHORTESTDAYNAME2</span><span class="sxs-lookup"><span data-stu-id="ba3fe-235">CAL_SSHORTESTDAYNAME2</span></span></td>
<td><span data-ttu-id="ba3fe-236"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del segundo día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-236"><strong>Windows Vista and later:</strong> Short native name of the second day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-237">CAL_SSHORTESTDAYNAME3</span><span class="sxs-lookup"><span data-stu-id="ba3fe-237">CAL_SSHORTESTDAYNAME3</span></span></td>
<td><span data-ttu-id="ba3fe-238"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del tercer día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-238"><strong>Windows Vista and later:</strong> Short native name of the third day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-239">CAL_SSHORTESTDAYNAME4</span><span class="sxs-lookup"><span data-stu-id="ba3fe-239">CAL_SSHORTESTDAYNAME4</span></span></td>
<td><span data-ttu-id="ba3fe-240"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del cuarto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-240"><strong>Windows Vista and later:</strong> Short native name of the fourth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-241">CAL_SSHORTESTDAYNAME5</span><span class="sxs-lookup"><span data-stu-id="ba3fe-241">CAL_SSHORTESTDAYNAME5</span></span></td>
<td><span data-ttu-id="ba3fe-242"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del quinto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-242"><strong>Windows Vista and later:</strong> Short native name of the fifth day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-243">CAL_SSHORTESTDAYNAME6</span><span class="sxs-lookup"><span data-stu-id="ba3fe-243">CAL_SSHORTESTDAYNAME6</span></span></td>
<td><span data-ttu-id="ba3fe-244"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del sexto día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-244"><strong>Windows Vista and later:</strong> Short native name of the sixth day of the week.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ba3fe-245">CAL_SSHORTESTDAYNAME7</span><span class="sxs-lookup"><span data-stu-id="ba3fe-245">CAL_SSHORTESTDAYNAME7</span></span></td>
<td><span data-ttu-id="ba3fe-246"><strong>Windows Vista y versiones posteriores:</strong> Nombre nativo corto del séptimo día de la semana.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-246"><strong>Windows Vista and later:</strong> Short native name of the seventh day of the week.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="ba3fe-247">CAL_SYEARMONTH</span><span class="sxs-lookup"><span data-stu-id="ba3fe-247">CAL_SYEARMONTH</span></span></td>
<td><span data-ttu-id="ba3fe-248"><strong>Windows Me/98, windows 2000:</strong> Formatos de año/mes para los calendarios especificados.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-248"><strong>Windows Me/98, Windows 2000:</strong> The year/month formats for the specified calendars.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="ba3fe-249">Si el nombre nativo para el día de la semana o para un mes es una cadena vacía, ese nombre es idéntico al nombre especificado en la información de configuración regional correspondiente y, por tanto, no se duplica aquí.</span><span class="sxs-lookup"><span data-stu-id="ba3fe-249">If the native name for the day of the week or for a month is an empty string, that name is identical to the name specified in the corresponding locale information and therefore is not duplicated here.</span></span>

 

 

 




