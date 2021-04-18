---
description: 'Windows Vista y versiones posteriores: NLS define varias configuraciones regionales que se usan además de las configuraciones regionales de Windows existentes.'
ms.assetid: 8ec3038e-da18-47fc-a689-dd9162a41faa
title: Pseudo-Locales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bad7d4b161440cade65f24fb0157d42958c64d19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686717"
---
# <a name="pseudo-locales"></a><span data-ttu-id="17eb3-103">Pseudo-Locales</span><span class="sxs-lookup"><span data-stu-id="17eb3-103">Pseudo-Locales</span></span>

<span data-ttu-id="17eb3-104">**Windows Vista y versiones posteriores:** NLS define varias configuraciones regionales que se usan además de las configuraciones regionales de Windows existentes.</span><span class="sxs-lookup"><span data-stu-id="17eb3-104">**Windows Vista and later:** NLS defines several pseudo-locales for use in addition to the existing Windows locales.</span></span> <span data-ttu-id="17eb3-105">Use estas pseudo-configuraciones regionales para probar la localización de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="17eb3-105">Use these pseudo-locales for testing the localization of your applications.</span></span> <span data-ttu-id="17eb3-106">Para obtener información detallada sobre la implementación, consulte [uso de Pseudo-Locales para las pruebas de localización](using-pseudo-locales-for-localization-testing.md).</span><span class="sxs-lookup"><span data-stu-id="17eb3-106">For implementation details, see [Using Pseudo-Locales for Localization Testing](using-pseudo-locales-for-localization-testing.md).</span></span>

## <a name="supported-pseudo-locales"></a><span data-ttu-id="17eb3-107">Pseudo-Locales admitidos</span><span class="sxs-lookup"><span data-stu-id="17eb3-107">Supported Pseudo-Locales</span></span>

<span data-ttu-id="17eb3-108">Las pseudo configuraciones regionales admitidas por NLS son:</span><span class="sxs-lookup"><span data-stu-id="17eb3-108">The pseudo-locales supported by NLS are:</span></span>

-   <span data-ttu-id="17eb3-109">Pseudo-configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-109">Base pseudo-locale</span></span>
-   <span data-ttu-id="17eb3-110">Pseudo-configuración regional reflejada (de derecha a izquierda)</span><span class="sxs-lookup"><span data-stu-id="17eb3-110">Mirrored (right-to-left) pseudo-locale</span></span>
-   <span data-ttu-id="17eb3-111">Sudeste asiático-idioma</span><span class="sxs-lookup"><span data-stu-id="17eb3-111">East Asian-language pseudo-locale</span></span>

<span data-ttu-id="17eb3-112">Elija la configuración regional específica que se va a usar en función de las asignaciones de páginas de códigos y las cadenas para la localización; por ejemplo, los nombres de los meses y los días.</span><span class="sxs-lookup"><span data-stu-id="17eb3-112">Choose the particular pseudo-locale to use based on its code page assignments and the strings for localization, for example, month names, day names.</span></span> <span data-ttu-id="17eb3-113">Los datos de cada pseudo-configuración regional incluyen no solo las páginas de códigos relevantes y las cadenas de día y mes para la localización, sino también los datos de otros casos de prueba para NLS.</span><span class="sxs-lookup"><span data-stu-id="17eb3-113">Data for each pseudo-locale includes not only relevant code pages and day and month strings for localization, but also data for several other test cases for NLS.</span></span> <span data-ttu-id="17eb3-114">Los casos de prueba examinan los siguientes tipos de datos:</span><span class="sxs-lookup"><span data-stu-id="17eb3-114">The test cases examine the following types of data:</span></span>

