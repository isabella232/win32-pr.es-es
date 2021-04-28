---
description: 'Interfaz de usuario: reconocimiento de valores altos de PPP'
ms.assetid: 5b753340-366c-44b3-87e9-19c580f1c5d5
title: 'Interfaz de usuario: reconocimiento de valores altos de PPP'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 118b566d35f753a77f6cfd9706c2e69819f3fbaa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116073"
---
# <a name="user-interface---high-dpi-awareness"></a><span data-ttu-id="77d34-103">Interfaz de usuario: reconocimiento de valores altos de PPP</span><span class="sxs-lookup"><span data-stu-id="77d34-103">User Interface - High DPI Awareness</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="77d34-104">Plataformas afectadas</span><span class="sxs-lookup"><span data-stu-id="77d34-104">Affected Platforms</span></span>

 <span data-ttu-id="77d34-105">**Clientes:** Windows XP \| Windows Vista Windows \| 7</span><span class="sxs-lookup"><span data-stu-id="77d34-105">**Clients** - Windows XP \| Windows Vista \| Windows 7</span></span>  

## <a name="feature-impact"></a><span data-ttu-id="77d34-106">Impacto en las características</span><span class="sxs-lookup"><span data-stu-id="77d34-106">Feature Impact</span></span>

<span data-ttu-id="77d34-107">**Gravedad:** media</span><span class="sxs-lookup"><span data-stu-id="77d34-107">**Severity** - Medium</span></span>  
<span data-ttu-id="77d34-108">**Frecuencia:** media</span><span class="sxs-lookup"><span data-stu-id="77d34-108">**Frequency** - Medium</span></span>  

## <a name="description"></a><span data-ttu-id="77d34-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="77d34-109">Description</span></span>

<span data-ttu-id="77d34-110">El objetivo es animar a los usuarios finales a establecer sus pantallas en resolución nativa y usar PPP en lugar de la resolución de pantalla para cambiar el tamaño del texto y las imágenes mostrados.</span><span class="sxs-lookup"><span data-stu-id="77d34-110">The goal is to encourage end users to set their displays to native resolution and use DPI rather than screen resolution to change the size of displayed text and images.</span></span> <span data-ttu-id="77d34-111">Windows 7 puede detectar y configurar automáticamente un valor predeterminado de PPP en las máquinas configuradas por sus OEM mediante la configuración de PPP.</span><span class="sxs-lookup"><span data-stu-id="77d34-111">Windows 7 can auto-detect and configure a default DPI on clean installs on machines configured by their OEMs using DPI settings.</span></span> <span data-ttu-id="77d34-112">Hay herramientas que puede usar para ayudar a diseñar aplicaciones que tienen en cuenta valores altos de PPP con el fin de garantizar los resultados más legibles.</span><span class="sxs-lookup"><span data-stu-id="77d34-112">There are tools you can use to help design applications that are high DPI aware in order to ensure the most readable results.</span></span>

<span data-ttu-id="77d34-113">Hemos agregado dos nuevas características de valores altos de PPP a Windows 7:</span><span class="sxs-lookup"><span data-stu-id="77d34-113">We have added two new High DPI features to Windows 7:</span></span>

-   <span data-ttu-id="77d34-114">Configuración de PPP por usuario (anteriormente por equipo)</span><span class="sxs-lookup"><span data-stu-id="77d34-114">Per-user DPI setting (previously per machine)</span></span>
-   <span data-ttu-id="77d34-115">Cambio de PPP sin reiniciar (todavía se requiere cierre de sesión o inicio de sesión)</span><span class="sxs-lookup"><span data-stu-id="77d34-115">Change DPI without rebooting (logoff/logon is still required)</span></span>

## <a name="manifestation-of-impact"></a><span data-ttu-id="77d34-116">Demostración del impacto</span><span class="sxs-lookup"><span data-stu-id="77d34-116">Manifestation of Impact</span></span>

<span data-ttu-id="77d34-117">Es probable que las aplicaciones que no controlan el caso de valores altos de PPP expondrán artefactos visuales, entre los que se incluyen:</span><span class="sxs-lookup"><span data-stu-id="77d34-117">Applications that do not handle the high DPI case are likely to exhibit visual artifacts, including:</span></span>

