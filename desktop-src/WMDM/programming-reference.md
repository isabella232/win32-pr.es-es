---
title: Referencia de WMDM
description: Windows Media Administrador de dispositivos SDK consta de una colección de interfaces, estructuras, enumeraciones y constantes. Use estos artículos de referencia.
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media Administrador de dispositivos, referencia de programación
- Administrador de dispositivos,referencia de programación
- Windows Media Administrador de dispositivos aplicaciones de escritorio
- Administrador de dispositivos aplicaciones de escritorio
- Windows Media Administrador de dispositivos,proveedores de servicios
- Administrador de dispositivos,proveedores de servicios
- aplicaciones de escritorio, referencia de programación
- proveedores de servicios, referencia de programación
- referencia de programación, aplicaciones de escritorio
- referencia de programación, proveedores de servicios
- referencia de programación, Windows Media Administrador de dispositivos
- referencia de Windows Media Administrador de dispositivos, acerca de
- referencia de Windows Media Administrador de dispositivos aplicaciones de escritorio
- referencia de Windows Media Administrador de dispositivos,proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e624bbc445d5d5e376cad926248ae4ee4db17a6e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406528"
---
# <a name="wmdm-reference"></a><span data-ttu-id="020a3-118">Referencia de WMDM</span><span class="sxs-lookup"><span data-stu-id="020a3-118">WMDM reference</span></span>

<span data-ttu-id="020a3-119">Windows Media Administrador de dispositivos SDK consta de una colección de interfaces, estructuras, enumeraciones y constantes.</span><span class="sxs-lookup"><span data-stu-id="020a3-119">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="020a3-120">La sección de referencia divide las interfaces en grupos según el tipo de objeto que las usa.</span><span class="sxs-lookup"><span data-stu-id="020a3-120">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="020a3-121">Sección</span><span class="sxs-lookup"><span data-stu-id="020a3-121">Section</span></span>                                                                                                    | <span data-ttu-id="020a3-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="020a3-122">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="020a3-123">Interfaces para aplicaciones</span><span class="sxs-lookup"><span data-stu-id="020a3-123">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="020a3-124">Describe las interfaces que solo usan o implementan aplicaciones de escritorio, Reproductor de Windows Media complementos u objetos COM que necesitan acceso de alto nivel a un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="020a3-124">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="020a3-125">Interfaces para proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="020a3-125">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="020a3-126">Describe las interfaces que solo usan o implementan los proveedores de servicios, que controlan la comunicación real de bajo nivel con un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="020a3-126">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="020a3-127">Windows Media DRM-Implemented Interfaces</span><span class="sxs-lookup"><span data-stu-id="020a3-127">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="020a3-128">Describe interfaces que no están diseñadas para ser implementadas por proveedores de servicios de terceros, pero que se implementan y llaman internamente mediante DRM de Windows Media y Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="020a3-128">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="020a3-129">Interfaces para proveedores de servicios y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="020a3-129">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="020a3-130">Describe las interfaces que pueden usar las aplicaciones o los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="020a3-130">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="020a3-131">Interfaces para proveedores de contenido seguro</span><span class="sxs-lookup"><span data-stu-id="020a3-131">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="020a3-132">Describe las interfaces que debe implementar un dispositivo o aplicación que usará contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="020a3-132">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="020a3-133">Estructuras</span><span class="sxs-lookup"><span data-stu-id="020a3-133">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="020a3-134">Describe las estructuras usadas para los métodos de Administrador de dispositivos Windows Media.</span><span class="sxs-lookup"><span data-stu-id="020a3-134">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="020a3-135">Tipos de enumeración</span><span class="sxs-lookup"><span data-stu-id="020a3-135">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="020a3-136">Describe las enumeraciones usadas para los métodos de Administrador de dispositivos Windows Media.</span><span class="sxs-lookup"><span data-stu-id="020a3-136">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="020a3-137">Constantes de metadatos</span><span class="sxs-lookup"><span data-stu-id="020a3-137">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="020a3-138">Describe las constantes definidas por el SDK de Windows Media Administrador de dispositivos para establecer o recuperar varias propiedades de metadatos para un dispositivo u objeto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="020a3-138">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="020a3-139">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="020a3-139">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="020a3-140">Describe los códigos de error que pueden devolver los métodos del SDK de Windows Media Administrador de dispositivos SDK.</span><span class="sxs-lookup"><span data-stu-id="020a3-140">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




