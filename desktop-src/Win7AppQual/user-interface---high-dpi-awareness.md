---
description: .
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Interfaz de usuario: reconocimiento de valores altos de PPP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e93aeed452f421e8e38df8d6d75f6bbe1f97cc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105717300"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="f0bc8-103">Interfaz de usuario: reconocimiento de valores altos de PPP</span><span class="sxs-lookup"><span data-stu-id="f0bc8-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="f0bc8-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="f0bc8-104">Affected Platforms</span></span>

 <span data-ttu-id="f0bc8-105">**Clientes** -Windows XP Windows \| vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="f0bc8-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="f0bc8-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="f0bc8-106">Feature Impact</span></span>

<span data-ttu-id="f0bc8-107">**Gravedad** : medio</span><span class="sxs-lookup"><span data-stu-id="f0bc8-107">**Severity** - Medium</span></span>  
<span data-ttu-id="f0bc8-108">**Frecuencia** : medio</span><span class="sxs-lookup"><span data-stu-id="f0bc8-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="f0bc8-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="f0bc8-109">Description</span></span>

<span data-ttu-id="f0bc8-110">El objetivo es animar a los usuarios finales a establecer sus visualizaciones en la resolución nativa y usar PPP en lugar de la resolución de pantalla para cambiar el tamaño del texto y las imágenes que se muestran.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="f0bc8-111">Windows 7 puede detectar automáticamente y configurar un valor de PPP predeterminado en las instalaciones limpias en los equipos configurados por los OEM mediante la configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="f0bc8-112">Hay herramientas que puede usar para diseñar aplicaciones que tienen un reconocimiento de PPP elevado para garantizar los resultados más legibles.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="f0bc8-113">Hemos agregado dos nuevas características de PPP altas a Windows 7:</span><span class="sxs-lookup"><span data-stu-id="f0bc8-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="f0bc8-114">Configuración de PPP por usuario (antes por equipo)</span><span class="sxs-lookup"><span data-stu-id="f0bc8-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="f0bc8-115">Cambiar PPP sin reinicio (cierre de sesión o inicio de sesión sigue siendo necesario)</span><span class="sxs-lookup"><span data-stu-id="f0bc8-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="f0bc8-116">Manifiesto de impacto</span><span class="sxs-lookup"><span data-stu-id="f0bc8-116">Manifestation of Impact</span></span>

<span data-ttu-id="f0bc8-117">Es probable que las aplicaciones que no controlan el uso de mayúsculas altas de PPP muestren artefactos visuales, como:</span><span class="sxs-lookup"><span data-stu-id="f0bc8-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="f0bc8-118">Recorte de la interfaz de usuario o texto por otros elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f0bc8-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="f0bc8-119">Tamaños de fuente incoherentes</span><span class="sxs-lookup"><span data-stu-id="f0bc8-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="f0bc8-120">Ius de pantalla</span><span class="sxs-lookup"><span data-stu-id="f0bc8-120">Off-screen UIs</span></span>
-   <span data-ttu-id="f0bc8-121">Desenfoque de texto o interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f0bc8-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="f0bc8-122">Arrastre y colocación rotos u otras entradas</span><span class="sxs-lookup"><span data-stu-id="f0bc8-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="f0bc8-123">Representación parcial de las aplicaciones DX en pantalla completa</span><span class="sxs-lookup"><span data-stu-id="f0bc8-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="f0bc8-124">Solución</span><span class="sxs-lookup"><span data-stu-id="f0bc8-124">Solution</span></span>

<span data-ttu-id="f0bc8-125">Para hacer que las aplicaciones sean compatibles con PPP:</span><span class="sxs-lookup"><span data-stu-id="f0bc8-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="f0bc8-126">Realice una prueba funcional de alto nivel, incluida la instalación y desinstalación en la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="f0bc8-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="f0bc8-127">Configuración</span><span class="sxs-lookup"><span data-stu-id="f0bc8-127">Setting</span></span>                                              | <span data-ttu-id="f0bc8-128">Qué se debe tener presente</span><span class="sxs-lookup"><span data-stu-id="f0bc8-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="f0bc8-129">1024x768 a 120 ppp (125% de escala)</span><span class="sxs-lookup"><span data-stu-id="f0bc8-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="f0bc8-130">Esta es una resolución eficaz de ~ 800x600, por lo que debe buscar la interfaz de usuario recortada de los problemas de pantalla o diseño.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="f0bc8-131">Busque también pixelado bitmaps & iconos.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="f0bc8-132">1600x1200 @144 PPP (escala del 150%)</span><span class="sxs-lookup"><span data-stu-id="f0bc8-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="f0bc8-133">Interfaz de usuario borrosa.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-133">Blurry UI.</span></span> <span data-ttu-id="f0bc8-134">Compruebe que todas las operaciones del mouse funcionan, especialmente arrastre & operaciones de colocar.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="f0bc8-135">Compruebe también que los modos de pantalla completa funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="f0bc8-136">1600x1200 @ 144 ppp con la virtualización de PPP deshabilitada</span><span class="sxs-lookup"><span data-stu-id="f0bc8-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="f0bc8-137">A menudo, los botones y la interfaz de usuario no se escalarán en relación con el texto más grande & habrá un recorte significativo del texto.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="f0bc8-138">Busque problemas de diseño en los iconos generales & pixelado bitmats &.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="f0bc8-139">Anote todos los problemas encontrados, incluidos la configuración de la ubicación, la resolución de pantalla y el PPP, y cómo se comporta la aplicación en las demás configuraciones de PPP/resolución para integridad</span><span class="sxs-lookup"><span data-stu-id="f0bc8-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="f0bc8-140">Comprobar cada problema con los problemas de codificación de PPP comunes</span><span class="sxs-lookup"><span data-stu-id="f0bc8-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="f0bc8-141">Evalúe el costo de que la aplicación sea totalmente compatible con el reconocimiento de PPP</span><span class="sxs-lookup"><span data-stu-id="f0bc8-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="f0bc8-142">Haga una lista de los activos de valores altos de PPP necesarios (por ejemplo, botones, iconos)</span><span class="sxs-lookup"><span data-stu-id="f0bc8-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="f0bc8-143">Trabajar y corregir la lista de problemas de PPP encontrados en el paso 1</span><span class="sxs-lookup"><span data-stu-id="f0bc8-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="f0bc8-144">Integre los nuevos recursos del paso 5</span><span class="sxs-lookup"><span data-stu-id="f0bc8-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="f0bc8-145">Declarar el reconocimiento de PPP de la aplicación</span><span class="sxs-lookup"><span data-stu-id="f0bc8-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="f0bc8-146">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="f0bc8-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="f0bc8-147">Vuelva a ejecutar la evaluación de reconocimiento de PPP y compruebe que los problemas se han corregido.</span><span class="sxs-lookup"><span data-stu-id="f0bc8-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="f0bc8-148">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="f0bc8-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="f0bc8-149">Desarrollo de aplicaciones de escritorio de alto nivel de PPP en Windows</span><span class="sxs-lookup"><span data-stu-id="f0bc8-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="f0bc8-150">**Póngase en contacto con para obtener preguntas técnicas:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="f0bc8-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
