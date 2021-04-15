---
description: En Windows Vista y versiones posteriores, puede usar pseudo-configuraciones regionales para probar la localizabilidad de las aplicaciones. En este tema se incluyen procedimientos para usar pseudo-codes.
ms.assetid: 1eccdbb9-a1bd-443a-a5f6-d64c9e5c87b3
title: Usar pseudo-configuraciones regionales para pruebas de localizabilidad
ms.topic: article
ms.date: 07/05/2018
ms.openlocfilehash: f8c6b435b85a5bef98eff9bf76681096779433e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688693"
---
# <a name="using-pseudo-locales-for-localizability-testing"></a><span data-ttu-id="244ed-104">Usar pseudo-configuraciones regionales para pruebas de localizabilidad</span><span class="sxs-lookup"><span data-stu-id="244ed-104">Using pseudo-locales for localizability testing</span></span>

<span data-ttu-id="244ed-105">Las [pseudo configuraciones regionales](pseudo-locales.md) están integradas en Windows Vista y versiones posteriores, por lo que puede tener acceso a ellas a través de las API de compatibilidad con el idioma nacional (NLS).</span><span class="sxs-lookup"><span data-stu-id="244ed-105">[Pseudo-locales](pseudo-locales.md) are built in to Windows Vista and later, so that you can access them via National Language Support (NLS) APIs.</span></span> <span data-ttu-id="244ed-106">Puede usar pseudo-configuraciones regionales para probar la [localizabilidad](/windows/uwp/design/globalizing/globalizing-portal) de las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="244ed-106">You can use pseudo-locales to test the [localizability](/windows/uwp/design/globalizing/globalizing-portal) of your applications.</span></span> <span data-ttu-id="244ed-107">En este tema se incluyen procedimientos para usar pseudo-codes.</span><span class="sxs-lookup"><span data-stu-id="244ed-107">This topic includes procedures for using pseudo-codes.</span></span>

> [!NOTE]
> <span data-ttu-id="244ed-108">Una tarea que necesita una consideración especial en el momento en que se enumeran las configuraciones regionales, ya sea en el código o en la parte configuración regional y de idioma del panel de control.</span><span class="sxs-lookup"><span data-stu-id="244ed-108">One task that needs special consideration when it comes to pseudo-locales is enumerating them; whether in your code, or in the regional and language options portion of the Control Panel.</span></span> <span data-ttu-id="244ed-109">Más adelante en este tema.</span><span class="sxs-lookup"><span data-stu-id="244ed-109">More on that later in this topic.</span></span>

<span data-ttu-id="244ed-110">Los nombres de las pseudo-configuraciones regionales son "QPS-PLOC", "QPS-Ploca" y "QPS-plocm".</span><span class="sxs-lookup"><span data-stu-id="244ed-110">The names of the pseudo-locales are "qps-ploc", "qps-ploca", and "qps-plocm".</span></span> <span data-ttu-id="244ed-111">A partir de Windows 10, también está disponible la pseudo configuración regional "QPS-latn-x-SH".</span><span class="sxs-lookup"><span data-stu-id="244ed-111">As of Windows 10, the pseudo-locale "qps-Latn-x-sh" is also available.</span></span>

## <a name="retrieve-information-about-pseudo-locales"></a><span data-ttu-id="244ed-112">Recuperación de información acerca de las pseudo-configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="244ed-112">Retrieve information about pseudo-locales</span></span>

<span data-ttu-id="244ed-113">Puede usar [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) para recuperar información sobre una pseudo-configuración regional.</span><span class="sxs-lookup"><span data-stu-id="244ed-113">You can use [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) to retrieve information about a pseudo-locale.</span></span> <span data-ttu-id="244ed-114">Pase a la función el nombre de la pseudo-configuración regional concreta (vea la lista de nombres anteriores).</span><span class="sxs-lookup"><span data-stu-id="244ed-114">Pass into the function the name of the particular pseudo-locale (see the list of names above).</span></span> <span data-ttu-id="244ed-115">Por ejemplo, "QPS-plocm" para la pseudo-configuración regional reflejada.</span><span class="sxs-lookup"><span data-stu-id="244ed-115">For example, "qps-plocm" for the mirrored pseudo-locale.</span></span>

```cpp
wchar_t languageIdentifier[5];
int rc{ ::GetLocaleInfoEx(L"qps-plocm", LOCALE_ILANGUAGE, languageIdentifier, 5) };
```

## <a name="use-localenametolcid-with-pseudo-locales"></a><span data-ttu-id="244ed-116">Uso de LocaleNameToLCID con pseudo-configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="244ed-116">Use LocaleNameToLCID with pseudo-locales</span></span>

<span data-ttu-id="244ed-117">Puede llamar a la función de asignación NLS [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) con el nombre de una pseudo-configuración regional.</span><span class="sxs-lookup"><span data-stu-id="244ed-117">You can call the NLS mapping function [**LocaleNameToLCID**](/windows/desktop/api/Winnls/nf-winnls-localenametolcid) with the name of a pseudo-locale.</span></span>

```cpp
LCID lcid{ ::LocaleNameToLCID(L"qps-plocm", 0) };
```

