---
description: El árabe y muchos otros idiomas tienen formas clásicas para números que son diferentes de los dígitos occidentales convencionales que se usan con más frecuencia en los equipos.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formas de dígito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6e6581b8b0eb87ae09b387c038c1ceba43125ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668417"
---
# <a name="digit-shapes"></a><span data-ttu-id="20aed-103">Formas de dígito</span><span class="sxs-lookup"><span data-stu-id="20aed-103">Digit Shapes</span></span>

<span data-ttu-id="20aed-104">El árabe y muchos otros idiomas tienen formas clásicas para números que son diferentes de los dígitos occidentales convencionales que se usan con más frecuencia en los equipos.</span><span class="sxs-lookup"><span data-stu-id="20aed-104">Arabic and many other languages have classical shapes for numbers that are different from the conventional western digits most often used on computers.</span></span> <span data-ttu-id="20aed-105">Para evitar la ambigüedad en la asignación de nombres a estas formas, en este documento se usan los siguientes nombres del estándar Unicode.</span><span class="sxs-lookup"><span data-stu-id="20aed-105">To avoid ambiguity in naming these shapes, this document uses the following names from the Unicode standard.</span></span>



| <span data-ttu-id="20aed-106">Nombre Unicode de los dígitos</span><span class="sxs-lookup"><span data-stu-id="20aed-106">Unicode name of the digits</span></span>                                     | <span data-ttu-id="20aed-107">País o región donde se usa</span><span class="sxs-lookup"><span data-stu-id="20aed-107">Country/region where used</span></span>                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| <span data-ttu-id="20aed-108">Dígitos europeos</span><span class="sxs-lookup"><span data-stu-id="20aed-108">European digits</span></span>                                                | <span data-ttu-id="20aed-109">Europa, América y muchos otros países o regiones</span><span class="sxs-lookup"><span data-stu-id="20aed-109">Europe, the Americas, and many other countries/regions</span></span>       |
| <span data-ttu-id="20aed-110">Dígitos de Arabic-Indic</span><span class="sxs-lookup"><span data-stu-id="20aed-110">Arabic-Indic digits</span></span>                                            | <span data-ttu-id="20aed-111">Países o regiones árabes (aunque muchos usan dígitos europeos)</span><span class="sxs-lookup"><span data-stu-id="20aed-111">Arabic countries/regions (although many use European digits)</span></span> |
| <span data-ttu-id="20aed-112">Otros dígitos nacionales: dígitos índicos, dígitos tailandeses y similares</span><span class="sxs-lookup"><span data-stu-id="20aed-112">Other national digits: Indic digits, Thai digits, and the like</span></span> | <span data-ttu-id="20aed-113">Varios países o regiones</span><span class="sxs-lookup"><span data-stu-id="20aed-113">Various countries/regions</span></span>                                    |



 

<span data-ttu-id="20aed-114">Unicode proporciona puntos de código independientes para cada forma de dígito.</span><span class="sxs-lookup"><span data-stu-id="20aed-114">Unicode provides separate code points for each digit shape.</span></span> <span data-ttu-id="20aed-115">Por lo tanto, para tener acceso a las formas de dígitos del idioma especial, la aplicación puede usar los códigos de caracteres Unicode pertinentes para los dígitos anteriores, U + 0030 a U + 0039.</span><span class="sxs-lookup"><span data-stu-id="20aed-115">Thus, to access special language digit shapes, your application can use the relevant Unicode character codes for the digits above, U+0030 through U+0039.</span></span> <span data-ttu-id="20aed-116">Estos códigos siempre se muestran con la forma adecuada, en función de la disponibilidad de la fuente.</span><span class="sxs-lookup"><span data-stu-id="20aed-116">These codes are always displayed with the appropriate shape, subject to font availability.</span></span>

