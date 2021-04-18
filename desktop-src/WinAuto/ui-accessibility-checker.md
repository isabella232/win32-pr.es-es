---
title: 'Herramientas de accesibilidad: AccChecker (comprobador de accesibilidad de IU)'
description: Describe AccChecker (comprobador de accesibilidad de IU), una herramienta para probar la automatización de la interfaz de usuario de una aplicación o la implementación de Microsoft Active Accessibility (MSAA).
ms.assetid: 92155984-356A-4774-A99D-35B15A3BB704
keywords:
- UI Accessibility Checker
- AccChecker
- Implementación de automatización de la interfaz de usuario, prueba
- Implementación de UIA, pruebas
- Implementación de Microsoft Active Accessibility, pruebas
- Implementación de MSAA, pruebas
- probar la automatización de la interfaz de usuario
- probar UIA
- probar Microsoft Active Accessibility
- prueba de MSAA
- Herramientas de prueba de UIA
- Herramientas de pruebas de UI Automation
- Herramientas de pruebas de MSAA
- Herramientas de prueba de Microsoft Active Accessibility
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49d2b85436735bfa08f8fc73cf4e465b11d71630
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "105704905"
---
# <a name="accessibility-tools---accchecker-ui-accessibility-checker"></a><span data-ttu-id="42813-117">Herramientas de accesibilidad: AccChecker (comprobador de accesibilidad de IU)</span><span class="sxs-lookup"><span data-stu-id="42813-117">Accessibility tools - AccChecker (UI Accessibility Checker)</span></span>

<span data-ttu-id="42813-118">**AccChecker** (comprobador de accesibilidad de IU) comprueba que se cumplen los requisitos de accesibilidad de la interfaz de usuario clave en el diseño y la implementación de la automatización de la interfaz de usuario (UIA) o Microsoft Active ACCESSIBILITY (MSAA) independientemente del marco de interfaz de usuario subyacente.</span><span class="sxs-lookup"><span data-stu-id="42813-118">**AccChecker** (UI Accessibility Checker) verifies that key UI accessibility requirements are met in the design and implementation of UI Automation (UIA) or Microsoft Active Accessibility (MSAA) regardless of the underlying UI framework.</span></span> <span data-ttu-id="42813-119">**AccChecker** también incluye un conjunto de comprobaciones de accesibilidad Web.</span><span class="sxs-lookup"><span data-stu-id="42813-119">**AccChecker** also includes a set of web accessibility verifications.</span></span>

<span data-ttu-id="42813-120">**AccChecker** proporciona los siguientes niveles de funcionalidad:</span><span class="sxs-lookup"><span data-stu-id="42813-120">**AccChecker** provides the following levels of functionality:</span></span>

- <span data-ttu-id="42813-121">Aplicación GUI de Windows que admite pruebas manuales, registro de mensajes y generación de supresiones.</span><span class="sxs-lookup"><span data-stu-id="42813-121">A Windows GUI application that supports manual testing, message logging, and suppression generation.</span></span>
- <span data-ttu-id="42813-122">Una API que se utiliza en marcos de pruebas automatizadas.</span><span class="sxs-lookup"><span data-stu-id="42813-122">An API for use in automated testing frameworks.</span></span>
- <span data-ttu-id="42813-123">Aplicación de consola que admite la automatización de pruebas no administradas en escenarios donde no se puede usar la API administrada **AccChecker** .</span><span class="sxs-lookup"><span data-stu-id="42813-123">A console application that supports unmanaged test automations for scenarios where the **AccChecker** managed API can't be used.</span></span>

<span data-ttu-id="42813-124">Todos los niveles de funcionalidad de **AccChecker** proporcionan rutinas para comprobar el acceso mediante programación a Microsoft Active Accessibility, generación de eventos mediante programación, diseño de control y navegación mediante el teclado.</span><span class="sxs-lookup"><span data-stu-id="42813-124">All levels of **AccChecker** functionality provide routines for verifying Microsoft Active Accessibility programmatic access, programmatic event generation, control layout, and keyboard navigation.</span></span> <span data-ttu-id="42813-125">**AccChecker** también proporciona un servicio básico de transcripción de lector de pantalla.</span><span class="sxs-lookup"><span data-stu-id="42813-125">**AccChecker** also provides a basic screen reader transcription service.</span></span>