## <a name="enable-pseudo-locales-for-enumeration"></a><span data-ttu-id="244ed-118">Habilitar las pseudo-configuraciones regionales para la enumeración</span><span class="sxs-lookup"><span data-stu-id="244ed-118">Enable pseudo-locales for enumeration</span></span>

<span data-ttu-id="244ed-119">En la aplicación, puede llamar a [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) para enumerar las configuraciones regionales que reconoce el sistema.</span><span class="sxs-lookup"><span data-stu-id="244ed-119">In your application, you can call [**EnumSystemLocalesEx**](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex) to enumerate the locales that the system recognizes.</span></span> <span data-ttu-id="244ed-120">La parte de las opciones de configuración regional y de idioma del panel de control también llama a **EnumSystemLocalesEx** para generar la lista de configuraciones regionales que muestra.</span><span class="sxs-lookup"><span data-stu-id="244ed-120">The regional and language options portion of the Control Panel also calls **EnumSystemLocalesEx** to build the list of locales that it displays.</span></span> <span data-ttu-id="244ed-121">Sin embargo, de forma predeterminada, el sistema no reconoce las cuatro pseudo configuraciones regionales mencionadas anteriormente, por lo que **EnumSystemLocalesEx** no las devolverá.</span><span class="sxs-lookup"><span data-stu-id="244ed-121">However, by default, the four pseudo-locales listed above are not recognized by the system, so they won't be returned by **EnumSystemLocalesEx**.</span></span> <span data-ttu-id="244ed-122">En el caso de los sistemas desde Windows vista hasta la versión 1709 de Windows 10, la solución es habilitar las pseudo-configuraciones regionales agregando claves al registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="244ed-122">For systems from Windows Vista up to and including Windows 10, version 1709, the solution is to enable pseudo-locales by adding keys to the Windows Registry.</span></span>

<span data-ttu-id="244ed-123">Las modificaciones se realizan en la clave de \_ \_ \\ NLS del control System de la máquina local HKEY \\ \\ \\ para los idiomas instalados en el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="244ed-123">The edits are made under the HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Nls key for the languages installed on the operating system.</span></span> <span data-ttu-id="244ed-124">Puede establecer esta configuración para habilitar las pseudo configuraciones regionales.</span><span class="sxs-lookup"><span data-stu-id="244ed-124">You can make these settings to enable the pseudo-locales.</span></span> <span data-ttu-id="244ed-125">Cada clave que se muestra a continuación es el LCID hexadecimal correspondiente a la configuración regional que se está habilitando.</span><span class="sxs-lookup"><span data-stu-id="244ed-125">Each key shown below is the hexadecimal LCID corresponding to the pseudo-locale being enabled.</span></span> <span data-ttu-id="244ed-126">Cada valor es de tipo String (REG \_ SZ).</span><span class="sxs-lookup"><span data-stu-id="244ed-126">Each value is of type string (REG\_SZ).</span></span>

```
[HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Nls\Locale]
"00000501"="1" // qps-ploc (Windows Vista and later)
"000005fe"="7" // qps-ploca (Windows Vista and later)
"00000901"="1" // qps-Latn-x-sh (Windows 10 and later)
"000009ff"="d" // qps-plocm (Windows Vista and later)
```

<span data-ttu-id="244ed-127">En Windows 10, versión 1803, la edición del registro de Windows como esta no tiene ningún efecto.</span><span class="sxs-lookup"><span data-stu-id="244ed-127">For Windows 10, version 1803, editing the Windows Registry like this has no effect.</span></span> <span data-ttu-id="244ed-128">Pero puede seguir llamando a las API NLS sin enumeración con los nombres de las pseudo-configuraciones regionales (vea los ejemplos de código anteriores) para rellenar la interfaz de usuario (UI).</span><span class="sxs-lookup"><span data-stu-id="244ed-128">But you can still call the non-enumerating NLS APIs with the names of the pseudo-locales (see the code examples above) to populate your user interface (UI).</span></span>

## <a name="related-topics"></a><span data-ttu-id="244ed-129">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="244ed-129">Related topics</span></span>

* [<span data-ttu-id="244ed-130">Uso de la compatibilidad con National Language</span><span class="sxs-lookup"><span data-stu-id="244ed-130">Using National Language Support</span></span>](using-national-language-support.md)
* [<span data-ttu-id="244ed-131">Pseudo-configuraciones regionales</span><span class="sxs-lookup"><span data-stu-id="244ed-131">Pseudo-Locales</span></span>](pseudo-locales.md)
* [<span data-ttu-id="244ed-132">EnumSystemLocalesEx</span><span class="sxs-lookup"><span data-stu-id="244ed-132">EnumSystemLocalesEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-enumsystemlocalesex)
* [<span data-ttu-id="244ed-133">GetLocaleInfoEx</span><span class="sxs-lookup"><span data-stu-id="244ed-133">GetLocaleInfoEx</span></span>](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
* [<span data-ttu-id="244ed-134">LocaleNameToLCID</span><span class="sxs-lookup"><span data-stu-id="244ed-134">LocaleNameToLCID</span></span>](/windows/desktop/api/Winnls/nf-winnls-localenametolcid)