-   <span data-ttu-id="77d34-118">Recorte de la interfaz de usuario o texto por otros elementos de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="77d34-118">Clipping of UI or text by other UI elements</span></span>
-   <span data-ttu-id="77d34-119">Tamaños de fuente incoherentes</span><span class="sxs-lookup"><span data-stu-id="77d34-119">Inconsistent font sizes</span></span>
-   <span data-ttu-id="77d34-120">IOS fuera de la pantalla</span><span class="sxs-lookup"><span data-stu-id="77d34-120">Off-screen UIs</span></span>
-   <span data-ttu-id="77d34-121">Desenfoque de texto o interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="77d34-121">Blurring of text or UI</span></span>
-   <span data-ttu-id="77d34-122">Arrastrar y colocar rotos u otras entradas</span><span class="sxs-lookup"><span data-stu-id="77d34-122">Broken drag-and-drop or other inputs</span></span>
-   <span data-ttu-id="77d34-123">Representación de aplicaciones DX de pantalla completa parcialmente fuera de la pantalla</span><span class="sxs-lookup"><span data-stu-id="77d34-123">Rendering of full-screen DX applications partially off screen</span></span>

## <a name="solution"></a><span data-ttu-id="77d34-124">Solución</span><span class="sxs-lookup"><span data-stu-id="77d34-124">Solution</span></span>

<span data-ttu-id="77d34-125">Para que las aplicaciones tenga en cuenta ppp:</span><span class="sxs-lookup"><span data-stu-id="77d34-125">To make your applications DPI-aware:</span></span>

1.  <span data-ttu-id="77d34-126">Realice una prueba funcional de alto nivel, incluida la instalación y desinstalación en la siguiente configuración:</span><span class="sxs-lookup"><span data-stu-id="77d34-126">Do a high-level functional test pass, including install and uninstall at the following settings:</span></span>

    | <span data-ttu-id="77d34-127">Parámetro</span><span class="sxs-lookup"><span data-stu-id="77d34-127">Setting</span></span>                                              | <span data-ttu-id="77d34-128">Qué se debe tener presente</span><span class="sxs-lookup"><span data-stu-id="77d34-128">What to look for</span></span>                                                                                                                                                      |
    |------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="77d34-129">1024 x 768 a 120 PPP (escalado del 125 %)</span><span class="sxs-lookup"><span data-stu-id="77d34-129">1024x768 @ 120 DPI (125% scaling)</span></span>                    | <span data-ttu-id="77d34-130">Se trata de una resolución efectiva de ~800 x 600, así que busque la interfaz de usuario recortada de la pantalla o los problemas de diseño.</span><span class="sxs-lookup"><span data-stu-id="77d34-130">This is an effective resolution of ~800x600, so look for UI clipped off the screen or layout issues.</span></span> <span data-ttu-id="77d34-131">Busque también mapas de bits con forma de & iconos.</span><span class="sxs-lookup"><span data-stu-id="77d34-131">Also look for pixilated bitmaps & icons.</span></span>                         |
    | <span data-ttu-id="77d34-132">1600 x 1200 @144 PPP (escalado del 150 %)</span><span class="sxs-lookup"><span data-stu-id="77d34-132">1600x1200 @144 DPI (150% scaling)</span></span>                    | <span data-ttu-id="77d34-133">Interfaz de usuario desenfoque.</span><span class="sxs-lookup"><span data-stu-id="77d34-133">Blurry UI.</span></span> <span data-ttu-id="77d34-134">Compruebe que todas las operaciones del mouse funcionan, especialmente para arrastrar & operaciones de colocación.</span><span class="sxs-lookup"><span data-stu-id="77d34-134">Verify that all mouse operations work, especially drag & drop operations.</span></span> <span data-ttu-id="77d34-135">Compruebe también que los modos de pantalla completa funcionan correctamente.</span><span class="sxs-lookup"><span data-stu-id="77d34-135">Also verify full-screen modes work properly.</span></span>                                     |
    | <span data-ttu-id="77d34-136">1600x1200 @ 144 PPP con la virtualización de PPP deshabilitada</span><span class="sxs-lookup"><span data-stu-id="77d34-136">1600x1200 @ 144 DPI with DPI Virtualization Disabled</span></span> | <span data-ttu-id="77d34-137">A menudo, los botones y la interfaz de usuario no se escalan en relación con el texto & habrá un recorte de texto significativo.</span><span class="sxs-lookup"><span data-stu-id="77d34-137">Often buttons and UI won't scale in relation to larger text & there will be significant text clipping.</span></span> <span data-ttu-id="77d34-138">Busque problemas de diseño en general & bits con forma de & iconos.</span><span class="sxs-lookup"><span data-stu-id="77d34-138">Look for layout issues in general & pixilated bitmats & icons.</span></span> |

    

     

