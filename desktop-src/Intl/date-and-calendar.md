---
description: Cada configuración regional tiene un tipo de calendario predeterminado (tipo de datos CALTYPE) asociado. Una configuración regional también puede tener un tipo de calendario alternativo. Para más información sobre los tipos de calendario, vea información de tipo de calendario.
ms.assetid: 32772cba-eb30-4cd3-adaf-57fb8425a6d5
title: Fecha y calendario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a3c21965bfbf8c4215b478e5c3b4adbae579ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912554"
---
# <a name="date-and-calendar"></a><span data-ttu-id="239ca-105">Fecha y calendario</span><span class="sxs-lookup"><span data-stu-id="239ca-105">Date and Calendar</span></span>

<span data-ttu-id="239ca-106">Cada [configuración regional](locales-and-languages.md) tiene un tipo de calendario predeterminado (tipo de datos CALTYPE) asociado.</span><span class="sxs-lookup"><span data-stu-id="239ca-106">Each [locale](locales-and-languages.md) has a default calendar type (data type CALTYPE) associated with it.</span></span> <span data-ttu-id="239ca-107">Una configuración regional también puede tener un tipo de calendario alternativo.</span><span class="sxs-lookup"><span data-stu-id="239ca-107">A locale can also have an alternate calendar type.</span></span> <span data-ttu-id="239ca-108">Para más información sobre los tipos de calendario, vea [información de tipo de calendario](calendar-type-information.md).</span><span class="sxs-lookup"><span data-stu-id="239ca-108">For details of calendar types, see [Calendar Type Information](calendar-type-information.md).</span></span>

> [!Note]  
> <span data-ttu-id="239ca-109">Para usar un tipo de calendario alternativo para una configuración regional, la aplicación debe establecer la constante [ \_ IOPTIONALCALENDAR de configuración regional](locale-ioptionalcalendar.md) en el tipo de calendario alternativo para la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="239ca-109">To use an alternate calendar type for a locale, your application must set the [LOCALE\_IOPTIONALCALENDAR](locale-ioptionalcalendar.md) constant to the alternate calendar type for the locale.</span></span>

 

<span data-ttu-id="239ca-110">La mayoría de las configuraciones regionales utilizan el calendario gregoriano estándar y un número establecido de formatos de fecha.</span><span class="sxs-lookup"><span data-stu-id="239ca-110">Most locales use the standard Gregorian calendar and a set number of date formats.</span></span> <span data-ttu-id="239ca-111">Estas opciones predeterminadas para formatos de fecha están disponibles para su presentación mediante la función [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) o [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) .</span><span class="sxs-lookup"><span data-stu-id="239ca-111">These default choices for date formats are available for display by using the [**EnumDateFormatsEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa) or [**EnumDateFormatsExEx**](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex) function.</span></span>

<span data-ttu-id="239ca-112">Algunas configuraciones regionales requieren consideraciones especiales a la hora de crear una lista completa de opciones de formato.</span><span class="sxs-lookup"><span data-stu-id="239ca-112">Some locales require special considerations when creating a complete list of format choices.</span></span> <span data-ttu-id="239ca-113">Algunas de estas configuraciones regionales requieren que se inserten cadenas de texto en la cadena de formato de fecha, mientras que otras requieren un método completamente diferente de cálculo de los valores.</span><span class="sxs-lookup"><span data-stu-id="239ca-113">Some of these locales require text strings to be inserted in the date format string, while others require a completely different method of computation of the values.</span></span> <span data-ttu-id="239ca-114">Una aplicación aborda estos requisitos especiales mediante la adición de determinados tipos de información de configuración regional y tipos de calendario.</span><span class="sxs-lookup"><span data-stu-id="239ca-114">An application addresses these special requirements by the addition of certain locale information types and calendar types.</span></span>

<span data-ttu-id="239ca-115">Para obtener más información sobre cómo implementar fechas y calendarios en las aplicaciones, vea [recuperar información de fecha y hora](retrieving-time-and-date-information.md).</span><span class="sxs-lookup"><span data-stu-id="239ca-115">For details about implementing dates and calendars in your applications, see [Retrieving Time and Date Information](retrieving-time-and-date-information.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="239ca-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="239ca-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="239ca-117">Acerca de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="239ca-117">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="239ca-118">Información de tipo de calendario</span><span class="sxs-lookup"><span data-stu-id="239ca-118">Calendar Type Information</span></span>](calendar-type-information.md)
</dt> <dt>

[<span data-ttu-id="239ca-119">Recuperar información de fecha y hora</span><span class="sxs-lookup"><span data-stu-id="239ca-119">Retrieving Time and Date Information</span></span>](retrieving-time-and-date-information.md)
</dt> <dt>

[<span data-ttu-id="239ca-120">**EnumDateFormatsEx**</span><span class="sxs-lookup"><span data-stu-id="239ca-120">**EnumDateFormatsEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)
</dt> <dt>

[<span data-ttu-id="239ca-121">**EnumDateFormatsExEx**</span><span class="sxs-lookup"><span data-stu-id="239ca-121">**EnumDateFormatsExEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)
</dt> </dl>

 

 