<span data-ttu-id="20aed-117">Los códigos de caracteres Unicode U + 0030 a U + 0039 representan nominalmente los dígitos europeos del 0 al 9, pero se puede modificar su forma de dígito.</span><span class="sxs-lookup"><span data-stu-id="20aed-117">The Unicode character codes U+0030 through U+0039 nominally represent the European digits 0 through 9, but their digit shape can be altered.</span></span> <span data-ttu-id="20aed-118">Las API de texto GDI y DirectWrite proporcionan mecanismos para que las aplicaciones controlen este comportamiento.</span><span class="sxs-lookup"><span data-stu-id="20aed-118">GDI and DirectWrite text APIs provide mechanisms for applications to control this behavior.</span></span> <span data-ttu-id="20aed-119">(Vea, por ejemplo, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) o [**IDWriteTextAnalysisSink:: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution)). El comportamiento en algunos controles de Shell y marcos de la interfaz de usuario puede responder a la configuración regional del usuario para la sustitución de dígitos. la configuración [regional \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE se puede usar para obtener la configuración de sustitución de dígitos predeterminada para diferentes configuraciones regionales o la configuración de escritorio del usuario actual para la sustitución de dígitos.</span><span class="sxs-lookup"><span data-stu-id="20aed-119">(See, for instance, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) or [**IDWriteTextAnalysisSink::SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) The behavior in some shell controls and user interface frameworks may respond to user locale settings for digit substitution; the [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE can be used to obtain default digit substitution settings for different locales or the current user's desktop settings for digit substitution.</span></span>

## <a name="native-digits"></a><span data-ttu-id="20aed-120">Dígitos nativos</span><span class="sxs-lookup"><span data-stu-id="20aed-120">Native Digits</span></span>

<span data-ttu-id="20aed-121">Los dígitos nativos son las formas de dígitos que elige el usuario en la hoja de propiedades **número** de la parte configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="20aed-121">Native digits are the digit shapes chosen by the user in the **Number** property sheet in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="20aed-122">Para buscar la presentación de dígitos preferida por el usuario, la aplicación usa la función [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) o [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) con la constante [ \_ SNATIVEDIGITS de configuración regional](locale-snative-constants.md) que representa la información de configuración regional.</span><span class="sxs-lookup"><span data-stu-id="20aed-122">To find the digit presentation preferred by the user, your application uses the [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) or [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) function with the [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) constant representing the locale information.</span></span>

> [!Note]  
> <span data-ttu-id="20aed-123">Normalmente, los códigos de dígitos Unicode se generan en rutinas del sistema operativo en tiempo de ejecución.</span><span class="sxs-lookup"><span data-stu-id="20aed-123">Typically, Unicode digit codes are generated in runtime operating system routines.</span></span> <span data-ttu-id="20aed-124">Por lo tanto, los sistemas operativos en tiempo de ejecución comunes deben actualizarse para que la aplicación inspeccione de forma adecuada la [configuración regional \_ SNATIVEDIGITS](locale-snative-constants.md) .</span><span class="sxs-lookup"><span data-stu-id="20aed-124">Therefore, common runtime operating systems must be upgraded for the application to inspect [LOCALE\_SNATIVEDIGITS](locale-snative-constants.md) appropriately.</span></span>

 

## <a name="digit-substitution"></a><span data-ttu-id="20aed-125">Sustitución de dígitos</span><span class="sxs-lookup"><span data-stu-id="20aed-125">Digit Substitution</span></span>

<span data-ttu-id="20aed-126">La aplicación puede utilizar la sustitución de dígitos para indicar al sistema operativo cómo imprimir dígitos U + 0030 a U + 0039.</span><span class="sxs-lookup"><span data-stu-id="20aed-126">The application can use digit substitution to tell the operating system how to print digits U+0030 through U+0039.</span></span> <span data-ttu-id="20aed-127">La constante [ \_ IDIGITSUBSTITUTION de configuración regional](locale-idigitsubstitution.md) controla esta operación.</span><span class="sxs-lookup"><span data-stu-id="20aed-127">The [LOCALE\_IDIGITSUBSTITUTION](locale-idigitsubstitution.md) constant controls this operation.</span></span>

## <a name="digit-shaping-for-a-single-function"></a><span data-ttu-id="20aed-128">Forma de dígitos para una sola función</span><span class="sxs-lookup"><span data-stu-id="20aed-128">Digit Shaping for a Single Function</span></span>

<span data-ttu-id="20aed-129">Las funciones de [ \_ resultados](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)y GCP tienen marcas que rigen la sustitución de códigos Unicode U + 0030 a u + 0039 mientras dure la llamada a la función.</span><span class="sxs-lookup"><span data-stu-id="20aed-129">The [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa), and [GCP\_RESULTS](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) functions have flags that govern the substitution of Unicode codes U+0030 through U+0039 for the duration of the function call.</span></span> <span data-ttu-id="20aed-130">Estas marcas invalidan la configuración regional en el panel de control, pero no restablecen la configuración.</span><span class="sxs-lookup"><span data-stu-id="20aed-130">These flags override regional settings in the Control Panel, but do not reset the settings.</span></span> <span data-ttu-id="20aed-131">Además, no invalidan los códigos Unicode NADS y nodos.</span><span class="sxs-lookup"><span data-stu-id="20aed-131">Also, they do not override the Unicode codes NADS and NODS.</span></span> <span data-ttu-id="20aed-132">Están disponibles las marcas siguientes.</span><span class="sxs-lookup"><span data-stu-id="20aed-132">The following flags are available.</span></span>



| <span data-ttu-id="20aed-133">Marcas</span><span class="sxs-lookup"><span data-stu-id="20aed-133">Flags</span></span>                 | <span data-ttu-id="20aed-134">Dígitos usados</span><span class="sxs-lookup"><span data-stu-id="20aed-134">Digits used</span></span>                      | <span data-ttu-id="20aed-135">Se usa en</span><span class="sxs-lookup"><span data-stu-id="20aed-135">Used in</span></span>                   |
|-----------------------|----------------------------------|---------------------------|
| <span data-ttu-id="20aed-136">ETO \_ NUMERICSLATIN</span><span class="sxs-lookup"><span data-stu-id="20aed-136">ETO\_NUMERICSLATIN</span></span>    | <span data-ttu-id="20aed-137">Dígitos europeos</span><span class="sxs-lookup"><span data-stu-id="20aed-137">European digits</span></span>                  | <span data-ttu-id="20aed-138">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="20aed-138">**ExtTextOut**</span></span>            |
| <span data-ttu-id="20aed-139">ETO \_ NUMERICSLOCAL</span><span class="sxs-lookup"><span data-stu-id="20aed-139">ETO\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="20aed-140">Dígitos adecuados para la configuración regional</span><span class="sxs-lookup"><span data-stu-id="20aed-140">Digits appropriate to the locale</span></span> | <span data-ttu-id="20aed-141">**ExtTextOut**</span><span class="sxs-lookup"><span data-stu-id="20aed-141">**ExtTextOut**</span></span>            |
| <span data-ttu-id="20aed-142">\_NUMERICSLATIN GCP</span><span class="sxs-lookup"><span data-stu-id="20aed-142">GCP\_NUMERICSLATIN</span></span>    | <span data-ttu-id="20aed-143">Dígitos europeos</span><span class="sxs-lookup"><span data-stu-id="20aed-143">European digits</span></span>                  | <span data-ttu-id="20aed-144">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="20aed-144">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="20aed-145">\_NUMERICSLOCAL GCP</span><span class="sxs-lookup"><span data-stu-id="20aed-145">GCP\_NUMERICSLOCAL</span></span>    | <span data-ttu-id="20aed-146">Dígitos adecuados para la configuración regional</span><span class="sxs-lookup"><span data-stu-id="20aed-146">Digits appropriate to the locale</span></span> | <span data-ttu-id="20aed-147">**GetCharacterPlacement**</span><span class="sxs-lookup"><span data-stu-id="20aed-147">**GetCharacterPlacement**</span></span> |
| <span data-ttu-id="20aed-148">GCPCLASS \_ LATINNUMBER</span><span class="sxs-lookup"><span data-stu-id="20aed-148">GCPCLASS\_LATINNUMBER</span></span> | <span data-ttu-id="20aed-149">Dígitos europeos</span><span class="sxs-lookup"><span data-stu-id="20aed-149">European digits</span></span>                  | <span data-ttu-id="20aed-150">**resultados de GCP \_**</span><span class="sxs-lookup"><span data-stu-id="20aed-150">**GCP\_RESULTS**</span></span>          |
| <span data-ttu-id="20aed-151">GCPCLASS \_ LOCALNUMBER</span><span class="sxs-lookup"><span data-stu-id="20aed-151">GCPCLASS\_LOCALNUMBER</span></span> | <span data-ttu-id="20aed-152">Dígitos adecuados para la configuración regional</span><span class="sxs-lookup"><span data-stu-id="20aed-152">Digits appropriate to the locale</span></span> | <span data-ttu-id="20aed-153">**resultados de GCP \_**</span><span class="sxs-lookup"><span data-stu-id="20aed-153">**GCP\_RESULTS**</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="20aed-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="20aed-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="20aed-155">Acerca de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="20aed-155">About National Language Support</span></span>](about-national-language-support.md)
</dt> <dt>

[<span data-ttu-id="20aed-156">**GetLocaleInfo**</span><span class="sxs-lookup"><span data-stu-id="20aed-156">**GetLocaleInfo**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[<span data-ttu-id="20aed-157">**GetLocaleInfoEx**</span><span class="sxs-lookup"><span data-stu-id="20aed-157">**GetLocaleInfoEx**</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