2.  <span data-ttu-id="77d34-139">Anote todos los problemas encontrados, incluida la ubicación, la resolución de pantalla y la configuración de PPP, así como el comportamiento de la aplicación en las demás configuraciones de PPP/Resolución para que sea completa.</span><span class="sxs-lookup"><span data-stu-id="77d34-139">Write down all the issues found, including location, screen resolution, and DPI settings, as well as how the application behaves in the other DPI/Resolution configurations for completeness</span></span>
3.  <span data-ttu-id="77d34-140">Comprobar cada problema con los problemas comunes de codificación de PPP</span><span class="sxs-lookup"><span data-stu-id="77d34-140">Check each issue against the Common DPI Coding Issues</span></span>
4.  <span data-ttu-id="77d34-141">Evaluar el costo de hacer que la aplicación sea totalmente compatible con PPP</span><span class="sxs-lookup"><span data-stu-id="77d34-141">Assess the cost of making the application fully DPI aware</span></span>
5.  <span data-ttu-id="77d34-142">Crear una lista de los recursos de valores altos de PPP necesarios (por ejemplo, botones o iconos)</span><span class="sxs-lookup"><span data-stu-id="77d34-142">Make a list of the High DPI assets required (for example, buttons, icons)</span></span>
6.  <span data-ttu-id="77d34-143">Solucionar y corregir la lista de problemas de PPP que se encuentran en el paso 1</span><span class="sxs-lookup"><span data-stu-id="77d34-143">Work through and fix the list of DPI issues found in Step 1</span></span>
7.  <span data-ttu-id="77d34-144">Integración de los nuevos recursos del paso 5</span><span class="sxs-lookup"><span data-stu-id="77d34-144">Integrate the new assets from Step 5</span></span>
8.  <span data-ttu-id="77d34-145">Declaración de la aplicación compatible con PPP</span><span class="sxs-lookup"><span data-stu-id="77d34-145">Declare your application DPI Aware</span></span>

## <a name="compatibility-performance-reliability-and-usability-testing"></a><span data-ttu-id="77d34-146">Pruebas de compatibilidad, rendimiento, confiabilidad y facilidad de uso</span><span class="sxs-lookup"><span data-stu-id="77d34-146">Compatibility, Performance, Reliability, and Usability Testing</span></span>

<span data-ttu-id="77d34-147">Vuelva a ejecutar la evaluación de reconocimiento de PPP y compruebe que los problemas se han corregido.</span><span class="sxs-lookup"><span data-stu-id="77d34-147">Re-run the DPI Awareness assessment and verify the issues are fixed.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="77d34-148">Vínculos a otros recursos</span><span class="sxs-lookup"><span data-stu-id="77d34-148">Links to Other Resources</span></span>

-   [<span data-ttu-id="77d34-149">Desarrollo de aplicaciones de escritorio con valores altos de PPP en Windows</span><span class="sxs-lookup"><span data-stu-id="77d34-149">High DPI Desktop Application Development on Windows</span></span>](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   <span data-ttu-id="77d34-150">**Póngase en contacto con para preguntas técnicas:**<disup@microsoft.com></span><span class="sxs-lookup"><span data-stu-id="77d34-150">**Contact for technical questions:** <disup@microsoft.com></span></span>

 

 
