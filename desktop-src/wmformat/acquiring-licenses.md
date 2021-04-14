---
title: Adquisición de licencias
description: Adquisición de licencias
ms.assetid: dde33d57-6c63-4e1a-8398-5db466fb22fa
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, adquisición de licencias
- SDK de Windows Media Format, licencias
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), adquisición de licencias
- DRM (administración de derechos digitales), adquisición de licencias
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- API extendidas del cliente DRM, adquisición de licencias
- API extendidas del cliente, adquisición de licencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c024789823ca0cd1b38959d78535ce71e2514897
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418391"
---
# <a name="acquiring-licenses"></a><span data-ttu-id="536d5-122">Adquisición de licencias</span><span class="sxs-lookup"><span data-stu-id="536d5-122">Acquiring Licenses</span></span>

<span data-ttu-id="536d5-123">Un escenario común para adquirir licencias es cuando un usuario tiene un archivo de Windows Media protegido e intenta tener acceso al contenido por primera vez.</span><span class="sxs-lookup"><span data-stu-id="536d5-123">A common scenario for acquiring licenses is when a user has a protected Windows Media file and tries to access the content for the first time.</span></span> <span data-ttu-id="536d5-124">Dado que las API extendidas del cliente DRM de Windows Media son independientes de las rutinas de control de archivos ASF, el escenario de adquisición de licencias básico, aunque se admite, requiere más llamadas API que el SDK de Windows Media Format y el SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="536d5-124">Because the Windows Media DRM Client Extended APIs are separate from ASF file handling routines, the basic license acquisition scenario, while supported, requires more API calls than using the Windows Media Format SDK and the Media Foundation SDK.</span></span>

<span data-ttu-id="536d5-125">En esta sección se describe cómo usar las API extendidas del cliente DRM de Windows Media para adquirir licencias almacenadas en el almacén de licencias local en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="536d5-125">This section describes how to use the Windows Media DRM Client Extended APIs to acquire licenses that are stored in the local license store on a client computer.</span></span> <span data-ttu-id="536d5-126">Contiene los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="536d5-126">It contains the following topics.</span></span>



| <span data-ttu-id="536d5-127">Tema</span><span class="sxs-lookup"><span data-stu-id="536d5-127">Topic</span></span>                                                                | <span data-ttu-id="536d5-128">Descripción</span><span class="sxs-lookup"><span data-stu-id="536d5-128">Description</span></span>                                                                                                                                |
|----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="536d5-129">Adquisición de licencias silenciosa</span><span class="sxs-lookup"><span data-stu-id="536d5-129">Silent License Acquisition</span></span>](silent-license-acquisition.md)         | <span data-ttu-id="536d5-130">Describe cómo adquirir licencias sin intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="536d5-130">Describes how to acquire licenses without user intervention.</span></span>                                                                               |
| [<span data-ttu-id="536d5-131">Adquisición de licencias no silenciosa</span><span class="sxs-lookup"><span data-stu-id="536d5-131">Non-Silent License Acquisition</span></span>](non-silent-license-acquisition.md) | <span data-ttu-id="536d5-132">Describe cómo adquirir licencias cuando se requiere la intervención del usuario (por ejemplo, pagar por el contenido).</span><span class="sxs-lookup"><span data-stu-id="536d5-132">Describes how to acquire licenses when user intervention (such as paying for the content) is required.</span></span>                                     |
| [<span data-ttu-id="536d5-133">Entrega previa de licencias</span><span class="sxs-lookup"><span data-stu-id="536d5-133">License Pre-Delivery</span></span>](license-pre-delivery.md)                     | <span data-ttu-id="536d5-134">Describe cómo extraer licencias de un servidor de licencias a un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="536d5-134">Describes how to pull licenses from a license server to a client computer.</span></span>                                                                 |
| [<span data-ttu-id="536d5-135">Crear licencias localmente</span><span class="sxs-lookup"><span data-stu-id="536d5-135">Creating Licenses Locally</span></span>](creating-licenses-locally.md)           | <span data-ttu-id="536d5-136">Describe cómo crear sus propias licencias sin descargarlas desde un servidor de licencias y cómo almacenarlas en el almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="536d5-136">Describes how to create your own licenses without downloading them from a license server and how to store them in the local license store.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="536d5-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="536d5-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="536d5-138">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="536d5-138">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