-   <span data-ttu-id="17eb3-115">[identificadores de configuración regional](locale-identifiers.md)de 9 bits.</span><span class="sxs-lookup"><span data-stu-id="17eb3-115">9-bit [locale identifiers](locale-identifiers.md).</span></span> <span data-ttu-id="17eb3-116">Las pseudo-configuraciones regionales proporcionan una buena oportunidad para probar el funcionamiento de los identificadores de configuración regional de 9 bits.</span><span class="sxs-lookup"><span data-stu-id="17eb3-116">Pseudo-locales provide a good opportunity to test the operation of 9-bit locale identifiers.</span></span>
-   <span data-ttu-id="17eb3-117">Cadenas de lenguajes que deben usar fuentes pequeñas.</span><span class="sxs-lookup"><span data-stu-id="17eb3-117">Strings from languages that must use small fonts.</span></span> <span data-ttu-id="17eb3-118">Debido a las limitaciones de la interfaz de dispositivo gráfico (GDI), la fuente de la interfaz de usuario para algunos idiomas es más pequeña que la óptima.</span><span class="sxs-lookup"><span data-stu-id="17eb3-118">Because of limitations in the graphics device interface (GDI), the user interface font for some languages is smaller than optimal.</span></span> <span data-ttu-id="17eb3-119">Las configuraciones regionales incluyen varias cadenas de estos lenguajes, combinadas con cadenas de idiomas con control de fuentes más estándar.</span><span class="sxs-lookup"><span data-stu-id="17eb3-119">Pseudo-locales include several strings from these languages, combined with strings from languages with more standard font handling.</span></span> <span data-ttu-id="17eb3-120">Puede utilizar estas cadenas en las pruebas para determinar cómo se representa una fuente limitada por GDI.</span><span class="sxs-lookup"><span data-stu-id="17eb3-120">You can use these strings in testing to determine how a GDI-limited font renders.</span></span>
-   <span data-ttu-id="17eb3-121">Longitudes de cadena inusuales.</span><span class="sxs-lookup"><span data-stu-id="17eb3-121">Unusual string lengths.</span></span> <span data-ttu-id="17eb3-122">Algunas constantes de información de configuración regional, por ejemplo, la [configuración regional \_ SLIST](locale-slist.md) y la [configuración regional \_ ICURRENCY](locale-icurrency.md), tienen límites convencionales en el tamaño de la cadena.</span><span class="sxs-lookup"><span data-stu-id="17eb3-122">Some locale information constants, for example, [LOCALE\_SLIST](locale-slist.md) and [LOCALE\_ICURRENCY](locale-icurrency.md), have conventional limits on string size.</span></span> <span data-ttu-id="17eb3-123">Las pseudo configuraciones regionales admiten el examen de longitudes de cadena variables.</span><span class="sxs-lookup"><span data-stu-id="17eb3-123">The pseudo-locales support the examination of varied string lengths.</span></span>
-   <span data-ttu-id="17eb3-124">Ordenaciones alternativas.</span><span class="sxs-lookup"><span data-stu-id="17eb3-124">Alternate sorts.</span></span> <span data-ttu-id="17eb3-125">Las pseudo configuraciones regionales se pueden usar para probar la funcionalidad de ordenación alternativa cuando el identificador de criterio de [ordenación](sort-order-identifiers.md) alternativo difiere del identificador de criterio de ordenación base que normalmente está asociado a la configuración regional.</span><span class="sxs-lookup"><span data-stu-id="17eb3-125">Pseudo-locales can be used to test alternate sort functionality when the alternate [sort order identifier](sort-order-identifiers.md) differs from the base sort order identifier that is usually associated with the locale.</span></span>

## <a name="pseudo-locale-names-and-identifiers"></a><span data-ttu-id="17eb3-126">Nombres e identificadores de pseudo-configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-126">Pseudo-locale Names and Identifiers</span></span>