<span data-ttu-id="42813-126">**AccChecker** se instala con el kit de desarrollo de software (SDK) de Windows.</span><span class="sxs-lookup"><span data-stu-id="42813-126">**AccChecker** is installed with the Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="42813-127">Se encuentra en la \\ carpeta bin \\ < *version* > \\ < *Platform* > \\ AccChecker de la ruta de instalación del SDK.</span><span class="sxs-lookup"><span data-stu-id="42813-127">It is located in the \\bin\\<*version*>\\<*platform*>\\AccChecker folder of the SDK installation path.</span></span>

> [!NOTE]
> <span data-ttu-id="42813-128">**AccChecker** es una herramienta heredada.</span><span class="sxs-lookup"><span data-stu-id="42813-128">**AccChecker** is a legacy tool.</span></span> <span data-ttu-id="42813-129">En su lugar, se recomienda usar [información de accesibilidad](https://accessibilityinsights.io/) .</span><span class="sxs-lookup"><span data-stu-id="42813-129">We recommend using [Accessibility Insights](https://accessibilityinsights.io/) instead.</span></span>

## <a name="requirements"></a><span data-ttu-id="42813-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="42813-130">Requirements</span></span>

<span data-ttu-id="42813-131">Requiere .NET Framework 2,0 o posterior.</span><span class="sxs-lookup"><span data-stu-id="42813-131">Requires .NET Framework 2.0 or later.</span></span>

<span data-ttu-id="42813-132">**AccChecker** se puede usar para examinar los datos de accesibilidad de los sistemas que no tienen automatización de la interfaz de usuario de Microsoft, pero solo pueden examinar las propiedades de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="42813-132">**AccChecker** can be used to examine accessibility data on systems that don't have Microsoft UI Automation, but can only examine the Microsoft Active Accessibility properties.</span></span> <span data-ttu-id="42813-133">Para examinar la automatización de la interfaz de usuario, la automatización de la interfaz de usuario debe estar presente en el sistema.</span><span class="sxs-lookup"><span data-stu-id="42813-133">To examine UI Automation, UI Automation must be present on the system.</span></span> <span data-ttu-id="42813-134">Para obtener más información, vea la sección "requirements" de automatización de la [interfaz de usuario](entry-uiauto-win32.md).</span><span class="sxs-lookup"><span data-stu-id="42813-134">For more information, see the "Requirements" section of [UI Automation](entry-uiauto-win32.md).</span></span>

<span data-ttu-id="42813-135">**AccChecker** se instala como parte del conjunto general de herramientas en el SDK de Windows, no se distribuye como una descarga independiente de exe.</span><span class="sxs-lookup"><span data-stu-id="42813-135">**AccChecker** is installed as part of the overall set of tools in theWindows SDK, it is not distributed as a separate exe download.</span></span> <span data-ttu-id="42813-136">El Windows SDK incluye todas las herramientas relacionadas con la accesibilidad que se documentan en esta sección.</span><span class="sxs-lookup"><span data-stu-id="42813-136">The Windows SDK includes all of the accessibility-related tools documented in this section.</span></span> [<span data-ttu-id="42813-137">Obtiene el Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="42813-137">Get the Windows SDK.</span></span>](https://developer.microsoft.com/) <span data-ttu-id="42813-138">(También hay un archivo de descarga de SDK vinculado desde esa página, si necesita una versión anterior).</span><span class="sxs-lookup"><span data-stu-id="42813-138">(There's also an SDK download archive linked from that page, if you need a previous version.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="42813-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="42813-139">Related topics</span></span>

- [<span data-ttu-id="42813-140">Accessible Event Watcher</span><span class="sxs-lookup"><span data-stu-id="42813-140">Accessible Event Watcher</span></span>](accessible-event-watcher.md)
- [<span data-ttu-id="42813-141">Inspeccionar</span><span class="sxs-lookup"><span data-stu-id="42813-141">Inspect</span></span>](inspect-objects.md)
- [<span data-ttu-id="42813-142">Herramientas de pruebas</span><span class="sxs-lookup"><span data-stu-id="42813-142">Testing Tools</span></span>](testing-tools.md)
- [<span data-ttu-id="42813-143">UI Automation Verify</span><span class="sxs-lookup"><span data-stu-id="42813-143">UI Automation Verify</span></span>](ui-automation-verify.md)
