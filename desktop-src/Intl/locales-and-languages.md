---
description: El término &\# 0034; language&\# 0034; indica una colección de propiedades utilizadas en la comunicación oral y escrita.
ms.assetid: 8214c00d-4ec6-4597-8088-7819a160f0dc
title: Configuraciones regionales e idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df2c0d0fa41b9186b2135d9497d52de24577bbae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687098"
---
# <a name="locales-and-languages"></a><span data-ttu-id="74266-103">Configuraciones regionales e idiomas</span><span class="sxs-lookup"><span data-stu-id="74266-103">Locales and Languages</span></span>

<span data-ttu-id="74266-104">El término "idioma" indica una colección de propiedades que se utilizan en la comunicación escrita y oral.</span><span class="sxs-lookup"><span data-stu-id="74266-104">The term "language" indicates a collection of properties used in spoken and written communication.</span></span> <span data-ttu-id="74266-105">Cada idioma tiene un nombre de idioma y un identificador de idioma que indican la [Página de códigos](code-pages.md) determinada (ANSI, dos, Macintosh) que se usa para representar la [ubicación geográfica](table-of-geographical-locations.md) del idioma en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="74266-105">Each language has a language name and a language identifier that indicate the particular [code page](code-pages.md) (ANSI, DOS, Macintosh) used to represent the [geographical location](table-of-geographical-locations.md) for the language on the operating system.</span></span> <span data-ttu-id="74266-106">Un idioma neutro se indica con un nombre como "en" para inglés.</span><span class="sxs-lookup"><span data-stu-id="74266-106">A neutral language is indicated by a name such as "en" for English.</span></span> <span data-ttu-id="74266-107">Un idioma más específico geográficamente puede indicarse mediante un nombre que incluya información de configuración regional y país o región.</span><span class="sxs-lookup"><span data-stu-id="74266-107">A more geographically specific language can be indicated by a name that includes both locale and country/region information.</span></span> <span data-ttu-id="74266-108">Por ejemplo, la configuración regional inglés (Estados Unidos) tiene el nombre de idioma "en-US".</span><span class="sxs-lookup"><span data-stu-id="74266-108">For example, the locale English (United States) has the language name "en-US".</span></span>

<span data-ttu-id="74266-109">Una "configuración regional" es una colección de información de preferencias de usuario relacionada con el lenguaje que se representa como una lista de valores.</span><span class="sxs-lookup"><span data-stu-id="74266-109">A "locale" is a collection of language-related user preference information represented as a list of values.</span></span> <span data-ttu-id="74266-110">Windows XP admite más de 150 configuraciones regionales y Windows Vista admite aproximadamente 200.</span><span class="sxs-lookup"><span data-stu-id="74266-110">Windows XP supports more than 150 locales, and Windows Vista supports about 200.</span></span> <span data-ttu-id="74266-111">Cada configuración regional se define mediante un lenguaje y un criterio de ordenación, y tiene un nombre de configuración regional y un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="74266-111">Each locale is defined by a language and a sort order, and has both a locale name and a locale identifier.</span></span> <span data-ttu-id="74266-112">Un ejemplo de un nombre de configuración regional para alemán (Alemania) es "de-DE la \_ Guía de teléfonos".</span><span class="sxs-lookup"><span data-stu-id="74266-112">An example of a locale name for German (Germany) is "de-DE\_phonebook".</span></span>

<span data-ttu-id="74266-113">Cada sistema operativo tiene al menos una configuración regional instalada y a menudo tiene muchas configuraciones regionales desde las que el usuario puede seleccionar.</span><span class="sxs-lookup"><span data-stu-id="74266-113">Each operating system has at least one installed locale and often has many locales from which the user can select.</span></span> <span data-ttu-id="74266-114">Cada configuración regional tiene una gran variedad de información asociada, aparte de su nombre y identificador.</span><span class="sxs-lookup"><span data-stu-id="74266-114">Each locale has a variety of information associated with it, other than its name and identifier.</span></span> <span data-ttu-id="74266-115">Los tipos de información de configuración regional se describen en [constantes de información de configuración regional](locale-information-constants.md).</span><span class="sxs-lookup"><span data-stu-id="74266-115">Locale information types are described in [Locale Information Constants](locale-information-constants.md).</span></span>

<span data-ttu-id="74266-116">El sistema operativo asigna una configuración regional a cada subproceso, asignando inicialmente la "configuración regional predeterminada del sistema", definida por el [ \_ \_ valor predeterminado del sistema de configuración regional](locale-system-default.md).</span><span class="sxs-lookup"><span data-stu-id="74266-116">The operating system assigns a locale to each thread, initially assigning the "system default locale," defined by [LOCALE\_SYSTEM\_DEFAULT](locale-system-default.md).</span></span> <span data-ttu-id="74266-117">Esta configuración regional se establece cuando se instala el sistema operativo o cuando el usuario lo selecciona mediante la parte de configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="74266-117">This locale is set when the operating system is installed or when the user selects it using the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="74266-118">Cuando se ejecuta un subproceso en un proceso que pertenece al usuario, el sistema operativo asigna la "configuración regional predeterminada del usuario" al subproceso.</span><span class="sxs-lookup"><span data-stu-id="74266-118">When running a thread in a process belonging to the user, the operating system assigns the "user default locale" to the thread.</span></span> <span data-ttu-id="74266-119">Esta configuración regional se define mediante el [ \_ \_ valor predeterminado de usuario de configuración regional](locale-user-default.md).</span><span class="sxs-lookup"><span data-stu-id="74266-119">This locale is defined by [LOCALE\_USER\_DEFAULT](locale-user-default.md).</span></span> <span data-ttu-id="74266-120">Una aplicación puede invalidar de forma predeterminada mediante la función [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) para establecer explícitamente la configuración regional de un subproceso.</span><span class="sxs-lookup"><span data-stu-id="74266-120">An application can override either default by using the [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) function to explicitly set the locale for a thread.</span></span>

