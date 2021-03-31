---
description: En este tema se definen los identificadores de calendario (tipo de datos CALID) que se usan para especificar calendarios diferentes.
ms.assetid: ba2e841e-e24e-476a-851e-a29b3af4f04d
title: Identificadores de calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab9b931aea4a186af0849dfe8f6642c53744d364
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103809517"
---
# <a name="calendar-identifiers"></a><span data-ttu-id="cac42-103">Identificadores de calendario</span><span class="sxs-lookup"><span data-stu-id="cac42-103">Calendar Identifiers</span></span>

<span data-ttu-id="cac42-104">En este tema se definen los identificadores de calendario (tipo de datos CALID) que se usan para especificar calendarios diferentes.</span><span class="sxs-lookup"><span data-stu-id="cac42-104">This topic defines the calendar identifiers (data type CALID) that are used to specify different calendars.</span></span> <span data-ttu-id="cac42-105">Las aplicaciones pueden utilizar estos identificadores al usar las siguientes funciones NLS y funciones de devolución de llamada, que tienen parámetros que toman el tipo de datos CALID:</span><span class="sxs-lookup"><span data-stu-id="cac42-105">Your applications can use these identifiers when using the following NLS functions and callback functions, which have parameters that take the CALID data type:</span></span>

-   [<span data-ttu-id="cac42-106">**ConvertSystemTimeToCalDateTime**</span><span class="sxs-lookup"><span data-stu-id="cac42-106">**ConvertSystemTimeToCalDateTime**</span></span>](convertsystemtimetocaldatetime.md)
-   [<span data-ttu-id="cac42-107">**EnumCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="cac42-107">**EnumCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa)
-   [<span data-ttu-id="cac42-108">**EnumCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="cac42-108">**EnumCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa)
-   [<span data-ttu-id="cac42-109">**EnumCalendarInfoExEx**</span><span class="sxs-lookup"><span data-stu-id="cac42-109">**EnumCalendarInfoExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexex)
-   <span data-ttu-id="cac42-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cac42-110">[**EnumCalendarInfoProcEx**](/previous-versions/windows/desktop/legacy/dd317807(v=vs.85))</span></span>
-   <span data-ttu-id="cac42-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="cac42-111">[**EnumDateFormatsProcEx**](/previous-versions/windows/desktop/legacy/dd317814(v=vs.85))</span></span>
-   [<span data-ttu-id="cac42-112">**GetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="cac42-112">**GetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoa)
-   [<span data-ttu-id="cac42-113">**GetCalendarInfoEx**</span><span class="sxs-lookup"><span data-stu-id="cac42-113">**GetCalendarInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getcalendarinfoex)
-   [<span data-ttu-id="cac42-114">**GetCalendarSupportedDateRange**</span><span class="sxs-lookup"><span data-stu-id="cac42-114">**GetCalendarSupportedDateRange**</span></span>](getcalendarsupporteddaterange.md)
-   [<span data-ttu-id="cac42-115">**IsCalendarLeapYear**</span><span class="sxs-lookup"><span data-stu-id="cac42-115">**IsCalendarLeapYear**</span></span>](iscalendarleapyear.md)
-   [<span data-ttu-id="cac42-116">**SetCalendarInfo**</span><span class="sxs-lookup"><span data-stu-id="cac42-116">**SetCalendarInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setcalendarinfoa)

<span data-ttu-id="cac42-117">Se definen los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="cac42-117">The following values are defined.</span></span> <span data-ttu-id="cac42-118">Todos los demás valores están reservados.</span><span class="sxs-lookup"><span data-stu-id="cac42-118">All other values are reserved.</span></span> <span data-ttu-id="cac42-119">Estos valores no se pueden combinar entre sí.</span><span class="sxs-lookup"><span data-stu-id="cac42-119">These values cannot be combined with one another.</span></span>



<span data-ttu-id="cac42-120">Identificador de calendario</span><span class="sxs-lookup"><span data-stu-id="cac42-120">Calendar identifier</span></span>

<span data-ttu-id="cac42-121">Significado</span><span class="sxs-lookup"><span data-stu-id="cac42-121">Meaning</span></span>

<span data-ttu-id="cac42-122">1</span><span class="sxs-lookup"><span data-stu-id="cac42-122">1</span></span>

