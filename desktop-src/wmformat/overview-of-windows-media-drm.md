---
title: Información general de DRM de Windows Media
description: Información general de DRM de Windows Media
ms.assetid: 944b5e0b-649f-4955-8df3-4762726b9893
keywords:
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- SDK de Windows Media Format, licencias de DRM
- SDK de Windows Media Format, licencias de DRM
- Administración de derechos digitales (DRM), acerca de
- DRM (administración de derechos digitales), acerca de
- Administración de derechos digitales (DRM), empaquetar archivos de Windows Media
- DRM (administración de derechos digitales), empaquetar archivos de Windows Media
- Administración de derechos digitales (DRM), licencias de archivos protegidos
- DRM (administración de derechos digitales), licencias de archivos protegidos
- Administración de derechos digitales (DRM), licencias
- DRM (administración de derechos digitales), licencias
- Administración de derechos digitales (DRM), lectura de archivos protegidos
- DRM (administración de derechos digitales), leer archivos protegidos
- Advanced Systems Format (ASF), administración de derechos digitales (DRM)
- ASF (formato de sistemas avanzados), administración de derechos digitales (DRM)
- licencias, DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d14cb76fcf61346aab9bd68746afc7e50a2f146d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704579"
---
# <a name="overview-of-windows-media-drm"></a><span data-ttu-id="360ef-119">Información general de DRM de Windows Media</span><span class="sxs-lookup"><span data-stu-id="360ef-119">Overview of Windows Media DRM</span></span>

<span data-ttu-id="360ef-120">Windows Media Digital Rights Management (DRM) es un sistema para proteger el contenido de los archivos de Windows Media para que los usuarios no autorizados no puedan tener acceso a él.</span><span class="sxs-lookup"><span data-stu-id="360ef-120">Windows Media Digital Rights Management (DRM) is a system for protecting the content in Windows Media files so that unauthorized users cannot access it.</span></span> <span data-ttu-id="360ef-121">Hay tres fases en el ciclo básico de DRM: empaquetado, licencias y lectura.</span><span class="sxs-lookup"><span data-stu-id="360ef-121">There are three phases to the basic DRM cycle: packaging, licensing, and reading.</span></span>

## <a name="packaging-windows-media-files"></a><span data-ttu-id="360ef-122">Empaquetar archivos de Windows Media</span><span class="sxs-lookup"><span data-stu-id="360ef-122">Packaging Windows Media Files</span></span>

<span data-ttu-id="360ef-123">Windows Media DRM está diseñado para trabajar con archivos de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="360ef-123">Windows Media DRM is designed to work with Windows Media files.</span></span> <span data-ttu-id="360ef-124">Un archivo de Windows Media es un archivo que se ajusta a la especificación de Advanced Systems Format (ASF) y que solo contiene audio y vídeo comprimidos mediante los códecs de Windows Media Audio y vídeo.</span><span class="sxs-lookup"><span data-stu-id="360ef-124">A Windows Media file is a file that conforms to the Advanced Systems Format (ASF) specification and only contains Audio and Video that has been compressed by using the Windows Media Audio and Video codecs.</span></span>

<span data-ttu-id="360ef-125">Cuando se empaqueta un archivo ASF, se agrega una sección específica de DRM al encabezado.</span><span class="sxs-lookup"><span data-stu-id="360ef-125">When an ASF file is packaged, a DRM-specific section is added to the header.</span></span> <span data-ttu-id="360ef-126">El encabezado DRM contiene un identificador de clave que identifica el contenido con fines de licencia y una dirección URL de adquisición de licencias, que es la dirección de una página web que puede emitir licencias para leer el contenido protegido.</span><span class="sxs-lookup"><span data-stu-id="360ef-126">The DRM header contains a Key ID, which identifies the content for the purposes of licensing, and a license acquisition URL, which is the address of a Web page that can issue licenses to read the protected content.</span></span> <span data-ttu-id="360ef-127">Hay mucha más información que se puede colocar en el encabezado DRM, pero es opcional.</span><span class="sxs-lookup"><span data-stu-id="360ef-127">There is much more information that can be put in the DRM header, but it is optional.</span></span> <span data-ttu-id="360ef-128">El encabezado DRM está firmado para que se pueda comprobar el empaquetador.</span><span class="sxs-lookup"><span data-stu-id="360ef-128">The DRM header is signed so that the packager can be verified.</span></span>