<span data-ttu-id="74266-121">La implementación de un lenguaje requiere una configuración regional correspondiente.</span><span class="sxs-lookup"><span data-stu-id="74266-121">Implementation of a language requires a corresponding locale.</span></span> <span data-ttu-id="74266-122">El sistema operativo implementa un idioma neutro seleccionando los datos de la configuración regional asociada a una versión específica del idioma, normalmente la configuración regional más generalizada.</span><span class="sxs-lookup"><span data-stu-id="74266-122">The operating system implements a neutral language by selecting the data for the locale associated with a specific version of the language, usually the most widespread locale.</span></span>

<span data-ttu-id="74266-123">A partir de Windows Vista, es posible que un idioma determinado se corresponda con una configuración regional complementaria, que es un tipo de configuración regional personalizada.</span><span class="sxs-lookup"><span data-stu-id="74266-123">Starting with Windows Vista, it is possible for a particular language to correspond to a supplemental locale, which is a type of custom locale.</span></span> <span data-ttu-id="74266-124">Como las configuraciones regionales complementarias comparten un único identificador de configuración regional, las aplicaciones deben controlar estas configuraciones regionales y los idiomas correspondientes por nombre en lugar de por identificador.</span><span class="sxs-lookup"><span data-stu-id="74266-124">Since supplemental locales all share a single locale identifier, your applications should handle these locales and the corresponding languages by name instead of by identifier.</span></span>

<span data-ttu-id="74266-125">Los conceptos del lenguaje están estrechamente relacionados con los conceptos de configuración regional, pero los dos términos no son intercambiables.</span><span class="sxs-lookup"><span data-stu-id="74266-125">Language concepts are closely related to locale concepts, but the two terms are not interchangeable.</span></span> <span data-ttu-id="74266-126">Como norma general, las funciones relacionadas con la [interfaz de usuario multilingüe](multilingual-user-interface.md) se ocupan de los lenguajes, mientras que las funciones NLS actúan en configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="74266-126">As a general rule, functions related to the [Multilingual User Interface](multilingual-user-interface.md) deal with languages, while the NLS functions act upon locales.</span></span>

<span data-ttu-id="74266-127">En esta sección se tratan los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="74266-127">The following topics are covered in this section:</span></span>

-   [<span data-ttu-id="74266-128">Configuraciones regionales personalizadas</span><span class="sxs-lookup"><span data-stu-id="74266-128">Custom Locales</span></span>](custom-locales.md)
-   [<span data-ttu-id="74266-129">Identificadores de idioma</span><span class="sxs-lookup"><span data-stu-id="74266-129">Language Identifiers</span></span>](language-identifiers.md)
-   [<span data-ttu-id="74266-130">Nombres de idioma</span><span class="sxs-lookup"><span data-stu-id="74266-130">Language Names</span></span>](language-names.md)
-   [<span data-ttu-id="74266-131">Identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="74266-131">Locale Identifiers</span></span>](locale-identifiers.md)
-   [<span data-ttu-id="74266-132">Nombres de configuración regional</span><span class="sxs-lookup"><span data-stu-id="74266-132">Locale Names</span></span>](locale-names.md)
-   [<span data-ttu-id="74266-133">Pseudo-configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="74266-133">Pseudo-Locales</span></span>](pseudo-locales.md)

## <a name="related-topics"></a><span data-ttu-id="74266-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="74266-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74266-135">Acerca de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="74266-135">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="74266-136">Páginas de códigos</span><span class="sxs-lookup"><span data-stu-id="74266-136">Code Pages</span></span>](code-pages.md)
</dt> <dt>

[<span data-ttu-id="74266-137">Constantes de información de configuración regional</span><span class="sxs-lookup"><span data-stu-id="74266-137">Locale Information Constants</span></span>](locale-information-constants.md)
</dt> <dt>

[<span data-ttu-id="74266-138">Interfaz de usuario multilingüe</span><span class="sxs-lookup"><span data-stu-id="74266-138">Multilingual User Interface</span></span>](multilingual-user-interface.md)
</dt> <dt>

[<span data-ttu-id="74266-139">Tabla de ubicaciones geográficas</span><span class="sxs-lookup"><span data-stu-id="74266-139">Table of Geographical Locations</span></span>](table-of-geographical-locations.md)
</dt> <dt>

[<span data-ttu-id="74266-140">Administración del idioma de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="74266-140">User Interface Language Management</span></span>](user-interface-language-management.md)
</dt> <dt>

[<span data-ttu-id="74266-141">**SetThreadLocale**</span><span class="sxs-lookup"><span data-stu-id="74266-141">**SetThreadLocale**</span></span>](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale)
</dt> </dl>

 

 



