---
title: Importación de DRM
description: Importación de DRM
ms.assetid: 5e67a721-830b-4d99-9f90-4cb2d7c61104
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, importación de DRM
- SDK de Windows Media Format, importar
- SDK de Windows Media Format, sistema de protección de contenido (CPS)
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), importar
- DRM (administración de derechos digitales), importar
- Administración de derechos digitales (DRM), sistema de protección de contenido (CPS)
- DRM (administración de derechos digitales), sistema de protección de contenido (CPS)
- API extendidas del cliente DRM, importar
- API extendidas de cliente, importar
- API extendidas del cliente DRM, sistema de protección de contenido (CPS)
- API extendidas de cliente, sistema de protección de contenido (CPS)
- sistema de protección de contenido (CPS)
- CPS (sistema de protección de contenido)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20fc20cfd682df975c10a8f39785c0e8d69610d0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776663"
---
# <a name="drm-import"></a><span data-ttu-id="05264-127">Importación de DRM</span><span class="sxs-lookup"><span data-stu-id="05264-127">DRM Import</span></span>

<span data-ttu-id="05264-128">En las secciones siguientes se explica cómo convertir el contenido multimedia de un sistema de protección de contenido (CPS) de terceros en DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="05264-128">The following sections explain how to convert media content from a third-party content protection system (CPS) to Windows Media DRM.</span></span> <span data-ttu-id="05264-129">Este proceso se conoce como importación de DRM y consta esencialmente de los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="05264-129">This process is known as DRM Import and consists essentially of the following steps:</span></span>

1.  <span data-ttu-id="05264-130">Crear el archivo ASF.</span><span class="sxs-lookup"><span data-stu-id="05264-130">Creating the ASF file.</span></span>
2.  <span data-ttu-id="05264-131">Crear la licencia.</span><span class="sxs-lookup"><span data-stu-id="05264-131">Creating the license.</span></span>
3.  <span data-ttu-id="05264-132">Opcionalmente, se elimina la licencia.</span><span class="sxs-lookup"><span data-stu-id="05264-132">Optionally deleting the license.</span></span>

<span data-ttu-id="05264-133">La importación de DRM se explica en las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="05264-133">DRM Import is explained in the following sections.</span></span>



| <span data-ttu-id="05264-134">Sección</span><span class="sxs-lookup"><span data-stu-id="05264-134">Section</span></span>                                                                              | <span data-ttu-id="05264-135">Descripción</span><span class="sxs-lookup"><span data-stu-id="05264-135">Description</span></span>                                                                          |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="05264-136">Importación de la licencia y el material de clave</span><span class="sxs-lookup"><span data-stu-id="05264-136">Importing License and Key Material</span></span>](importing-license-and-key-material.md)         | <span data-ttu-id="05264-137">Describe cómo emitir licencias localmente e importarlas en Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="05264-137">Describes how to issue licenses locally and import them into Windows Media DRM.</span></span>      |
| [<span data-ttu-id="05264-138">Comprobación de la revocación de certificados</span><span class="sxs-lookup"><span data-stu-id="05264-138">Checking Certificate Revocation</span></span>](checking-certificate-revocation.md)               | <span data-ttu-id="05264-139">Describe cómo comprobar la revocación de certificados.</span><span class="sxs-lookup"><span data-stu-id="05264-139">Describes how to check certificate revocation.</span></span>                                       |
| [<span data-ttu-id="05264-140">Creación de una licencia de XMR</span><span class="sxs-lookup"><span data-stu-id="05264-140">Building an XMR License</span></span>](building-an-xmr-license.md)                               | <span data-ttu-id="05264-141">Describe cómo crear una licencia de XMR y pasarla al subsistema DRM.</span><span class="sxs-lookup"><span data-stu-id="05264-141">Describes how to create an XMR license and pass it to the DRM subsystem.</span></span>             |
| [<span data-ttu-id="05264-142">Creación e inicialización de un escritor DRM</span><span class="sxs-lookup"><span data-stu-id="05264-142">Creating and Initializing a DRM Writer</span></span>](creating-and-initializing-a-drm-writer.md) | <span data-ttu-id="05264-143">Describe cómo inicializar un objeto de escritura ASF para preparar la importación de DRM.</span><span class="sxs-lookup"><span data-stu-id="05264-143">Describes how to initialize an ASF writer object to prepare for DRM Import.</span></span>          |
| [<span data-ttu-id="05264-144">Cifrado e importación de ejemplos de medios</span><span class="sxs-lookup"><span data-stu-id="05264-144">Encrypting and Importing Media Samples</span></span>](encrypting-and-importing-media-samples.md) | <span data-ttu-id="05264-145">Describe cómo cifrar e importar ejemplos de medios individuales en DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="05264-145">Describes how to encrypt and import individual media samples into Windows Media DRM.</span></span> |
| [<span data-ttu-id="05264-146">Eliminación de licencias</span><span class="sxs-lookup"><span data-stu-id="05264-146">License Deletion</span></span>](license-deletion.md)                                             | <span data-ttu-id="05264-147">Describe cómo eliminar licencias creadas localmente.</span><span class="sxs-lookup"><span data-stu-id="05264-147">Describes how to delete locally created licenses.</span></span>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="05264-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="05264-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05264-149">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="05264-149">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




