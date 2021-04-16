---
description: Cada configuración regional tiene un identificador único, un valor de 32 bits que consta de un identificador de idioma y un identificador de criterio de ordenación.
ms.assetid: ea45b0e5-7df7-47fb-8dad-fccfbe53fec0
title: Identificadores de configuración regional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7b2f11189f44b8555081d589f3e9ba2ed131cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686496"
---
# <a name="locale-identifiers"></a><span data-ttu-id="b50f7-103">Identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="b50f7-103">Locale Identifiers</span></span>

<span data-ttu-id="b50f7-104">Cada [configuración regional](locales-and-languages.md) tiene un identificador único, un valor de 32 bits que consta de un [identificador de idioma](language-identifiers.md) y un identificador de [criterio de ordenación](sort-order-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="b50f7-104">Each [locale](locales-and-languages.md) has a unique identifier, a 32-bit value that consists of a [language identifier](language-identifiers.md) and a [sort order identifier](sort-order-identifiers.md).</span></span> <span data-ttu-id="b50f7-105">El identificador de configuración regional es una abreviatura numérica internacional estándar y tiene los componentes necesarios para identificar de forma única una de las configuraciones regionales definidas por el sistema operativo instaladas.</span><span class="sxs-lookup"><span data-stu-id="b50f7-105">The locale identifier is a standard international numeric abbreviation and has the components necessary to uniquely identify one of the installed operating system-defined locales.</span></span> <span data-ttu-id="b50f7-106">NLS es compatible con los identificadores de configuración regional predefinidos y los identificadores personalizados.</span><span class="sxs-lookup"><span data-stu-id="b50f7-106">NLS supports both predefined locale identifiers and custom identifiers.</span></span>

> [!Note]  
> <span data-ttu-id="b50f7-107">Los nombres de configuración regional se pueden usar con las funciones introducidas en Windows Vista que toman un [nombre de configuración regional](locale-names.md) como parámetro, en lugar de un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b50f7-107">Locale names can be used with functions introduced in Windows Vista that take a [locale name](locale-names.md) as a parameter, instead of a locale identifier.</span></span> <span data-ttu-id="b50f7-108">Para obtener más información, consulte [llamar a las funciones de "nombre de la configuración regional"](calling-the--locale-name--functions.md).</span><span class="sxs-lookup"><span data-stu-id="b50f7-108">For more information, see [Calling the "Locale Name" Functions](calling-the--locale-name--functions.md).</span></span> <span data-ttu-id="b50f7-109">Siempre se prefiere el uso de nombres de configuración regional en lugar de los identificadores de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b50f7-109">Use of locale names instead of locale identifiers is always preferable.</span></span>

 

<span data-ttu-id="b50f7-110">En la ilustración siguiente se muestra el formato de los bits en un identificador de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b50f7-110">The following illustration shows the format of the bits in a locale identifier.</span></span>

``` syntax
+-------------+---------+-------------------------+
|   Reserved  | Sort ID |      Language ID        |
+-------------+---------+-------------------------+
31         20 19     16 15                      0   bit
```

## <a name="predefined-locale-identifiers"></a><span data-ttu-id="b50f7-111">Identificadores de configuración regional predefinidos</span><span class="sxs-lookup"><span data-stu-id="b50f7-111">Predefined Locale Identifiers</span></span>

<span data-ttu-id="b50f7-112">Los identificadores de configuración regional predefinidos que admite NLS se definen en la referencia de la [API de compatibilidad con el idioma nacional (NLS)](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span><span class="sxs-lookup"><span data-stu-id="b50f7-112">The predefined locale identifiers supported by NLS are defined in the [National Language Support (NLS) API Reference](/openspecs/windows_protocols/ms-lcid/a9eac961-e77d-41a6-90a5-ce1a8b0cdb9c).</span></span>

<span data-ttu-id="b50f7-113">NLS usa las siguientes constantes de información de configuración regional para representar los identificadores de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b50f7-113">NLS uses the following locale information constants to represent locale identifiers.</span></span>

-   <span data-ttu-id="b50f7-114">[Configuración \_ regional SLANGUAGE](locale-slanguage.md) o [configuración regional \_ SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span><span class="sxs-lookup"><span data-stu-id="b50f7-114">[LOCALE\_SLANGUAGE](locale-slanguage.md) or [LOCALE\_SLOCALIZEDLANGUAGENAME](locale-slocalized-constants.md)</span></span>
-   [<span data-ttu-id="b50f7-115">configuración regional \_ SNAME</span><span class="sxs-lookup"><span data-stu-id="b50f7-115">LOCALE\_SNAME</span></span>](locale-sname.md)
-   [<span data-ttu-id="b50f7-116">configuración regional \_ SSCRIPTS</span><span class="sxs-lookup"><span data-stu-id="b50f7-116">LOCALE\_SSCRIPTS</span></span>](locale-sscripts.md)
-   [<span data-ttu-id="b50f7-117">configuración regional \_ IDEFAULTANSICODEPAGE</span><span class="sxs-lookup"><span data-stu-id="b50f7-117">LOCALE\_IDEFAULTANSICODEPAGE</span></span>](locale-idefault-constants.md)

## <a name="custom-locale-identifiers"></a><span data-ttu-id="b50f7-118">Identificadores de configuración regional personalizados</span><span class="sxs-lookup"><span data-stu-id="b50f7-118">Custom Locale Identifiers</span></span>

<span data-ttu-id="b50f7-119">**Windows Vista:** NLS es compatible con los identificadores de configuración regional personalizados que representan las siguientes constantes de información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="b50f7-119">**Windows Vista:** NLS supports the custom locale identifiers represented by the following locale information constants.</span></span>

-   [<span data-ttu-id="b50f7-120">CONFIGURACIÓN \_ predeterminada personalizada \_</span><span class="sxs-lookup"><span data-stu-id="b50f7-120">LOCALE\_CUSTOM\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="b50f7-121">CONFIGURACIÓN predeterminada de la \_ \_ interfaz de usuario personalizada \_</span><span class="sxs-lookup"><span data-stu-id="b50f7-121">LOCALE\_CUSTOM\_UI\_DEFAULT</span></span>](locale-custom-constants.md)
-   [<span data-ttu-id="b50f7-122">configuración regional \_ personalizada no \_ especificada</span><span class="sxs-lookup"><span data-stu-id="b50f7-122">LOCALE\_CUSTOM\_UNSPECIFIED</span></span>](locale-custom-constants.md)

## <a name="building-a-locale"></a><span data-ttu-id="b50f7-123">Creación de una configuración regional</span><span class="sxs-lookup"><span data-stu-id="b50f7-123">Building a Locale</span></span>

<span data-ttu-id="b50f7-124">Puede usar la utilidad de configuración regional que proporciona NLS para compilar configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="b50f7-124">You can use the Locale Builder utility provided by NLS to build locales.</span></span> <span data-ttu-id="b50f7-125">Para obtener más información, vea [generador de configuración regional de Microsoft](https://www.microsoft.com/download/details.aspx?id=41158).</span><span class="sxs-lookup"><span data-stu-id="b50f7-125">For more information, see [Microsoft Locale Builder](https://www.microsoft.com/download/details.aspx?id=41158).</span></span>

<span data-ttu-id="b50f7-126">La aplicación puede construir un identificador de configuración regional mediante la macro [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) .</span><span class="sxs-lookup"><span data-stu-id="b50f7-126">Your application can construct a locale identifier using the [**MAKELCID**](/windows/desktop/api/Winnt/nf-winnt-makelcid) macro.</span></span> <span data-ttu-id="b50f7-127">También puede usar uno de los identificadores predeterminados correspondientes a las constantes que se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="b50f7-127">Alternatively it can use one of the default identifiers corresponding to the constants listed below.</span></span>

-   [<span data-ttu-id="b50f7-128">configuración regional \_ INvariable</span><span class="sxs-lookup"><span data-stu-id="b50f7-128">LOCALE\_INVARIANT</span></span>](locale-invariant.md)
-   [<span data-ttu-id="b50f7-129">configuración \_ predeterminada del sistema local \_</span><span class="sxs-lookup"><span data-stu-id="b50f7-129">LOCALE\_SYSTEM\_DEFAULT</span></span>](locale-system-default.md)
-   [<span data-ttu-id="b50f7-130">\_valor predeterminado del usuario de configuración regional \_</span><span class="sxs-lookup"><span data-stu-id="b50f7-130">LOCALE\_USER\_DEFAULT</span></span>](locale-user-default.md)

## <a name="retrieval-of-locale-identifiers"></a><span data-ttu-id="b50f7-131">Recuperación de los identificadores de configuración regional</span><span class="sxs-lookup"><span data-stu-id="b50f7-131">Retrieval of Locale Identifiers</span></span>

<span data-ttu-id="b50f7-132">Una aplicación puede recuperar los identificadores de configuración regional actuales mediante las funciones [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) y [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) .</span><span class="sxs-lookup"><span data-stu-id="b50f7-132">An application can retrieve the current locale identifiers by using the [**GetSystemDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getsystemdefaultlcid) and [**GetUserDefaultLCID**](/windows/desktop/api/Winnls/nf-winnls-getuserdefaultlcid) functions.</span></span> <span data-ttu-id="b50f7-133">Cada subproceso puede establecer y recuperar su propia configuración regional con [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) y [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span><span class="sxs-lookup"><span data-stu-id="b50f7-133">Each thread can set and retrieve its own locale with [**SetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-setthreadlocale) and [**GetThreadLocale**](/windows/desktop/api/Winnls/nf-winnls-getthreadlocale).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b50f7-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b50f7-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b50f7-135">Configuraciones regionales e idiomas</span><span class="sxs-lookup"><span data-stu-id="b50f7-135">Locales and Languages</span></span>](locales-and-languages.md)
</dt> <dt>

[<span data-ttu-id="b50f7-136">Identificadores de idioma</span><span class="sxs-lookup"><span data-stu-id="b50f7-136">Language Identifiers</span></span>](language-identifiers.md)
</dt> <dt>

[<span data-ttu-id="b50f7-137">Nombres de configuración regional</span><span class="sxs-lookup"><span data-stu-id="b50f7-137">Locale Names</span></span>](locale-names.md)
</dt> <dt>

[<span data-ttu-id="b50f7-138">Identificadores de criterio de ordenación</span><span class="sxs-lookup"><span data-stu-id="b50f7-138">Sort Order Identifiers</span></span>](sort-order-identifiers.md)
</dt> <dt>

[<span data-ttu-id="b50f7-139">**MAKELCID**</span><span class="sxs-lookup"><span data-stu-id="b50f7-139">**MAKELCID**</span></span>](/windows/desktop/api/Winnt/nf-winnt-makelcid)
</dt> </dl>

 

 