<span data-ttu-id="17eb3-127">Las pseudo-configuraciones regionales tienen [nombres de configuración regional](locale-names.md) que se eligen en el espacio de uso privado para evitar conflictos con las posibles cadenas introducidas en los estándares organización internacional de normalización (iso) 639 e ISO 3166.</span><span class="sxs-lookup"><span data-stu-id="17eb3-127">The pseudo-locales have [locale names](locale-names.md) that are chosen from the private use space to avoid conflict with possible strings introduced into the International Organization for Standardization (ISO) 639 and ISO 3166 standards.</span></span> <span data-ttu-id="17eb3-128">Cada pseudo-configuración regional también tiene su propio identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="17eb3-128">Each pseudo-locale also has its own locale identifier.</span></span> <span data-ttu-id="17eb3-129">En la tabla siguiente se proporcionan los nombres y los identificadores de las pseudo configuraciones regionales definidas.</span><span class="sxs-lookup"><span data-stu-id="17eb3-129">The following table provides the names and identifiers for the defined pseudo-locales.</span></span>



| <span data-ttu-id="17eb3-130">Pseudo-configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-130">Pseudo-locale</span></span>       | <span data-ttu-id="17eb3-131">Nombre de configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-131">Locale name</span></span> | <span data-ttu-id="17eb3-132">Identificador de configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-132">Locale identifier</span></span> |
|---------------------|-------------|-------------------|
| <span data-ttu-id="17eb3-133">Base</span><span class="sxs-lookup"><span data-stu-id="17eb3-133">Base</span></span>                | <span data-ttu-id="17eb3-134">QPS-PLOC</span><span class="sxs-lookup"><span data-stu-id="17eb3-134">qps-ploc</span></span>    | <span data-ttu-id="17eb3-135">0501</span><span class="sxs-lookup"><span data-stu-id="17eb3-135">0501</span></span>              |
| <span data-ttu-id="17eb3-136">Reflejado</span><span class="sxs-lookup"><span data-stu-id="17eb3-136">Mirrored</span></span>            | <span data-ttu-id="17eb3-137">QPS-plocm</span><span class="sxs-lookup"><span data-stu-id="17eb3-137">qps-plocm</span></span>   | <span data-ttu-id="17eb3-138">09ff</span><span class="sxs-lookup"><span data-stu-id="17eb3-138">09ff</span></span>              |
| <span data-ttu-id="17eb3-139">Idioma asiático oriental</span><span class="sxs-lookup"><span data-stu-id="17eb3-139">East Asian-language</span></span> | <span data-ttu-id="17eb3-140">QPS-Ploca</span><span class="sxs-lookup"><span data-stu-id="17eb3-140">qps-ploca</span></span>   | <span data-ttu-id="17eb3-141">05fe</span><span class="sxs-lookup"><span data-stu-id="17eb3-141">05fe</span></span>              |



 

## <a name="example"></a><span data-ttu-id="17eb3-142">Ejemplo</span><span class="sxs-lookup"><span data-stu-id="17eb3-142">Example</span></span>

<span data-ttu-id="17eb3-143">En el ejemplo siguiente se muestra el texto que se muestra para una seudoclase de base:</span><span class="sxs-lookup"><span data-stu-id="17eb3-143">The following example shows text displayed for a base pseudo-locale:</span></span>

<span data-ttu-id="17eb3-144">\[Шěđлеśđαỳ!!! \] , 8 ōf \[ Μäŕςћ! \] ōf 2006</span><span class="sxs-lookup"><span data-stu-id="17eb3-144">\[Шěđлеśđαỳ !!!\], 8 ōf \[Μäŕςћ !!\] ōf 2006</span></span>

## <a name="related-topics"></a><span data-ttu-id="17eb3-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="17eb3-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17eb3-146">Configuraciones regionales e idiomas</span><span class="sxs-lookup"><span data-stu-id="17eb3-146">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="17eb3-147">Identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-147">Locale Identifiers</span></span>](locale-identifiers.md)
</dt> <dt>

[<span data-ttu-id="17eb3-148">Nombres de configuración regional</span><span class="sxs-lookup"><span data-stu-id="17eb3-148">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="17eb3-149">Identificadores de criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="17eb3-149">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="17eb3-150">Usar Pseudo-Locales para las pruebas de localización</span><span class="sxs-lookup"><span data-stu-id="17eb3-150">Using Pseudo-Locales for Localization Testing</span></span>](using-pseudo-locales-for-localization-testing.md)
</dt> </dl>

 

 