<span data-ttu-id="cac42-123">\_calendario gregoriano</span><span class="sxs-lookup"><span data-stu-id="cac42-123">CAL\_GREGORIAN</span></span>

<span data-ttu-id="cac42-124">Gregoriano (localizado)</span><span class="sxs-lookup"><span data-stu-id="cac42-124">Gregorian (localized)</span></span>

<span data-ttu-id="cac42-125">2</span><span class="sxs-lookup"><span data-stu-id="cac42-125">2</span></span>

<span data-ttu-id="cac42-126">CAL \_ gregoriano \_</span><span class="sxs-lookup"><span data-stu-id="cac42-126">CAL\_GREGORIAN\_US</span></span>

<span data-ttu-id="cac42-127">Gregoriano (cadenas en inglés siempre)</span><span class="sxs-lookup"><span data-stu-id="cac42-127">Gregorian (English strings always)</span></span>

<span data-ttu-id="cac42-128">3</span><span class="sxs-lookup"><span data-stu-id="cac42-128">3</span></span>

<span data-ttu-id="cac42-129">CAL \_ Japón</span><span class="sxs-lookup"><span data-stu-id="cac42-129">CAL\_JAPAN</span></span>

<span data-ttu-id="cac42-130">Era del Emperador japonés</span><span class="sxs-lookup"><span data-stu-id="cac42-130">Japanese Emperor Era</span></span>

<span data-ttu-id="cac42-131">4</span><span class="sxs-lookup"><span data-stu-id="cac42-131">4</span></span>

<span data-ttu-id="cac42-132">CAL \_ Taiwán</span><span class="sxs-lookup"><span data-stu-id="cac42-132">CAL\_TAIWAN</span></span>

<span data-ttu-id="cac42-133">Calendario taiwanés</span><span class="sxs-lookup"><span data-stu-id="cac42-133">Taiwan calendar</span></span>

<span data-ttu-id="cac42-134">5</span><span class="sxs-lookup"><span data-stu-id="cac42-134">5</span></span>

<span data-ttu-id="cac42-135">CAL \_ Corea</span><span class="sxs-lookup"><span data-stu-id="cac42-135">CAL\_KOREA</span></span>

<span data-ttu-id="cac42-136">Coreano Tangun era</span><span class="sxs-lookup"><span data-stu-id="cac42-136">Korean Tangun Era</span></span>

<span data-ttu-id="cac42-137">6</span><span class="sxs-lookup"><span data-stu-id="cac42-137">6</span></span>

<span data-ttu-id="cac42-138">HIJRI de CAL \_</span><span class="sxs-lookup"><span data-stu-id="cac42-138">CAL\_HIJRI</span></span>

<span data-ttu-id="cac42-139">Hijri (Árabe lunar)</span><span class="sxs-lookup"><span data-stu-id="cac42-139">Hijri (Arabic Lunar)</span></span>

<span data-ttu-id="cac42-140">7</span><span class="sxs-lookup"><span data-stu-id="cac42-140">7</span></span>

<span data-ttu-id="cac42-141">CAL \_ tailandés</span><span class="sxs-lookup"><span data-stu-id="cac42-141">CAL\_THAI</span></span>

<span data-ttu-id="cac42-142">Tailandés</span><span class="sxs-lookup"><span data-stu-id="cac42-142">Thai</span></span>

<span data-ttu-id="cac42-143">8</span><span class="sxs-lookup"><span data-stu-id="cac42-143">8</span></span>

<span data-ttu-id="cac42-144">hebreo de CAL \_</span><span class="sxs-lookup"><span data-stu-id="cac42-144">CAL\_HEBREW</span></span>

<span data-ttu-id="cac42-145">Hebreo (lunar)</span><span class="sxs-lookup"><span data-stu-id="cac42-145">Hebrew (Lunar)</span></span>

<span data-ttu-id="cac42-146">9</span><span class="sxs-lookup"><span data-stu-id="cac42-146">9</span></span>

<span data-ttu-id="cac42-147">\_calendario gregoriano \_ \_ francés de cal</span><span class="sxs-lookup"><span data-stu-id="cac42-147">CAL\_GREGORIAN\_ME\_FRENCH</span></span>

<span data-ttu-id="cac42-148">Gregorian Middle East French</span><span class="sxs-lookup"><span data-stu-id="cac42-148">Gregorian Middle East French</span></span>

<span data-ttu-id="cac42-149">10</span><span class="sxs-lookup"><span data-stu-id="cac42-149">10</span></span>

