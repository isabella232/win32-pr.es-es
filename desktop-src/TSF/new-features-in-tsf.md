---
title: Nuevas características de TSF
description: Con el lanzamiento de Microsoft WindowsXP Service Pack1, el marco de trabajo de servicios de texto (TSF) tiene varias características nuevas.
ms.assetid: d69fec9a-9304-45af-806a-dcc476c95759
keywords:
- Text Services Framework (TSF), nuevas características
- TSF (marco de trabajo de servicios de texto), nuevas características
- servicios de texto, nuevas características
- Aplicaciones habilitadas para TSF, nuevas características
- Text Services Framework (TSF), soporte técnico avanzado
- TSF (marco de trabajo de servicios de texto), soporte técnico avanzado
- servicios de texto, soporte técnico avanzado
- Aplicaciones habilitadas para TSF, compatibilidad avanzada
- Marco de trabajo de servicios de texto (TSF), edición enriquecida
- TSF (marco de trabajo de servicios de texto), edición enriquecida
- servicios de texto, edición enriquecida
- Aplicaciones habilitadas para TSF, edición enriquecida
- Edición enriquecida
- Marco de trabajo de servicios de texto (TSF), seguridad
- TSF (marco de trabajo de servicios de texto), seguridad
- servicios de texto, seguridad
- Aplicaciones habilitadas para TSF, seguridad
- seguridad para TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7a345087304be638be93fa352845cdd468bf15
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420806"
---
# <a name="new-features-in-tsf"></a><span data-ttu-id="88e7e-121">Nuevas características de TSF</span><span class="sxs-lookup"><span data-stu-id="88e7e-121">New Features in TSF</span></span>

<span data-ttu-id="88e7e-122">Con el lanzamiento de Microsoft WindowsXP Service Pack1, el marco de trabajo de servicios de texto (TSF) tiene varias características nuevas.</span><span class="sxs-lookup"><span data-stu-id="88e7e-122">With the release of Microsoft WindowsXP Service Pack1, Text Services Framework (TSF) has several new features.</span></span>

## <a name="extended-support-of-advanced-text-services"></a><span data-ttu-id="88e7e-123">Compatibilidad ampliada con servicios de texto avanzados</span><span class="sxs-lookup"><span data-stu-id="88e7e-123">Extended Support of Advanced Text Services</span></span>

<span data-ttu-id="88e7e-124">Se ha agregado compatibilidad con TSF y Windows para proporcionar una interfaz de usuario coherente para todas las aplicaciones en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="88e7e-124">Support has been added to TSF and Windows to provide a consistent user interface for all applications across the desktop.</span></span> <span data-ttu-id="88e7e-125">Esta nueva compatibilidad permite a las aplicaciones heredadas o a los controles que no saben que TSF aproveche algunos servicios de texto avanzados de forma gratuita.</span><span class="sxs-lookup"><span data-stu-id="88e7e-125">This new support enables legacy applications or controls that are not aware of TSF to take advantage of some advanced text services for free.</span></span> <span data-ttu-id="88e7e-126">Por ejemplo, el dictado de voz y la escritura a mano ahora se pueden usar para escribir texto en un documento de cualquier aplicación.</span><span class="sxs-lookup"><span data-stu-id="88e7e-126">For example, speech dictation and handwriting can now be used to enter text into a document in any application.</span></span>

<span data-ttu-id="88e7e-127">Esta nueva característica solo está disponible para WindowsXP Service Pack1 o posterior.</span><span class="sxs-lookup"><span data-stu-id="88e7e-127">This new feature is available only for WindowsXP Service Pack1 or later.</span></span> <span data-ttu-id="88e7e-128">Está desactivada de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="88e7e-128">It is turned off by default.</span></span> <span data-ttu-id="88e7e-129">Para habilitarlo, haga clic en la casilla de la ficha Opciones **avanzadas** de la sección **servicios de texto e idiomas de entrada** del panel de control **configuración regional y de idioma** .</span><span class="sxs-lookup"><span data-stu-id="88e7e-129">To enable it, click the check box in the new **Advanced** tab in the **Text Services and Input Languages** portion of the **Regional and Language Options** control panel.</span></span>

![compatibilidad con aplicaciones deshabilitadas en el panel de control de TSF](images/advanced-text-services.gif)

## <a name="rich-edit-support"></a><span data-ttu-id="88e7e-131">Compatibilidad con la edición enriquecida</span><span class="sxs-lookup"><span data-stu-id="88e7e-131">Rich Edit Support</span></span>

<span data-ttu-id="88e7e-132">[Edición enriquecida de Microsoft®](../controls/rich-edit-controls.md) La versión 4,1, usada por las aplicaciones para ver y editar texto con formato de caracteres y párrafos especiales, ahora expone la funcionalidad TSF.</span><span class="sxs-lookup"><span data-stu-id="88e7e-132">[Microsoft® Rich Edit](../controls/rich-edit-controls.md) Version 4.1, used by applications to view and edit text with special character and paragraph formatting, now exposes TSF functionality.</span></span> <span data-ttu-id="88e7e-133">De forma predeterminada, esta compatibilidad está desactivada.</span><span class="sxs-lookup"><span data-stu-id="88e7e-133">By default this support is turned off.</span></span> <span data-ttu-id="88e7e-134">Para habilitar TSF en Rich Edit, una aplicación de hospedaje envía un mensaje de ventana especial al control Rich Edit.</span><span class="sxs-lookup"><span data-stu-id="88e7e-134">To enable TSF in Rich Edit, a hosting application sends a special window message to the Rich Edit control.</span></span>

## <a name="security-improvements"></a><span data-ttu-id="88e7e-135">Mejoras de seguridad</span><span class="sxs-lookup"><span data-stu-id="88e7e-135">Security Improvements</span></span>

<span data-ttu-id="88e7e-136">La seguridad y la solidez de TSF se han mejorado sustancialmente, para reducir la probabilidad de que un programa hostil pueda acceder a la pila, al montón o a otras ubicaciones de memoria seguras.</span><span class="sxs-lookup"><span data-stu-id="88e7e-136">The security and robustness of TSF have been substantially improved, to reduce the likelihood of a hostile program being able to access the stack, heap, or other secure memory locations.</span></span> <span data-ttu-id="88e7e-137">También se ha mejorado la seguridad de las aplicaciones de ejemplo y los servicios de texto del kit de desarrollo de software (SDK).</span><span class="sxs-lookup"><span data-stu-id="88e7e-137">The security of software development kit (SDK) sample applications and text services has also been improved.</span></span>

 

 