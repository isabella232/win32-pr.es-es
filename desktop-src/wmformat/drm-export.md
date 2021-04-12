---
title: Exportación de DRM
description: Exportación de DRM
ms.assetid: 0b44f2e5-e63c-4bdb-8123-097a5d5e3756
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, exportación de DRM
- SDK de Windows Media Format, exportar
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- Administración de derechos digitales (DRM), exportar
- DRM (administración de derechos digitales), exportar
- API extendidas del cliente DRM, exportar
- API extendidas del cliente, exportar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2917cfd0c9042f4547540618b44ed4c2f324edb8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357169"
---
# <a name="drm-export"></a><span data-ttu-id="91ce7-120">Exportación de DRM</span><span class="sxs-lookup"><span data-stu-id="91ce7-120">DRM Export</span></span>

<span data-ttu-id="91ce7-121">La funcionalidad de exportación de DRM de Windows Media le permite crear aplicaciones con licencia que descifren el contenido protegido por DRM de Windows Media y volver a cifrar en un esquema de protección de contenido (CPS) de salida especificado explícitamente por el emisor de la licencia asociada.</span><span class="sxs-lookup"><span data-stu-id="91ce7-121">Windows Media DRM export functionality enables you to create licensed applications that decrypt content protected by Windows Media DRM, and re-encrypt in an output content protection scheme (CPS) explicitly specified by the associated license issuer.</span></span> <span data-ttu-id="91ce7-122">El emisor de la licencia autoriza explícitamente la exportación de contenido a una CPS específica a través de una lista de inclusión.</span><span class="sxs-lookup"><span data-stu-id="91ce7-122">The license issuer explicitly authorizes the export of content to a specific CPS through an inclusion list.</span></span>

> [!Note]  
> <span data-ttu-id="91ce7-123">Para obtener acceso a la funcionalidad de exportación, debe solicitar un [certificado de aplicación de exportación](export-application-certificate.md) de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91ce7-123">To access export functionality, you must apply for an [Export Application Certificate](export-application-certificate.md) from Microsoft.</span></span>

 

<span data-ttu-id="91ce7-124">En las secciones siguientes se explica la funcionalidad de exportación de DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="91ce7-124">Windows Media DRM export functionality is explained in the following sections.</span></span>



| <span data-ttu-id="91ce7-125">Sección</span><span class="sxs-lookup"><span data-stu-id="91ce7-125">Section</span></span>                                                                                      | <span data-ttu-id="91ce7-126">Descripción</span><span class="sxs-lookup"><span data-stu-id="91ce7-126">Description</span></span>                                                                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="91ce7-127">Exportar certificado de aplicación</span><span class="sxs-lookup"><span data-stu-id="91ce7-127">Export Application Certificate</span></span>](export-application-certificate.md)                         | <span data-ttu-id="91ce7-128">Describe un certificado de aplicación de exportación.</span><span class="sxs-lookup"><span data-stu-id="91ce7-128">Describes an export application certificate.</span></span>                                                        |
| [<span data-ttu-id="91ce7-129">Listas de inclusión y autorización explícitas</span><span class="sxs-lookup"><span data-stu-id="91ce7-129">Explicit Authorization and Inclusion Lists</span></span>](explicit-authorization-and-inclusion-lists.md) | <span data-ttu-id="91ce7-130">Explica el proceso de autorización explícita y cómo funcionan las inclusiones.</span><span class="sxs-lookup"><span data-stu-id="91ce7-130">Explains the process of explicit authorization, and how inclusions lists work.</span></span>                      |
| [<span data-ttu-id="91ce7-131">Exportar contenido comprimido</span><span class="sxs-lookup"><span data-stu-id="91ce7-131">Exporting Compressed Content</span></span>](exporting-compressed-content.md)                             | <span data-ttu-id="91ce7-132">Describe cómo exportar contenido comprimido del contenido de audio o vídeo protegido con DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="91ce7-132">Describes how to export compressed content from Windows Media DRM protected audio or video content.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="91ce7-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91ce7-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91ce7-134">**Listas de inclusión y autorización explícitas**</span><span class="sxs-lookup"><span data-stu-id="91ce7-134">**Explicit Authorization and Inclusion Lists**</span></span>](explicit-authorization-and-inclusion-lists.md)
</dt> <dt>

[<span data-ttu-id="91ce7-135">**Guía de programación**</span><span class="sxs-lookup"><span data-stu-id="91ce7-135">**Programming Guide**</span></span>](drm-programming-guide.md)
</dt> </dl>

 

 