<span data-ttu-id="cac42-150">CAL \_ gregoriano \_ Árabe</span><span class="sxs-lookup"><span data-stu-id="cac42-150">CAL\_GREGORIAN\_ARABIC</span></span>

<span data-ttu-id="cac42-151">Gregorian Arabic</span><span class="sxs-lookup"><span data-stu-id="cac42-151">Gregorian Arabic</span></span>

<span data-ttu-id="cac42-152">11</span><span class="sxs-lookup"><span data-stu-id="cac42-152">11</span></span>

<span data-ttu-id="cac42-153">CAL \_ gregoriano \_ XLIT \_ Inglés</span><span class="sxs-lookup"><span data-stu-id="cac42-153">CAL\_GREGORIAN\_XLIT\_ENGLISH</span></span>

<span data-ttu-id="cac42-154">Gregoriano (transliteración) Inglés</span><span class="sxs-lookup"><span data-stu-id="cac42-154">Gregorian transliterated English</span></span>

<span data-ttu-id="cac42-155">12</span><span class="sxs-lookup"><span data-stu-id="cac42-155">12</span></span>

<span data-ttu-id="cac42-156">CAL \_ gregoriano \_ XLIT \_ Francés</span><span class="sxs-lookup"><span data-stu-id="cac42-156">CAL\_GREGORIAN\_XLIT\_FRENCH</span></span>

<span data-ttu-id="cac42-157">Gregoriano (transliteración) francés</span><span class="sxs-lookup"><span data-stu-id="cac42-157">Gregorian transliterated French</span></span>

<span data-ttu-id="cac42-158">23</span><span class="sxs-lookup"><span data-stu-id="cac42-158">23</span></span>

<span data-ttu-id="cac42-159">CAL \_ UMALQURA</span><span class="sxs-lookup"><span data-stu-id="cac42-159">CAL\_UMALQURA</span></span>

<span data-ttu-id="cac42-160">**Windows Vista y versiones posteriores:** Calendario de Um al-Qura (Árabe lunar)</span><span class="sxs-lookup"><span data-stu-id="cac42-160">**Windows Vista and later:** Um Al Qura (Arabic lunar) calendar</span></span>



 

> [!Note]  
> <span data-ttu-id="cac42-161">El intervalo de numeración entre los identificadores CAL \_ gregoriano \_ XLIT \_ francés y cal \_ UMALQURA es intencionado.</span><span class="sxs-lookup"><span data-stu-id="cac42-161">The gap in numbering between the identifiers CAL\_GREGORIAN\_XLIT\_FRENCH and CAL\_UMALQURA is intentional.</span></span> <span data-ttu-id="cac42-162">El designador de CAL \_ UMALQURA es 23, no 13.</span><span class="sxs-lookup"><span data-stu-id="cac42-162">The designator for CAL\_UMALQURA is 23, not 13.</span></span>

 

<span data-ttu-id="cac42-163">Además, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) y [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) permiten el uso del valor enumerar \_ todos los \_ calendarios para solicitar una enumeración de todos los calendarios aplicables.</span><span class="sxs-lookup"><span data-stu-id="cac42-163">In addition, [**EnumCalendarInfo**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoa) and [**EnumCalendarInfoEx**](/windows/desktop/api/Winnls/nf-winnls-enumcalendarinfoexa) allow the use of the value ENUM\_ALL\_CALENDARS to request an enumeration of all applicable calendars.</span></span>

<span data-ttu-id="cac42-164">Value</span><span class="sxs-lookup"><span data-stu-id="cac42-164">Value</span></span>

<span data-ttu-id="cac42-165">Significado</span><span class="sxs-lookup"><span data-stu-id="cac42-165">Meaning</span></span>

<span data-ttu-id="cac42-166">0xFFFFFFFF</span><span class="sxs-lookup"><span data-stu-id="cac42-166">0xffffffff</span></span>

<span data-ttu-id="cac42-167">ENUMERAr \_ todos los \_ calendarios</span><span class="sxs-lookup"><span data-stu-id="cac42-167">ENUM\_ALL\_CALENDARS</span></span>

<span data-ttu-id="cac42-168">Todos los calendarios aplicables para la configuración regional especificada</span><span class="sxs-lookup"><span data-stu-id="cac42-168">All applicable calendars for the specified locale</span></span>



 

 

 
