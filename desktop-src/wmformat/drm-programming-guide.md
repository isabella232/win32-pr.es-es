---
title: Guía de programación del cliente DRM de Microsoft Windows Media
description: Guía de programación del cliente DRM de Microsoft Windows Media
ms.assetid: e7b179b3-ed14-4ea0-9a00-9d96557a2e2e
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, guía de programación
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), guía de programación
- DRM (administración de derechos digitales), guía de programación
- API extendidas del cliente DRM, acerca de
- API extendidas de cliente, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b338ea6ebd9cb132c8e6b1c76c8e1d7f6c6aa182
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104488777"
---
# <a name="microsoft-windows-media-drm-client-programming-guide"></a><span data-ttu-id="b57c0-119">Guía de programación del cliente DRM de Microsoft Windows Media</span><span class="sxs-lookup"><span data-stu-id="b57c0-119">Microsoft Windows Media DRM Client Programming Guide</span></span>

<span data-ttu-id="b57c0-120">En esta guía se proporciona información sobre el uso de las características de las API extendidas del cliente DRM de Windows Media en las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="b57c0-120">This guide provides information about using the features of the Windows Media DRM Client Extended APIs in your applications.</span></span> <span data-ttu-id="b57c0-121">En las siguientes secciones se explican detalladamente los pasos necesarios para implementar las características de DRM.</span><span class="sxs-lookup"><span data-stu-id="b57c0-121">The following sections explain, in detail, the steps involved in implementing DRM features.</span></span>



| <span data-ttu-id="b57c0-122">Sección</span><span class="sxs-lookup"><span data-stu-id="b57c0-122">Section</span></span>                                                                                                                          | <span data-ttu-id="b57c0-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="b57c0-123">Description</span></span>                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b57c0-124">Introducción</span><span class="sxs-lookup"><span data-stu-id="b57c0-124">Getting Started</span></span>](drm-getting-started.md)                                                                                       | <span data-ttu-id="b57c0-125">Proporciona información sobre la configuración de proyectos de C++ que usan las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b57c0-125">Provides information about setting up C++ projects that use the Windows Media DRM Client Extended APIs.</span></span>    |
| [<span data-ttu-id="b57c0-126">Adquisición de licencias</span><span class="sxs-lookup"><span data-stu-id="b57c0-126">Acquiring Licenses</span></span>](acquiring-licenses.md)                                                                                     | <span data-ttu-id="b57c0-127">Describe cómo obtener licencias en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="b57c0-127">Describes how to get licenses on the client computer.</span></span>                                                      |
| [<span data-ttu-id="b57c0-128">Obtención de información de licencias en el almacén de licencias local</span><span class="sxs-lookup"><span data-stu-id="b57c0-128">Getting Information from Licenses in the Local License Store</span></span>](getting-information-from-licenses-in-the-local-license-store.md) | <span data-ttu-id="b57c0-129">Describe cómo obtener información sobre los derechos del contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="b57c0-129">Describes how to get information about rights for protected content.</span></span>                                       |
| [<span data-ttu-id="b57c0-130">Realización de una individualización DRM</span><span class="sxs-lookup"><span data-stu-id="b57c0-130">Performing DRM Individualization</span></span>](performing-drm-individualization.md)                                                         | <span data-ttu-id="b57c0-131">Describe cómo actualizar y individualizar el componente DRM en el equipo cliente para que sea más seguro.</span><span class="sxs-lookup"><span data-stu-id="b57c0-131">Describes how to update and individualize the DRM component on the client computer to make it more secure.</span></span> |
| [<span data-ttu-id="b57c0-132">Exportación de DRM</span><span class="sxs-lookup"><span data-stu-id="b57c0-132">DRM Export</span></span>](drm-export.md)                                                                                                     | <span data-ttu-id="b57c0-133">Describe cómo exportar el contenido protegido por DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b57c0-133">Describes how to export content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="b57c0-134">Importación de DRM</span><span class="sxs-lookup"><span data-stu-id="b57c0-134">DRM Import</span></span>](drm-import.md)                                                                                                     | <span data-ttu-id="b57c0-135">Describe cómo importar contenido protegido por DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="b57c0-135">Describes how to import content protected by Windows Media DRM.</span></span>                                            |
| [<span data-ttu-id="b57c0-136">Revocación de licencia</span><span class="sxs-lookup"><span data-stu-id="b57c0-136">License Revocation</span></span>](drm-license-revocation.md)                                                                                 | <span data-ttu-id="b57c0-137">Describe cómo quitar licencias del almacén de licencias local.</span><span class="sxs-lookup"><span data-stu-id="b57c0-137">Describes how to remove licenses from the local license store.</span></span>                                             |
| [<span data-ttu-id="b57c0-138">Revocación y renovación de componentes automatizados</span><span class="sxs-lookup"><span data-stu-id="b57c0-138">Automated Component Revocation and Renewal</span></span>](automated-component-revocation-and-renewal.md)                                     | <span data-ttu-id="b57c0-139">Describe el sistema de revocación automatizada y renovación de DRM de Windows Media mediante habilitadores de contenido.</span><span class="sxs-lookup"><span data-stu-id="b57c0-139">Describes the Windows Media DRM automated revocation and renewal system using content enablers.</span></span>            |



 

## <a name="related-topics"></a><span data-ttu-id="b57c0-140">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="b57c0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b57c0-141">**API extendidas del cliente DRM de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="b57c0-141">**Windows Media DRM Client Extended APIs**</span></span>](windows-media-drm-client-extended-apis.md)
</dt> <dt>

<span data-ttu-id="b57c0-142">[SDK de Windows Media Rights Manager](/previous-versions/ms986509(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="b57c0-142">[Windows Media Rights Manager SDK](/previous-versions/ms986509(v=msdn.10))</span></span>
</dt> </dl>

 

 
