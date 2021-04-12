---
title: API extendidas del cliente DRM de Windows Media
description: API extendidas del cliente DRM de Windows Media
ms.assetid: c0397aa8-1f5a-48f5-a96b-555079e9a292
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
ms.openlocfilehash: 01c33ef3649f2cda63713ebd22a0116fdd025144
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420793"
---
# <a name="windows-media-drm-client-extended-apis"></a><span data-ttu-id="2ed70-116">API extendidas del cliente DRM de Windows Media</span><span class="sxs-lookup"><span data-stu-id="2ed70-116">Windows Media DRM Client Extended APIs</span></span>

<span data-ttu-id="2ed70-117">\[La característica Windows Media DRM está en desuso y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="2ed70-117">\[The Windows Media DRM feature is deprecated and should not be used.</span></span> <span data-ttu-id="2ed70-118">En su lugar, use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) .\]</span><span class="sxs-lookup"><span data-stu-id="2ed70-118">Use [Microsoft PlayReady](/windows/uwp/audio-video-camera/playready-client-sdk) instead.\]</span></span>

<span data-ttu-id="2ed70-119">En esta documentación se describen las interfaces de programación de aplicaciones (API) extendidas del cliente de Microsoft Windows Media Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="2ed70-119">This documentation describes the Microsoft Windows Media Digital Rights Management (DRM) Client Extended Application Programming Interfaces (APIs).</span></span> <span data-ttu-id="2ed70-120">Las API extendidas del cliente DRM de Windows Media incluyen objetos que se pueden usar para administrar operaciones de Rights Management digitales (DRM) de Windows Media en un equipo cliente.</span><span class="sxs-lookup"><span data-stu-id="2ed70-120">The Windows Media DRM Client Extended APIs include objects that can be used to manage Windows Media Digital Rights Management (DRM) operations on a client computer.</span></span>

<span data-ttu-id="2ed70-121">El objetivo principal de estas API es la administración de licencias de contenido multimedia digital protegido.</span><span class="sxs-lookup"><span data-stu-id="2ed70-121">The primary focus of these APIs is the management of licenses for protected digital media content.</span></span> <span data-ttu-id="2ed70-122">Además, las API se pueden usar para actualizar los componentes de DRM en el equipo cliente y para crear aplicaciones que transmiten contenido mediante DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="2ed70-122">In addition, the APIs can be used to update the DRM components on the client computer and to create applications that transmit content using Windows Media DRM for Network Devices.</span></span>

<span data-ttu-id="2ed70-123">Estas API constituyen el homólogo del lado cliente al SDK de Windows Media Rights Manager.</span><span class="sxs-lookup"><span data-stu-id="2ed70-123">These APIs constitute the client-side counterpart to the Windows Media Rights Manager SDK.</span></span> <span data-ttu-id="2ed70-124">Cuando se usa Windows Media Rights Manager para crear servicios en línea que protegen archivos y emiten licencias, se usan las API extendidas del cliente DRM de Windows Media para crear aplicaciones que consumen ese contenido.</span><span class="sxs-lookup"><span data-stu-id="2ed70-124">Where Windows Media Rights Manager is used to create online services that protect files and issue licenses, the Windows Media DRM Client Extended APIs are used to create applications that consume that content.</span></span>

<span data-ttu-id="2ed70-125">En este documento se incluyen las siguientes secciones.</span><span class="sxs-lookup"><span data-stu-id="2ed70-125">This document includes the following sections.</span></span>



| <span data-ttu-id="2ed70-126">Sección</span><span class="sxs-lookup"><span data-stu-id="2ed70-126">Section</span></span>                                                                                                  | <span data-ttu-id="2ed70-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ed70-127">Description</span></span>                                                                                                                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2ed70-128">Acerca de las API extendidas del cliente DRM de Windows Media</span><span class="sxs-lookup"><span data-stu-id="2ed70-128">About the Windows Media DRM Client Extended APIs</span></span>](about-the-windows-media-drm-client-extended-apis.md) | <span data-ttu-id="2ed70-129">Proporciona información general e información general que debe conocer antes de desarrollar aplicaciones que usan las API.</span><span class="sxs-lookup"><span data-stu-id="2ed70-129">Provides overview and background information that you should be familiar with before developing applications that use the APIs.</span></span>                                                        |
| [<span data-ttu-id="2ed70-130">Guía de programación</span><span class="sxs-lookup"><span data-stu-id="2ed70-130">Programming Guide</span></span>](drm-programming-guide.md)                                                           | <span data-ttu-id="2ed70-131">Proporciona instrucciones detalladas para realizar diversas operaciones DRM del lado cliente.</span><span class="sxs-lookup"><span data-stu-id="2ed70-131">Provides detailed instructions for performing various client-side DRM operations.</span></span>                                                                                                      |
| [<span data-ttu-id="2ed70-132">Referencia de programación</span><span class="sxs-lookup"><span data-stu-id="2ed70-132">Programming Reference</span></span>](drm-programming-reference.md)                                                   | <span data-ttu-id="2ed70-133">Proporciona información de referencia sobre las interfaces, los métodos, las funciones, las estructuras, los tipos de enumeración y las constantes que se incluyen en las API extendidas del cliente DRM de Windows Media.</span><span class="sxs-lookup"><span data-stu-id="2ed70-133">Provides reference information about the interfaces, methods, functions, structures, enumeration types, and constants that are included in the Windows Media DRM Client Extended APIs.</span></span> |



 

 

 