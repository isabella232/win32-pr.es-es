---
title: Introducción para los usuarios del SDK de Windows Media Format
description: Introducción para los usuarios del SDK de Windows Media Format
ms.assetid: 21f06c43-213e-4fbf-a33a-c1890b4b40ce
keywords:
- SDK de Windows Media Format, API extendidas del cliente DRM
- SDK de Windows Media Format, API extendidas de cliente
- SDK de Windows Media Format, API extendidas
- SDK de Windows Media Format, API
- SDK de Windows Media Format, administración de derechos digitales (DRM)
- Administración de derechos digitales (DRM), API extendidas de cliente
- DRM (administración de derechos digitales), API extendidas de cliente
- Administración de derechos digitales (DRM), API extendidas
- DRM (administración de derechos digitales), API extendidas
- Administración de derechos digitales (DRM), API
- DRM (administración de derechos digitales), API
- API extendidas del cliente DRM, acerca de
- API extendidas de cliente, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 538978305e4df952ed97e063b3512ce9fd5cfc34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418747"
---
# <a name="introduction-for-users-of-the-windows-media-format-sdk"></a><span data-ttu-id="18dab-116">Introducción para los usuarios del SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="18dab-116">Introduction for Users of the Windows Media Format SDK</span></span>

<span data-ttu-id="18dab-117">Gran parte de la funcionalidad proporcionada por las API extendidas del cliente DRM de Windows Media es la misma que la funcionalidad proporcionada por los objetos del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="18dab-117">Much of the functionality provided by the Windows Media DRM Client Extended APIs is the same as the functionality provided by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="18dab-118">El SDK de Windows Media Format proporciona a los desarrolladores los objetos necesarios para crear, obtener acceso y manipular archivos multimedia que usan la estructura de archivos Advanced Systems Format (ASF).</span><span class="sxs-lookup"><span data-stu-id="18dab-118">The Windows Media Format SDK provides developers with the objects needed to create, access, and manipulate media files that use the Advanced Systems Format (ASF) file structure.</span></span> <span data-ttu-id="18dab-119">Como Windows Media DRM está diseñado para proteger los archivos ASF, se incluyó la funcionalidad DRM del lado cliente en el SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="18dab-119">Because Windows Media DRM is intended to protect ASF files, client-side DRM functionality was included in the Windows Media Format SDK.</span></span>

<span data-ttu-id="18dab-120">Las API extendidas del cliente DRM de Windows Media se publican junto con la plataforma multimedia digital de última generación de Microsoft, el SDK de Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="18dab-120">The Windows Media DRM Client Extended APIs are being released in conjunction with Microsoft's next-generation digital media platform, the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="18dab-121">Media Foundation incluirá la funcionalidad de ASF que se superpone a algunas de las características del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="18dab-121">Media Foundation will include ASF functionality that overlaps some of the features of the Windows Media Format SDK.</span></span> <span data-ttu-id="18dab-122">Dado que ahora hay dos SDK de Microsoft que manipulan archivos ASF, la funcionalidad DRM del lado cliente se separa del SDK de Windows Media Format en las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18dab-122">Because there are now two Microsoft SDKs that manipulate ASF files, the client-side DRM functionality is being separated from the Windows Media Format SDK into the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="18dab-123">Se puede tener acceso a estas API a través de los usuarios de Windows Media Format SDK y del SDK de Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="18dab-123">These APIs can be accessed by users of both the Windows Media Format SDK and the Media Foundation SDK.</span></span> <span data-ttu-id="18dab-124">En la actualidad, estas API se incluyen como parte del paquete de instalación del SDK de Windows Media Format y se documentan como parte del SDK de Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="18dab-124">At present, these APIs are included as part of the Windows Media Format SDK installation package and are documented as part of the Windows Media Format SDK.</span></span> <span data-ttu-id="18dab-125">Sin embargo, las API extendidas del cliente DRM de Windows Media se implementan en su propia biblioteca y tienen su propio archivo de encabezado.</span><span class="sxs-lookup"><span data-stu-id="18dab-125">However, the Windows Media DRM Client Extended APIs are implemented in their own library and have their own header file.</span></span> <span data-ttu-id="18dab-126">Después de instalar el SDK de Windows Media Format, estas API se pueden usar una por su cuenta, sin incluir ningún encabezado o biblioteca de Windows Media Format SDK en la aplicación.</span><span class="sxs-lookup"><span data-stu-id="18dab-126">After installing the Windows Media Format SDK, these APIs can be used one their own, without including any Windows Media Format SDK headers or libraries in your application.</span></span>

<span data-ttu-id="18dab-127">Si desarrolla aplicaciones que usan el SDK de Windows Media Format, debe decidir si va a usar la funcionalidad DRM que proporciona el SDK o si desea usar las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="18dab-127">If you develop applications that use the Windows Media Format SDK you must decide whether to use the DRM functionality that SDK provides, or to use the Windows Media DRM Client Extended APIs.</span></span> <span data-ttu-id="18dab-128">Aunque muchas de las características de estos dos SDK son muy similares, las API extendidas del cliente DRM de Windows Media ofrecen las siguientes características que no están disponibles para los usuarios de las rutinas DRM anteriores:</span><span class="sxs-lookup"><span data-stu-id="18dab-128">While many of the features of these two SDKs are very similar, the Windows Media DRM Client Extended APIs offer the following features not available to users of the older DRM routines:</span></span>

-   <span data-ttu-id="18dab-129">Capacidad de importar contenido protegido por un sistema de administración de derechos de terceros.</span><span class="sxs-lookup"><span data-stu-id="18dab-129">Ability to import content protected by a third-party rights management system.</span></span>
-   <span data-ttu-id="18dab-130">Capacidad de exportar contenido protegido por DRM de Windows Media a un sistema de administración de derechos de terceros.</span><span class="sxs-lookup"><span data-stu-id="18dab-130">Ability to export content protected by Windows Media DRM to a third-party rights management system.</span></span>
-   <span data-ttu-id="18dab-131">Enumeración directa de licencias en el almacén de licencias.</span><span class="sxs-lookup"><span data-stu-id="18dab-131">Direct enumeration of licenses in the license store.</span></span>
-   <span data-ttu-id="18dab-132">Consultas de derechos simples y agregadas basadas en el identificador de clave (no es necesario cargar el archivo multimedia).</span><span class="sxs-lookup"><span data-stu-id="18dab-132">Simple, aggregated rights querying based on key ID (no need to load the media file).</span></span>
-   <span data-ttu-id="18dab-133">Capacidad de renovar componentes revocados mediante la interfaz de Media Foundation estándar, **IMFContentEnabler**.</span><span class="sxs-lookup"><span data-stu-id="18dab-133">Ability to renew revoked components by using the standard Media Foundation interface, **IMFContentEnabler**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="18dab-134">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="18dab-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18dab-135">**Acerca de las API extendidas del cliente DRM de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="18dab-135">**About the Windows Media DRM Client Extended APIs**</span></span>](about-the-windows-media-drm-client-extended-apis.md)
</dt> </dl>

 

 




