---
title: Referencia de WMDM
description: Referencia de programación
ms.assetid: 1d2260a8-bc9f-41b3-a3b0-0176b45fff1f
keywords:
- Windows Media Administrador de dispositivos, referencia de programación
- Administrador de dispositivos, referencia de programación
- Windows Media Administrador de dispositivos, aplicaciones de escritorio
- Administrador de dispositivos, aplicaciones de escritorio
- Windows Media Administrador de dispositivos, proveedores de servicios
- Administrador de dispositivos, proveedores de servicios
- aplicaciones de escritorio, referencia de programación
- proveedores de servicios, referencia de programación
- referencia de programación, aplicaciones de escritorio
- referencia de programación, proveedores de servicios
- referencia de programación, Administrador de dispositivos de Windows Media
- referencia de Windows Media Administrador de dispositivos, acerca de
- referencia de Windows Media Administrador de dispositivos, aplicaciones de escritorio
- referencia de Windows Media Administrador de dispositivos, proveedores de servicios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1498d42e65de99abc1d32895f3628d93502c70f
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/23/2019
ms.locfileid: "104420019"
---
# <a name="wmdm-reference"></a><span data-ttu-id="17843-117">Referencia de WMDM</span><span class="sxs-lookup"><span data-stu-id="17843-117">WMDM reference</span></span>

<span data-ttu-id="17843-118">El SDK de Administrador de dispositivos de Windows Media se compone de una colección de interfaces, estructuras, enumeraciones y constantes.</span><span class="sxs-lookup"><span data-stu-id="17843-118">The Windows Media Device Manager SDK consists of a collection of interfaces, structures, enumerations, and constants.</span></span> <span data-ttu-id="17843-119">La sección de referencia divide las interfaces en grupos según el tipo de objeto que las utiliza.</span><span class="sxs-lookup"><span data-stu-id="17843-119">The reference section divides the interfaces into groups according to the type of object that uses them.</span></span>



| <span data-ttu-id="17843-120">Sección</span><span class="sxs-lookup"><span data-stu-id="17843-120">Section</span></span>                                                                                                    | <span data-ttu-id="17843-121">Descripción</span><span class="sxs-lookup"><span data-stu-id="17843-121">Description</span></span>                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17843-122">Interfaces para aplicaciones</span><span class="sxs-lookup"><span data-stu-id="17843-122">Interfaces for Applications</span></span>](interfaces-for-applications.md)                                             | <span data-ttu-id="17843-123">Describe las interfaces que solo usan las aplicaciones de escritorio, los complementos de Media Player de Windows o los objetos COM que necesitan un acceso de alto nivel a un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="17843-123">Describes interfaces that are used or implemented only by desktop applications, Windows Media Player plug-ins, or COM objects that need high-level access to a portable device.</span></span>                     |
| [<span data-ttu-id="17843-124">Interfaces para proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="17843-124">Interfaces for Service Providers</span></span>](interfaces-for-service-providers.md)                                   | <span data-ttu-id="17843-125">Describe las interfaces que solo usan los proveedores de servicios, que administran la comunicación real de bajo nivel con un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="17843-125">Describes interfaces that are used or implemented only by service providers, which handle the actual low-level communication with a portable device.</span></span>                                                |
| [<span data-ttu-id="17843-126">Interfaces de DRM-Implemented de Windows Media</span><span class="sxs-lookup"><span data-stu-id="17843-126">Windows Media DRM-Implemented Interfaces</span></span>](windows-media-drm-implemented-interfaces.md)                   | <span data-ttu-id="17843-127">Describe las interfaces que no están diseñadas para ser implementadas por proveedores de servicios de terceros, pero que se implementan internamente mediante Windows Media DRM y Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="17843-127">Describes interfaces that are not intended to be implemented by third-party service providers, but are implemented and called internally by the Windows Media DRM and Windows Media Device Manager.</span></span> |
| [<span data-ttu-id="17843-128">Interfaces para proveedores de servicios y aplicaciones</span><span class="sxs-lookup"><span data-stu-id="17843-128">Interfaces for Service Providers and Applications</span></span>](interfaces-for-service-providers-and-applications.md) | <span data-ttu-id="17843-129">Describe las interfaces que pueden usar las aplicaciones o los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="17843-129">Describes interfaces that can be used either by applications or by service providers.</span></span>                                                                                                               |
| [<span data-ttu-id="17843-130">Interfaces para proveedores de contenido seguros</span><span class="sxs-lookup"><span data-stu-id="17843-130">Interfaces for Secure Content Providers</span></span>](interfaces-for-secure-content-providers.md)                     | <span data-ttu-id="17843-131">Describe las interfaces que debe implementar un dispositivo o una aplicación que usará contenido protegido con DRM.</span><span class="sxs-lookup"><span data-stu-id="17843-131">Describes interfaces that must be implemented by a device or application that will use DRM-protected content.</span></span>                                                                                       |
| [<span data-ttu-id="17843-132">Estructuras</span><span class="sxs-lookup"><span data-stu-id="17843-132">Structures</span></span>](structures.md)                                                                               | <span data-ttu-id="17843-133">Describe las estructuras utilizadas para los métodos de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="17843-133">Describes structures used for Windows Media Device Manager methods.</span></span>                                                                                                                                 |
| [<span data-ttu-id="17843-134">Tipos de enumeración</span><span class="sxs-lookup"><span data-stu-id="17843-134">Enumeration Types</span></span>](enumeration-types.md)                                                                 | <span data-ttu-id="17843-135">Describe las enumeraciones utilizadas para los métodos de Administrador de dispositivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="17843-135">Describes enumerations used for Windows Media Device Manager methods.</span></span>                                                                                                                               |
| [<span data-ttu-id="17843-136">Constantes de metadatos</span><span class="sxs-lookup"><span data-stu-id="17843-136">Metadata Constants</span></span>](metadata-constants.md)                                                               | <span data-ttu-id="17843-137">Describe las constantes definidas por el SDK de Windows Media Administrador de dispositivos para establecer o recuperar diversas propiedades de metadatos para un dispositivo o un objeto en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="17843-137">Describes the constants defined by the Windows Media Device Manager SDK for setting or retrieving various metadata properties for a device or object on the device.</span></span>                                 |
| [<span data-ttu-id="17843-138">Códigos de error</span><span class="sxs-lookup"><span data-stu-id="17843-138">Error Codes</span></span>](error-codes.md)                                                                             | <span data-ttu-id="17843-139">Describe los códigos de error que pueden ser devueltos por los métodos del SDK de Windows Media Administrador de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="17843-139">Describes the error codes that can be returned by Windows Media Device Manager SDK methods.</span></span>                                                                                                         |



 

 

 




