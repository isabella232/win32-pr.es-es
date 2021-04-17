---
title: Arquitectura (marco de trabajo de servicios de texto)
description: Architecture
ms.assetid: 6ef6ba1f-fcbb-4ede-bc6f-3da66135ea69
keywords:
- Plataforma de servicios de texto (TSF), arquitectura
- TSF (marco de trabajo de servicios de texto), arquitectura
- servicios de texto, arquitectura
- Aplicaciones habilitadas para TSF, arquitectura
- Text Services Framework (TSF), componentes
- TSF (marco de trabajo de servicios de texto), componentes
- servicios de texto, componentes
- Aplicaciones habilitadas para TSF, componentes
- Text Services Framework (TSF), aplicaciones
- TSF (marco de trabajo de servicios de texto), aplicaciones
- servicios de texto, aplicaciones
- Aplicaciones habilitadas para TSF, acerca de
- Text Services Framework (TSF), servicios de texto
- TSF (marco de trabajo de servicios de texto), servicios de texto
- servicios de texto, acerca de
- Aplicaciones habilitadas para TSF, servicios de texto
- Text Services Framework (TSF), administrador de TSF
- TSF (marco de trabajo de servicios de texto), administrador de TSF
- servicios de texto, administrador de TSF
- Aplicaciones habilitadas para TSF, administrador de TSF
- Administrador de TSF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e0a300307b3099b4a28a883d5c830c4078cd0bb
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104571252"
---
# <a name="architecture-text-services-framework"></a><span data-ttu-id="9c391-124">Arquitectura (marco de trabajo de servicios de texto)</span><span class="sxs-lookup"><span data-stu-id="9c391-124">Architecture (Text Services Framework)</span></span>

<span data-ttu-id="9c391-125">El marco de trabajo de servicios de texto incluye tres componentes principales:</span><span class="sxs-lookup"><span data-stu-id="9c391-125">Text Services Framework includes three primary components:</span></span>

-   <span data-ttu-id="9c391-126">**Aplicaciones:** Las operaciones de aplicación suelen incluir la visualización, la edición directa y el almacenamiento de texto.</span><span class="sxs-lookup"><span data-stu-id="9c391-126">**Applications:** Application operations typically include display, direct editing, and storage of text.</span></span> <span data-ttu-id="9c391-127">Una aplicación proporciona acceso al texto implementando un servidor COM que admite ciertas interfaces y se comunica con TSF mediante interfaces que expone el administrador de TSF.</span><span class="sxs-lookup"><span data-stu-id="9c391-127">An application provides access to text by implementing a COM server that supports certain interfaces and communicates with TSF using interfaces that the TSF manager exposes.</span></span> <span data-ttu-id="9c391-128">En esta documentación, el término "aplicación" hace referencia a una aplicación habilitada para TSF, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="9c391-128">Throughout this documentation, the term, application, refers to a TSF-enabled application, unless otherwise specified.</span></span>
-   <span data-ttu-id="9c391-129">**Servicios de texto:** Un servicio de texto funciona como un proveedor de texto en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c391-129">**Text Services:** A text service functions as a text provider to an application.</span></span> <span data-ttu-id="9c391-130">Un servicio de texto puede obtener texto y escribir texto en una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c391-130">A text service can obtain text from, and write text to, an application.</span></span> <span data-ttu-id="9c391-131">Un servicio de texto también puede asociar datos y propiedades con un bloque de texto.</span><span class="sxs-lookup"><span data-stu-id="9c391-131">A text service can also associate data and properties with a block of text.</span></span> <span data-ttu-id="9c391-132">Un servicio de texto se implementa como un servidor en proceso COM que se registra a sí mismo con TSF.</span><span class="sxs-lookup"><span data-stu-id="9c391-132">A text service is implemented as a COM in-proc server that registers itself with TSF.</span></span> <span data-ttu-id="9c391-133">Cuando se registra, el usuario interactúa con el servicio de texto mediante la barra de idioma o los métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="9c391-133">When registered, the user interacts with the text service using the language bar or keyboard shortcuts.</span></span> <span data-ttu-id="9c391-134">Se pueden instalar varios servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="9c391-134">Multiple text services can be installed.</span></span>
-   <span data-ttu-id="9c391-135">**Administrador de TSF:** El administrador de TSF funciona como un mediador entre una aplicación y uno o más servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="9c391-135">**TSF Manager:** The TSF manager functions as a mediator between an application and one or more text services.</span></span> <span data-ttu-id="9c391-136">Un servicio de texto nunca interactúa directamente con una aplicación.</span><span class="sxs-lookup"><span data-stu-id="9c391-136">A text service never interacts directly with an application.</span></span> <span data-ttu-id="9c391-137">Todas las comunicaciones pasan a través del administrador de TSF.</span><span class="sxs-lookup"><span data-stu-id="9c391-137">All communication passes through the TSF manager.</span></span> <span data-ttu-id="9c391-138">El sistema operativo implementa el administrador TSF y no se puede reemplazar.</span><span class="sxs-lookup"><span data-stu-id="9c391-138">The TSF manager is implemented by the operating system and cannot be replaced.</span></span> <span data-ttu-id="9c391-139">En esta documentación, el término administrador hace referencia al administrador de TSF, a menos que se especifique lo contrario.</span><span class="sxs-lookup"><span data-stu-id="9c391-139">Throughout this documentation, the term, manager, refers to the TSF manager, unless otherwise specified.</span></span>

<span data-ttu-id="9c391-140">En la ilustración siguiente se muestran los elementos arquitectónicos principales de TSF.</span><span class="sxs-lookup"><span data-stu-id="9c391-140">The following illustration shows the primary architectural elements of TSF.</span></span>

![arquitectura del marco de trabajo de servicios de texto](images/tsf-arch.gif)

<span data-ttu-id="9c391-142">Con esta arquitectura, el administrador de TSF proporciona una capa de abstracción entre aplicaciones y servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="9c391-142">With this architecture, the TSF manager provides an abstraction layer between applications and text services.</span></span> <span data-ttu-id="9c391-143">Esta capa de abstracción permite a una aplicación y a uno o varios servicios de texto compartir texto, y permite al administrador de TSF administrar servicios de texto.</span><span class="sxs-lookup"><span data-stu-id="9c391-143">This abstraction layer enables an application and one or more text services to share text, and it enables the TSF manager to manage text services.</span></span>

 

 




