---
title: Novedades (controles de Windows)
description: En este tema se describen las diferencias entre la compatibilidad con temas y estilos visuales entre Windows 8 y versiones anteriores de Windows.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488711"
---
# <a name="whats-new-windows-controls"></a><span data-ttu-id="c3282-103">Novedades (controles de Windows)</span><span class="sxs-lookup"><span data-stu-id="c3282-103">What's New (Windows Controls)</span></span>

<span data-ttu-id="c3282-104">En este tema se describen las diferencias entre la compatibilidad con temas y estilos visuales entre Windows 8 y versiones anteriores de Windows.</span><span class="sxs-lookup"><span data-stu-id="c3282-104">This topic describes the differences in support for theming and visual styles between Windows 8 and previous versions of Windows .</span></span>

## <a name="through-windows-7"></a><span data-ttu-id="c3282-105">A través de Windows 7</span><span class="sxs-lookup"><span data-stu-id="c3282-105">Through Windows 7</span></span>

<span data-ttu-id="c3282-106">A través de Windows 7, los estilos visuales están activados de forma predeterminada, pero el usuario puede desactivarlos seleccionando el tema clásico de Windows o desactivando el servicio de temas.</span><span class="sxs-lookup"><span data-stu-id="c3282-106">Through Windows 7, visual styles are on by default but the user can turn them off by selecting Windows Classic theme or by turning off the Themes service.</span></span> <span data-ttu-id="c3282-107">Cuando los estilos visuales están desactivados, todas las interfaces de usuario obtienen el aspecto clásico y la mayoría de las API de estilos visuales no están disponibles.</span><span class="sxs-lookup"><span data-stu-id="c3282-107">When visual styles are off, all UI gets the classic look, and most visual styles APIs are not available.</span></span> <span data-ttu-id="c3282-108">El modo de estilos visuales desactivado se ha mantenido a través de Windows 7 para admitir los diversos temas de contraste alto, así como el tema clásico de Windows.</span><span class="sxs-lookup"><span data-stu-id="c3282-108">Visual styles off mode has been retained through Windows 7 to support the various high contrast themes, as well as Windows Classic theme.</span></span> <span data-ttu-id="c3282-109">Si desea admitir tanto estilos visuales como temas de contraste alto en la misma aplicación, normalmente necesitará mantener dos rutas de acceso de código independientes para la representación de controles.</span><span class="sxs-lookup"><span data-stu-id="c3282-109">If you want to support both visual styles and high contrast themes in the same application, you typically need to maintain two separate code paths for rendering controls.</span></span>

## <a name="windows-8-and-later"></a><span data-ttu-id="c3282-110">Windows 8 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="c3282-110">Windows 8 and Later</span></span>

<span data-ttu-id="c3282-111">En Windows 8, los estilos visuales no se pueden desactivar a través de la página **Personalización** de la **configuración del equipo** o desactivando el servicio temas.</span><span class="sxs-lookup"><span data-stu-id="c3282-111">In Windows 8, visual styles can't be turned off through the **Personalization** page of **PC Settings** or by turning off the Themes service.</span></span> <span data-ttu-id="c3282-112">El modo clásico de Windows ya no existe y se ha modificado el modo de contraste alto para trabajar con estilos visuales.</span><span class="sxs-lookup"><span data-stu-id="c3282-112">Windows Classic mode no longer exists, and high contrast mode has been modified to work with visual styles.</span></span> <span data-ttu-id="c3282-113">Debido a estos cambios, las aplicaciones destinadas solo a Windows 8 ya no necesitan dos rutas de acceso de código independientes para admitir los estilos visuales y los temas de contraste alto.</span><span class="sxs-lookup"><span data-stu-id="c3282-113">Because of these changes, applications that target only Windows 8 no longer need two separate code paths to support visual styles and high contrast themes.</span></span>

<span data-ttu-id="c3282-114">Los estilos visuales de Windows 8 incluyen compatibilidad con versiones anteriores del modo de Windows clásico.</span><span class="sxs-lookup"><span data-stu-id="c3282-114">Visual styles in Windows 8 includes backward compatibility support for Windows Classic theming mode.</span></span> <span data-ttu-id="c3282-115">Cualquier código de representación de la interfaz de usuario que funcione en versiones anteriores continuará funcionando en Windows 8 sin modificaciones.</span><span class="sxs-lookup"><span data-stu-id="c3282-115">Any UI rendering code that works on previous versions will continue to work on Windows 8 without modifications.</span></span>

<span data-ttu-id="c3282-116">En Windows 8, si desea que la aplicación admita los temas de contraste alto basados en estilos visuales, debe incluir el GUID de Windows 8 en la sección de compatibilidad del manifiesto de aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3282-116">In Windows 8, if you want your application to support the high contrast themes that are based on visual styles, you need to include the Windows 8 GUID in the compatibility section of your application manifest.</span></span> <span data-ttu-id="c3282-117">De lo contrario, el sistema supone que la aplicación está diseñada para una versión anterior y representa el área cliente mediante la simulación de los temas de contraste alto de Windows clásico.</span><span class="sxs-lookup"><span data-stu-id="c3282-117">Otherwise, the system assumes that the application is designed for a previous version and renders the client area by simulating Windows classic high contrast themes.</span></span> <span data-ttu-id="c3282-118">Para obtener más información, consulte [compatibilidad con temas de contraste alto](supporting-high-contrast-themes.md).</span><span class="sxs-lookup"><span data-stu-id="c3282-118">For more information, see [Supporting High Contrast Themes](supporting-high-contrast-themes.md).</span></span>

<span data-ttu-id="c3282-119">Como en versiones anteriores, Windows 8 es compatible con la versión 5 y la versión 6 de los controles comunes, siendo la versión 5 la predeterminada.</span><span class="sxs-lookup"><span data-stu-id="c3282-119">As in previous versions, Windows 8 supports both version 5 and version 6 of the common controls, with version 5 being the default.</span></span> <span data-ttu-id="c3282-120">Dado que solo la versión 6 admite estilos visuales, debe especificar la versión 6 en el manifiesto de aplicación si desea que los estilos visuales se apliquen a los controles comunes en el área cliente de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="c3282-120">Because only version 6 supports visual styles, you must specify version 6 in your application manifest if you want visual styles to be applied to the common controls in your application's client area.</span></span> <span data-ttu-id="c3282-121">Para obtener más información, vea [habilitar estilos visuales](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c3282-121">For more information, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="c3282-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c3282-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c3282-123">Habilitar los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c3282-123">Enabling Visual Styles</span></span>](cookbook-overview.md)
</dt> <dt>

[<span data-ttu-id="c3282-124">Compatibilidad con temas de contraste alto</span><span class="sxs-lookup"><span data-stu-id="c3282-124">Supporting High Contrast Themes</span></span>](supporting-high-contrast-themes.md)
</dt> <dt>

[<span data-ttu-id="c3282-125">Estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c3282-125">Visual Styles</span></span>](themes-overview.md)
</dt> <dt>

[<span data-ttu-id="c3282-126">Información general sobre los estilos visuales</span><span class="sxs-lookup"><span data-stu-id="c3282-126">Visual Styles Overview</span></span>](visual-styles-overview.md)
</dt> </dl>

 

 




