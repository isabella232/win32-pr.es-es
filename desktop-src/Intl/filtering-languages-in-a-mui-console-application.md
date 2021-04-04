---
description: Una aplicación de consola de MUI puede admitir la configuración del sistema o la configuración específica de la aplicación para sus idiomas de interfaz de usuario. En este tema se describe el filtrado de idiomas para este tipo de aplicación.
ms.assetid: 6d3c491f-3f5e-4592-aada-49b8b415b497
title: Filtrar idiomas en una aplicación de consola de MUI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d484835af211f59cc559f8e1cd0dd414af13a8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910121"
---
# <a name="filtering-languages-in-a-mui-console-application"></a><span data-ttu-id="ffce1-104">Filtrar idiomas en una aplicación de consola de MUI</span><span class="sxs-lookup"><span data-stu-id="ffce1-104">Filtering Languages in a MUI Console Application</span></span>

<span data-ttu-id="ffce1-105">Una aplicación de consola de MUI puede admitir la configuración del sistema o la configuración específica de la aplicación para sus idiomas de interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ffce1-105">A MUI console application can support either system settings or application-specific settings for its user interface languages.</span></span> <span data-ttu-id="ffce1-106">En este tema se describe el filtrado de idiomas para este tipo de aplicación.</span><span class="sxs-lookup"><span data-stu-id="ffce1-106">This topic discusses the filtering of languages for this type of application.</span></span>

## <a name="limit-the-languages-to-display"></a><span data-ttu-id="ffce1-107">Limitar los idiomas para mostrar</span><span class="sxs-lookup"><span data-stu-id="ffce1-107">Limit the Languages to Display</span></span>

<span data-ttu-id="ffce1-108">A diferencia de las ventanas gráficas, la consola de Windows no puede mostrar [scripts complejos](uniscribe-glossary.md), como árabe, hebreo, persa, Hindi, Urdu, tailandés y muchos otros.</span><span class="sxs-lookup"><span data-stu-id="ffce1-108">Unlike a graphical window, the Windows console cannot display [complex scripts](uniscribe-glossary.md), such as Arabic, Hebrew, Persian, Hindi, Urdu, Thai, and many others.</span></span> <span data-ttu-id="ffce1-109">Por lo tanto, la consola no puede mostrar muchos idiomas de la interfaz de usuario en ninguna circunstancia.</span><span class="sxs-lookup"><span data-stu-id="ffce1-109">Therefore, many user interface languages cannot be displayed by the console under any circumstances.</span></span>

<span data-ttu-id="ffce1-110">La consola de solo puede mostrar caracteres de la [Página de códigos OEM](code-pages.md) única asociada al idioma actual para aplicaciones no Unicode.</span><span class="sxs-lookup"><span data-stu-id="ffce1-110">The console can display only characters from the single [OEM code page](code-pages.md) associated with the current language for non-Unicode applications.</span></span> <span data-ttu-id="ffce1-111">Para cada página de códigos de OEM, la consola de usa una fuente determinada, y es posible que esto no proporcione una cobertura completa para esa página de códigos.</span><span class="sxs-lookup"><span data-stu-id="ffce1-111">For each OEM code page, the console uses a particular font, and this might not provide full coverage for that code page.</span></span>

<span data-ttu-id="ffce1-112">Estas limitaciones relacionadas con la consola reducen el número de idiomas de interfaz de usuario que la consola de puede mostrar en un equipo determinado.</span><span class="sxs-lookup"><span data-stu-id="ffce1-112">These console-related limitations reduce the number of user interface languages that the console can display on a particular computer.</span></span> <span data-ttu-id="ffce1-113">Por ejemplo, si el idioma actual de las aplicaciones que no son Unicode es el japonés y el usuario intenta mostrar texto en alemán en la consola, los caracteres con diéresis no se muestran correctamente.</span><span class="sxs-lookup"><span data-stu-id="ffce1-113">For example, if the current language for non-Unicode applications is Japanese and the user tries to display German text in the console, characters with umlauts do not display correctly.</span></span> <span data-ttu-id="ffce1-114">Si el idioma actual de las aplicaciones que no son Unicode es el alemán y el usuario desea mostrar texto en japonés en la consola, los resultados son mucho peores, lo que representa el texto prácticamente incomprensible.</span><span class="sxs-lookup"><span data-stu-id="ffce1-114">If the current language for non-Unicode applications is German and the user wants to display Japanese text in the console, the results are much worse, rendering the text almost incomprehensible.</span></span>

> [!Note]  
> <span data-ttu-id="ffce1-115">Al proporcionar compatibilidad con la consola para las aplicaciones de MUI, recuerde que la consola solo proporciona compatibilidad limitada para los [editores de métodos de entrada](input-method-manager.md).</span><span class="sxs-lookup"><span data-stu-id="ffce1-115">When providing console support for your MUI applications, remember that the console provides only limited support for [input method editors](input-method-manager.md).</span></span>

 

## <a name="set-the-language-for-console-output"></a><span data-ttu-id="ffce1-116">Establecer el idioma para la salida de la consola</span><span class="sxs-lookup"><span data-stu-id="ffce1-116">Set the Language for Console Output</span></span>

<span data-ttu-id="ffce1-117">En Windows Vista y versiones posteriores, una aplicación de consola establece el idioma para que admita la presentación de la consola mediante una llamada a [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span><span class="sxs-lookup"><span data-stu-id="ffce1-117">On Windows Vista and later, a console application sets the language to support the console display by calling [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span> <span data-ttu-id="ffce1-118">En esta llamada, la aplicación pasa el \_ \_ filtro de la consola de MUI en el parámetro *dwFlags* y **null** para *pwszLanguagesBuffer*.</span><span class="sxs-lookup"><span data-stu-id="ffce1-118">In this call, the application passes MUI\_CONSOLE\_FILTER in the *dwFlags* parameter and **NULL** for *pwszLanguagesBuffer*.</span></span> <span data-ttu-id="ffce1-119">Una alternativa es llamar a [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificador de idioma de 0.</span><span class="sxs-lookup"><span data-stu-id="ffce1-119">An alternative is to call [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span> <span data-ttu-id="ffce1-120">Esta configuración hace que la función Seleccione el idioma que mejor admite la presentación de la consola.</span><span class="sxs-lookup"><span data-stu-id="ffce1-120">This setting causes the function to select the language that best supports the console display.</span></span>

<span data-ttu-id="ffce1-121">En Windows XP, la aplicación solo puede establecer el idioma para la salida de la consola mediante una llamada a [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) con un identificador de idioma de 0.</span><span class="sxs-lookup"><span data-stu-id="ffce1-121">On Windows XP, the application can only set the language for console output by calling [**SetThreadUILanguage**](/windows/win32/api/winnls/nf-winnls-setthreaduilanguage) with a language identifier of 0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffce1-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ffce1-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffce1-123">Configuración de las preferencias de idioma de la aplicación</span><span class="sxs-lookup"><span data-stu-id="ffce1-123">Setting Application Language Preferences</span></span>](setting-application-language-preferences.md)
</dt> </dl>

 

 