<span data-ttu-id="360ef-129">El contenido del archivo ASF se cifra durante el proceso de empaquetado.</span><span class="sxs-lookup"><span data-stu-id="360ef-129">The content in the ASF file is encrypted during the packing process.</span></span> <span data-ttu-id="360ef-130">Sin embargo, la siguiente información en el archivo empaquetado está disponible incluso para los clientes que no tienen una licencia:</span><span class="sxs-lookup"><span data-stu-id="360ef-130">However, the following information in the packaged file is available even to clients that do not have a license:</span></span>

-   <span data-ttu-id="360ef-131">Metadatos que se almacenan en el encabezado ASF.</span><span class="sxs-lookup"><span data-stu-id="360ef-131">Metadata that is stored in the ASF header.</span></span>
-   <span data-ttu-id="360ef-132">Algunos metadatos que se almacenan en el encabezado DRM (por ejemplo, siempre puede obtener la dirección URL de adquisición de licencias).</span><span class="sxs-lookup"><span data-stu-id="360ef-132">Some metadata that is stored in the DRM header (for example, you can always get the license acquisition URL).</span></span>

## <a name="licensing-protected-files"></a><span data-ttu-id="360ef-133">Archivos protegidos con licencias</span><span class="sxs-lookup"><span data-stu-id="360ef-133">Licensing Protected Files</span></span>

<span data-ttu-id="360ef-134">Para que se pueda leer un archivo empaquetado, debe emitirse una licencia para el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="360ef-134">For a packaged file to be read, a license must be issued to the client computer.</span></span> <span data-ttu-id="360ef-135">Una licencia es un conjunto de datos que describe las condiciones en las que se pueden leer los datos de los archivos protegidos.</span><span class="sxs-lookup"><span data-stu-id="360ef-135">A license is a set of data that describes the conditions under which data in protected files can be read.</span></span> <span data-ttu-id="360ef-136">La mayoría de las veces, se emite una licencia para un archivo protegido en respuesta al usuario que intenta realizar alguna operación en el archivo.</span><span class="sxs-lookup"><span data-stu-id="360ef-136">Most often, a license is issued for a protected file in response to the user trying to perform some operation on the file.</span></span> <span data-ttu-id="360ef-137">Sin embargo, también es posible que un emisor de licencias entregue licencias a un cliente antes de que se solicite explícitamente.</span><span class="sxs-lookup"><span data-stu-id="360ef-137">It is also possible, however, for a license issuer to deliver licenses to a client before it is explicitly requested.</span></span> <span data-ttu-id="360ef-138">Para obtener más información sobre las licencias, consulte [licencias](licenses.md).</span><span class="sxs-lookup"><span data-stu-id="360ef-138">For more information about licenses, see [Licenses](licenses.md).</span></span>

## <a name="reading-data-from-protected-files"></a><span data-ttu-id="360ef-139">Leer datos de archivos protegidos</span><span class="sxs-lookup"><span data-stu-id="360ef-139">Reading Data from Protected Files</span></span>

<span data-ttu-id="360ef-140">Cuando un usuario intenta realizar una operación en un archivo protegido (reproducir, grabar en CD, copiar en un dispositivo, etc.), la aplicación debe comprobar si hay licencias para el contenido en el equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="360ef-140">When a user tries to perform an operation on a protected file (play, burn to CD, copy to a device, and so on), the application must check for licenses for the content on the client computer.</span></span> <span data-ttu-id="360ef-141">Si existe una licencia válida en el equipo cliente, la operación puede continuar.</span><span class="sxs-lookup"><span data-stu-id="360ef-141">If a valid license exists on the client computer, the operation can proceed.</span></span> <span data-ttu-id="360ef-142">Si no hay una licencia para el contenido, o si ninguna licencia para el contenido que se encuentra en el equipo cliente permite la acción solicitada, se debe adquirir una licencia.</span><span class="sxs-lookup"><span data-stu-id="360ef-142">If there isn't a license for the content, or if no license for the content that is on the client computer allows the requested action, then a license must be acquired.</span></span>

## <a name="related-topics"></a><span data-ttu-id="360ef-143">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="360ef-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="360ef-144">**Acerca de las API extendidas del cliente DRM de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="360ef-144">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




